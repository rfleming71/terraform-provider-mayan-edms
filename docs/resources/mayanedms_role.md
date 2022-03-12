---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "mayanedms_role Resource - terraform-provider-mayan-edms"
subcategory: ""
description: |-
  
---

# mayanedms_role (Resource)



## Example Usage

```terraform
resource "mayanedms_role" "automated" {
  label  = "Automated"
  groups = [mayanedms_group.automated.id]
  permissions = [
    "cabinets.cabinet_add_document",
    "comments.comment_create",
    "document_states.workflow_transition",
    "document_states.workflow_view",
    "documents.document_edit",
    "documents.document_properties_edit",
    "documents.document_version_edit",
    "documents.document_version_view",
    "documents.document_view",
    "metadata.metadata_document_add",
    "metadata.metadata_document_edit",
    "metadata.metadata_document_remove",
    "metadata.metadata_document_view",
    "metadata_setup.metadata_type_view",
    "ocr.ocr_content_view",
    "search.search_tools",
    "tags.tag_attach",
    "tags.tag_remove",
    "tags.tag_view",
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **label** (String) A short text describing the role.

### Optional

- **groups** (Set of Number) Add groups to be part of a role. They will inherit the role's permissions and access controls.
- **id** (String) The ID of this resource.
- **permissions** (Set of String)

