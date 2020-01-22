---
title: "Logs"
linkTitle: "Logs"
description: >
  Learn how to view step logs.
---

## Endpoint

```
GET  /api/v1/repos/:org/:repo/builds/:build/steps/:step/logs
```

## Parameters

The following parameters are used to configure the endpoint:

| Name    | Description          |
| ------- | -------------------- |
| `org`   | name of organization |
| `repo`  | name of repository   |
| `build` | number of build      |
| `step`  | number of step       |

## Permissions

COMING SOON!

## Responses

| Status Code | Description                                         |
| ----------- | --------------------------------------------------- |
| `200`       | indicates the request has succeeded                 |
| `401`       | indicates the user does not have proper permissions |

## Sample

#### Request

```sh
curl \
  -X GET \
  -H "Authorization: Bearer <token>" \
  "http://127.0.0.1:8080/api/v1/repos/github/octocat/builds/1/steps/1/logs"
```

#### Response

```json
{
  "id": 1,
  "build_id": 1,
  "repo_id": 1,
  "step_id": 1,
  "data": "SGVsbG8sIFdvcmxkIQ=="
}
```