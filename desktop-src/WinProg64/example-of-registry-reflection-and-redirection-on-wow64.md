---
title: Esempio di reindirizzamento del Registro di sistema in WOW64
description: Nell'esempio di codice seguente vengono illustrate le visualizzazioni separate del Registro di sistema fornite dal redirector del Registro di sistema in un Windows a 64 bit.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- Esempi di programmazione Windows a 64 bit
- Esempi di guida alla programmazione Windows a 64 bit Windows a 64 bit
- Esempi di guida alla programmazione Windows a 64 bit Windows programmazione a 64 bit, reindirizzamento del Registro di sistema in WOW64
- esempio di reindirizzamento del Registro di sistema a 64 bit Windows programmazione
- 64-bit Windows 64-bit Windows Programming ( Programmazione di applicazioni a 64 bit), esempi Vedere esempi della guida alla programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83428edb31e53bdd1c70825c7fa5a4d799a36536fa9c17f9ce1c4587ab096048
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680230"
---
# <a name="example-of-registry-redirection-on-wow64"></a>Esempio di reindirizzamento del Registro di sistema in WOW64

Nell'esempio di codice seguente vengono illustrate le visualizzazioni separate del Registro di sistema fornite dal redirector del Registro di sistema in un Windows a 64 bit. Viene inoltre illustrato come vengono impostati i valori delle chiavi a seconda che una chiave sia condivisa o reindirizzata. Per altre informazioni, vedere [Chiavi del Registro di sistema interessate da WOW64.](shared-registry-keys.md)

Compilare il codice seguente separatamente per le applicazioni a 32 bit e a 64 bit Windows. Eseguire ogni file eseguibile risultante in un Windows a 64 bit e confrontare l'output. L'output di esempio per entrambe le versioni è elencato sotto il codice sorgente.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



Quando viene eseguita la versione a 64 bit dell'esempio, viene generato l'output seguente. I valori delle visualizzazioni predefinite e alternative di **HKCR \\ Hello** sono gli stessi perché questa chiave è condivisa. I valori delle altre chiavi sono diversi perché vengono reindirizzati.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Quando questo esempio viene eseguito in questi sistemi operativi, le viste predefinite e alternative della chiave LocalServer32 hanno lo stesso valore. Ciò è dovuto al fatto che la chiave LocalServer32 viene reindirizzata e riflessa, causando la sincronizzazione del relativo valore tra le visualizzazioni a 64 bit e a 32 bit del Registro di sistema non appena l'handle per la chiave viene chiuso. La reflection del Registro di sistema è stata rimossa a partire Windows 7. Per altre informazioni, vedere Reflection [del Registro di sistema.](registry-reflection.md)

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

Quando viene eseguita la versione a 32 bit dell'esempio, viene generato l'output seguente. Per un'applicazione a 32 bit, la visualizzazione a 64 bit del Registro di sistema è la visualizzazione alternativa, quindi i valori vengono invertati, ad eccezione di HKCR Hello, che è una chiave \\ condivisa.

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

Per esaminare l'effetto dell'esecuzione di questo esempio con regedit, esaminare i valori delle chiavi seguenti. Si noti che le applicazioni devono evitare l'uso di Wow6432Node nei percorsi del Registro di sistema hard-coded.

**HKLM \\ SOFTWARE \\ Hello World**  
**HKLM \\ SOFTWARE \\ Wow6432Node \\ Hello World**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ CLSID \\ {000000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**  
**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ Wow6432Node \\ CLSID \\ {000000000-0000-0000-0000-ABCD000000000} \\ InprocServer32**  
**HKCR \\ Wow6432Node \\ CLSID \\ {000000000-0000-0000-0000-ABCD000000000} \\ LocalServer32**  
**HKCR \\ Wow6432Node \\ Hello**  


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del Registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del Registro di sistema](registry-reflection.md)
</dt> </dl>

 

 




