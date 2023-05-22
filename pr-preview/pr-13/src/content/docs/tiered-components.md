---
layout: docs
title: Tiered Components
permalink: /docs/tiered-components
---

## Open Data Hub Components

As the AI/ML landscape has matured, Open Data Hub is refocusing on providing an opinionated deployment of components to focus on providing a core part of the AI/ML workflow while also supporting an open community model where ODH maintainers will officially support a well defined integrated ODH Core functionality with integration points for additional components that have a designated maintainers and clearly defined levels of support.

Under the new model ODH will support a Tiered component structure that clearly defines the requirements for a component integrating with Open Data Hub.

### Tiered Architecture
All components/projects will be required to designate dedicated maintainers/owners that will be responsible for meeting the requirements or support of the respective tiers

#### ODH Core (Tier 0) - opendatahub-io
* Available under [https://github.com/opendatahub-io](https://github.com/opendatahub-io)
* These are integrated components that will provide functionality that the ODH Community decides is a core part of the Data Science workflow with an opinionated deployment that provides a seamless user experience.
* These components will be included as part of the downstream offering provided by Red Hat
* Requirements:
  * Long term support by ODH Maintainers for the life of the component
  * Regular updates
  * Full testsuite - Unit, Functional, Integration, Regression
  * Security scanning for all container images
* Component list based on components deployed downstream
  * Open Data Hub Operator
  * Notebook Controller
  * Default ODH notebook images
  * ODH Dashboard
  * Data Science Pipelines
  * [https://opendatahub.io](https://opendatahub.io)

#### ODH Incubating (Tier 1) - opendatahub-io
* Available under [https://github.com/opendatahub-io](https://github.com/opendatahub-io)
* These components have the same requirements as ODH Core components but they will not be included as part of the default core deployment.  The focus of Tier 1 is to incubate projects/features that will be owned by the Open Data Hub community and a candidate for ODH Core OR provide advanced functionality that is of strong interest to the community at large. These incubated features could
* Requirements:
  * Same requirements as ODH Core components so that upon promotion no additional changes are required.

#### ODH Contrib (Tier 2) - opendatahub-io-contrib
* Available under [https://github.com/opendatahub-io-contrib](https://github.com/opendatahub-io-contrib)
* These are components that want to integrate with Open Data Hub but are not candidates to provide ODH Core functionality –OR– the maintainer is unable to commit to the requirements of an ODH Incubating component to provide long term support
* Requirements:
  * A basic testsuite will be required as part of Tier 2 acceptance as part of a simple smoke test to verify that the application is still compatible with each ODH release.  Components that fail to validate successfully after <X> number of ODH releases with no updates/fixes from the designated maintainer(s) will be archived/deprecated
* Proposed List
  * Apache Spark on OpenShift
  * Apache Airflow on OpenShift
  * Ray.io