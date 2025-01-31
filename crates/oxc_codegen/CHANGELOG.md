# Changelog

All notable changes to this package will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project does not adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) until v1.0.0.

## [0.14.0] - 2024-06-12

### Refactor

- f98f777 linter: Add rule fixer (#3589) (Don Isaac)

## [0.13.4] - 2024-06-07

### Features

- 5c8e16c coverage: Second transformer build does not print typescript (#3561) (Dunqing)

### Bug Fixes

- affb2c8 codegen: Print indentation before directive (#3512) (Dunqing)

## [0.13.3] - 2024-06-04

### Bug Fixes

- 98c9029 codegen: Should be double quote for jsx attribute value (#3516) (Dunqing)
- d8063b6 codegen: Wrong escape string (#3514) (Dunqing)

### Refactor

- ddac2a0 codegen: Reduce allocation for print_unquoted_str (#3525) (Dunqing)

## [0.13.2] - 2024-06-03

### Features

- 0cdb45a oxc_codegen: Preserve annotate comment (#3465) (IWANABETHATGUY)

## [0.13.1] - 2024-05-22

### Features

- e2dd8ac syntax: Export `is_reserved_keyword` and `is_global_object` method (#3384) (Boshen)

### Bug Fixes

- a12ed0f codegen: Using declaration in for statement (#3285) (Don Isaac)

### Refactor

- 9ced605 parser: Start porting arrow function parsing from tsc (#3340) (Boshen)
- e879685 sourcemap: Using binary search to search original position (#3360) (underfin)

## [0.13.0] - 2024-05-14

### Features

- eefb66f ast: Add type to AccessorProperty to support TSAbractAccessorProperty (#3256) (Dunqing)

### Bug Fixes

- 0ba7778 parser: Correctly parse cls.fn<C> = x (#3208) (Dunqing)

### Refactor

- 7e1fe36 ast: Squash nested enums (#3115) (overlookmotel)
- 0185eb2 ast: Remove duplicate `TSNamedTupleMember` representation (#3101) (overlookmotel)
- a8af5de syntax: Move number related functions to number module (#3130) (Boshen)

## [0.12.5] - 2024-04-22

### Features

- 92d709b ast: Add `CatchParameter` node (#3049) (Boshen)

## [0.12.4] - 2024-04-19

### Features

- fd5002b codegen: Correctly print type-only imports/exports (#2993) (Dunqing)

## [0.12.1] - 2024-04-03

### Bug Fixes

- 28fae2e sourcemap: Using serde_json::to_string to quote sourcemap string (#2889) (underfin)

### Refactor

- 114f68e codegen: Make codegen sourcemap builder clearer (#2894) (underfin)

## [0.11.0] - 2024-03-30

### Features

- 243131d transformer: Numeric separator plugin. (#2795) (Ali Rezvani)- b199cb8 Add oxc sourcemap crate (#2825) (underfin)- a2cfc86 SourcemapVisualizer (#2773) (underfin)

### Bug Fixes

- 6177c2f codegen: Sourcemap token name should be original name (#2843) (underfin)
- b76b02d parser: Add support for empty module declaration (#2834) (Ali Rezvani)

### Performance

- 2be5f9d codegen: Avoid unnecessary copy (#2727) (underfin)
- d7004da sourcemap: Remove unnecessary binary search (#2728) (underfin)

### Refactor

- d9b77d8 sourcemap: Change sourcemap name to take a reference (#2779) (underfin)

## [0.10.0] - 2024-03-14

- c3477de ast: [**BREAKING**] Rename BigintLiteral to BigIntLiteral (#2659) (Arnaud Barré)

### Bug Fixes

- 9609c34 codegen: `CallExpression` sourcemap (#2717) (underfin)
- b453a07 parser: Parse named rest element in type tuple (#2655) (Arnaud Barré)

## [0.9.0] - 2024-03-05

- f66059e ast: [**BREAKING**] Align TSImportType with ESTree (#2578) (Arnaud Barré)

### Features

- 20c7bf7 ast: Add `AssignmentTargetRest` (#2601) (Boshen)
- 3efbbb2 ast: Add "abstract" type to `MethodDefinition` and `PropertyDefinition` (#2536) (Boshen)
- 8bb1084 codegen: Add sourcemap (#2565) (Boshen)

### Bug Fixes

- ea30fd5 codegen: Fix adding mapping to sourcemaps (#2590) (overlookmotel)
- fe29fa4 codegen: Correct sourcemaps when Windows line breaks + unicode (#2584) (overlookmotel)
- 517026b codegen: Correct sourcemaps when unicode chars (#2583) (overlookmotel)

### Performance

- b7f5c63 codegen: Speed up generating sourcemap mappings (#2597) (overlookmotel)
- 42fa8eb codegen: Speed up building sourcemap line tables (#2591) (overlookmotel)

### Refactor

- ef932a3 codegen: Clean up API around building sourcemaps (#2602) (Boshen)

## [0.8.0] - 2024-02-26

### Features

- 6b3b260 Codegen: Improve codegen (#2460) (Andrew McClenaghan)
- e6d536c codegen: Configurable typescript codegen (#2443) (Andrew McClenaghan)

### Bug Fixes

- 4327916 codegen: Remove redundant semicolon in PropertyDefinition (#2511) (Dunqing)
- b5deb9a codegen: When `async` is on the left-hand side of a for-of, wrap it in parentheses (#2407) (Dunqing)
- 384d5ac codegen: Lower the level of precedence in TaggedTemplateExpression (#2391) (Wenzhe Wang)

### Refactor

- 540f917 ast: Remove `TSEnumBody` (#2509) (Boshen)
- 9087f71 ast: S/TSThisKeyword/TSThisType to align with estree (Boshen)
- d08abc6 ast: S/NumberLiteral/NumericLiteral to align with estree (Boshen)
- e6b391a ast: S/ArrowExpression/ArrowFunctionExpression to align estree (Boshen)- a2c173d Remove `panic!` from examples (#2454) (Boshen)

## [0.7.0] - 2024-02-09

### Features

- 55011e2 codegen: Avoid printing comma in ArrayAssignmentTarget if the elements is empty (#2331) (Dunqing)

### Bug Fixes

- 2eb489e codegen: Format new expession + import expression with the correct parentheses (#2346) (Dunqing)
- 721f6cb codegen: Format new expression + call expression with the correct parentheses (#2330) (Boshen)

### Refactor

- 1822cfe ast: Fix BigInt memory leak by removing it (#2293) (Boshen)

## [0.6.0] - 2024-02-03

### Features

- 8ac0202 codegen: Keep shorthand in ObjectPattern and ObjectProperty (#2265) (Dunqing)
- fa555ce codegen: Change back to read raw (#2222) (Wenzhe Wang)
- 9333264 codegen: Print TemplateLiteral with `print_str` (#2207) (Wenzhe Wang)
- 1ee6d8c codegen: Move string test to codegen (#2150) (Wenzhe Wang)

### Bug Fixes

- 0c225a4 codegen: Print space before with clause in import (#2278) (Wenzhe Wang)
- d34650a codegen: Print necessary spaces for `ExportAllDeclaration` (#2190) (Yunfei He)
- 989ab88 codegen: Print `Directive` original string (#2157) (underfin)
- 29dc5e6 codegen: Add parenthesis in binary expression by precedence (#2067) (Wenzhe Wang)

### Refactor

- 766ca63 ast: Rename RestElement to BindingRestElement (#2116) (Dunqing)

## [0.5.0] - 2024-01-12

### Refactor

- a6717db formatter,linter,codegen: Remove oxc_formatter (#1968) (Boshen)

## [0.4.0] - 2023-12-08

### Features

- 9ff0ffc ast: Implement new proposal-import-attributes (#1476) (magic-akari)

### Refactor

- 1a576f6 rust: Move to workspace lint table (#1444) (Boshen)

## [0.3.0] - 2023-11-06

### Features

- cef78ac codegen: Indent inner class (#1085) (Wenzhe Wang)
- 854b55a codegen: Json strings proposal (#1039) (Boshen)
- 6c18b3e codegen: Beauty class print (#995) (Wenzhe Wang)
- e0ca09b codegen: Implement the basics of non-minifying codegen (#987) (Boshen)
- 809f050 codegen: Move minifying printer to codegen crate (#985) (Boshen)
- f28d96c codegen: Initialize the codegen crate and struct (#983) (Boshen)
- 2e2b758 playground: Add transform and minify (#993) (Boshen)
- e8a4e81 transformer: Implement some of jsx decode entities (#1086) (Boshen)
- af1a76b transformer: Implement some of needs_explicit_esm for typescript (#1047) (Boshen)
- dfee853 transformer: Add utils to make logical_assignment_operators pass (#1017) (Boshen)
- 678db1d transformer: ES2020 Nullish Coalescing Operator (#1004) (Boshen)- 094dfa5 Support filter exec snap (#1084) (Wenzhe Wang)- 0e91044 Adjust the order of print semicolon (#1003) (Wenzhe Wang)

### Bug Fixes

- 6295f9c ast: Jsx attribute value and text child should be jsx string (#1089) (Boshen)
- f32bf27 codegen: Fix some typescript codegen problems (#989) (Boshen)
- a455c81 linter: Revert changes to JSX attribute strings (#1101) (Boshen)

### Refactor

- 801d78a minifier: Make the minifier api only accept an ast (#990) (Boshen)
- 110059f rust: Change `RefCell.clone().into_inner()` to `RefCell.get()` (Boshen)

