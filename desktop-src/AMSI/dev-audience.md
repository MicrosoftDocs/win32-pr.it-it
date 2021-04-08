---
title: Pubblico degli sviluppatori e codice di esempio
description: Questo argomento descrive i gruppi di sviluppatori per cui è stata progettata l'interfaccia di analisi antimalware.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2020
ms.locfileid: "104046231"
---
# <a name="developer-audience-and-sample-code"></a>Pubblico degli sviluppatori e codice di esempio

L'interfaccia di analisi antimalware è progettata per l'uso da parte di due gruppi di sviluppatori.

- Sviluppatori di applicazioni che desiderano eseguire richieste ai prodotti antimalware dall'interno delle app.
- Autori di terze parti di prodotti antimalware che vogliono offrire ai propri prodotti le funzionalità migliori per le applicazioni.

## <a name="application-developers"></a>Sviluppatori di applicazioni

AMSI è progettato in particolare per contrastare il "malware non file". I tipi di applicazioni che possono sfruttare in modo ottimale la tecnologia AMSI includono i motori di script, le applicazioni che necessitano di buffer di memoria da analizzare prima di usarli e le applicazioni che elaborano file che possono contenere codice eseguibile non PE, ad esempio macro di Microsoft Word ed Excel o documenti PDF. Tuttavia, l'utilità della tecnologia AMSI non è limitata a questi esempi.

Esistono due modi in cui è possibile interfacciarsi con AMSI nell'applicazione.

- Utilizzando le API Win32 AMSI. Vedere [funzioni AMSI (antimalware Scan Interface)](/windows/desktop/amsi/antimalware-scan-interface-functions).
- Utilizzando le interfacce COM AMSI. Vedere [interfaccia **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Per il codice di esempio che illustra come usare AMSI all'interno dell'applicazione COM, vedere l' [applicazione di esempio interfaccia IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Autori di terze parti di prodotti antimalware

In qualità di creatore di prodotti antimalware, è possibile scegliere di creare e registrare il proprio server COM in-process (DLL) per funzionare come provider AMSI. Il provider AMSI deve implementare l' [interfaccia **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)e deve essere eseguito in-process.

Si noti che, dopo Windows 10, versione 1709 (l'aggiornamento degli autori di cadute 2017), è possibile che la DLL del provider AMSI non funzioni se dipende da altre DLL nel percorso da caricare nello stesso momento. Per evitare il Hijack della DLL, è consigliabile che la DLL del provider carichi le relative dipendenze in modo esplicito (con un percorso completo) utilizzando chiamate [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) sicure o equivalenti. Questa operazione è consigliata invece di basarsi sul comportamento di ricerca **LoadLibrary** .

La sezione seguente illustra come registrare il provider AMSI. Per il codice di esempio completo che illustra come creare la propria DLL del provider AMSI, vedere l' [applicazione di esempio interfaccia IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registrare la DLL del provider con AMSI

Per iniziare, è necessario verificare che siano presenti le chiavi del registro di sistema di Windows.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Un provider AMSI è un server COM in-process. Di conseguenza, è necessario registrarsi con COM. Le classi COM sono registrate in `HKLM\SOFTWARE\Classes\CLSID` .

Il codice seguente illustra come registrare un provider AMSI, il cui GUID (per questo esempio) si presuppone che sia `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

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

Se la DLL implementa la [funzione DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), come nell'esempio precedente, è possibile registrarla usando l'eseguibile fornito da Windows `regsvr32.exe` . Da un prompt dei comandi con privilegi elevati, eseguire un comando di questo form.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

In questo esempio, il comando crea le voci seguenti.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**Predefinita    REG_SZ implementazione del provider AMSI di esempio**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Predefinita    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ entrambi**

Oltre alla normale registrazione COM, è anche necessario registrare il provider con AMSI. A tale scopo, aggiungere una voce alla chiave seguente.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Ad esempio,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
