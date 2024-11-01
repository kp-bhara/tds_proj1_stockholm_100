How web scraping was done
To extract users, the code sent synchronous requests with the `requests` library and a PAT (Personal Access Token) to fetch GitHub users based in Stockholm with over 100 followers, saving results to `users.csv`. To extract the repositories, the code was written to asynchronously extract each user's repositories, using `aiohttp` and `asyncio` for efficient async requests and chunking users for rate-limit handling, storing repository data in multiple `repository_chunk.csv` files. Pagination was implemented in both cases to extract all users.

Interesting insights after analyzing the data
JavaScript emerges as the most popular language among these developers, followed by TypeScript. This suggests a shift towards modern web development practices, particularly as TypeScript is increasingly adopted to enhance JavaScript applications.
Using regression analysis, the slope of 48.601 indicates that, on average, each additional public repository leads to approximately 48.601 additional followers. This points to the value of active contributions in increasing visibility.The regression slope of 6.565 suggests that for every additional word in a user's bio, they gain approximately 6.565 more followers, indicating that longer and more engaging bios can attract additional attention.


Insights for developers
Developers should focus on creating and maintaining multiple repositories
Developers should invest time in crafting detailed and engaging bios that highlight their skills, interests, and contributions. Using keywords relevant to their expertise can enhance discoverability.
Given the popularity of JavaScript and TypeScript, developers should consider improving their skills in these languages. Creating projects or repositories that utilize these languages can align their work with industry trends, making it more relevant and attractive to potential followers.
