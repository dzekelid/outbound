---
swagger: "2.0"
x-collection-name: Postmark
x-complete: 0
info:
  title: Postmark Get Stats Outbound Clicks Location
  description: Get stats outbound clicks location.
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
  /messages/outbound/clicks:
    get:
      summary: Get Messages Outbound Clicks
      description: Get messages outbound clicks.
      operationId: getMessagesOutboundClicks
      x-api-path-slug: messagesoutboundclicks-get
      parameters:
      - in: query
        name: city
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: client_company
        description: Filter by company, i
      - in: query
        name: client_family
        description: Filter by client family, i
      - in: query
        name: client_name
        description: Filter by client name, i
      - in: query
        name: count
        description: Number of message clicks to return per request
      - in: query
        name: country
        description: Filter by country messages were opened in, i
      - in: query
        name: offset
        description: Number of messages to skip
      - in: query
        name: os_company
        description: Filter by company which produced the OS, i
      - in: query
        name: os_family
        description: Filter by kind of OS used without specific version, i
      - in: query
        name: os_name
        description: Filter by full OS name and specific version, i
      - in: query
        name: platform
        description: Filter by platform, i
      - in: query
        name: recipient
        description: Filter by To, Cc, Bcc
      - in: query
        name: region
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: tag
        description: Filter by tag
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
      - Clicks
  /messages/outbound/clicks/{messageid}:
    get:
      summary: Get Messages Outbound Clicks Message
      description: Get messages outbound clicks message.
      operationId: getMessagesOutboundClicksMessage
      x-api-path-slug: messagesoutboundclicksmessageid-get
      parameters:
      - in: query
        name: count
        description: Number of message clicks to return per request
      - in: path
        name: messageid
        description: The ID of the Outbound Message for which click statistics should
          be retrieved
      - in: query
        name: offset
        description: Number of messages to skip
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
      - Clicks
      - Messageid
  /messages/outbound/opens:
    get:
      summary: Get Messages Outbound Opens
      description: Get messages outbound opens.
      operationId: getMessagesOutboundOpens
      x-api-path-slug: messagesoutboundopens-get
      parameters:
      - in: query
        name: city
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: client_company
        description: Filter by company, i
      - in: query
        name: client_family
        description: Filter by client family, i
      - in: query
        name: client_name
        description: Filter by client name, i
      - in: query
        name: count
        description: Number of message opens to return per request
      - in: query
        name: country
        description: Filter by country messages were opened in, i
      - in: query
        name: offset
        description: Number of messages to skip
      - in: query
        name: os_company
        description: Filter by company which produced the OS, i
      - in: query
        name: os_family
        description: Filter by kind of OS used without specific version, i
      - in: query
        name: os_name
        description: Filter by full OS name and specific version, i
      - in: query
        name: platform
        description: Filter by platform, i
      - in: query
        name: recipient
        description: Filter by To, Cc, Bcc
      - in: query
        name: region
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: tag
        description: Filter by tag
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
      - Opens
  /messages/outbound/opens/{messageid}:
    get:
      summary: Get Messages Outbound Opens Message
      description: Get messages outbound opens message.
      operationId: getMessagesOutboundOpensMessage
      x-api-path-slug: messagesoutboundopensmessageid-get
      parameters:
      - in: query
        name: count
        description: Number of message opens to return per request
      - in: path
        name: messageid
        description: The ID of the Outbound Message for which open statistics should
          be retrieved
      - in: query
        name: offset
        description: Number of messages to skip
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
      - Opens
      - Messageid
  /messages/outbound/{messageid}/details:
    get:
      summary: Get Messages Outbound Message Details
      description: Get messages outbound message details.
      operationId: getMessagesOutboundMessageDetails
      x-api-path-slug: messagesoutboundmessageiddetails-get
      parameters:
      - in: path
        name: messageid
        description: The ID of the message for which to retrieve details
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
      - Messageid
      - Details
  /messages/outbound/{messageid}/dump:
    get:
      summary: Get Messages Outbound Message Dump
      description: Get messages outbound message dump.
      operationId: getMessagesOutboundMessageDump
      x-api-path-slug: messagesoutboundmessageiddump-get
      parameters:
      - in: path
        name: messageid
        description: The ID of the message for which to retrieve a dump
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
      - Messageid
      - Dump
  /stats/outbound:
    get:
      summary: Get Stats Outbound
      description: Get stats outbound.
      operationId: getStatsOutbound
      x-api-path-slug: statsoutbound-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
  /stats/outbound/bounces:
    get:
      summary: Get Stats Outbound Bounces
      description: Get stats outbound bounces.
      operationId: getStatsOutboundBounces
      x-api-path-slug: statsoutboundbounces-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Bounces
  /stats/outbound/clicks:
    get:
      summary: Get Stats Outbound Clicks
      description: Get stats outbound clicks.
      operationId: getStatsOutboundClicks
      x-api-path-slug: statsoutboundclicks-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Clicks
  /stats/outbound/clicks/browserfamilies:
    get:
      summary: Get Stats Outbound Clicks Browserfamilies
      description: Get stats outbound clicks browserfamilies.
      operationId: getStatsOutboundClicksBrowserfamilies
      x-api-path-slug: statsoutboundclicksbrowserfamilies-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Clicks
      - Browserfamilies
  /stats/outbound/clicks/location:
    get:
      summary: Get Stats Outbound Clicks Location
      description: Get stats outbound clicks location.
      operationId: getStatsOutboundClicksLocation
      x-api-path-slug: statsoutboundclickslocation-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Clicks
      - Location
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