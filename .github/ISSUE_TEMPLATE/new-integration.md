name: New Tool Integration 2
description: Keptn should integrate with this tool. Let's make it happen...
title: "[integration]: "
labels: ["integration"]
assignees:
  - agardnerit
body:
  - type: markdown
    attributes:
      value: |
        Keptn is designed to work with any tool. Use this form to request a new integration for a tool you use.

        Before you start!

        - If your tool is already containerised or can run as a script (PowerShell, Shell or Python), look into the [job executor service](https://github.com/keptn-contrib/job-executor-service).
        - If you only need to notify a tool of a Keptn event, use the [webhook service](https://github.com/keptn/keptn/tree/master/webhook-service) (comes preinstalled with Keptn).

  - type: input
    id: tool
    attributes:
      label: "Tool / Product Name"
      description: "What tool / product / project would you like to integrate with?"
    validations:
      required: true

  - type: textarea
    id: tool_how
    attributes:
      label: "Goal"
      description: "What are you looking to achieve with this integration?"
      placeholder: "eg. I want to trigger this tool from a Keptn task"
      render: shell

  - type: checkboxes
    id: joined_slack
    attributes:
      label: "#help-integrations on Slack"
      description: "I have joined #help-integrations channel on [Keptn Slack](https://slack.keptn.sh)."
      options:
        - label: "Yes"
          required: true

  - type: checkboxes
    id: existing_integrations
    attributes:
      label: No Existing Integrations
      description: I have checked [here](https://keptn.sh/docs/integrations) that an integration does not already exist.
      options:
        - label: "Yes"
          required: true

  - type: dropdown
    id: assisted
    attributes:
      label: Assisted
      description: |
        Are you willing to assist during development of this integration?
        Integration requests that are "assisted" (that is, the requester [you] are willing to assist in developing this integration) will have a higher priority.
      options:
        - "Yes"
        - "No"
    validations:
      required: true

  - type: input
    id: contact
    attributes:
      label: Contact Details
      description: How can we get in touch with you if we need more info?
      placeholder: ex. email@example.com
    validations:
      required: false

  - type: textarea
    id: other_info
    attributes:
      label: Any other info?
      description: Any other info that might assist in developing / prioritising this integration?
