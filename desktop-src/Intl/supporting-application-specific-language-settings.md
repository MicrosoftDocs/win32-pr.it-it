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
# <a name="supporting-application-specific-language-settings"></a>Supporto delle impostazioni della lingua Application-Specific

L'applicazione può supportare un diverso set di lingue dell'interfaccia utente da quelle supportate dal sistema operativo di destinazione. In questo argomento viene illustrato questo tipo di supporto, utilizzando frammenti di esempi completi.

## <a name="interpret-users-language-preference"></a>Interpretare le preferenze della lingua dell'utente

L'applicazione deve innanzitutto determinare quale lingua dell'interfaccia utente visualizzare, in base alle preferenze dell'utente. Il codice può leggere le impostazioni da un file di configurazione o dalle impostazioni del registro di sistema.

Nell'esempio seguente vengono definite due funzioni utilizzate per interpretare le preferenze di lingua dell'utente. La prima funzione illustra la lettura di un elenco delimitato di lingue da un file, rappresentato nel codice come "langs.txt". I delimitatori supportati nell'esempio sono ",", ";"; "." e "". La seconda funzione converte la stringa letta dal file in un valore a più stringhe. Questa operazione è necessaria perché le funzioni MUI utilizzate per impostare i linguaggi accettano solo valori multistringhe.


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



## <a name="set-the-application-language"></a>Imposta la lingua dell'applicazione

Dopo aver letto le informazioni sulle preferenze della lingua, il codice dell'applicazione deve usare l'impostazione recuperata per impostare la lingua dell'applicazione. In Windows 7 e versioni successive, l'applicazione può impostare la lingua a livello di processo chiamando la funzione [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) .


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



In Windows Vista e versioni successive la lingua dell'applicazione viene impostata a livello di thread chiamando la funzione [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle preferenze di lingua dell'applicazione](setting-application-language-preferences.md)
</dt> <dt>

[Esempio di impostazioni di MUI: Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



