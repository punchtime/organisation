---
layout: default
---

[back](.)

todo: draw a diagram of:

```json
{"users": {
  "test-user": {
    "name": "Test User",
    "employee": {
      "test-company": "true"
    },
    "employer": {},
    "pulses": {
      "test-pulse-1": true,
      "test-pulse-2": true
    },
    "image": "https://scontent..."
  },
  "test-employer": {
    "name":"Test Employer",
    "employee": {},
    "employer": {
      "test-company": true
    },
    "image": "data:image/png;base64,iVBO..."
  }
},
"companies": {
  "test-company": {
    "employees": {
      "test-user": true
    },
    "employers": {
      "test-employer": true
    },
    "tier": "free"
  }
},
"pulses": {
  "test-pulse-1": {
    "user": "test-user",
    "checkin": 1456410617812,
    "checkout": 1456410618812,
    "latitude": 51.0537,
    "longitude": 3.73295,
    "note": "this is a test check out",
    "confirmed": true
  },
  "test-pulse-2": {
    "user": "test-user",
    "checkin": 1456410661398,
    "checkout": 1456410671398,
    "latitude": 51.03492,
    "longitude": 3.71166,
    "note": "this is a test check in",
    "confirmed": false
  }
}}

```
