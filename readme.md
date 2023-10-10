# Overview

This PowerShell script uses ffprobe.exe to get the duration of each mp4 file in an input directiory. It then uses ffmpeg.exe to trim the beginning and end of each file based on the input parameters 'BeginTrimTime' and 'EndTrimTime'. The edited files are then saved to a seperate output directory.

Using this script, replace the "C:\path\to\ffmpeg\bin" with the actual path where ffmpeg.exe and ffprobe.exe are located on your local system.

# Input Parameters

* ffmpegPath
    * The path to which your ffmpeg.exe and ffprobe.exe files are located on your local systm
    * EX: "C:\ffmpeg\bin"
* inputDir
    * The directory containing the source files to be edited
* outputDir
    * The directory for the copied, destination files
* BeginTrimtime
    * The seconds from the beginning of the mp4 file that you would like removed
* EndTrimTime
    * The seconds from the end of the mp4 file that you would like removed

# ffmpeg command

Here is a description of the options used in the ffmpeg command for those who would like the addditoinal description:

``-ss``: option that is used to specify the start time for the trim
``-to``: option that is used to specify the end time 
``-c``: Copy opotion that is uesed to ensure the video is copied without re-encoding