licenses(["notice"])

java_library(
  name = "auto_value",
  exported_plugins = [
    ":auto_annotation_plugin",
    ":auto_value_plugin",
  ],
  visibility = ["//visibility:public"],
  exports = ["@auto_value//jar"],
  neverlink = True,
)

java_library(
  name = "auto_value_annotations",
  exported_plugins = [
    ":auto_annotation_plugin",
    ":auto_value_plugin",
  ],
  visibility = ["//visibility:public"],
  exports = ["@auto_value_annotations//jar"],
)

java_plugin(
  name = "auto_annotation_plugin",
  processor_class = "com.google.auto.value.processor.AutoAnnotationProcessor",
  deps = [
    "@auto_value_annotations//jar",
    "@auto_value//jar",
  ],
)

java_plugin(
  name = "auto_value_plugin",
  processor_class = "com.google.auto.value.processor.AutoValueProcessor",
  deps = [
    "@auto_value_annotations//jar",
    "@auto_value//jar",
  ],
)

