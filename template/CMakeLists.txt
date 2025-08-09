set(template_src
    template.cpp
)

add_executable(template
    ${template_src}
)

set_target_properties(template PROPERTIES
    OUTPUT_NAME_DEBUG "templated"
)