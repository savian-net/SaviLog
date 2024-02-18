# SaviLog

## Overview

SaviLog is designed to parse SAS logs and convert them into a number of reports. It is written in C# under .NET 8+.

## Architecture

SaviLog.exe is compiled as x64 and as a single exe. It relies on the JSON settings file and is .NET 8 dependent. Please install .NET 8 before using.

## Parameters

To see the available parameters, execute SaviLog with a /? or a --help at the command line. This will display the help for the commands.

## Reports

SaviLog generates the following reports:

- Error Analysis
- Frequency Analysis
- Large Log Files
- Note Analysis
- Performance Analysis
- Sas Log Analysis

## Logging

All parsing logs are written to the user temp path (%temp%) and are under the directory *Savian\SaviLog*

## Regex and Patterns

See the SaviLogSettings.json file for regex patterns and note patterns

## Sample call

.\SaviLog.exe --MaxLogSize 1000000 --Output "C:\temp\LogAnalysis" --Path "[C:\temp\SasLogs; X:\repos\SasSamples\Logs\QuickTestLogs]" --ParseWarnings --Work "C:\temp\ExportSasDataset"
