CoreFlow
============================================================

Free CPU Power Management Utility for Windows 11

Manage CPU frequency limits and turbo/boost behavior with simple, straightforward controls.

Developed by MasaTech / Itachi, Spica and Mahiru


============================================================
1. INTRODUCTION
============================================================

CoreFlow is a free CPU power-management utility for Windows 11, supporting Intel CPUs and AMD Ryzen CPUs.

It uses standard Windows power-management features to adjust maximum CPU frequency, minimum processor performance, and turbo/boost behavior.

Settings can be configured separately for AC power (plugged in) and DC power (battery operation).

CoreFlow automatically detects the CPU model. When the model exactly matches an entry in its embedded CPU specification database, the application refers to the registered base and maximum frequencies.

CoreFlow is intended for users who want to adjust CPU performance, heat generation, and power-management behavior according to their system and usage requirements.

The application does not directly control CPU voltage, change BIOS settings, or perform overclocking.

Instead, it applies settings through Windows power management and allows Windows and the CPU to manage actual operating frequencies.

CoreFlow is completely free to use.

No license key, activation, or trial period is required.


============================================================
2. PRODUCT RENAMING AND FREE RELEASE
============================================================

[2-1. From Astra CPU Silencer Standard to CoreFlow]

The application previously distributed as:

Astra CPU Silencer Standard

has been renamed to:

CoreFlow

This change represents more than a product rename.

CoreFlow builds on the development and testing performed during the Astra CPU Silencer project, while adopting a revised approach to CPU frequency management and software distribution.

The previous Astra CPU Silencer Standard edition included a trial period and license activation.

CoreFlow is now distributed as free software without those requirements.

The new name also reflects the application's focus on managing CPU power and performance behavior through Windows power-management features.


[2-2. Why CoreFlow Is Now Free]

During development and testing, we investigated how Windows manages CPU operating frequencies, processor performance states, and turbo/boost behavior.

We observed that the results of CPU frequency control can differ depending on the selected Windows power plan and the PC's hardware and software configuration.

Even when identical frequency settings are applied, actual CPU behavior may vary.

Windows manages processor performance through several mechanisms, including:

- Windows power plans
- Processor performance policies
- CPU performance-state control
- CPU firmware
- BIOS settings
- Manufacturer-specific power-management features
- Thermal and electrical power limits

These mechanisms can affect how frequency limits and boost settings are interpreted and applied.

As a result, it is not possible to guarantee identical CPU frequency behavior across all supported systems.

After reviewing these limitations, we decided to redesign the free edition around a defined maximum-frequency input range.

Within that range, users can adjust CPU power-management settings according to their own environment.

We also decided to make CoreFlow available without license fees or trial restrictions.

Our goal is to provide an accessible utility that allows users to explore CPU power-management settings without requiring a purchase.


[2-3. Frequency Management Philosophy]

CoreFlow uses Windows power-management settings to request a maximum CPU frequency limit.

Rather than attempting to force the CPU to operate at one fixed clock speed, CoreFlow allows Windows and the CPU to manage operating frequency within the applicable power-management constraints.

For CPUs verified by the embedded specification database, the free edition uses a manual maximum-frequency input ceiling based on the CPU's rated maximum frequency minus 1200 MHz.

This restriction defines the available manual input range in CoreFlow.

It does not mean that the CPU is permanently limited to that frequency.

Users can also select 0 MHz for Maximum Frequency.

A value of 0 MHz means that no maximum-frequency cap is requested through that Windows setting.

This allows Windows and the CPU to manage operating frequency without an additional maximum-frequency restriction imposed by CoreFlow.

However, other Windows, CPU, firmware, thermal, and power-management limitations remain effective.

CoreFlow does not guarantee that the CPU will reach its highest advertised frequency.


[2-4. Differences from the Previous Astra Edition]

CoreFlow differs from Astra CPU Silencer Standard in several important ways.

- The product name is now CoreFlow.
- CoreFlow is free to use.
- License registration is no longer required.
- The previous 60-minute trial restriction has been removed.
- Maximum-frequency manual input limits have been revised.
- The free edition uses a ceiling based on the verified CPU's rated maximum frequency minus 1200 MHz.
- The application remains focused on Windows CPU power-management controls.

Some settings and features available in the previous Astra edition may differ from those in CoreFlow.

Users upgrading from Astra CPU Silencer Standard should review the new frequency restrictions and operating instructions before applying settings.


============================================================
3. MAIN FEATURES
============================================================

CoreFlow provides the following features:

- Maximum CPU frequency control
- Minimum processor performance control
- Processor Performance Boost Mode control
- Separate AC and DC settings
- Windows power-plan selection and switching
- Automatic CPU model detection
- Embedded CPU specification database
- Restore Original Settings
- Built-in update checking
- Diagnostic log saving

CoreFlow changes CPU power-management settings through standard Windows mechanisms.

It does not use a custom kernel driver or directly modify CPU voltage, CPU multipliers, or BIOS settings.

After settings are applied, Windows and the CPU continue to manage actual clock frequencies and boost behavior according to operating conditions.

CoreFlow does not lock the CPU to a fixed clock frequency.

It is not an overclocking utility.


============================================================
4. SUPPORTED ENVIRONMENT
============================================================

Supported operating system:
Windows 11 64-bit

Supported processors:
Intel CPUs
AMD Ryzen CPUs

Required privileges:
Administrator privileges

Price:
Free

License activation:
Not required

Usage time limit:
None


[Windows 10 Compatibility]

Windows 10 may work, but it is not officially supported.

Official support is provided for Windows 11.


[System Compatibility]

Actual behavior may vary depending on:

- CPU model and architecture
- BIOS and firmware
- Windows version
- Windows power plans
- CPU performance-control mechanisms
- Manufacturer-specific power-management features
- System cooling and thermal conditions

Even systems using the same CPU model may behave differently.

CoreFlow cannot guarantee identical results across all PC configurations.


============================================================
5. FREQUENCY LIMITS IN THE FREE EDITION
============================================================

CoreFlow includes input restrictions for maximum and minimum CPU frequency settings.

These restrictions define the values that can be entered through the application.

They do not guarantee that the CPU will operate continuously at the entered frequency.


[5-1. Maximum Frequency Input Limit]

Maximum-frequency values use 100 MHz increments.

CoreFlow identifies the CPU model and compares it with its embedded CPU specification database.

Only when the CPU model matches a database entry exactly does CoreFlow use the registered maximum frequency.

In the free edition, the manual maximum-frequency input ceiling is based on the CPU's rated maximum frequency minus 1200 MHz.

Calculation:

CPU Rated Maximum Frequency - 1200 MHz
= Manual Input Ceiling Reference

Examples:

- CPU rated maximum: 4000 MHz
  Input ceiling reference: 2800 MHz

- CPU rated maximum: 4500 MHz
  Input ceiling reference: 3300 MHz

- CPU rated maximum: 4800 MHz
  Input ceiling reference: 3600 MHz

- CPU rated maximum: 5000 MHz
  Input ceiling reference: 3800 MHz

- CPU rated maximum: 5500 MHz
  Input ceiling reference: 4300 MHz

These are calculation examples.

The actual available input range is determined by CoreFlow and should be confirmed on the application screen.

All frequency inputs use 100 MHz increments.


[5-2. Maximum Frequency: 0 MHz]

Setting Maximum Frequency to 0 MHz means Unlimited.

A value of 0 MHz does not stop the CPU or force it to operate at 0 MHz.

Instead, it indicates that no maximum-frequency cap is being requested through this Windows power-management setting.

When 0 MHz is selected, CoreFlow does not impose an additional maximum-frequency restriction through that setting.

Windows and the CPU can then manage operating frequencies according to the system's normal power-management behavior.

This is useful when users want to remove the maximum-frequency cap previously configured through CoreFlow.

However, Unlimited does not mean that the CPU will always operate at its highest rated frequency.

It also does not remove other restrictions imposed by Windows, BIOS, firmware, temperature, electrical power limits, or manufacturer-specific controls.

Actual CPU clock speed continues to depend on system conditions.


[5-3. CPUs Not Found in the Database]

CoreFlow uses exact CPU model matching.

If the detected CPU model cannot be verified against the embedded database, CoreFlow does not estimate its maximum frequency.

It does not substitute specifications from a similar CPU model or another processor in the same product family.

If your CPU cannot be verified, set Maximum Frequency to 0 MHz (Unlimited).

This avoids relying on an unverified frequency specification.


[5-4. Minimum Frequency Input Limit]

The minimum-frequency input floor in the free edition is normally 1400 MHz.

Use the minimum value displayed on the CoreFlow screen when selecting a setting.

The entered minimum-frequency value is converted into the Windows "Minimum processor state (%)" setting.

This means the value is not applied as a continuously fixed CPU clock frequency.

For example, entering 1400 MHz does not guarantee that the CPU will always operate at or above exactly 1400 MHz.

Windows and CPU power-management mechanisms may produce different observed clock speeds.


[5-5. Maximum and Minimum Frequency Settings]

Maximum Frequency and Minimum Frequency have different purposes.

Maximum Frequency specifies a frequency cap through Windows CPU power management.

Minimum Frequency is converted into a minimum processor performance percentage.

The two settings are not identical types of control.

Always use the input ranges displayed by CoreFlow.


[5-6. Entered Values and Actual CPU Clock Speeds]

The frequency values entered in CoreFlow do not lock the processor to those exact clock speeds.

Actual CPU frequency depends on several factors, including:

- Current CPU workload
- CPU temperature
- Power limits
- AC or battery operation
- Windows power-plan settings
- CPU power-management architecture
- BIOS and firmware
- Manufacturer-specific power and thermal controls

CPU monitoring software may report clock frequencies that differ from the values entered in CoreFlow.


============================================================
6. BASIC USAGE
============================================================

[Step 1: Launch CoreFlow]

Start CoreFlow on a 64-bit Windows 11 system.

Administrator privileges are required because CoreFlow modifies Windows CPU power-management settings.

If Windows displays an administrator permission prompt, review and approve it to continue.


[Step 2: Select a Power Plan]

Select the Windows power plan you want to configure.

Windows stores CPU power-management settings separately for different power plans.


[Step 3: Configure AC and DC Settings]

Enter the desired values for AC and DC operation.

The main settings are:

- Maximum Frequency
- Minimum Frequency
- Boost Mode

Use values within the available input ranges for the free edition.


[Step 4: Select a Boost Mode]

Choose the desired processor boost policy.

Depending on the available settings, boost behavior can be disabled or adjusted using performance- and efficiency-oriented modes.


[Step 5: Apply Settings]

Review the selected values and click [Apply Settings].

CoreFlow applies the settings to the selected Windows power plan and switches to that plan.


[Step 6: Verify System Behavior]

After applying the settings, check how your PC behaves during normal operation.

Lower maximum-frequency limits may reduce processing performance.

Changes to CPU temperature and power consumption depend on the processor, cooling system, workload, and overall PC configuration.

Adjust settings according to your requirements and observed system behavior.


============================================================
7. MAXIMUM CPU FREQUENCY
============================================================

Maximum Frequency is a Windows CPU power-management setting that specifies an upper frequency limit.

On processors that support turbo or boost operation, the selected limit may include frequencies above the CPU's base frequency.

This allows users to adjust the frequency ceiling without necessarily disabling boost entirely.

For example, a processor may have a relatively low base frequency but support much higher frequencies under turbo or boost conditions.

A maximum-frequency cap may be used to request a limit within that operating range.

However, the maximum-frequency setting does not independently determine every aspect of boost behavior.

Actual operation depends on the CPU, firmware, Windows power-management mechanisms, and other system conditions.

The configured value is not guaranteed to appear as an exact, continuously enforced clock frequency in every environment.


[Maximum Frequency and Boost]

Maximum Frequency and Boost Mode are separate settings.

A boost-capable processor may still use boost within the configured maximum-frequency limit.

To request that boost be disabled, review the Boost Mode setting rather than relying only on Maximum Frequency.


[Maximum Frequency and Overclocking]

CoreFlow does not raise CPU clock speeds beyond manufacturer specifications through overclocking.

It does not directly modify CPU voltage, multipliers, or BIOS overclocking parameters.


============================================================
8. MINIMUM CPU FREQUENCY
============================================================

CoreFlow uses the Windows "Minimum processor state (%)" setting for minimum processor performance control.

The entered minimum-frequency value in MHz is converted into a percentage and applied through Windows power management.

This does not force the CPU to remain at the entered MHz value.

For example, selecting a minimum frequency of 1400 MHz does not mean that every CPU core will continuously operate at exactly 1400 MHz.

Observed frequencies may change because of workload, power-saving behavior, CPU architecture, and Windows power management.

Minimum Frequency should therefore be understood as a processor-performance setting rather than a fixed-clock command.


============================================================
9. TURBO BOOST AND BOOST MODES
============================================================

Boost-capable processors may temporarily operate above their nominal or base frequency when workload, temperature, power, and other conditions allow.

CoreFlow uses the Windows "Processor Performance Boost Mode" setting to configure the policy for this behavior.

Boost policies can determine whether boost is permitted and how aggressively Windows requests additional performance.


[9-1. Processor Performance Boost Mode Values]

Windows defines the following boost-policy values.

0: Disabled

Disables boost behavior above the processor's nominal performance level.


1: Enabled

Allows boost under normal Windows and CPU power-management behavior.


2: Aggressive

On supported control interfaces, Windows requests higher boost performance more aggressively.


3: Efficient Enabled

Allows boost while taking efficiency into account.


4: Efficient Aggressive

Combines efficiency-aware behavior with more aggressive boost requests.


5: Aggressive At Guaranteed

An aggressive boost-request policy referenced to the CPU's guaranteed performance level.


6: Efficient Aggressive At Guaranteed

An efficiency-aware boost-request policy referenced to the CPU's guaranteed performance level.


Note:

These boost-policy descriptions are based on the Windows settings documented in the previous Astra edition.

The modes actually available in the current CoreFlow edition should be checked in the application interface.


[9-2. Important Boost Mode Information]

Boost Mode does not lock the CPU to a fixed clock frequency.

A higher mode number does not necessarily mean higher performance.

The results depend on CPU architecture, firmware, Windows power management, and the processor's performance-control interface.

Depending on the system, different boost modes may produce very similar results.

More aggressive boost settings do not guarantee higher clocks for every workload.

Efficiency-oriented modes do not guarantee lower temperatures.

On boost-capable processors, a maximum-frequency cap may still permit boosting within that limit, including operation above the base frequency.

Entered MHz values do not guarantee exact operating frequencies.


============================================================
10. SEPARATE AC AND DC SETTINGS
============================================================

CoreFlow supports separate CPU power-management settings for AC and DC operation.


[AC: Plugged-In Operation]

AC refers to operation while the PC is connected to an external power source.

Users may configure settings to prioritize performance, reduce heat generation, or balance these objectives.


[DC: Battery Operation]

DC refers to operation while the PC is running on battery power.

Maximum-frequency limits and boost policies can be adjusted to explore a different balance between CPU performance and power consumption.

However, total battery life depends on many components besides the CPU.

Display brightness, storage activity, wireless devices, background applications, and manufacturer-specific power controls can all influence power consumption.

CoreFlow does not guarantee a particular improvement in battery runtime.


============================================================
11. WINDOWS POWER PLANS
============================================================

CoreFlow changes CPU power-management settings stored in Windows power plans.

When [Apply Settings] is selected, CoreFlow writes the configured values to the selected power plan and switches to that plan.

If Windows is subsequently switched to another power plan, the settings belonging to that other plan will be used.

Always check which power plan is currently active.

Windows updates and manufacturer-specific power-management software may also affect system power behavior.


[11-1. Differences Between Power Plans]

CPU frequency and boost-control behavior can vary depending on the active Windows power plan.

Even when similar values are configured, the actual response may differ because of processor performance policies or other power-management settings associated with the plan.

CPU architecture, BIOS, firmware, and manufacturer-specific controls can also influence the results.

This is one of the reasons CoreFlow adopts a defined frequency-input range rather than guaranteeing the same clock behavior across every PC.


[11-2. Changes in Windows Power Management]

Windows processor performance is managed through multiple policies and hardware interfaces.

The results of frequency and boost settings can change depending on Windows configuration, processor architecture, and supported power-management mechanisms.

CoreFlow applies its settings through Windows rather than bypassing these mechanisms.

Consequently, the application cannot override every frequency or performance restriction imposed by the operating system or the hardware.


============================================================
12. MICROSOFT PROCESSOR POWER MANAGEMENT DOCUMENTATION
============================================================

Microsoft provides official documentation describing Windows processor power management.

These documents explain available processor performance policies, maximum-frequency settings, and boost-mode behavior.

They can help users understand why CPU operating frequencies may differ from configured values.


[Processor Power Management]

Microsoft documentation covering Windows processor power-management options:

https://learn.microsoft.com/en-us/windows-hardware/customize/power-settings/configure-processor-power-management-options


[Maximum Processor Frequency]

Microsoft documentation covering the maximum processor frequency setting:

https://learn.microsoft.com/en-us/windows-hardware/customize/power-settings/options-for-perf-state-engine-maxfrequency


[Processor Performance Boost Mode]

Microsoft documentation covering processor boost policies:

https://learn.microsoft.com/en-us/windows-hardware/customize/power-settings/options-for-perf-state-engine-perfboostmode


These references describe Windows power-management mechanisms.

They do not establish that every Windows 11 system has one identical or universal CPU clock-speed restriction.

Actual processor behavior depends on the system configuration and supported control methods.


============================================================
13. CPU SPECIFICATION DATABASE
============================================================

CoreFlow includes an embedded CPU specification database.

It automatically detects the CPU model and checks whether the detected model exactly matches a registered entry.

When an exact match is found, the application can refer to the registered base and maximum frequencies.


[Exact Model Matching]

CoreFlow uses CPU specification data only when the CPU model matches a database entry exactly.

It does not assume that similar model names have identical specifications.

Specifications from other CPUs in the same product family are not substituted automatically.


[Unverified CPU Models]

If the CPU model cannot be verified, CoreFlow does not guess its rated maximum frequency.

For the free edition's maximum-frequency setting, use 0 MHz (Unlimited) when the CPU cannot be verified.


[Offline CPU Lookup]

The CPU specification database is included in the application.

CPU model verification does not require an Internet connection.


[Free Edition Input Ceiling]

For CPUs verified through exact database matching, CoreFlow uses the CPU's rated maximum frequency minus 1200 MHz as the reference for the manual maximum-frequency input ceiling.

For details, see Section 5.


============================================================
14. RESTORING ORIGINAL SETTINGS
============================================================

If you want to undo changes made by CoreFlow, use [Restore Original Settings].

This function is intended to restore the settings saved before CoreFlow modified the CPU power-management configuration.

It can be useful when reverting previous adjustments or preparing to remove the application.


[Before Removing CoreFlow]

Windows CPU power settings may remain changed even after the CoreFlow executable has been deleted.

If you want to return to your previous configuration, use the restore function before removing CoreFlow.


[Restore Limitations]

The restore function is not intended to reset BIOS settings or manufacturer-specific firmware controls.

Its purpose is to restore the Windows power-management settings previously saved and managed by CoreFlow.


============================================================
15. VERSION INFORMATION
============================================================

You can check the installed CoreFlow version through:

Help -> About

When requesting support, please check the version of CoreFlow you are using.


============================================================
16. UPDATES
============================================================

CoreFlow provides an update-checking function through the Help menu.

Use:

Help -> Check for Updates

The application can check the latest release published through GitHub Releases.

An Internet connection may be required for update checking.

CPU specification database lookup itself does not require Internet access.


============================================================
17. DIAGNOSTIC LOGS
============================================================

CoreFlow provides diagnostic logging to assist with troubleshooting and support.


[Saving a Diagnostic Log]

Use the diagnostic log option in the Help menu.

Follow the on-screen instructions to select where the diagnostic log should be saved.


[Information in Diagnostic Logs]

Diagnostic logs may contain information such as:

- CPU information
- Windows power plans
- CPU power-management settings
- Configuration and application operations
- Other diagnostic information needed for troubleshooting


[Sharing Diagnostic Logs]

Review diagnostic logs before sending them to support.

Make sure they do not contain information that you do not wish to share.

CoreFlow does not require license keys or license registration.


============================================================
18. UNINSTALLING COREFLOW
============================================================

CoreFlow does not use a dedicated uninstaller.

To remove it:

1. Launch CoreFlow.

2. Use [Restore Original Settings] if you want to undo its changes.

3. Exit CoreFlow.

4. Delete the CoreFlow executable.

Deleting the executable does not necessarily restore Windows CPU power-management settings automatically.

If you want your previous settings restored, perform the restore operation before deleting the application.


============================================================
19. DISTRIBUTION FILES AND THIRD-PARTY SOFTWARE
============================================================

Extract the entire distribution ZIP before launching the executable.

The distribution includes materials relating to third-party software and applicable licenses.


[THIRD_PARTY_NOTICES.txt]

Contains notices and acknowledgements for third-party software used by the application.


[licenses/]

Contains third-party license texts and related materials.


[source/]

Contains third-party software source materials and associated documentation.


Third-party software remains subject to its own copyright notices and license terms.

CoreFlow's product terms do not restrict copying, modification, redistribution, or other rights granted under applicable third-party licenses.

When distributing the package, retain the required license materials and the complete distribution set.


[Acknowledgements]

We sincerely thank the authors and developers of AutoHotkey and the other third-party software components used by this project.

We also acknowledge the contributions of the third-party software authors whose work supports the application's distribution and operation.


============================================================
20. IMPORTANT NOTES
============================================================

CoreFlow changes Windows CPU power-management settings using standard Windows mechanisms.

It does not use a custom kernel driver or directly modify CPU voltage or BIOS settings.

However, changing CPU power-management settings can affect system performance and stability.

Depending on the PC and selected values, the following may occur:

- Reduced system responsiveness
- Lower application performance
- Temporary system freezes
- Unexpected differences in CPU frequency behavior
- Changes in thermal or power-management behavior

Actual CPU frequency depends on many factors:

- CPU architecture
- Windows power management
- Current workload
- Temperature
- Power limits
- BIOS and firmware
- Manufacturer-specific power and thermal controls

The entered frequency does not guarantee that the CPU will operate at exactly that value at all times.

CoreFlow also does not guarantee a specific temperature reduction, power-consumption reduction, or performance improvement.

Use settings appropriate for your system and verify behavior after applying changes.


============================================================
21. DISCLAIMER AND COMPATIBILITY
============================================================

CoreFlow modifies Windows CPU power-management settings.

Although it uses standard Windows power-management mechanisms, selected settings may reduce responsiveness, temporarily freeze the system, or cause other unexpected behavior depending on the PC configuration.

To the extent permitted by applicable law, the developers disclaim liability for direct or indirect losses arising from use or inability to use the software, including hardware damage, data loss, business interruption, or lost opportunities.

Users are responsible for checking compatibility with their own systems and selecting appropriate settings.

Some manufacturer-specific motherboard, BIOS, firmware, or power-management configurations may prevent certain controls from working as expected.

Applicable third-party license rights and warranty terms remain governed by their original license texts.


============================================================
22. COREFLOW AND COREFLOW EXTREME
============================================================

CoreFlow is a free CPU power-management utility.

In the free edition, the manual maximum-frequency input ceiling is based on the rated maximum frequency of a CPU verified through the embedded specification database, minus 1200 MHz.

The normal minimum-frequency input floor is 1400 MHz.

CoreFlow Extreme is a separate higher-tier edition.

This document describes the free edition of CoreFlow.

For information about CoreFlow Extreme and its available settings, refer to the documentation provided for that edition.


============================================================
23. DEVELOPMENT AND SUPPORT
============================================================

Developed by:
MasaTech / Itachi, Spica and Mahiru

Support:
masatech.dev.apps@gmail.com

BOOTH:
https://masatech.booth.pm/


============================================================
CoreFlow
Free CPU Power Management Utility for Windows 11
============================================================
