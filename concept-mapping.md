# Construction
## Forms

* Creates the `form.base_fields` attribute
* Creates the `form.fields` attribute
* Modifies the `form.fields` members
* Parent field inheritance by subclassing

# Existing data input
## Forms
### Unbound form
* `initial` dictionary parameter to `Form.__init__`
* Creates the `form.initial` attribute

# New data input
## Forms
### Bound form
* `data` dictionary parameter to `Form.__init__`
* Creates the `form.changed_data` attribute
* `file_data` dictionary parameter to `Form.__init__`

# Validation / data processing
## Forms
### Bound form
* `form.clean` method
* `form.is_valid` method
* Creates the `form.errors` attribute
* `form.add_error` method
* `form.has_error` method ??
* `form.non_field_errors` method ??
* `form.has_changed` method
* Uses the `form.changed_data` attribute
* Creates the `form.cleaned_data` attribute

# Rendering
## Forms

* Uses the `form.is_bound` attribute
* Uses the `form.fields` attribute
* `form.__str__` method
* `form.as_p` method
* `form.as_ul` method
* `form.as_table` method
* Set the `form.error_css_class`
* Set the `form.required_css_class`
* `form.auto_id` attribute / parameter
* `form.label_suffix` attribute / parameter
* `form.field_order` attribute / parameter
* `form.order_fields` method
* `error_class` parameter to `Form.__init__` (`ErrorList` class/subclass)
* `form[field]` (`BoundField` instance)
* `BoundField.__str__` method
* `iter(form)` (`BoundField` instances)
* `BoundField.auto_id` attribute
* `BoundField.data` attribute ??
* `BoundField.errors` attribute
* `BoundField.field` attribute ??
* `BoundField.form` attribute ??
* `BoundField.help_text` attribute
* `BoundField.html_name` attribute
* `BoundField.id_for_label` property
* `BoundField.is_hidden` attribute
* `BoundField.label` attribute
* `BoundField.name` attribute
* `BoundField.as_hidden` method
* `BoundField.as_widget` method
* `BoundField.css_classes` method
* `BoundField.label_tag` method
* `BoundField.value` method
* `Field.get_bound_field` method
* `form.is_multipart` method
* `form.prefix` attribute

### Unbound form
* Uses the `form.initial` attribute

### Bound form
* Uses the `form.errors` attribute
 * `form.errors.as_data` method
 * `form.errors.as_json` method
* `form.has_error` method
* `form.non_field_errors` method
* `form.has_changed` method ??
* Uses the `form.changed_data` attribute ??

# Data output
## Forms
### Bound form

* `form.has_changed` method
* Uses the `form.changed_data` attribute
* Uses the `form.cleaned_data` attribute
