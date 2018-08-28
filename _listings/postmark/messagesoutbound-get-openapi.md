---
swagger: "2.0"
x-collection-name: Postmark
x-complete: 0
info:
  title: Postmark Get Messages Outbound
  description: Get messages outbound.
  version: 1.0.0
host: spamcheck.postmarkapp.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /messages/outbound:
    get:
      summary: Get Messages Outbound
      description: Get messages outbound.
      operationId: getMessagesOutbound
      x-api-path-slug: messagesoutbound-get
      parameters:
      - in: query
        name: count
        description: Number of messages to return per request
      - in: query
        name: fromdate
        description: Filter messages starting from the date specified
      - in: query
        name: fromemail
        description: Filter by the sender email address
      - in: query
        name: offset
        description: Number of messages to skip
      - in: query
        name: recipient
        description: Filter by the user who was receiving the email
      - in: query
        name: status
        description: Filter by status (`queued` or `sent`)
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter messages up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Messages
      - Outbound
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---