# Sparkplug

Sparkplug®, Sparkplug Compatible, and the Sparkplug Logo are trademarks of the Eclipse Foundation.

Sparkplug is a specification for MQTT enabled devices and applications to send and receive messages in a stateful way.
While MQTT is stateful by nature it doesn't ensure that all data on a receiving MQTT application is current or valid.
Sparkplug provides a mechanism for ensuring that remote device or application data is current and valid.

Sparkplug A was the original version of the Sparkplug specification and used Eclipse Kura's protobuf definition for
payload encoding.  However, it was quickly determined that this definition was too limited to handle the metadata that
typical Sparkplug payloads require.  As a result, Sparkplug B was developed to add additional features and capabilities
that were not possible in the original Kura payload definition.  These features include:
* Complex data types using templates
* Datasets
* Richer metrics with the ability to add property metadata for each metric
* Metric alias support to maintain rich metric naming while keeping bandwidth usage to a minimum
* Historical data
* File data

Sparkplug B Specification:
https://www.eclipse.org/tahu/spec/Sparkplug%20Topic%20Namespace%20and%20State%20ManagementV2.2-with%20appendix%20B%20format%20-%20Eclipse.pdf

# Eclipse Tahu

Eclipse Tahu provide client libraries and reference implementations in various languages and for various devices
to show how the device/remote application must connect and disconnect from the MQTT server using the Sparkplug
specification explained below.  This includes device lifecycle messages such as the required birth and last will &
testament messages that must be sent to ensure the device lifecycle state and data integrity.

Source code: https://github.com/eclipse/tahu

# Contributing
Contributing to the Sparkplug Specification is easy and contributions are welcome. In order to submit a pull request (PR) you must follow these steps. Failure to follow these steps will likely lead to the PR being rejected.
1. Sign the Eclipse Contributor Agreement (ECA): https://accounts.eclipse.org/user/eca
2. Make sure the email tied to your Github account is the same one you used to sign the ECA.
3. Submit your PR against the develop branch of the repository. PRs against master will not be accepted: https://github.com/eclipse/sparkplug/tree/develop
4. Sign off on your PR using the '-s' flag. For example: 'git commit -m"My brief comment" ChangedFile'
5. Make sure to include any important context or information associated with the PR in the PR submission. Keep your commit comment brief.
6. Make sure Java code follows the styles provided by the 'Sparkplug Formatter' for the Eclispe IDE
<details><summary>Sparkplug Formatter</summary>
<p>
  
```xml
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<profiles version="21">
    <profile kind="CodeFormatterProfile" name="Sparkplug Formatter" version="21">
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_ellipsis" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_enum_declarations" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_allocation_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_for_statment" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.new_lines_at_block_boundaries" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_constructor_declaration_parameters" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.insert_new_line_for_parameter" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_package" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_parens_in_enum_constant" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_while" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_parens_in_annotation_type_member_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_javadoc_comments" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.indentation.size" value="4"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_enum_constant_declaration" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_semicolon_in_for" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.align_with_spaces" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.continuation_indentation" value="2"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_before_code_block" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_switch_case_expressions" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_after_package" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_multiple_local_declarations" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_enum_constant" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_angle_bracket_in_parameterized_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.indent_root_tags" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_or_operator_multicatch" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.enabling_tag" value="@formatter:on"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.count_line_length_from_starting_position" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_record_components" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_throws_clause_in_method_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_parameter" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_multiplicative_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_then_statement_on_same_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_explicitconstructorcall_arguments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_prefix_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_brace_in_array_initializer" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_angle_bracket_in_type_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_method" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_parameterized_type_references" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_logical_operator" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_parenthesized_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_annotation_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_record_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_enum_constant" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_multiplicative_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_and_in_type_parameter" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_parens_in_method_invocation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_assignment_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_type_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_for" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.preserve_white_space_between_code_and_line_comments" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_local_variable" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_abstract_method" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_enum_constant_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.align_variable_declarations_on_columns" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_method_invocation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_union_type_in_multicatch" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_at_beginning_of_method_body" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_else_statement_on_same_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_catch_clause" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_parameterized_type_reference" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_array_initializer" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_explicit_constructor_call" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_multiplicative_operator" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_anonymous_type_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_switch_case_expressions" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_shift_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_body_declarations_compare_to_annotation_declaration_header" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_block" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_at_end_of_code_block" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_bitwise_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.put_empty_statement_on_new_line" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_parameters_in_constructor_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_type_parameters" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_compact_loops" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.clear_blank_lines_in_block_comment" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_simple_for_body_on_same_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_at_end_of_file_if_missing" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_array_initializer" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_unary_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.format_line_comment_starting_on_first_column" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_annotation" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_ellipsis" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_semicolon_in_try_resources" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_colon_in_assert" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_enum_constant" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_and_in_type_parameter" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_parenthesized_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.text_block_indentation" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.align_type_members_on_columns" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_assignment" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_module_statements" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_body_declarations_compare_to_type_header" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_parens_in_method_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.align_tags_names_descriptions" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_enum_constant" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_if_then_body_block_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_first_class_body_declaration" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_before_closing_brace_in_array_initializer" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_constructor_declaration_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.format_guardian_clause_on_one_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_if" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.align_assignment_statements_on_columns" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_block_in_case" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_constructor_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_conditional_expression_chain" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_header" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_type_annotations" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_allocation_expression" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_assertion_message_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_switch" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_method_declaration" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.align_fields_grouping_blank_lines" value="2147483647"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.new_lines_at_javadoc_boundaries" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_bitwise_operator" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_annotation_type_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_for" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_resources_in_try" value="80"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_selector_in_method_invocation" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.never_indent_block_comments_on_first_column" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_synchronized" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_allocation_expression" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_source_code" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_array_initializer" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_field" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_at_in_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_method" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_superclass_in_type_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_parenthesized_expression_in_throw" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_not_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_type_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_brace_in_array_initializer" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_parenthesized_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_html" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_at_in_annotation_type_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_method_delcaration" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_compact_if" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_empty_lines" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_type_arguments" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_unary_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_enum_constant" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_annotation" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_enum_declarations" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_package" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_switchstatements_compare_to_switch" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_before_else_in_if_statement" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_assignment_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_label" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_body_declarations_compare_to_enum_declaration_header" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_conditional" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_method_declaration_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_cast" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_arrow_in_switch_case" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_before_while_in_do_statement" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_bracket_in_array_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_body_declarations_compare_to_record_header" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_angle_bracket_in_parameterized_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_opening_brace_in_array_initializer" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_breaks_compare_to_cases" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_method_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_bitwise_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_try" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_lambda_arrow" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_method_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.indent_tag_description" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_imple_if_on_one_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_record_constructor" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_enum_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_brackets_in_array_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_angle_bracket_in_type_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_string_concatenation" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_semicolon_in_for" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_bracket_in_array_allocation_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_multiple_fields" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_enum_constant_arguments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_prefix_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_array_initializer" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_shift_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_method_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_type_parameters" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_catch" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_shift_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_braces_in_array_initializer" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_multiple_local_declarations" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_simple_do_while_body_on_same_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_annotation_type_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_record_components" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_outer_expressions_when_nested" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_closing_paren_in_cast" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_synchronized" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_annotation_type_member_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_expressions_in_for_loop_header" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_additive_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_simple_getter_setter_on_one_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_while" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_angle_bracket_in_type_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_string_concatenation" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_lambda_arrow" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.join_lines_in_comments" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_record_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_relational_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_multiple_field_declarations" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_between_import_groups" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_at_in_annotation_type_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_logical_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_method_invocation" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_after_imports" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.insert_new_line_before_root_tags" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_record_declaration" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_method_declaration_throws" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_switch_statement" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_postfix_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_for_increments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_type_arguments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_arrow_in_switch_default" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_for_inits" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.disabling_tag" value="@formatter:off"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_enum_constants" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_imports" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_at_end_of_method_body" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_if_while_statement" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_closing_brace_in_block" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_parenthesized_expression_in_return" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_arrow_in_switch_case" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_field" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_between_type_declarations" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_for" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_catch" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_switch" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_anonymous_type_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.never_indent_line_comments_on_first_column" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_for_inits" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_statements_compare_to_block" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_anonymous_type_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_question_in_wildcard" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_method_invocation_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_switch" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.align_tags_descriptions_grouped" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.line_length" value="120"/>
        <setting id="org.eclipse.jdt.core.formatter.use_on_off_tags" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_method_body_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_brackets_in_array_allocation_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_loop_body_block_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_enum_constant" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_method_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_colon_in_for" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_type_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_closing_angle_bracket_in_type_arguments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_additive_operator" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_multiple_field_declarations" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_record_constructor" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_relational_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_superinterfaces" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_record_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_default" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_question_in_conditional" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_constructor_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_lambda_body" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.compact_else_if" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_type_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_catch" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_method_invocation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_method_invocation_arguments" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_method_invocation" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_throws_clause_in_constructor_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_before_catch_in_try_statement" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_try" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_parameter" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.clear_blank_lines_in_javadoc_comment" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_relational_operator" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_expressions_in_array_initializer" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_empty_lines_to_preserve" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_colon_in_case" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_additive_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_if" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_type_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_string_concatenation" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_line_comments" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_record_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_colon_in_labeled_statement" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_after_code_block" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_superinterfaces_in_type_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_conditional_expression" value="48"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_after_annotation_on_type" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_type" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_block" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_local_variable" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_enum_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_arrow_in_switch_default" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.insert_new_line_between_different_tags" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_additive_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_method_invocation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_while" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.join_wrapped_lines" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_between_empty_parens_in_constructor_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_field" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_conditional_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_switchstatements_compare_to_cases" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_bracket_in_array_allocation_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_synchronized" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_shift_operator" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.use_tabs_only_for_leading_indentations" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_try_clause" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_code_block_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_constructor_declaration_throws" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_record_components" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.tabulation.size" value="4"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_bitwise_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_bracket_in_array_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_colon_in_conditional" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_try" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_semicolon_in_try_resources" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.continuation_indentation_for_array_initializer" value="2"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_question_in_wildcard" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_record_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_superinterfaces_in_enum_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_assignment_operator" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_labeled_statement" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_switch" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_superinterfaces" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_method_declaration_parameters" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_closing_angle_bracket_in_type_parameters" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_lambda_body_block_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_annotations_on_method" value="49"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_parameterized_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_record_constructor_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_record_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_empty_array_initializer_on_one_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_assertion_message" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_constructor_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_new_chunk" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_bracket_in_array_allocation_expression" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_constructor_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_angle_bracket_in_parameterized_type_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_angle_bracket_in_type_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_assert" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_member_type" value="1"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_logical_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_arguments_in_qualified_allocation_expression" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_superinterfaces_in_record_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_if" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_semicolon" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_relational_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_postfix_operator" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_angle_bracket_in_type_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_cast" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.format_block_comments" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.alignment_for_parameters_in_method_declaration" value="16"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_method_declaration_throws" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_after_last_class_body_declaration" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_statements_compare_to_body" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_simple_while_body_on_same_line" value="false"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_logical_operator" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_between_statement_group_in_switch" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_bracket_in_array_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_comma_in_annotation" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_enum_constant_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.parentheses_positions_in_lambda_declaration" value="common_lines"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_colon_in_case" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_bracket_in_array_reference" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.keep_enum_declaration_on_one_line" value="one_line_never"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_method_declaration" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_enum_constant" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.brace_position_for_type_declaration" value="end_of_line"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_multiplicative_operator" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.blank_lines_before_package" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_for" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_for_increments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_enum_constant" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_explicitconstructorcall_arguments" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_paren_in_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.indent_body_declarations_compare_to_enum_constant_header" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_brace_in_constructor_declaration" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_comma_in_constructor_declaration_throws" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_closing_angle_bracket_in_type_parameters" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_question_in_conditional" value="insert"/>
        <setting id="org.eclipse.jdt.core.formatter.comment.indent_parameter_description" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.number_of_blank_lines_at_beginning_of_code_block" value="0"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_new_line_before_finally_in_try_statement" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.tabulation.char" value="tab"/>
        <setting id="org.eclipse.jdt.core.formatter.wrap_before_string_concatenation" value="true"/>
        <setting id="org.eclipse.jdt.core.formatter.lineSplit" value="120"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_after_opening_paren_in_annotation" value="do not insert"/>
        <setting id="org.eclipse.jdt.core.formatter.insert_space_before_opening_paren_in_switch" value="insert"/>
    </profile>
</profiles>
```
  
</p>
</details>