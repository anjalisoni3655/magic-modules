---
subcategory: "Dataplex"
description: |-
  A datasource to retrieve the data quality rules generated based on a data profile scan.
---


# `google_dataplex_data_quality_rules`
Retrieves the generated data quality rules for the creating a new data quality scan. 
For more information see
the [official documentation](https://cloud.google.com/dataplex/docs)
and [API](https://cloud.google.com/dataplex/docs/reference/rest/v1/projects.locations.dataScans/generateDataQualityRules).

## example

```hcl
data "google_dataplex_data_quality_rules" "dqrs" {
  project      = "my-project"
  location     = "use-central1"
  data_scan_id = "my-datascan-profile"
}
```

## Argument Reference

The following arguments are supported:

* `project` - (Required) The ID of the project in which the datascan belongs.

* `location` - (Required) The location where the referenced data profile scan resides.

* `data_scan_id` - (Required) The ID of the data profile scan which the generation of quality rules will be basing on.

## Attributes Reference

The attributes are exported:

* `rules` - (Computed) The list of generated data quality rules. For more details, please see the [datascan page](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/dataplex_datascan#nested_data_quality_spec_rules).