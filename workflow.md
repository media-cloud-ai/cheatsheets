---
title: MCAI Workflow
category: Media-Cloud-AI
layout: 2017/sheet
tags: [Featured]
updated: 2021-01-25
weight: -10
intro: 
---

Getting started
---------------
{: .-one-column}
<!-- {: .-three-column} -->

### Root level

| Json key         | Required   | Example   | Description                                          |
| ---              | ---        | ---       | ---                                                  |
| `schema_version` | `required` | `1.8`     | Version of the schema that describe this workflow    |
| `steps`          | `required` |           | Array of [steps](#step) defined in this workflow     |
| `major_version`  | `required` | `1`       | Major version of this workflow                       |
| `minor_version`  | `required` | `0`       | Minor version of this workflow                       |
| `micro_version`  | `required` | `0`       | Micro version of this workflow                       |
| `identifier`     | `required` | `0`       | The Identifier of the workflow, used to reference it |
| `rights`         | `required` |           | Array of rights that allow action on this workflow   |
| `tags`           | `optional` | `["tag"]` | List of tags to classify the worklow                 |
| `is_live`        | `optional` | `true`    | Switch the workflow as live (default is not live)    |

Step
---------------
{: .-tree-column}

### Step

| Json key            | Description                   |
| ---                 | ---                           |
| `icon`              | Icon that represents the step |
| `id`                | Unique index of this step     |
| `mode`              | Mode of the step              |

### Step mode

| Value          | Description                              |
| ---            | ---                                      |
| `one_for_one`  | (Default) One job for each source path   |
| `one_for_many` | One job for multiple source paths        |
| `notification` | Specific step that generate notification |

