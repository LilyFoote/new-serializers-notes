# Construction
## Forms

* Creates the `form.base_fields` attribute
* Creates the `form.fields` attribute
* Modifies the `form.fields` members
* Parent field inheritance by subclassing

## Fields

* `Field.required` attribute/parameter

## Model Form Functions

* `modelform_factory` function
 * `fields`
 * `exclude`
 * `formfield_callback`
 * `localized_fields`
 * `labels`
 * `help_texts`
 * `error_messages`
 * `field_classes`
* `modelformset_factory` function
* `inlineformset_factory` function

## Formset Functions

* `formset_factory` function

# Existing data input
## Forms
### Unbound form
* `initial` dictionary parameter to `Form.__init__`
* Creates the `form.initial` attribute

## Fields

* `initial` parameter to `Field.__init__`
* Creates the `Field.initial` attribute
* `choices` parameter to `ChoiceField`
* `path` parameter to `FilePathField`
* `recursive` parameter to `FilePathField`
* `match` parameter to `FilePathField`
* `allow_files` parameter to `FilePathField`
* `allow_folders` parameter to `FilePathField`
* `choices` parameter to `MultipleChoiceField`
* `queryset` parameter to `ModelChoiceField`
* `queryset` parameter to `ModelMultipleChoiceField`

# New data input
## Forms
### Bound form
* `data` dictionary parameter to `Form.__init__`
* Creates the `form.changed_data` attribute
* `file_data` dictionary parameter to `Form.__init__`

## Fields

* `Field.localize` attribute/parameter
* `Field.disabled` attribute/parameter

## Widgets

* `MultiWidget.decompress` method
* `Widget.value_from_datadict` method

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

## Fields

* `Field.clean` method
* `Field.has_changed` method
* `max_length` parameter to `CharField`
* `min_length` parameter to `CharField`
* `strip` parameter to `CharField`
* `choices` parameter to `ChoiceField`
* `coerce` parameter to `TypedChoiceField`
* `input_formats` parameter to `DateField`
* `input_formats` parameter to `DateTimeField`
* `max_value` parameter to `DecimalField`
* `min_value` parameter to `DecimalField`
* `max_digits` parameter to `DecimalField`
* `decimal_places` parameter to `DecimalField`
* `max_length` parameter to `EmailField`
* `min_length` parameter to `EmailField`
* `max_length` parameter to `FileField`
* `allow_empty_file` parameter to `FileField`
* `path` parameter to `FilePathField`
* `recursive` parameter to `FilePathField`
* `match` parameter to `FilePathField`
* `max_value` parameter to `FloatField`
* `min_value` parameter to `FloatField`
* `max_value` parameter to `IntegerField`
* `min_value` parameter to `IntegerField`
* `protocol` parameter to `GenericIPAddressField`
* `unpack_ipv4` parameter to `GenericIPAddressField`
* `choices` parameter to `MultipleChoiceField`
* `coerce` parameter to `TypedMultipleChoiceField`
* `regex` parameter to `RegexField`
* `max_length` parameter to `RegexField`
* `min_length` parameter to `RegexField`
* `strip` parameter to `RegexField`
* `allow_unicode` parameter to `SlugField`
* `input_formats` parameter to `TimeField`
* `max_length` parameter to `URLField`
* `min_length` parameter to `URLField`
* `fields` parameter to `ComboField`
* `MultiValueField`
 * `fields` parameter
 * `require_all_fields` parameter
 * `compress` method
* `input_date_formats` parameter to `SplitDateTimeField`
* `input_time_formats` parameter to `SplitDateTimeField`
* `queryset` parameter to `ModelChoiceField`
* `queryset` parameter to `ModelMultipleChoiceField`

## Form and field validation

* `raise ValidationError`
* `Field.to_python` method
* `Field.validate` method
* `Field.run_validators` method
* `Field.clean` method
* `clean_<fieldname>` methods on `Form` subclasses
* `form.clean` method
 * optional `cleaned_data` return
 * `self.cleaned_data`
* `code` parameter to `ValidationError`
* `params` parameter to `ValidationError`
* `Field.default_validators` attribute
* `validators` parameter to `Field`
* `form.add_error`

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

## Fields

* `Field.label` attribute/parameter
* `Field.label_suffix` attribute / parameter
* Renders the `Field.initial` values
* `Field.widget` attribute/parameter
* `Field.help_text` attribute/parameter
* `Field.error_messages` attribute/parameter
* `Field.validators` attribute/parameter
* `Field.localize` attribute/parameter
* `Field.disabled` attribute/parameter
* `Field.has_changed` method
* `choices` parameter to `ChoiceField`
* `empty_value` parameter to `TypedChoiceField`
* `input_formats` parameter to `DateField`
* `input_formats` parameter to `DateTimeField`
* `path` parameter to `FilePathField`
* `recursive` parameter to `FilePathField`
* `match` parameter to `FilePathField`
* `choices` parameter to `MultipleChoiceField`
* `empty_value` parameter to `TypedMultipleChoiceField`
* `input_formats` parameter to `TimeField`
* `empty_label` parameter to `ModelChoiceField`
* `to_field_name` parameter to `ModelChoiceField`
* `ModelChoiceField.label_from_instance` method
* `ModelMultipleChoiceField.label_from_instance` method

## Model Form Functions

* `modelform_factory` function
 * `widgets`
 * `labels`
 * `help_texts`

## Formset Functions

* `formset_factory` function

# Data output
## Forms
### Bound form

* `form.has_changed` method
* Uses the `form.changed_data` attribute
* Uses the `form.cleaned_data` attribute

## Fields

* `Field.has_changed` method
* `path` parameter to `FilePathField`
* `recursive` parameter to `FilePathField`
* `match` parameter to `FilePathField`
