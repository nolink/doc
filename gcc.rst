
==================
gcc_build.json
==================

::
{
    "cmd": [
        "g++",
        "-Wall",
        "${file}",
        "-o",
        "${file_path}/${file_base_name}"
    ],
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c, source.c++",
    "encoding": "cp936",
    "variants": [
        {
            "name": "Run",
            "cmd": [
                "cmd",
                "/c",
                "g++",
                "-Wall",
                "${file}",
                "-o",
                "${file_path}/${file_base_name}",
                "&&",
                "cmd",
                "/c",
                "${file_path}/${file_base_name}"
            ]
        },
        {
            "name": "RunInCommand",
            "cmd": [
                "cmd",
                "/c",
                "g++",
                "-Wall",
                "${file}",
                "-o",
                "${file_path}/${file_base_name}",
                "&&",
                "start",
                "cmd",
                "/c",
                "${file_path}/${file_base_name} & echo.&pause"
            ]
        }
    ]
}
