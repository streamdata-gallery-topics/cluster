swagger: "2.0"
x-collection-name: Google Cloud Dataproc
x-complete: 1
info:
  title: Google Cloud Dataproc
  description: manages-hadoopbased-clusters-and-jobs-on-google-cloud-platform-
  contact:
    name: Google
    url: https://google.com
  version: v1
host: dataproc.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/projects/{projectId}/regions/{region}/clusters:
    get:
      summary: Get Region Clusters
      description: Lists all regions/{region}/clusters in a project.
      operationId: dataproc.projects.regions.clusters.list
      x-api-path-slug: v1projectsprojectidregionsregionclusters-get
      parameters:
      - in: query
        name: filter
        description: Optional A filter constraining the clusters to list
      - in: query
        name: pageSize
        description: Optional The standard List page size
      - in: query
        name: pageToken
        description: Optional The standard List page token
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project that the
          cluster belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      responses:
        200:
          description: OK
      tags:
      - Cluster
    post:
      summary: Create Cluster
      description: Creates a cluster in a project.
      operationId: dataproc.projects.regions.clusters.create
      x-api-path-slug: v1projectsprojectidregionsregionclusters-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project that the
          cluster belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      responses:
        200:
          description: OK
      tags:
      - Cluster
  /v1/projects/{projectId}/regions/{region}/clusters/{clusterName}:
    delete:
      summary: Delete Cluster
      description: Deletes a cluster in a project.
      operationId: dataproc.projects.regions.clusters.delete
      x-api-path-slug: v1projectsprojectidregionsregionclustersclustername-delete
      parameters:
      - in: path
        name: clusterName
        description: Required The cluster name
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project that the
          cluster belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      responses:
        200:
          description: OK
      tags:
      - Cluster
    get:
      summary: Get Cluster
      description: Gets the resource representation for a cluster in a project.
      operationId: dataproc.projects.regions.clusters.get
      x-api-path-slug: v1projectsprojectidregionsregionclustersclustername-get
      parameters:
      - in: path
        name: clusterName
        description: Required The cluster name
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project that the
          cluster belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      responses:
        200:
          description: OK
      tags:
      - Cluster
    patch:
      summary: Update Cluster
      description: Updates a cluster in a project.
      operationId: dataproc.projects.regions.clusters.patch
      x-api-path-slug: v1projectsprojectidregionsregionclustersclustername-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterName
        description: Required The cluster name
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project the cluster
          belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      - in: query
        name: updateMask
        description: Required Specifies the path, relative to Cluster, of the field
          to update
      responses:
        200:
          description: OK
      tags:
      - Cluster
  /v1/projects/{projectId}/regions/{region}/clusters/{clusterName}:diagnose:
    post:
      summary: Get Cluster Diagnostic
      description: Gets cluster diagnostic information. After the operation completes,
        the Operation.response field contains DiagnoseClusterOutputLocation.
      operationId: dataproc.projects.regions.clusters.diagnose
      x-api-path-slug: v1projectsprojectidregionsregionclustersclusternamediagnose-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterName
        description: Required The cluster name
      - in: path
        name: projectId
        description: Required The ID of the Google Cloud Platform project that the
          cluster belongs to
      - in: path
        name: region
        description: Required The Cloud Dataproc region in which to handle the request
      responses:
        200:
          description: OK
      tags:
      - Cluster