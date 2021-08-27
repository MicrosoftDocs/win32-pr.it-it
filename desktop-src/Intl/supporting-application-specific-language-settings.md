---
description: L'applicazione può supportare un set diverso di lingue dell'interfaccia utente da quelle supportate dal sistema operativo di destinazione. Questo argomento illustra questo tipo di supporto, usando frammenti di codice di esempi completi.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: Supporto di Application-Specific language Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130061"
---
# <a name="supporting-application-specific-language-settings"></a>Supporto di Application-Specific language Impostazioni

L'applicazione può supportare un set diverso di lingue dell'interfaccia utente da quelle supportate dal sistema operativo di destinazione. Questo argomento illustra questo tipo di supporto, usando frammenti di codice di esempi completi.

## <a name="interpret-users-language-preference"></a>Interpretare le preferenze di lingua dell'utente

L'applicazione deve prima determinare la lingua dell'interfaccia utente da visualizzare, in base alle preferenze dell'utente. Il codice può leggere le impostazioni da un file di configurazione o dalle impostazioni del Registro di sistema.

L'esempio seguente definisce due funzioni usate per interpretare le preferenze di lingua dell'utente. La prima funzione illustra la lettura di un elenco delimitato di lingue da un file, rappresentato nel codice come "langs.txt". I delimitatori supportati nell'esempio sono ",",";";"." e " ". La seconda funzione converte la stringa letta dal file in un valore a più stringhe. Questa operazione è necessaria perché le funzioni MUI usate per impostare le lingue accettano solo valori a più stringhe.


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



## <a name="set-the-application-language"></a>Impostare la lingua dell'applicazione

Dopo aver letto le informazioni sulle preferenze della lingua, il codice dell'applicazione deve usare l'impostazione recuperata per impostare la lingua dell'applicazione. In Windows 7 e versioni successive, l'applicazione può impostare la lingua a livello di processo chiamando la [**funzione SetProcessPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)


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



In Windows Vista e versioni successive, la lingua dell'applicazione viene impostata a livello di thread chiamando la [**funzione SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)


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

[MUI: Application-Specific Impostazioni esempio (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: Application-Specific Impostazioni esempio (pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



