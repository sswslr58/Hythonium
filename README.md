# Hythonium
A lightweight web browser built with PyQt5 and QtWebEngine.
It doesn't support HTML 5 Player.
# How to conifg
1.Put 'config.py' and 'hynium.py' or 'hynium.exe' in the same directory.  
The encoding MUST BE utf-8.
If there is NO config.py, You can make one by yourself.
  
2.Edit 'config.py'  
Edit it like Python. Make the content:

    config = {
      "Key1": Value1,  # You can add some notes here. Let it start with '#'
      "Key2": Value2,
    }
  The keys all must be str objects. 
  
  Keys are:
  
    homepage: (str)<URL> -- Set the homepage of Hythonium. eg:"https://www.baidu.com"
    search_engine: (str)<URL> -- Set the search engine of Hythonium. eg:"https://www.baidu.com/s?wd="
    new_tab: (str)<URL> -- Set the new tab when clicking '+' button. eg:"https://www.baidu.com"
    save_folder: (str)<PATH> -- Set the downloading path. eg:"Downloads" | "./Downloads" | "/home/usrname/Downloads" | "C:\\Downloads"
    User_Agent: (str) -- Set UA value. eg:"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36"
    default_dnload_filename: (str) -- Set default downloading file name. eg:"download_file"
The default code (v0.0.2):

    # coding=utf-8
    # Hythonium Config
    """
    
    This is a Pythonic Dictionary Config.
    Hythonium will load it as a dictionary and use it in the browser.
    
    Just put this file in the SAME directory as hynium.py | hynium.exe
    DO REMEMBER: The filename MUST BE "config.py" !!!
    
    ========================================================
    
    The sequence of the keys is not important, but the keys must be unique.
    The values can be any type of Python objects, including nested dictionaries.
    If a key is not found, the default value will be used.
    If there is an extra key, it won't be used.
    If the format is wrong, the program will use an empty dictionary as the default value.
    
    ========================================================
    
    Notices:
        1. Use 'KEY': VALUE to define a key-value pair.
        2. DO NOT use ';' instead of ':'.
        3. Don't forget to add ',' at the end of the line.
    
    ========================================================
    
    Keys are:
        homepage: (str)<URL> -- Set the homepage of Hythonium. eg: "https://www.baidu.com"
        search_engine: (str)<URL> -- Set the search engine of Hythonium. eg: "https://www.baidu.com/s?wd="
        new_tab: (str)<URL> -- Set the new tab when clicking '+' button. eg: "https://www.baidu.com"
        download_folder: (str)<PATH> -- Set the downloading path. eg: "Downloads" | "./Downloads" | "/home/usrname/Downloads" | "C:\\Downloads"
        User_Agent: (str) -- Set User-Agent value. eg: "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36"
    
    ========================================================
    
    And you should execute hynium.py or hynium.exe to start Hythonium. NOT THIS FILE!!!
    
    ========================================================
    
    For more information, see README.md => Click Here: https://github.com/sswslr58/Hythonium
    
    """
    
    if __name__ == "__main__":
        print("Execute hynium.py or hynium.exe to start Hythonium next time.")
        print("Do NOT execute this file again !")
    
    config = {
        "homepage": "https://www.baidu.com",
        "search_engine": "https://www.baidu.com/s?wd=",
        "new_tab": "https://www.baidu.com",
        "download_folder": "Downloads",
        "User_Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36",
    }


# How to build your own one
In the Shell (Powershell / Bash / Xterm / ...):

    pip install pyinstaller # When you have NOT installed pyinstaller. Continue if you have. If you use conda, you can change this command
    cd the_project_folder # where you download the project
    pyinstaller -F -w hynium.py # -F means one file mode. -w means without terminal window when running. You can change.
    dist/hynium.exe # Enjoy !

If you use Windows Cmd, delete the notes (start with '#').
