# Setup and connection checks

Use [MCP for Blender’s upstream instructions](https://github.com/ahujasid/mcp-for-blender) to install the Blender add-on and configure its MCP server for Codex or Claude Code. The installed release and agent host determine the exact controls. Install the workflow skill separately. The desk stand example was verified on Blender 5.2.2 LTS with MCP for Blender 2.1.9.

1. Open the intended Blender file or a disposable scene. Start the local server using the add-on panel. Keep a local connection bound to loopback.
2. Confirm the server appears in the agent’s available tools. Use the live schema to find add-on status and scene inspection operations. On the tested server these are `get_addon_status` and `get_scene_info`. Confirm the Blender version, file or scene identity, expected objects, units, and whether the scene has unsaved changes.
3. Match the requested actions to the available tools before editing. The tested server exposed `execute_blender_code` and `look`. Use the host's configured permissions and the installed server's schema.

If discovery fails, check that the add-on is running and target the correct local connection. If the MCP server reports an add-on mismatch, follow the upstream guidance for that version. With multiple Blender instances, check which scene responds before sending any write.

For authorized local batch work, Blender's background mode can reopen a saved source, render a frame, or verify an export. It operates on the saved file. Ask which source should be used if the live scene has unsaved work. Keep temporary files and outputs scoped to the task.
