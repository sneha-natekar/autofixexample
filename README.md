# autofixexample



``` mermaid
graph TD
    A[Install the GitHub App (grants initial permissions)] --> B[Redirect to GitHub Authorization Page (request permissions)]
    B --> C{3. User Grants Permissions?}
    C -- Yes --> D[4. App Requests Access Token (exchanges code for token)]
    C -- No --> E[End: Permissions Denied]
    D --> F[5. App Makes Authenticated API Requests (using access token)]
    F --> G{6. Token Expiry?}
    G -- Yes --> H[App Requests New Token (refresh token)]
    G -- No --> F
    H --> F
    F --> I{7. Revoking Permissions?}
    I -- Yes --> J[End: Access Revoked]
    I -- No --> K[Continue Using Token] --> F
```
