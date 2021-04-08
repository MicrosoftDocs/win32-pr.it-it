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
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="0ff76-103">Pubblico degli sviluppatori e codice di esempio</span><span class="sxs-lookup"><span data-stu-id="0ff76-103">Developer audience, and sample code</span></span>

<span data-ttu-id="0ff76-104">L'interfaccia di analisi antimalware è progettata per l'uso da parte di due gruppi di sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="0ff76-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="0ff76-105">Sviluppatori di applicazioni che desiderano eseguire richieste ai prodotti antimalware dall'interno delle app.</span><span class="sxs-lookup"><span data-stu-id="0ff76-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="0ff76-106">Autori di terze parti di prodotti antimalware che vogliono offrire ai propri prodotti le funzionalità migliori per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0ff76-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="0ff76-107">Sviluppatori di applicazioni</span><span class="sxs-lookup"><span data-stu-id="0ff76-107">Application developers</span></span>

<span data-ttu-id="0ff76-108">AMSI è progettato in particolare per contrastare il "malware non file".</span><span class="sxs-lookup"><span data-stu-id="0ff76-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="0ff76-109">I tipi di applicazioni che possono sfruttare in modo ottimale la tecnologia AMSI includono i motori di script, le applicazioni che necessitano di buffer di memoria da analizzare prima di usarli e le applicazioni che elaborano file che possono contenere codice eseguibile non PE, ad esempio macro di Microsoft Word ed Excel o documenti PDF.</span><span class="sxs-lookup"><span data-stu-id="0ff76-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="0ff76-110">Tuttavia, l'utilità della tecnologia AMSI non è limitata a questi esempi.</span><span class="sxs-lookup"><span data-stu-id="0ff76-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="0ff76-111">Esistono due modi in cui è possibile interfacciarsi con AMSI nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ff76-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="0ff76-112">Utilizzando le API Win32 AMSI.</span><span class="sxs-lookup"><span data-stu-id="0ff76-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="0ff76-113">Vedere [funzioni AMSI (antimalware Scan Interface)](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="0ff76-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="0ff76-114">Utilizzando le interfacce COM AMSI.</span><span class="sxs-lookup"><span data-stu-id="0ff76-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="0ff76-115">Vedere [interfaccia **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="0ff76-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="0ff76-116">Per il codice di esempio che illustra come usare AMSI all'interno dell'applicazione COM, vedere l' [applicazione di esempio interfaccia IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="0ff76-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="0ff76-117">Autori di terze parti di prodotti antimalware</span><span class="sxs-lookup"><span data-stu-id="0ff76-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="0ff76-118">In qualità di creatore di prodotti antimalware, è possibile scegliere di creare e registrare il proprio server COM in-process (DLL) per funzionare come provider AMSI.</span><span class="sxs-lookup"><span data-stu-id="0ff76-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="0ff76-119">Il provider AMSI deve implementare l' [interfaccia **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)e deve essere eseguito in-process.</span><span class="sxs-lookup"><span data-stu-id="0ff76-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="0ff76-120">Si noti che, dopo Windows 10, versione 1709 (l'aggiornamento degli autori di cadute 2017), è possibile che la DLL del provider AMSI non funzioni se dipende da altre DLL nel percorso da caricare nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="0ff76-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="0ff76-121">Per evitare il Hijack della DLL, è consigliabile che la DLL del provider carichi le relative dipendenze in modo esplicito (con un percorso completo) utilizzando chiamate [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) sicure o equivalenti.</span><span class="sxs-lookup"><span data-stu-id="0ff76-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="0ff76-122">Questa operazione è consigliata invece di basarsi sul comportamento di ricerca **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="0ff76-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="0ff76-123">La sezione seguente illustra come registrare il provider AMSI.</span><span class="sxs-lookup"><span data-stu-id="0ff76-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="0ff76-124">Per il codice di esempio completo che illustra come creare la propria DLL del provider AMSI, vedere l' [applicazione di esempio interfaccia IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="0ff76-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="0ff76-125">Registrare la DLL del provider con AMSI</span><span class="sxs-lookup"><span data-stu-id="0ff76-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="0ff76-126">Per iniziare, è necessario verificare che siano presenti le chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ff76-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="0ff76-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span><span class="sxs-lookup"><span data-stu-id="0ff76-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="0ff76-128">HKLM\SOFTWARE\Classes\CLSID</span><span class="sxs-lookup"><span data-stu-id="0ff76-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="0ff76-129">Un provider AMSI è un server COM in-process.</span><span class="sxs-lookup"><span data-stu-id="0ff76-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="0ff76-130">Di conseguenza, è necessario registrarsi con COM.</span><span class="sxs-lookup"><span data-stu-id="0ff76-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="0ff76-131">Le classi COM sono registrate in `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="0ff76-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="0ff76-132">Il codice seguente illustra come registrare un provider AMSI, il cui GUID (per questo esempio) si presuppone che sia `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="0ff76-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

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

<span data-ttu-id="0ff76-133">Se la DLL implementa la [funzione DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), come nell'esempio precedente, è possibile registrarla usando l'eseguibile fornito da Windows `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="0ff76-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="0ff76-134">Da un prompt dei comandi con privilegi elevati, eseguire un comando di questo form.</span><span class="sxs-lookup"><span data-stu-id="0ff76-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="0ff76-135">In questo esempio, il comando crea le voci seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ff76-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="0ff76-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="0ff76-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="0ff76-137">&nbsp;&nbsp;&nbsp;&nbsp;**Predefinita    REG_SZ implementazione del provider AMSI di esempio**</span><span class="sxs-lookup"><span data-stu-id="0ff76-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="0ff76-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="0ff76-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="0ff76-139">&nbsp;&nbsp;&nbsp;&nbsp;**Predefinita    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="0ff76-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="0ff76-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ entrambi**</span><span class="sxs-lookup"><span data-stu-id="0ff76-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="0ff76-141">Oltre alla normale registrazione COM, è anche necessario registrare il provider con AMSI.</span><span class="sxs-lookup"><span data-stu-id="0ff76-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="0ff76-142">A tale scopo, aggiungere una voce alla chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="0ff76-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="0ff76-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span><span class="sxs-lookup"><span data-stu-id="0ff76-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="0ff76-144">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="0ff76-144">For example,</span></span>

<span data-ttu-id="0ff76-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="0ff76-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
