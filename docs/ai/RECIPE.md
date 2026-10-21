# Spatial Voice Chat Tutorial

## Overview

Build a spatial voice chat experience where participant audio changes with position in a shared space.

Repository: [AgoraIO-Community/Agora-Spatial-Voice-Chat-Tutorial](https://github.com/AgoraIO-Community/Agora-Spatial-Voice-Chat-Tutorial)

## Prerequisites and Setup

1. Use the recorded Unity Editor version `2020.1.9f1` as the starting point; import the Agora Voice SDK `v3.3.1.71` and Photon PUN 2 `v2.18` identified in the README.
2. Configure the Photon application settings for your own project. In `Assets/Scripts/VoiceChatManager.cs`, replace the empty `appID` with your test App ID.
3. Open the project in Unity, resolve the listed assets and packages, and build two clients using the project's scenes.
4. Join the same Photon room from both clients. `VoiceChatManager` uses that room's name for the Agora channel.

## What To Check

- Verify Photon room membership and the Agora join callback in each client's logs.
- Move the players and confirm the perceived voice position follows their relative positions.
- Leave and rejoin the room, then confirm channel and engine cleanup.

## Integration Notes

This tutorial uses the older `agora_gaming_rtc` API. Do not replace it with a current SDK without a separate migration. Its direct channel join has no token argument; adapt authentication before using a token-protected project in production.

Keep App Certificates, customer secrets and privileged token generation on a trusted backend for production. Use only your own test credentials while configuring historical demos; do not commit them. Preserve the sample's existing dependency versions and lifecycle until a separate migration is tested.

## Source References

- [README.md](../../README.md)
- [ProjectSettings/ProjectVersion.txt](../../ProjectSettings/ProjectVersion.txt)
- [Assets/Scripts/VoiceChatManager.cs](../../Assets/Scripts/VoiceChatManager.cs)
- [Assets/Scripts/SpatialAudio.cs](../../Assets/Scripts/SpatialAudio.cs)

## Validation Status

This recipe was checked against the repository's source and setup documents. The platform build and live service/device flow have not been run as part of this documentation change. Complete the checks above in an environment with the required SDKs, hardware and service access before treating it as a validated deployment.

## Implementation Prompt

```text
You are working in AgoraIO-Community/Agora-Spatial-Voice-Chat-Tutorial. Use docs/ai/RECIPE.md and its linked source files to adapt the Spatial Voice Chat Tutorial reference to this project.

Start by inspecting the actual sample directory and configuration described above. Resolve its listed missing prerequisites before claiming it is runnable. Preserve the existing architecture and compatible dependency versions. Implement the recipe's feature-specific flow, permissions and resource cleanup. Use a trusted backend for privileged credentials and tokens in production.

Run the repository-specific build or launch flow, then perform each What To Check item. Report the commands run, the observed results and anything blocked by service access, hardware or incomplete sample code. Do not claim live validation from a documentation or catalog build alone.
```
