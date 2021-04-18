---
description: L'applicazione può supportare un diverso set di lingue dell'interfaccia utente da quelle supportate dal sistema operativo di destinazione. In questo argomento viene illustrato questo tipo di supporto, utilizzando frammenti di esempi completi.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: Supporto delle impostazioni della lingua Application-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bddfe94586751d3b0f4757c670c006317e49b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316276"
---
# <a name="supporting-application-specific-language-settings"></a><span data-ttu-id="b004e-104">Supporto delle impostazioni della lingua Application-Specific</span><span class="sxs-lookup"><span data-stu-id="b004e-104">Supporting Application-Specific Language Settings</span></span>

<span data-ttu-id="b004e-105">L'applicazione può supportare un diverso set di lingue dell'interfaccia utente da quelle supportate dal sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b004e-105">Your application can support a different set of user interface languages from those supported by the target operating system.</span></span> <span data-ttu-id="b004e-106">In questo argomento viene illustrato questo tipo di supporto, utilizzando frammenti di esempi completi.</span><span class="sxs-lookup"><span data-stu-id="b004e-106">This topic discusses this type of support, using snippets from complete samples.</span></span>

## <a name="interpret-users-language-preference"></a><span data-ttu-id="b004e-107">Interpretare le preferenze della lingua dell'utente</span><span class="sxs-lookup"><span data-stu-id="b004e-107">Interpret User's Language Preference</span></span>

<span data-ttu-id="b004e-108">L'applicazione deve innanzitutto determinare quale lingua dell'interfaccia utente visualizzare, in base alle preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b004e-108">Your application must first determine which user interface language to display, based on user preference.</span></span> <span data-ttu-id="b004e-109">Il codice può leggere le impostazioni da un file di configurazione o dalle impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b004e-109">The code can read the settings from a configuration file or from registry settings.</span></span>

<span data-ttu-id="b004e-110">Nell'esempio seguente vengono definite due funzioni utilizzate per interpretare le preferenze di lingua dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b004e-110">The following example defines two functions used to interpret the user's language preference.</span></span> <span data-ttu-id="b004e-111">La prima funzione illustra la lettura di un elenco delimitato di lingue da un file, rappresentato nel codice come "langs.txt".</span><span class="sxs-lookup"><span data-stu-id="b004e-111">The first function illustrates the reading of a delimited list of languages from a file, represented in the code as "langs.txt".</span></span> <span data-ttu-id="b004e-112">I delimitatori supportati nell'esempio sono ",", ";"; "." e "".</span><span class="sxs-lookup"><span data-stu-id="b004e-112">The delimiters supported in the sample are ",",";";"." and " ".</span></span> <span data-ttu-id="b004e-113">La seconda funzione converte la stringa letta dal file in un valore a più stringhe.</span><span class="sxs-lookup"><span data-stu-id="b004e-113">The second function converts the string read from the file to a multi-string value.</span></span> <span data-ttu-id="b004e-114">Questa operazione è necessaria perché le funzioni MUI utilizzate per impostare i linguaggi accettano solo valori multistringhe.</span><span class="sxs-lookup"><span data-stu-id="b004e-114">This operation is necessary because the MUI functions used to set languages only accept multi-string values.</span></span>


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
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
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a><span data-ttu-id="b004e-115">Imposta la lingua dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b004e-115">Set the Application Language</span></span>

<span data-ttu-id="b004e-116">Dopo aver letto le informazioni sulle preferenze della lingua, il codice dell'applicazione deve usare l'impostazione recuperata per impostare la lingua dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b004e-116">After reading the language preference information, the application code must use the retrieved setting to set the application language.</span></span> <span data-ttu-id="b004e-117">In Windows 7 e versioni successive, l'applicazione può impostare la lingua a livello di processo chiamando la funzione [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) .</span><span class="sxs-lookup"><span data-stu-id="b004e-117">On Windows 7 and later, the application can set the language at the process level by calling the [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



<span data-ttu-id="b004e-118">In Windows Vista e versioni successive la lingua dell'applicazione viene impostata a livello di thread chiamando la funzione [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .</span><span class="sxs-lookup"><span data-stu-id="b004e-118">On Windows Vista and later, the application language is set at the thread level by calling the [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a><span data-ttu-id="b004e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b004e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b004e-120">Impostazione delle preferenze di lingua dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b004e-120">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> <dt>

[<span data-ttu-id="b004e-121">Esempio di impostazioni di MUI: Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="b004e-121">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="b004e-122">Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="b004e-122">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



