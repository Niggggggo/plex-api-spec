# Plex Media Server OpenAPI Specification

Automation and SDKs provided by [Speakeasy](https://speakeasyapi.dev/)

An Open Source OpenAPI Specification for Plex Media Server

## Documentation

[API Documentation](https://plexapi.dev)

## SDKs

The following SDKs are generated from the OpenAPI Specification. They are automatically generated and may not be fully tested. If you find any issues, please open an issue on the respective repository.

| Language              | Repository                                        | Releases                                                                                         | Other                                                   |
| --------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------- |
| Python                | [GitHub](https://github.com/LukeHagar/plexpy)     | [PyPI](https://pypi.org/project/plex-api-client/)                                                | -                                                       |
| JavaScript/TypeScript | [GitHub](https://github.com/LukeHagar/plexjs)     | [NPM](https://www.npmjs.com/package/@lukehagar/plexjs) \ [JSR](https://jsr.io/@lukehagar/plexjs) | -                                                       |
| Go                    | [GitHub](https://github.com/LukeHagar/plexgo)     | [Releases](https://github.com/LukeHagar/plexgo/releases)                                         | [GoDoc](https://pkg.go.dev/github.com/LukeHagar/plexgo) |
| Ruby                  | [GitHub](https://github.com/LukeHagar/plexruby)   | [Releases](https://github.com/LukeHagar/plexruby/releases)                                       | -                                                       |
| Swift                 | [GitHub](https://github.com/LukeHagar/plexswift)  | [Releases](https://github.com/LukeHagar/plexswift/releases)                                      | -                                                       |
| PHP                   | [GitHub](https://github.com/LukeHagar/plexphp)    | [Releases](https://github.com/LukeHagar/plexphp/releases)                                        | -                                                       |
| Java                  | [GitHub](https://github.com/LukeHagar/plexjava)   | [Releases](https://github.com/LukeHagar/plexjava/releases)                                       | -                                                       |
| C#                    | [GitHub](https://github.com/LukeHagar/plexcsharp) | [Releases](https://github.com/LukeHagar/plexcsharp/releases)                                     | -                                                       |

## Project Structure

The main OpenAPI Specification is located in the root directory as [pms-spec.yaml](https://github.com/LukeHagar/plex-api-spec/blob/main/pms-spec.yaml). Which references 

 - [**/paths**](https://github.com/LukeHagar/plex-api-spec/tree/main/paths): The endpoints for the Plex Media Server API. Each endpoint is defined in a separate file.
 - [**/models**](https://github.com/LukeHagar/plex-api-spec/tree/main/models): The schema models used in the specification.
 - [**/parameters**](https://github.com/LukeHagar/plex-api-spec/tree/main/parameters): The parameters used in the specification.
 - [**/responses**](https://github.com/LukeHagar/plex-api-spec/tree/main/responses): The responses used in the specification.

In addition, there is a bundled single file OpenAPI Specification, [plex-media-server-spec-dereferenced.yaml](https://github.com/LukeHagar/plex-api-spec/blob/main/plex-media-server-spec-dereferenced.yaml) which is automatically bundled on any changes to the main specification.

## Styleguide

All spec files should adhere to the 3.1 OpenAPI Specification.
Every endpoint is defined in the /paths directory. Each endpoint is defined in a separate file. The file name should be the endpoint name with the method type. For example, the endpoint /library/sections is defined in the file /paths/library_sections.get.yaml. 

The file should contain data in the following order:

```yaml

[get/post/put/delete]:
  servers:
  security:
  tags:
  summary:
  description:
  operationId: lower snake case prefixed with the method type, post-user-sign-in-data
  parameters:
    $ref:
        name:
        description:
        required:
        schema:
  responses:
    2XX:
    4XX:
    5XX:
  
```

### Rules
 - A property in the response is only marked as required if it is always returned, regardless of the parameters sent with the request.

## Questions?

Reach out to me on the [Discord Server](https://discord.gg/mxqjsJHwUm)
