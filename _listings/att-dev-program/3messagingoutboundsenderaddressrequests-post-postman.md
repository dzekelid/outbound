{
  "info": {
    "name": "AT&T API Post Messaging Outbound Senderaddress Requests",
    "_postman_id": "a90a6098-e9b4-4c1d-86e7-f14ebf91e640",
    "description": "/3/messaging/outbound/{senderAddress}/requests",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Devicecapabilities",
      "item": [
        {
          "id": "7574df44-930a-459b-a46c-b5a1dd6c9a4c",
          "name": "1devicecapabilitiesacrauthorizationcapabilities",
          "request": {
            "url": "http://api.att.com/1/devicecapabilities/acr:authorization/capabilities",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/1/devicecapabilities/acr:authorization/capabilities"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1219dff7-adde-4c20-9cc7-ee376a541051"
            }
          ]
        }
      ]
    },
    {
      "name": "Messaging",
      "item": [
        {
          "id": "6c83a18b-0d8c-48d8-b755-f609eea5efb4",
          "name": "3messagingoutboundsenderaddressrequests",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.att.com",
              "path": [
                "3/messaging/outbound/:senderAddress/requests"
              ],
              "variable": [
                {
                  "id": "senderAddress",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/3/messaging/outbound/{senderAddress}/requests"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1cbb6ac1-2d0a-4faf-a02f-5ffe9abc4b4f"
            }
          ]
        }
      ]
    }
  ]
}