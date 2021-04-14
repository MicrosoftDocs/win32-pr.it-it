---
title: Sviluppo di applicazioni per versioni precedenti di Windows
description: Illustra le operazioni da eseguire per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare i vantaggi offerti dall'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104401844"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="10aac-103">Sviluppo di applicazioni per versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="10aac-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="10aac-104">Illustra le operazioni da eseguire per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare i vantaggi offerti dall'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10aac-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="10aac-105">Download necessari</span><span class="sxs-lookup"><span data-stu-id="10aac-105">Required Downloads</span></span>

<span data-ttu-id="10aac-106">Il download e l'installazione dei pacchetti descritti nelle sezioni seguenti sono necessari se si desidera sviluppare applicazioni che utilizzano API introdotte con Microsoft Windows Software Development Kit (SDK) per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10aac-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="10aac-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="10aac-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="10aac-108">Il Windows SDK per Windows 7 è necessario per la creazione di applicazioni che usano le API supportate con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10aac-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="10aac-109">Per accedere a risorse e informazioni aggiuntive, ad esempio download, post del forum e il Blog del team di Windows SDK, vedere il [centro per sviluppatori di Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10aac-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="10aac-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="10aac-110">.NET Framework</span></span>

<span data-ttu-id="10aac-111">Il .NET Framework 3,5 Service Pack 1 è necessario per la creazione di applicazioni che utilizzano le API supportate dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10aac-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="10aac-112">Per ulteriori risorse e informazioni, vedere il [centro per sviluppatori .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10aac-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="10aac-113">DirectX SDK è necessario quando si usa Direct3D</span><span class="sxs-lookup"><span data-stu-id="10aac-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="10aac-114">Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) è necessario per la creazione di applicazioni che usano le API supportate dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10aac-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="10aac-115">Aggiornare il computer di sviluppo</span><span class="sxs-lookup"><span data-stu-id="10aac-115">Update Your Development Computer</span></span>

<span data-ttu-id="10aac-116">Verificare che nel computer di sviluppo siano disponibili tutti gli aggiornamenti più recenti da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="10aac-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="10aac-117">Se si sviluppano applicazioni in una versione precedente di Windows, è necessario ottenere l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="10aac-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="10aac-118">L'installazione di uno di questi aggiornamenti consentirà di sfruttare la nuova API fornita dalla Windows SDK per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10aac-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="10aac-119">Per ulteriori informazioni su come ottenere gli aggiornamenti da Windows Update, vedere l' [articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="10aac-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="10aac-120">Ambiente di sviluppo</span><span class="sxs-lookup"><span data-stu-id="10aac-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="10aac-121">Impostare la destinazione di compilazione su Windows 7</span><span class="sxs-lookup"><span data-stu-id="10aac-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="10aac-122">Tutte le applicazioni che utilizzano le librerie nell'aggiornamento della piattaforma per Windows Vista devono essere compilate con la piattaforma di destinazione di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10aac-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="10aac-123">L'impostazione di WINVER sul valore della piattaforma di destinazione Windows 7 consente di sviluppare applicazioni che utilizzano API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 in un computer di sviluppo che esegue Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10aac-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="10aac-124">È possibile impostare la piattaforma di destinazione su Windows 7 nel codice sorgente o usando l'opzione/D con il compilatore di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="10aac-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="10aac-125">Nell'esempio seguente viene illustrato come impostare WINVER nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="10aac-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="10aac-126">Nell'esempio seguente viene illustrato come impostare WINVER utilizzando l'opzione del compilatore/D.</span><span class="sxs-lookup"><span data-stu-id="10aac-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="10aac-127">Distribuzione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="10aac-127">Application Deployment</span></span>

<span data-ttu-id="10aac-128">Se si compila l'applicazione usando le intestazioni e le librerie fornite dal Windows SDK per Windows 7, le API supportate vengono eseguite in qualsiasi versione di Windows con aggiornamento della piattaforma per Windows Vista o aggiornamento della piattaforma per Windows Server 2008 installato.</span><span class="sxs-lookup"><span data-stu-id="10aac-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="10aac-129">Il comportamento, le prestazioni o i requisiti per alcune API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono variare nelle diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="10aac-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="10aac-130">Per informazioni dettagliate su un'API specifica supportata dagli aggiornamenti, vedere [informazioni sull'aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10aac-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="10aac-131">Nessun componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="10aac-131">No Redistributable Components</span></span>

<span data-ttu-id="10aac-132">Non è necessario che l'applicazione installi componenti ridistribuibili, ad esempio dll o altri file di run-time.</span><span class="sxs-lookup"><span data-stu-id="10aac-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="10aac-133">Richiede il computer End-User aggiornato</span><span class="sxs-lookup"><span data-stu-id="10aac-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="10aac-134">Poiché l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono ospitati da Windows Update, gli utenti finali con aggiornamenti automatici abilitati hanno molto probabilmente già questi aggiornamenti, oltre ai Service Pack necessari.</span><span class="sxs-lookup"><span data-stu-id="10aac-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="10aac-135">Se nel computer dell'utente finale non è installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 e l'applicazione richiede API supportate con questi aggiornamenti, è possibile che l'applicazione non sia in grado di essere eseguita nel computer dell'utente finale o che si verifichino errori durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="10aac-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="10aac-136">Per evitare i problemi che potrebbero essere causati dal computer dell'utente non aggiornato, è necessario verificare che nel computer dell'utente sia installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 durante l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10aac-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="10aac-137">È possibile usare l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client) per verificare la presenza di aggiornamenti installati nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="10aac-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="10aac-138">È anche possibile usare l'API dell'agente di Windows Update per scaricare e installare gli aggiornamenti necessari durante l'installazione dell'applicazione se l'utente finale non ha ancora installato gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="10aac-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="10aac-139">Per un esempio di un programma di installazione che illustra come usare l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client), vedere la pagina relativa alla distribuzione di [Direct3D 11 per sviluppatori di giochi](../direct3darticles/direct3d11-deployment.md) in [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10aac-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="10aac-140">Sebbene l'esempio di programma di installazione di D3D11InstallHelper, illustrato nella [distribuzione di Direct3D 11 per gli sviluppatori di giochi](../direct3darticles/direct3d11-deployment.md), sia stato scritto per applicazioni che utilizzano Direct3D 11, fornisce un valido esempio di interazione con l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client) per avviare e tenere traccia del download e dell'installazione degli aggiornamenti ospitati da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="10aac-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="10aac-141">La compilazione di questo esempio potrebbe richiedere la Windows SDK per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10aac-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="10aac-142">Per ulteriori informazioni sull'esempio D3D11InstallHelper, inclusi i problemi noti, vedere [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) Note sulla versione per agosto 2009. aggiornamento della piattaforma per Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="10aac-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="10aac-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10aac-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10aac-144">Aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10aac-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="10aac-145">**Cenni preliminari**</span><span class="sxs-lookup"><span data-stu-id="10aac-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="10aac-146">Informazioni sull'aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10aac-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="10aac-147">Articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="10aac-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 