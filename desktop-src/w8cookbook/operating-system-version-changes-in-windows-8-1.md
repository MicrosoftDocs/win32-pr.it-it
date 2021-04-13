---
title: Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
description: Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399644"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="b2874-103">Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2874-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="b2874-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="b2874-104">Platforms</span></span>

<span data-ttu-id="b2874-105">**Client-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2874-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="b2874-106">**Server-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2874-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="b2874-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2874-107">Description</span></span>

<span data-ttu-id="b2874-108">Sono state apportate alcune modifiche significative al funzionamento delle API GetVersion (ex) in Windows 8.1 a causa di comportamenti indesiderati dei clienti che derivano dal modo in cui le API GetVersion (ex) sono state usate in passato.</span><span class="sxs-lookup"><span data-stu-id="b2874-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="b2874-109">Nelle versioni precedenti di Windows, la chiamata delle API GetVersion (ex) restituisce la versione effettiva del sistema operativo, a meno che il processo non sia stato mitigato da uno shim di compatibilità dell'app per assegnargli una versione diversa.</span><span class="sxs-lookup"><span data-stu-id="b2874-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="b2874-110">Questa operazione è stata eseguita su base provvisoria ed era relativamente incompleta in termini di numero di processi che Microsoft poteva ragionevolmente shim in una versione.</span><span class="sxs-lookup"><span data-stu-id="b2874-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="b2874-111">Molte applicazioni attraversano le crepe perché non ricevono sottoposto a shim a causa di verifiche della versione progettate in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="b2874-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="b2874-112">Il numero uno dei motivi per eseguire un controllo della versione consiste nel segnalare all'utente che l'applicazione deve essere eseguita in una versione più recente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b2874-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="b2874-113">Tuttavia, a causa dei controlli di scarsa qualità, le app spesso avvisano erroneamente che erano necessarie per l'esecuzione in Windows XP o versioni successive, ovviamente il sistema operativo più recente è.</span><span class="sxs-lookup"><span data-stu-id="b2874-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="b2874-114">Spesso, il sistema operativo più recente eseguirebbe l'applicazione senza problemi se non per questi controlli.</span><span class="sxs-lookup"><span data-stu-id="b2874-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b2874-115">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="b2874-115">Manifestation</span></span>

<span data-ttu-id="b2874-116">In Windows 8.1, le API GetVersion (ex) sono state deprecate.</span><span class="sxs-lookup"><span data-stu-id="b2874-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="b2874-117">Ciò significa che, sebbene sia comunque possibile chiamare queste funzioni API, se l'app non è destinata in modo specifico Windows 8.1, le funzioni restituiranno la versione di Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="b2874-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="b2874-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="b2874-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="b2874-119">Aggiunta di un manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b2874-119">Adding an app manifest</span></span>

<span data-ttu-id="b2874-120">Per fare in modo che l'app abbia come destinazione Windows 8.1, è necessario includere un [manifesto dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app.</span><span class="sxs-lookup"><span data-stu-id="b2874-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="b2874-121">Quindi, nella sezione [ **&lt; compatibilità &gt;**](../SbsCs/application-manifests.md#compatibility) del manifesto è necessario aggiungere un elemento **&lt; &gt; supportos** per ogni versione di Windows che si vuole dichiarare supportata dall'app.</span><span class="sxs-lookup"><span data-stu-id="b2874-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="b2874-122">Nell'esempio seguente viene illustrato un file manifesto dell'applicazione per un'applicazione che supporta tutte le versioni di Windows da Windows Vista a Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="b2874-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

<span data-ttu-id="b2874-123">La riga sopra contrassegnata `* ADD THIS LINE *` Mostra come indirizzare l'applicazione in modo accurato per Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b2874-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="b2874-124">La dichiarazione del supporto per Windows 8.1 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="b2874-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="b2874-125">Utilizzo di VersionHelpers anziché GetVersion (es)</span><span class="sxs-lookup"><span data-stu-id="b2874-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="b2874-126">Windows 8.1 introduce nuove funzioni API sostitutive per GetVersion (ex), noto come VersionHelpers.</span><span class="sxs-lookup"><span data-stu-id="b2874-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="b2874-127">Sono estremamente facili da usare. è sufficiente `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="b2874-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="b2874-128">Le funzioni inline disponibili nel file di intestazione VersionHelpers. h consentono al codice di richiedere se il sistema operativo è una versione specifica di Windows o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b2874-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="b2874-129">**Esempio** Se, ad esempio, l'applicazione richiede Windows 8 o versione successiva, usare il test seguente:</span><span class="sxs-lookup"><span data-stu-id="b2874-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="b2874-130">Le funzioni API VersionHelper disponibili sono:</span><span class="sxs-lookup"><span data-stu-id="b2874-130">The available VersionHelper API functions are:</span></span>

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

<span data-ttu-id="b2874-131">Verranno restituiti TRUE o FALSE a seconda della domanda richiesta ed è sufficiente definire il sistema operativo di livello minimo supportato.</span><span class="sxs-lookup"><span data-stu-id="b2874-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="b2874-132">Risorse</span><span class="sxs-lookup"><span data-stu-id="b2874-132">Resources</span></span>

-   [<span data-ttu-id="b2874-133">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="b2874-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="b2874-134">[Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b2874-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="b2874-135">API VersionHelpers</span><span class="sxs-lookup"><span data-stu-id="b2874-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)