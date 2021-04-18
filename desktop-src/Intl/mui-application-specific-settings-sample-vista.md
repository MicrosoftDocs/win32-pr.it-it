---
description: 'Esempio di impostazioni di MUI: Application-Specific (Windows Vista)'
ms.assetid: 348a51fb-aad1-4255-a5a2-224d5c94d762
title: 'Esempio di impostazioni di MUI: Application-Specific (Windows Vista)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9583e606a0f9023d02a4ef804fee22c56818a75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308693"
---
# <a name="mui-application-specific-settings-sample-windows-vista"></a><span data-ttu-id="ab298-103">Esempio di impostazioni di MUI: Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="ab298-103">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>

<span data-ttu-id="ab298-104">L'applicazione di esempio descritta in questo argomento è un'altra applicazione Hello MUI che supporta le impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente e viene eseguita in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ab298-104">The sample application described in this topic is another Hello MUI application that supports application-specific settings for its user interface languages and runs on Windows Vista and later.</span></span>

<span data-ttu-id="ab298-105">Questa applicazione analizza prima di tutto un elenco di linguaggi delimitati in un file di testo e lo converte in un elenco di lingue multistringhe per definire le preferenze di lingua specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab298-105">This application first parses a delimited language list in a text file and converts it to a multi-string language list to define the application-specific language preferences.</span></span> <span data-ttu-id="ab298-106">I delimitatori supportati nell'esempio sono ",", ";", ":" e "".</span><span class="sxs-lookup"><span data-stu-id="ab298-106">The delimiters supported in the sample are ",", ";", ":", and " ".</span></span> <span data-ttu-id="ab298-107">Dopo l'analisi dell'elenco, il codice trova e carica le risorse nella lingua identificata, esattamente come avviene nell'esempio di impostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="ab298-107">After parsing the list, the code finds and loads the resources in the identified language, just as the system settings sample does.</span></span> <span data-ttu-id="ab298-108">Questo codice carica e rilascia i file di risorse usando le chiamate alle funzioni del caricatore di risorse [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa) e [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).</span><span class="sxs-lookup"><span data-stu-id="ab298-108">This code loads and releases resource files using calls to the resource loader functions [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa) and [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).</span></span>


```C++
// Vista and later enabled application, this application will not work on OS versions prior to Vista

#include <windows.h>
#include <wchar.h>
#include <strsafe.h>
#include "resource.h"

#define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
#define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
#define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)

BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
{
    UNREFERENCED_PARAMETER(hInstance);
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);
    UNREFERENCED_PARAMETER(nCmdShow);

    // The following code presents a hypothetical, yet common use pattern of MUI technology
    WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

    // 1. Application starts by applying any user defined language preferences
    // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
    // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
    WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
    if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }
    // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
    WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
    if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }
    // 1c. Application now sets the appropriate fallback list
    DWORD langCount = 0;
    // next commented out line of code could be used on Windows 7 and forward
    // using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications)
//    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
    // the following line of code is supported on Windows Vista and forward
    if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }
    // NOTES on step #1:
    // an application developer that makes the assumption the fallback list provided by the
    // system / OS is entirely sufficient may or may not be making a good assumption based 
    // mostly on:
    // A. your choice of languages installed with your application
    // B. the languages on the OS at application install time
    // C. the OS users propensity to install/uninstall language packs
    // D. the OS users propensity to change laguage settings

    // 2. Application obtains access to the proper resource container 
    // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
    // LoadLibraryEx is the preferred alternative for resource modules as used below because it
    // provides increased security and performance over that of LoadLibrary
    HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
    if(!resContainer)
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }

    // 3. Application parses the resource container to find the appropriate item
    WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
    if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        FreeLibrary(resContainer);
        return 1; // exit
    }

    // 4. Application presents the discovered resource to the user via UI
    swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
    MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

    // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
    if(!FreeLibrary(resContainer))
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }

    return 0;
}

BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // very simple implementation - assumes that first 'langStrSize' characters of the 
    // L".\\langs.txt" file comprises a string of one or more languages
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
        NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // clear out the input variables
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}

BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // make sure you validate the user input
            if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL,L",; :",&context);
            if(next)
                last = next;
        }
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // fail and guard anyone whom might use the multi-string
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



 

 
