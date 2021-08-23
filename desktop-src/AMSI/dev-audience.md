---
title: Destinatari degli sviluppatori e codice di esempio
description: In questo argomento vengono descritti i gruppi di sviluppatori per i quali è stata progettata l'interfaccia di analisi antimalware.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 4ac11c75d5714d0706bed28264f9fa1bf03432af82107826178007e2c42243c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579911"
---
# <a name="developer-audience-and-sample-code"></a>Destinatari degli sviluppatori e codice di esempio

L'interfaccia di analisi antimalware è progettata per l'uso da parte di due gruppi di sviluppatori.

- Sviluppatori di applicazioni che vogliono effettuare richieste a prodotti antimalware dall'interno delle proprie app.
- Creatori di terze parti di prodotti antimalware che vogliono che i loro prodotti oftino le migliori funzionalità alle applicazioni.

## <a name="application-developers"></a>Sviluppatori di applicazioni

AMSI è progettato in particolare per contrastare il "malware senza file". I tipi di applicazione che possono sfruttare in modo ottimale la tecnologia AMSI includono i motori di script, le applicazioni che necessitano di buffer di memoria da analizzare prima di usarli e le applicazioni che elaborano file che possono contenere codice eseguibile non PE (ad esempio macro Microsoft Word e Excel o documenti PDF). Tuttavia, l'utilità della tecnologia AMSI non è limitata a questi esempi.

Esistono due modi per interfacciarsi con AMSI nell'applicazione.

- Usando le API Win32 AMSI. Vedere [Funzioni AMSI (Antimalware Scan Interface).](/windows/desktop/amsi/antimalware-scan-interface-functions)
- Tramite le interfacce COM AMSI. Vedere [ **Interfaccia IAmsiStream.**](/windows/desktop/api/amsi/nn-amsi-iamsistream)

Per il codice di esempio che illustra come usare AMSI all'interno dell'applicazione COM, vedere l'applicazione [di esempio dell'interfaccia IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Autori di prodotti antimalware di terze parti

Gli autori di prodotti antimalware possono scegliere di creare e registrare il proprio server COM in-process (una DLL) per funzionare come provider AMSI. Il provider AMSI deve implementare [ **l'interfaccia IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)e deve essere eseguito in-process.

Si noti che, dopo Windows 10 versione 1709 (Fall 2017 Creators' Update), la DLL del provider AMSI potrebbe non funzionare se dipende da altre DLL nel percorso da caricare contemporaneamente. Per impedire l'hijack delle DLL, è consigliabile che la DLL del provider carichi le dipendenze in modo esplicito (con un percorso completo) usando chiamate [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) sicure o equivalenti. È consigliabile usare questa opzione invece di basarsi sul **comportamento di ricerca di LoadLibrary.**

La sezione seguente illustra come registrare il provider AMSI. Per il codice di esempio completo che illustra come creare la DLL del provider AMSI, vedere l'applicazione di esempio [dell'interfaccia IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registrare la DLL del provider con AMSI

Per iniziare, è necessario assicurarsi che queste chiavi del Registro di Windows esistenti.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Un provider AMSI è un server COM in-process. Di conseguenza, deve registrarsi con COM. Le classi COM vengono registrate in `HKLM\SOFTWARE\Classes\CLSID` .

Il codice seguente illustra come registrare un provider AMSI il cui GUID (per questo esempio) si presuppone che sia `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

Se la DLL implementa la [funzione DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), come nell'esempio precedente, è possibile registrarla usando il file eseguibile Windows `regsvr32.exe` specificato. Da un prompt dei comandi con privilegi elevati, eseguire un comando di questo formato.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

In questo esempio il comando crea le voci seguenti.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**(Impostazione predefinita)    REG_SZ implementazione del provider AMSI di esempio**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**(Impostazione predefinita)    REG_EXPAND_SZ %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ Both**

Oltre alla normale registrazione COM, è anche necessario registrare il provider con AMSI. A tale scopo, aggiungere una voce alla chiave seguente.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Ad esempio,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
