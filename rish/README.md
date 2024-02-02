# RISH

<del>Rish is an Interactive SHell for android</del>

## Description

`rish` is an Android program for interacting with a shell that runs on a high-privileged daemon process.

Currently, Shizuku and Sui are two available backends.

## Usage

First of all, follow the guide from Shizuku or Sui to create the files of `rish`.

The remain is very simple, you only need to replace `sh` with `rish` in the command you want to run, `rish` will pass arguments directly to the remote shell.

Here is an example.

```
rish -c 'ls'
```

This is what will be executed at remote:

```
/system/bin/sh -c 'ls'
```

If you want to use other shells rather than `/system/bin/sh`, use `rish exec /path/to/other/shell`.

## Options

Since `rish` passes arguments directly to the remote, `rish` uses environment variable for options.

### RISH_PRESERVE_ENV

| Value | Description                                                          |
|-------|----------------------------------------------------------------------|
| `0`   | Do not change environment variables of the remote process            |
| `1`   | Replace the environment variables of the remote process with local's |

Termux app set `PATH` and `LD_PRELOAD` to Termux's internal path.
Adb (Shizuku can run under adb) does not have sufficient permissions to access such places, making users can even not using commands like `cd`.

If the backend runs under adb, `RISH_PRESERVE_ENV` will be treated as `0` when not set.

If the backend runs under root, `RISH_PRESERVE_ENV` will be treated as `1` when not set.[
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "status": {},
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)",
        "requestAttributes": {},
        "destinationAttributes": {}
      },
      "serviceName": "cloudresourcemanager.googleapis.com",
      "methodName": "CreateProject",
      "authorizationInfo": [
        {
          "resourceAttributes": {}
        }
      ],
      "resourceName": "projects/vigilant-result-413123",
      "request": {
        "@type": "type.googleapis.com/google.cloudresourcemanager.v1.CreateProjectRequest",
        "project": {
          "createTime": "2024-02-01T23:33:51.433452Z",
          "lifecycleState": "ACTIVE",
          "projectId": "vigilant-result-413123",
          "projectNumber": "145648255740",
          "name": "My First Project"
        }
      }
    },
    "insertId": "ldc77cd17va",
    "resource": {
      "type": "project",
      "labels": {
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:52.330005Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "receiveTimestamp": "2024-02-01T23:33:52.500769445Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)",
        "requestAttributes": {},
        "destinationAttributes": {}
      },
      "methodName": "google.api.serviceusage.v1.ServiceUsage.EnableService",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "services/cloudapis.googleapis.com",
          "permission": "servicemanagement.services.bind",
          "granted": true,
          "resourceAttributes": {}
        }
      ],
      "resourceName": "projects/vigilant-result-413123/services/cloudapis.googleapis.com"
    },
    "insertId": "3c92dsctcw",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "service": "",
        "method": "google.api.serviceusage.v1.ServiceUsage.EnableService",
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:53.515196Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "operation": {
      "id": "operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc",
      "producer": "serviceusage.googleapis.com",
      "first": true
    },
    "receiveTimestamp": "2024-02-01T23:33:55.128844017Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)",
        "requestAttributes": {},
        "destinationAttributes": {}
      },
      "serviceName": "serviceusage.googleapis.com",
      "methodName": "google.api.serviceusage.v1.ServiceUsage.EnableService",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "services/cloudapis.googleapis.com",
          "permission": "servicemanagement.services.bind",
          "granted": true,
          "resourceAttributes": {}
        }
      ],
      "resourceName": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
      "request": {
        "name": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
        "@type": "type.googleapis.com/google.api.serviceusage.v1.EnableServiceRequest"
      }
    },
    "insertId": "b3xp3ed54fr",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "method": "google.api.serviceusage.v1.ServiceUsage.EnableService",
        "project_id": "vigilant-result-413123",
        "service": "serviceusage.googleapis.com"
      }
    },
    "timestamp": "2024-02-01T23:33:53.515196Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "operation": {
      "id": "operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc",
      "producer": "serviceusage.googleapis.com",
      "first": true
    },
    "receiveTimestamp": "2024-02-01T23:33:54.721127892Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "status": {},
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)",
        "requestAttributes": {},
        "destinationAttributes": {}
      },
      "serviceName": "servicemanagement.googleapis.com",
      "methodName": "google.longrunning.Operations.GetOperation",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/operations/-",
          "permission": "serviceusage.operations.get",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/services/-",
          "permission": "serviceusage.services.get",
          "granted": true,
          "resourceAttributes": {}
        }
      ],
      "resourceName": "projects/145648255740/operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc"
    },
    "insertId": "1ca8xm8cj5p",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "method": "google.longrunning.Operations.GetOperation",
        "service": "servicemanagement.googleapis.com",
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:54.697184Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "receiveTimestamp": "2024-02-01T23:33:55.315088278Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "status": {},
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)"
      },
      "serviceName": "serviceusage.googleapis.com",
      "methodName": "google.api.serviceusage.v1.ServiceUsage.EnableService",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true
        },
        {
          "resource": "services/cloudapis.googleapis.com",
          "permission": "servicemanagement.services.bind",
          "granted": true
        }
      ],
      "resourceName": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
      "request": {
        "name": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
        "@type": "type.googleapis.com/google.api.serviceusage.v1.EnableServiceRequest"
      },
      "response": {
        "service": {
          "name": "projects/145648255740/services/cloudapis.googleapis.com",
          "config": {
            "name": "cloudapis.googleapis.com",
            "title": "Google Cloud APIs"
          },
          "state": "ENABLED",
          "parent": "projects/145648255740"
        },
        "@type": "type.googleapis.com/google.api.serviceusage.v1.EnableServiceResponse"
      }
    },
    "insertId": "n19wm6d61yk",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "method": "google.api.serviceusage.v1.ServiceUsage.EnableService",
        "service": "serviceusage.googleapis.com",
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:55.900555596Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "operation": {
      "id": "operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc",
      "producer": "serviceusage.googleapis.com",
      "last": true
    },
    "receiveTimestamp": "2024-02-01T23:33:55.900555596Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "status": {},
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)"
      },
      "serviceName": "serviceusage.googleapis.com",
      "methodName": "google.api.serviceusage.v1.ServiceUsage.EnableService",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740/services/cloudapis.googleapis.com",
          "permission": "serviceusage.services.enable",
          "granted": true
        },
        {
          "resource": "services/cloudapis.googleapis.com",
          "permission": "servicemanagement.services.bind",
          "granted": true
        }
      ],
      "resourceName": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
      "request": {
        "name": "projects/vigilant-result-413123/services/cloudapis.googleapis.com",
        "@type": "type.googleapis.com/google.api.serviceusage.v1.EnableServiceRequest"
      },
      "response": {
        "status": "ENABLED",
        "services": [
          "cloudapis.googleapis.com",
          "bigquery.googleapis.com",
          "bigquerymigration.googleapis.com",
          "bigquerystorage.googleapis.com",
          "cloudtrace.googleapis.com",
          "datastore.googleapis.com",
          "logging.googleapis.com",
          "monitoring.googleapis.com",
          "servicemanagement.googleapis.com",
          "serviceusage.googleapis.com",
          "sql-component.googleapis.com",
          "storage-api.googleapis.com",
          "storage-component.googleapis.com",
          "storage.googleapis.com"
        ],
        "@type": "type.googleapis.com/google.api.tenant.apis.shared.activation.CrossLoggingResponse"
      }
    },
    "insertId": "n19wm6d61ym",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "service": "serviceusage.googleapis.com",
        "method": "google.api.serviceusage.v1.ServiceUsage.EnableService",
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:55.900555596Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Factivity",
    "operation": {
      "id": "operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc",
      "producer": "serviceusage.googleapis.com",
      "last": true
    },
    "receiveTimestamp": "2024-02-01T23:33:55.900555596Z"
  },
  {
    "protoPayload": {
      "@type": "type.googleapis.com/google.cloud.audit.AuditLog",
      "status": {},
      "authenticationInfo": {
        "principalEmail": "modibash7@gmail.com"
      },
      "requestMetadata": {
        "callerIp": "85.208.204.16",
        "callerSuppliedUserAgent": "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Mobile Safari/537.36,gzip(gfe),gzip(gfe)",
        "requestAttributes": {},
        "destinationAttributes": {}
      },
      "serviceName": "servicemanagement.googleapis.com",
      "methodName": "google.longrunning.Operations.GetOperation",
      "authorizationInfo": [
        {
          "resource": "projectnumbers/145648255740",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740",
          "permission": "serviceusage.services.enable",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/operations/-",
          "permission": "serviceusage.operations.get",
          "granted": true,
          "resourceAttributes": {}
        },
        {
          "resource": "projectnumbers/145648255740/services/-",
          "permission": "serviceusage.services.get",
          "granted": true,
          "resourceAttributes": {}
        }
      ],
      "resourceName": "projects/145648255740/operations/acat.p2-145648255740-0a57f374-89a5-453c-8667-f473c365f3cc"
    },
    "insertId": "u8l5fd4u0f",
    "resource": {
      "type": "audited_resource",
      "labels": {
        "service": "servicemanagement.googleapis.com",
        "method": "google.longrunning.Operations.GetOperation",
        "project_id": "vigilant-result-413123"
      }
    },
    "timestamp": "2024-02-01T23:33:56.388547Z",
    "severity": "NOTICE",
    "logName": "projects/vigilant-result-413123/logs/cloudaudit.googleapis.com%2Fahctivity",
    "receiveTimestamp": "2024-02-01T23:33:57.324654830Z"
  }
]q
gcloud container clusters \
    get-credentials logcluster \
    --zone us-central1-c --project \
    package com.example;

parcelable ComplexType cpp_header "ComplexType.h";
{
  "name": "Human-readable vendor name",
  "manufacturer": ["name","alias1","alias2"],
  "url": "/relative-url-to-vendor",
  "award": number or null,
  "position": number or null,
  "explanation": "JSON-escaped HTML",
  "user_solution": "JSON-escaped HTML",
  "developer_solution": "JSON-escaped HTML"
}1682db03316b426dà170048d90b390fcb723f59e1
.class public final Lrikka/shizuku/shell/ShizukuShellLoader$a;
.class public final Lrikka/shizuku/shell/ShizukuShellLoader$a;

