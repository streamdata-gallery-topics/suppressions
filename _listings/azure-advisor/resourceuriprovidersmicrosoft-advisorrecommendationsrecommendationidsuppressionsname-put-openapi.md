---
swagger: "2.0"
x-collection-name: Azure Advisor
x-complete: 0
info:
  title: Azure Advisor API Create Suppressions
  description: Enables the snoozed or dismissed attribute of a recommendation. The
    snoozed or dismissed attribute is referred to as a suppression. Use this API to
    create or update the snoozed or dismissed status of a recommendation.
  version: "2017-04-19"
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{resourceUri}/providers/Microsoft.Advisor/recommendations/{recommendationId}/suppressions/{name}:
    get:
      summary: Get Suppressions
      description: Obtains the details of a suppression.
      operationId: Suppressions_Get
      x-api-path-slug: resourceuriprovidersmicrosoft-advisorrecommendationsrecommendationidsuppressionsname-get
      parameters:
      - in: path
        name: name
        description: The name of the suppression
      - in: query
        name: No Name
      - in: path
        name: recommendationId
        description: The recommendation ID
      - in: path
        name: resourceUri
        description: The fully qualified Azure Resource Manager identifier of the
          resource to which the recommendation applies
      responses:
        200:
          description: OK
      tags:
      - Suppressions
    put:
      summary: Create Suppressions
      description: Enables the snoozed or dismissed attribute of a recommendation.
        The snoozed or dismissed attribute is referred to as a suppression. Use this
        API to create or update the snoozed or dismissed status of a recommendation.
      operationId: Suppressions_Create
      x-api-path-slug: resourceuriprovidersmicrosoft-advisorrecommendationsrecommendationidsuppressionsname-put
      parameters:
      - in: path
        name: name
        description: The name of the suppression
      - in: query
        name: No Name
      - in: path
        name: recommendationId
        description: The recommendation ID
      - in: path
        name: resourceUri
        description: The fully qualified Azure Resource Manager identifier of the
          resource to which the recommendation applies
      - in: body
        name: suppressionContract
        description: The snoozed or dismissed attribute; for example, the snooze duration
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Suppressions
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