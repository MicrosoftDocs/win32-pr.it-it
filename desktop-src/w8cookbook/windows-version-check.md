---
title: Controllo della versione di Windows
description: La versione del sistema operativo è stata incrementata con la versione del sistema operativo Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118602"
---
# <a name="windows-version-check"></a><span data-ttu-id="a7fd3-103">Controllo della versione di Windows</span><span class="sxs-lookup"><span data-stu-id="a7fd3-103">Windows version check</span></span>

<span data-ttu-id="a7fd3-104">La versione del sistema operativo è stata incrementata con la versione del sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="a7fd3-105">Questo significa che anche il numero di versione interno per Windows 10 è stato modificato in 10,0.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="a7fd3-106">Come in passato, Microsoft si impegna al massimo per mantenere la compatibilità di applicazioni e dispositivi dopo un cambiamento di versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="a7fd3-107">Per la maggior parte delle categorie di app, senza alcuna dipendenza dal kernel, la modifica non influirà negativamente sulla funzionalità dell'app e le app esistenti continueranno a funzionare correttamente in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="a7fd3-108">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="a7fd3-108">Manifestations</span></span>

<span data-ttu-id="a7fd3-109">Gli effetti di questa modifica dipendono dalle app.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="a7fd3-110">Questo significa che le app che controllano in modo specifico la versione del sistema operativo otterranno un numero di versione superiore, con queste possibili conseguenze:</span><span class="sxs-lookup"><span data-stu-id="a7fd3-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="a7fd3-111">È possibile che i programmi di installazione delle app non riescano a installare le app e che le app non si avviino.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="a7fd3-112">Le app potrebbero diventare instabili o subire arresti anomali.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="a7fd3-113">Le app potrebbero generare messaggi di errore, ma continuare a funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="a7fd3-114">Alcune app eseguono un controllo della versione e si limitano a inviare un avviso agli utenti.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="a7fd3-115">Esistono tuttavia alcune app strettamente vincolate al controllo della versione (nei driver o in modalità kernel per evitare il rilevamento).</span><span class="sxs-lookup"><span data-stu-id="a7fd3-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="a7fd3-116">In questi casi, si verifica un errore dell'app se viene rilevata una versione errata.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="a7fd3-117">Invece del controllo della versione, è consigliabile uno degli approcci seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7fd3-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="a7fd3-118">Se l'app dipende da funzionalità API specifiche, assicurati di usare come destinazione la versione dell'API corretta.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="a7fd3-119">Il numero di versione di NTDDI (NT Device Driver Interface) viene incrementato solo se le funzionalità di destinazione nell'API cambiano.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="a7fd3-120">Assicurarsi di rilevare la modifica tramite l'API o altre API esposte create dal team di funzionalità e non usare la versione come proxy per alcune funzionalità o correzioni.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="a7fd3-121">Se sono presenti modifiche importanti e non viene esposto un controllo appropriato, si tratta di un bug.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="a7fd3-122">Assicurarsi che l'app non verifichi la versione in modo strano, ad esempio tramite il registro di sistema, le versioni dei file, gli offset, la modalità kernel, i driver o altri mezzi.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="a7fd3-123">Se l'app deve assolutamente verificare la versione, usare le API GetVersion, che devono restituire il numero principale, secondario e Build.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="a7fd3-124">Se si usa l'API GetVersion o altre funzioni di supporto della versione, ad esempio [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), tenere presente che il comportamento di questa API è stato modificato a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="a7fd3-125">Per altri dettagli, vedere [la documentazione dell'API](../SysInfo/version-helper-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fd3-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="a7fd3-126">Se si possiedono app come antimalware o firewall, è consigliabile usare i normali canali di feedback e il programma Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="a7fd3-127">Dichiarazione della compatibilità di Windows 10 con un manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a7fd3-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="a7fd3-128">Se l'app è compatibile con Windows 10, può dichiarare questo fatto nel manifesto dell' [app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="a7fd3-129">Indica al sistema che l'app riconosce il numero di versione del sistema di Windows 10 di 10,0 (pertanto l'API GetVersion non restituisce una versione precedente) e consente inoltre al sistema di disattivare altri comportamenti di compatibilità applicati alle app che non dichiarano la compatibilità con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="a7fd3-130">Per dichiarare la compatibilità di Windows 10 in un manifesto dell'applicazione, è necessario aggiungere una sezione di [ **&lt; compatibilità &gt;**](../SbsCs/application-manifests.md#compatibility) del manifesto, se non ne esiste già una, **&lt; &gt;** e quindi aggiungere gli elementi supportati per Windows 10 e tutte le altre versioni di Windows che si vuole dichiarare supportate dall'app.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="a7fd3-131">Nell'esempio seguente viene illustrato un file manifesto dell'applicazione per un'applicazione che supporta tutte le versioni di Windows da Windows Vista a Windows 10:</span><span class="sxs-lookup"><span data-stu-id="a7fd3-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
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

<span data-ttu-id="a7fd3-132">La riga sopra contrassegnata `* ADD THIS LINE *` Mostra come indirizzare l'applicazione in modo accurato per Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="a7fd3-133">La dichiarazione del supporto per Windows 10 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="a7fd3-134">Risorse</span><span class="sxs-lookup"><span data-stu-id="a7fd3-134">Resources</span></span>

-   [<span data-ttu-id="a7fd3-135">Download di Application Compatibility Toolkit: scaricare Windows ADK per Windows 10</span><span class="sxs-lookup"><span data-stu-id="a7fd3-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="a7fd3-136">[Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a7fd3-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="a7fd3-137">API della versione Helper</span><span class="sxs-lookup"><span data-stu-id="a7fd3-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)