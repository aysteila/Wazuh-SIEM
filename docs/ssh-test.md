# SSH Authentication Test

## Objective
Verify that SSH authentication events are recorded in Ubuntu logs.

## Environment
- OS: Ubuntu 24.04.5 LTS on WSL2
- SSH Server: OpenSSH
- SSH Port: 22
- Target: localhost (127.0.0.1)

## Test Procedure
1. Connect to the local SSH server.
2. Perform one failed password attempt.
3. Perform a successful password authentication.
4. Disconnect from the SSH session.
5. Inspect /var/log/auth.log.

## Observed Results

| Event | Result |
|---|---|
| Failed password | Detected in auth.log |
| Accepted password | Detected in auth.log |
| Session opened | Detected in auth.log |
| Session closed | Detected in auth.log |

## Conclusion
Ubuntu successfully recorded both failed and successful SSH authentication events.

Note: This test was performed locally. It is not an external attack and does not yet represent a Wazuh detection alert.
