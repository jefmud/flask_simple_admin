# flask_simple_admin
simple MongoDB administration panel

## Flask Simple Admin 
- implements Admin class user interface
for use with the Flask framework.

There is some refactoring from Minimus_admin and Bottle_simple_admin.
must have either MontyDB (stand-alone) or PyMongo (to a MongoDB instance)
if you expect it to do anything

## License - MIT License

no guarantees of suitability for your app

## version 0.0.1
   Added support for per collection schema
   requires TEMPLATE_PATH to find jinja2 templates (that's good that they are separate)
  TEMPLATE_PATH[:] = ['templates', 'bottle_simple_admin/templates']

## version 0.0.2
  Added support for v2 schema handles UI labels (backward compatible)

 version 0.0.3 - Added support for v3 schema (backward compatible to all)
   can add data via schema, schema supports JSON nesting with a
   dot notation. (reflected in UI)
  unfortunately more complex logic and Admin.edit_schema and Admin.edit_fields
   Admin.edit_fields() - more complex since it handles all
                    field-based and schema-based saves (new and existing)
      import known limitation - you cannot add a nested type without a schema!
   This version also allows support of a number of HTML5 input types

## version 0.0.4 - Added support for list-views.
    A list-view is a simple schema extension that allows the user to define
    a list-view by using a simple caret ('^') prefix in front of the field
    that will show up in a list view.  It paves the way for data required
    type validation in the
    next version by use of an asterisk ('*') in front of a required (validated) field
