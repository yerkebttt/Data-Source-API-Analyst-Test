# Data-Source-API-Analyst-Test
Homework assignment for Data Source API Analyst role.

Overview

This project was developed as part of the Data Source API Analyst Challenge. The goal is to demonstrate an understanding of APIs, data extraction requirements, troubleshooting, and documentation.

Repository Structure

README.md: This document outlines the project’s purpose, implementation details, and reflections.

/Content: Contains:

Python scripts for authentication, data extraction, error handling, rate limits, and pagination.

Troubleshooting guides and data-cleaning approach documentation.

/Postman_Collection: Includes the exported Postman collection and Google Colab notebook for API testing and extraction.

Implementation

Tools Used

Google Colab: For Python-based API testing and data extraction.

GitHub API: The source for repository and commit data.

Python Libraries:

requests for API interaction.

time for handling rate-limit waits.

logging for detailed process logging.

json for data processing.

Features Implemented

Authentication:

Used a GitHub personal access token for secure access to API endpoints.

Token securely retrieved via environment variables in Google Colab.

Data Extraction:

Extracted data for public repositories, commits, and contents.

Implemented pagination to handle multi-page responses.

Error Handling:

Addressed common HTTP errors (401, 403, 404) with specific troubleshooting steps.

Included dynamic rate-limit handling by waiting until reset.

Output Formatting:

Processed and displayed repository and commit data in a clear and structured format.

Key API Endpoints

Search Repositories:

Endpoint: /search/repositories

Parameters: language, sort, order, per_page

Commits:

Endpoint: /repos/{owner}/{repo}/commits

Parameters: per_page, page

Contents:

Endpoint: /repos/{owner}/{repo}/contents/{path}

Parameters: None for base directory contents.

Client Requirements

The client requested the following:

Search Repositories:

List public repositories filtered by language and sorted by stars.

View Commits:

Display recent commit messages for a given repository.

Retrieve Contents:

Fetch contents of a specific repository’s directory.

Troubleshooting Guide

Common Issues:

401 Unauthorized:

Verify the token’s validity and permissions.

Ensure environment variables are correctly set in Google Colab.

403 Forbidden:

Check for rate limits and wait until reset.

Verify token scopes and repository access rights.

404 Not Found:

Confirm the correctness of repository names and paths.

Rate Limit Handling:

When the rate limit is exceeded, the script waits until the reset time specified in the API headers.

Output Samples

Top Python Repositories

Name: public-apis, Stars: 319,173, URL: View Repository

Name: system-design-primer, Stars: 278,203, URL: View Repository

Recent Commits

Repository: torvalds/linux

Message: "Merge tag 'for-6.13-rc1-tag' of git://git.kernel.org/pub/scm/linux/kernel/git/kdave/linux"

Message: "Merge tag 'fs_for_v6.13-rc2' of git://git.kernel.org/pub/scm/linux/kernel/git/jack/linux-fs"

Reflection

This project provided valuable experience in working with APIs, handling data extraction challenges, and implementing troubleshooting mechanisms. Google Colab proved to be an excellent tool for collaborative coding and API testing. Future improvements could include dynamic error retries and enhanced data visualization.

Submission

Google Colab Notebook: Included in the /Postman_Collection directory.

Postman Collection: Exported and available in the /Postman_Collection directory.

For questions or feedback, feel free to contact me!


