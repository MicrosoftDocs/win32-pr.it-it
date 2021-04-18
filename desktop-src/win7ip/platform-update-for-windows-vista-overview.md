---
title: Informazioni sull'aggiornamento della piattaforma per Windows Vista
description: Viene fornita una panoramica sull'aggiornamento della piattaforma per Windows Vista e sull'aggiornamento della piattaforma per Windows Server 2008 e sulle relative funzionalità.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Aggiornamento della piattaforma per Windows Server 2008
- Aggiornamento della piattaforma per Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321128"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="fe23b-105">Informazioni sull'aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="fe23b-106">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono aggiornamenti del sistema operativo degli utenti finali che supportano l'utilizzo di tecnologie Windows 7 selezionate nelle versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="fe23b-107">Gli aggiornamenti includono un set di librerie di runtime che consentono agli sviluppatori di applicazioni di avere come destinazione le versioni correnti, Windows 7 e Windows Server 2008 R2, nonché le versioni precedenti, Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="fe23b-108">Riepilogo dell'API supportata per tecnologia</span><span class="sxs-lookup"><span data-stu-id="fe23b-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="fe23b-109">Ogni tecnologia supportata dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per gli aggiornamenti di Windows Server 2008 include un set di API che è possibile usare in un'applicazione destinata a una versione precedente di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="fe23b-110">Per ulteriori informazioni sull'utilizzo delle API supportate dagli aggiornamenti in un'applicazione destinata a versioni precedenti di Windows, vedere [sviluppo di applicazioni per versioni precedenti di Windows](developing-applications-for-previous-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fe23b-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="fe23b-111">Alcune API associate a una tecnologia potrebbero non essere supportate e il comportamento, le prestazioni o i requisiti per alcune API supportate possono variare nelle diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="fe23b-112">Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.</span><span class="sxs-lookup"><span data-stu-id="fe23b-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="fe23b-113">Tecnologie supportate con l'aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="fe23b-114">Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.</span><span class="sxs-lookup"><span data-stu-id="fe23b-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="fe23b-115">Nella tabella seguente sono illustrate le tecnologie supportate per Windows Vista e Windows XP con l'aggiornamento della piattaforma per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe23b-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="fe23b-116">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="fe23b-116">Technology</span></span>                                                                                    | <span data-ttu-id="fe23b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-117">Windows Vista</span></span> | <span data-ttu-id="fe23b-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe23b-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="fe23b-119">API di automazione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="fe23b-120">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-120">Yes</span></span>           | <span data-ttu-id="fe23b-121">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-121">Yes</span></span>        |
| [<span data-ttu-id="fe23b-122">Grafica di Windows, creazione di immagini e libreria XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="fe23b-123">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-123">Yes</span></span>           | <span data-ttu-id="fe23b-124">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-124">No</span></span>         |
| [<span data-ttu-id="fe23b-125">Libreria della barra multifunzione di Windows e gestione animazioni</span><span class="sxs-lookup"><span data-stu-id="fe23b-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="fe23b-126">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-126">Yes</span></span>           | <span data-ttu-id="fe23b-127">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-127">No</span></span>         |
| [<span data-ttu-id="fe23b-128">Piattaforma per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="fe23b-129">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-129">Yes</span></span>           | <span data-ttu-id="fe23b-130">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="fe23b-131">Tecnologie supportate con l'aggiornamento della piattaforma per Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe23b-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="fe23b-132">Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.</span><span class="sxs-lookup"><span data-stu-id="fe23b-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="fe23b-133">Nella tabella seguente sono illustrate le tecnologie supportate per Windows Server 2008 e Windows Server 2003 con l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="fe23b-134">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="fe23b-134">Technology</span></span>                                                                                    | <span data-ttu-id="fe23b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe23b-135">Windows Server 2008</span></span> | <span data-ttu-id="fe23b-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe23b-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="fe23b-137">API di automazione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="fe23b-138">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-138">Yes</span></span>                 | <span data-ttu-id="fe23b-139">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-139">Yes</span></span>                 |
| [<span data-ttu-id="fe23b-140">Grafica di Windows, creazione di immagini e libreria XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="fe23b-141">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-141">Yes</span></span>                 | <span data-ttu-id="fe23b-142">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-142">No</span></span>                  |
| [<span data-ttu-id="fe23b-143">Libreria della barra multifunzione di Windows e gestione animazioni</span><span class="sxs-lookup"><span data-stu-id="fe23b-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="fe23b-144">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-144">Yes</span></span>                 | <span data-ttu-id="fe23b-145">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-145">No</span></span>                  |
| [<span data-ttu-id="fe23b-146">Piattaforma per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="fe23b-147">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-147">No</span></span>                  | <span data-ttu-id="fe23b-148">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="fe23b-149">Descrizioni dell'API supportata per tecnologia</span><span class="sxs-lookup"><span data-stu-id="fe23b-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="fe23b-150">Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.</span><span class="sxs-lookup"><span data-stu-id="fe23b-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="fe23b-151">API di automazione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="fe23b-152">Grafica di Windows, creazione di immagini e libreria XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="fe23b-153">Libreria della barra multifunzione di Windows e gestione animazioni</span><span class="sxs-lookup"><span data-stu-id="fe23b-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="fe23b-154">Piattaforma per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="fe23b-155">API di automazione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-155">Windows Automation API</span></span>

<span data-ttu-id="fe23b-156">L'API di automazione di Windows 3,0 è un set di dll e di elementi API che consentono ai prodotti di Assistive Technology (AT) di offrire un migliore accesso ai computer per singoli utenti che hanno difficoltà fisiche o cognitive, problemi o disabilità.</span><span class="sxs-lookup"><span data-stu-id="fe23b-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="fe23b-157">Inoltre, poiché l'API di automazione di Windows 3,0 consente alle applicazioni di accedere e modificare gli elementi dell'interfaccia utente di altre applicazioni, è una tecnologia ideale per l'implementazione di strumenti di test automatizzati.</span><span class="sxs-lookup"><span data-stu-id="fe23b-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="fe23b-158">Microsoft Active Accessibility (MSAA) e l'automazione dell'interfaccia utente sono simili in quanto entrambi forniscono un mezzo per esporre e raccogliere informazioni sugli elementi e i controlli dell'interfaccia utente per supportare l'accessibilità dell'interfaccia utente e l'automazione dei test software.</span><span class="sxs-lookup"><span data-stu-id="fe23b-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="fe23b-159">Automazione interfaccia utente è un'implementazione di Windows della specifica di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="fe23b-160">Si tratta di una tecnologia più recente che risolve molte delle limitazioni di MSAA.</span><span class="sxs-lookup"><span data-stu-id="fe23b-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="fe23b-161">Per ulteriori informazioni sull'API di automazione di Windows 3,0, vedere [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span><span class="sxs-lookup"><span data-stu-id="fe23b-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="fe23b-162">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 supportano la seguente API di automazione Windows 3,0:</span><span class="sxs-lookup"><span data-stu-id="fe23b-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="fe23b-163">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="fe23b-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="fe23b-164">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fe23b-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="fe23b-165">Edizioni di Windows idonee per gli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="fe23b-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="fe23b-166">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto per l'API di automazione di Windows 3,0 nelle edizioni di Windows illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe23b-167">Versione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-167">Windows Version</span></span></th>
<th><span data-ttu-id="fe23b-168">Edizioni idonee per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe23b-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe23b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="fe23b-170">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="fe23b-171">Home Basic con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-172">Home Premium con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-173">Business con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-174">Enterprise con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-175">Ultimate con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe23b-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe23b-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="fe23b-177">Windows XP Home con SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="fe23b-178">Windows XP Professional con SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe23b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe23b-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="fe23b-180">Windows Server 2008 con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe23b-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe23b-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="fe23b-182">Windows Server 2003 con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="fe23b-183">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="fe23b-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="fe23b-184">Microsoft Active Accessibility (MSAA) è una tecnologia legacy introdotta per la prima volta con Windows 95.</span><span class="sxs-lookup"><span data-stu-id="fe23b-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="fe23b-185">Si tratta di un set di API che consente di migliorare il funzionamento dei prodotti Assistive Technology (AT) con le applicazioni eseguite in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="fe23b-186">L'API fornisce interfacce di programmazione e metodi per esporre le informazioni sugli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="fe23b-187">Per ulteriori informazioni su Microsoft Active Accessibility, vedere la [Panoramica tecnica](/windows/desktop/WinAuto/technical-overview).</span><span class="sxs-lookup"><span data-stu-id="fe23b-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="fe23b-188">Elementi API Microsoft Active Accessibility supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="fe23b-189">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="fe23b-190">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fe23b-190">UI Automation</span></span>

<span data-ttu-id="fe23b-191">Automazione interfaccia utente è una tecnologia più recente che implementa la specifica di automazione interfaccia utente e risolve molte delle limitazioni di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fe23b-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="fe23b-192">Si tratta di un set di API che fornisce l'accesso programmatico agli elementi dell'interfaccia utente delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fe23b-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="fe23b-193">L'API fornita consente ai prodotti di Assistive Technology e agli strumenti di test automatici di accedere, identificare e modificare gli elementi dell'interfaccia utente standard e personalizzati di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe23b-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="fe23b-194">Per altre informazioni sull'automazione dell'interfaccia utente, vedere [API di automazione di Windows: automazione interfaccia utente](../winauto/entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="fe23b-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="fe23b-195">Elementi API di automazione interfaccia utente supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="fe23b-196">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="fe23b-197">Esecuzione di automazione interfaccia utente nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="fe23b-198">A causa delle differenze nel modo in cui i controlli comuni e i controlli standard di Windows sono implementati in versioni diverse di Windows, è possibile che si verifichino lievi differenze nelle informazioni che i proxy di automazione interfaccia utente recuperano per questi controlli da una versione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="fe23b-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="fe23b-199">Grafica di Windows, creazione di immagini e libreria XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="fe23b-200">L'aggiornamento della piattaforma per Windows Vista supporta le seguenti API di Windows 7 dalla libreria grafica, imaging e XPS di Windows:</span><span class="sxs-lookup"><span data-stu-id="fe23b-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="fe23b-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="fe23b-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="fe23b-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="fe23b-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="fe23b-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="fe23b-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="fe23b-204">Packaging</span><span class="sxs-lookup"><span data-stu-id="fe23b-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="fe23b-205">Componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="fe23b-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="fe23b-206">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="fe23b-207">Stampa XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="fe23b-208">Edizioni di Windows idonee per gli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="fe23b-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="fe23b-209">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della libreria XPS, della grafica e della creazione di immagini di Windows nelle edizioni di Windows illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe23b-210">Versione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-210">Windows Version</span></span></th>
<th><span data-ttu-id="fe23b-211">Edizioni idonee per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe23b-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe23b-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="fe23b-213">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="fe23b-214">Home Basic con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-215">Home Premium con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-216">Business con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-217">Enterprise con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-218">Ultimate con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe23b-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe23b-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="fe23b-220">Windows Server 2008 con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="fe23b-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="fe23b-221">Direct2D</span></span>

<span data-ttu-id="fe23b-222">L'API Direct2D è una nuova API grafica 2D in modalità immediata e con accelerazione hardware che fornisce prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo.</span><span class="sxs-lookup"><span data-stu-id="fe23b-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="fe23b-223">L'API Direct2D è progettata per interagire correttamente con il codice esistente che usa GDI, GDI+ o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fe23b-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="fe23b-224">Per ulteriori informazioni su Direct2D, vedere [informazioni su Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span><span class="sxs-lookup"><span data-stu-id="fe23b-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="fe23b-225">Elementi API Direct2D supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="fe23b-226">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="fe23b-227">Esecuzione di Direct2D nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="fe23b-228">Se il driver WDDM 1,1 non è presente in Windows Vista, le prestazioni dell'interoperabilità Direct2D/GDI peggiorano.</span><span class="sxs-lookup"><span data-stu-id="fe23b-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="fe23b-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="fe23b-229">Direct3D</span></span>

<span data-ttu-id="fe23b-230">L'aggiornamento della piattaforma per Windows Vista fornisce il supporto di BGRA Surface per i percorsi di codice Direct3D10 e Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="fe23b-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="fe23b-231">Direct3D10Level9 consente la funzionalità di Direct3D10 per l'uso di hardware Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="fe23b-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="fe23b-232">Direct3D WARP10 è un'applicazione di rasterizzazione software a prestazioni elevate per le applicazioni Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="fe23b-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="fe23b-233">Direct3D11, la versione più recente di Direct3D, fornisce nuove funzionalità, ad esempio il supporto per il multithreading migliorato, il mosaico, la funzionalità DirectCompute e il collegamento dinamico dello shader.</span><span class="sxs-lookup"><span data-stu-id="fe23b-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="fe23b-234">Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) è obbligatorio).</span><span class="sxs-lookup"><span data-stu-id="fe23b-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="fe23b-235">Per ulteriori informazioni su Direct3D, vedere [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fe23b-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="fe23b-236">Elementi API Direct3D supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="fe23b-237">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="fe23b-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="fe23b-238">DirectWrite</span></span>

<span data-ttu-id="fe23b-239">L'API DirectWrite è una nuova API di testo che offre più livelli di funzionalità, tra cui il layout del testo, l'elaborazione di script, il rendering del glifo e il sistema di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="fe23b-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="fe23b-240">DirectWrite usa i tipi di carattere OpenType e il rendering ClearType in pixel per migliorare l'esperienza di testo fornita dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fe23b-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="fe23b-241">Il rendering del testo viene accelerato dall'hardware se usato con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fe23b-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="fe23b-242">Per ulteriori informazioni su DirectWrite, vedere [Introduzione a DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span><span class="sxs-lookup"><span data-stu-id="fe23b-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="fe23b-243">Elementi API DirectWrite supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="fe23b-244">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="fe23b-245">Esecuzione di DirectWrite nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="fe23b-246">I problemi di comportamento seguenti potrebbero influire sull'uso dell'API DirectWrite nelle versioni precedenti di Windows:</span><span class="sxs-lookup"><span data-stu-id="fe23b-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="fe23b-247">Gli script nuovi in Windows 7 potrebbero non essere visualizzati correttamente nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="fe23b-248">Le impostazioni locali non disponibili nelle versioni precedenti di Windows eseguono il fallback al comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="fe23b-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="fe23b-249">Il sintonizzatore ClearType non è disponibile nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="fe23b-250">L'interoperabilità GDI ha un costo di memoria superiore in alcuni scenari nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="fe23b-251">Packaging</span><span class="sxs-lookup"><span data-stu-id="fe23b-251">Packaging</span></span>

<span data-ttu-id="fe23b-252">L'aggiornamento della piattaforma per Windows Vista supporta un subset limitato di API per la creazione di pacchetti necessari per eseguire attività con l'API documenti XPS nelle applicazioni non gestite.</span><span class="sxs-lookup"><span data-stu-id="fe23b-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="fe23b-253">Per altre informazioni sulle API per la creazione di pacchetti, vedere [Panoramica dell'API](/previous-versions/windows/desktop/opc/packaging-api-overview)di creazione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fe23b-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="fe23b-254">Elementi API di creazione pacchetti supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="fe23b-255">Sono supportate solo le seguenti interfacce di creazione pacchetti:</span><span class="sxs-lookup"><span data-stu-id="fe23b-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="fe23b-256">IOpcUri</span><span class="sxs-lookup"><span data-stu-id="fe23b-256">IOpcUri</span></span>
-   <span data-ttu-id="fe23b-257">IOpcPartUri</span><span class="sxs-lookup"><span data-stu-id="fe23b-257">IOpcPartUri</span></span>
-   <span data-ttu-id="fe23b-258">IOpcFactory (sono supportati solo i metodi seguenti)</span><span class="sxs-lookup"><span data-stu-id="fe23b-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="fe23b-259">CreatePackageRootUri</span><span class="sxs-lookup"><span data-stu-id="fe23b-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="fe23b-260">CreatePartUri</span><span class="sxs-lookup"><span data-stu-id="fe23b-260">CreatePartUri</span></span>
    -   <span data-ttu-id="fe23b-261">CreateStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="fe23b-261">CreateStreamOnFile</span></span>

<span data-ttu-id="fe23b-262">Le API di creazione pacchetti supportate possono essere usate per creare flussi su file, nonché per creare e interagire con l'URI basato su pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fe23b-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="fe23b-263">Esecuzione dell'API di creazione pacchetti nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="fe23b-264">Il comportamento e le prestazioni delle interfacce e dei metodi di creazione di pacchetti supportati sono gli stessi in tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="fe23b-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="fe23b-265">Se un'applicazione tenta di creare un'istanza o chiamare un'interfaccia o un metodo di creazione pacchetto non supportato, il tentativo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fe23b-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="fe23b-266">Se la chiamata è a un metodo [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) non supportato, \_ viene restituito il codice di errore E NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="fe23b-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="fe23b-267">Componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="fe23b-267">Windows Imaging Component</span></span>

<span data-ttu-id="fe23b-268">Le nuove funzionalità di Windows Imaging Component (WIC) includono una sicurezza avanzata, il supporto per l'interoperabilità con un colore elevato e una migliore interoperabilità dei metadati.</span><span class="sxs-lookup"><span data-stu-id="fe23b-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="fe23b-269">Inoltre, il componente Windows Imaging amplia la conformità agli standard fornendo supporto per la decodifica progressiva delle immagini, le funzionalità PNG espanse, i metadati GIF, gli aggiornamenti delle foto HD e i metadati che si estendono sui segmenti APPn.</span><span class="sxs-lookup"><span data-stu-id="fe23b-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="fe23b-270">Per ulteriori informazioni sul componente Windows Imaging, vedere [Cenni preliminari sul componente Windows Imaging](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span><span class="sxs-lookup"><span data-stu-id="fe23b-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="fe23b-271">Elementi API WIC supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-271">Supported WIC API Elements</span></span>

<span data-ttu-id="fe23b-272">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="fe23b-273">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-273">XPS Document</span></span>

<span data-ttu-id="fe23b-274">Le API documento XPS supportano la creazione, la modifica e il salvataggio di documenti XPS in applicazioni non gestite</span><span class="sxs-lookup"><span data-stu-id="fe23b-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="fe23b-275">Per ulteriori informazioni sulle API per documenti XPS, vedere la [Guida alla programmazione dei documenti XPS.](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe23b-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="fe23b-276">Elementi API Document XPS supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="fe23b-277">Solo le interfacce delle [firme digitali XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) non sono supportate nelle versioni del sistema operativo di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="fe23b-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="fe23b-278">Stampa XPS</span><span class="sxs-lookup"><span data-stu-id="fe23b-278">XPS Print</span></span>

<span data-ttu-id="fe23b-279">Le API di stampa XPS supportano la stampa di documenti XPS da applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="fe23b-280">Per altre informazioni sulle API di stampa XPS, vedere l' [API XpsPrint](/windows/desktop/printdocs/xpsprint-api).</span><span class="sxs-lookup"><span data-stu-id="fe23b-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="fe23b-281">Elementi API di stampa XPS supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="fe23b-282">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="fe23b-283">Libreria della barra multifunzione di Windows e gestione animazioni</span><span class="sxs-lookup"><span data-stu-id="fe23b-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="fe23b-284">L'aggiornamento della piattaforma per Windows Vista supporta le seguenti API di Windows 7 dalla barra multifunzione di Windows e dalla libreria di animazioni:</span><span class="sxs-lookup"><span data-stu-id="fe23b-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="fe23b-285">Framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="fe23b-286">Gestione animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="fe23b-287">Edizioni di Windows idonee per gli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="fe23b-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="fe23b-288">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della libreria della barra multifunzione di Windows e di gestione animazioni nelle edizioni di Windows illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe23b-289">Versione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-289">Windows Version</span></span></th>
<th><span data-ttu-id="fe23b-290">Edizioni idonee per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe23b-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe23b-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="fe23b-292">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="fe23b-293">Home Basic con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-294">Home Premium con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-295">Business con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-296">Enterprise con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-297">Ultimate con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe23b-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe23b-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="fe23b-299">Windows Server 2008 con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="fe23b-300">Framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="fe23b-301">Il Framework della barra multifunzione di Windows è un sistema avanzato per la presentazione di comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri delle attività delle applicazioni Windows tradizionali.</span><span class="sxs-lookup"><span data-stu-id="fe23b-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="fe23b-302">Il Framework è una raccolta di API Microsoft Win32 che forniscono una serie di nuove funzionalità dell'interfaccia utente per gli sviluppatori Windows e includono sia la barra multifunzione che un sistema di menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="fe23b-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="fe23b-303">Per ulteriori informazioni sul Framework della barra multifunzione, vedere [Introduzione al framework della barra](../windowsribbon/windowsribbon-introduction.md)multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="fe23b-304">Elementi API Framework della barra multifunzione supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="fe23b-305">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="fe23b-306">Gestione animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-306">Windows Animation Manager</span></span>

<span data-ttu-id="fe23b-307">Gestione animazioni Windows (animazione Windows) è un'interfaccia a livello di codice che supporta l'animazione di elementi visivi delle applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="fe23b-308">L'animazione Windows è progettata per semplificare lo sviluppo e la gestione delle sequenze di animazione e consentire agli sviluppatori di implementare animazioni coerenti e intuitive.</span><span class="sxs-lookup"><span data-stu-id="fe23b-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="fe23b-309">L'animazione Windows può essere usata con qualsiasi piattaforma grafica, ad esempio Direct2D, Direct3D o GDI+.</span><span class="sxs-lookup"><span data-stu-id="fe23b-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="fe23b-310">Animazione Windows è un'API COM a thread singolo che fornisce tutto ciò che uno sviluppatore deve creare, gestire e guidare l'animazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="fe23b-311">Per ulteriori informazioni su Windows Animation Manager, vedere [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span><span class="sxs-lookup"><span data-stu-id="fe23b-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="fe23b-312">Elementi API di gestione animazioni supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="fe23b-313">Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fe23b-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="fe23b-314">Piattaforma per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="fe23b-315">L'aggiornamento della piattaforma per Windows Vista supporta le estensioni di Windows 7 per la piattaforma Windows Mobile Devices (WPD).</span><span class="sxs-lookup"><span data-stu-id="fe23b-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="fe23b-316">Questa funzionalità consente ai computer di comunicare con i supporti e i dispositivi di archiviazione collegati.</span><span class="sxs-lookup"><span data-stu-id="fe23b-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="fe23b-317">WPD offre una soluzione flessibile e affidabile per la comunicazione dei computer con fotocamere digitali, lettori musicali, telefoni cellulari e molti altri tipi di dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="fe23b-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="fe23b-318">Per ulteriori informazioni sui dispositivi portatili Windows, vedere [dispositivi portatili Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .</span><span class="sxs-lookup"><span data-stu-id="fe23b-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="fe23b-319">Edizioni di Windows idonee per gli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="fe23b-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="fe23b-320">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto per dispositivi portatili Windows (WPD) nelle edizioni di Windows illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fe23b-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe23b-321">Versione di Windows</span><span class="sxs-lookup"><span data-stu-id="fe23b-321">Windows Version</span></span></th>
<th><span data-ttu-id="fe23b-322">Edizioni idonee per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe23b-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe23b-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="fe23b-324">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="fe23b-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="fe23b-325">Home Basic con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-326">Home Premium con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-327">Business con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-328">Enterprise con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="fe23b-329">Ultimate con SP2 (x86 e amd64)</span><span class="sxs-lookup"><span data-stu-id="fe23b-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="fe23b-330">Elementi API WPD supportati</span><span class="sxs-lookup"><span data-stu-id="fe23b-330">Supported WPD API Elements</span></span>

<span data-ttu-id="fe23b-331">La tabella seguente identifica le funzionalità supportate per Windows 7, Windows Vista e Windows Vista con aggiornamento della piattaforma per le versioni di Windows Vista del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="fe23b-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="fe23b-332">Funzionalità WPD</span><span class="sxs-lookup"><span data-stu-id="fe23b-332">WPD Feature</span></span>                    | <span data-ttu-id="fe23b-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe23b-333">Windows 7</span></span> | <span data-ttu-id="fe23b-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-334">Windows Vista</span></span> | <span data-ttu-id="fe23b-335">Windows Vista con aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="fe23b-336">MTP su USB</span><span class="sxs-lookup"><span data-stu-id="fe23b-336">MTP over USB</span></span>                   | <span data-ttu-id="fe23b-337">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-337">Yes</span></span>       | <span data-ttu-id="fe23b-338">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-338">Yes</span></span>           | <span data-ttu-id="fe23b-339">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-339">Yes</span></span>                                                  |
| <span data-ttu-id="fe23b-340">MTP su IP</span><span class="sxs-lookup"><span data-stu-id="fe23b-340">MTP over IP</span></span>                    | <span data-ttu-id="fe23b-341">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-341">Yes</span></span>       | <span data-ttu-id="fe23b-342">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-342">Yes</span></span>           | <span data-ttu-id="fe23b-343">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-343">Yes</span></span>                                                  |
| <span data-ttu-id="fe23b-344">MTP su Bluetooth</span><span class="sxs-lookup"><span data-stu-id="fe23b-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="fe23b-345">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-345">Yes</span></span>       | <span data-ttu-id="fe23b-346">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-346">No</span></span>            | <span data-ttu-id="fe23b-347">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-347">Yes</span></span>                                                  |
| <span data-ttu-id="fe23b-348">Servizi per dispositivi WPD e MTP</span><span class="sxs-lookup"><span data-stu-id="fe23b-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="fe23b-349">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-349">Yes</span></span>       | <span data-ttu-id="fe23b-350">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-350">No</span></span>            | <span data-ttu-id="fe23b-351">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-351">Yes</span></span>                                                  |
| <span data-ttu-id="fe23b-352">Automazione WPD</span><span class="sxs-lookup"><span data-stu-id="fe23b-352">WPD Automation</span></span>                 | <span data-ttu-id="fe23b-353">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-353">Yes</span></span>       | <span data-ttu-id="fe23b-354">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-354">No</span></span>            | <span data-ttu-id="fe23b-355">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-355">No</span></span>                                                   |
| <span data-ttu-id="fe23b-356">Multifunzione/multitransport</span><span class="sxs-lookup"><span data-stu-id="fe23b-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="fe23b-357">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-357">Yes</span></span>       | <span data-ttu-id="fe23b-358">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-358">No</span></span>            | <span data-ttu-id="fe23b-359">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-359">No</span></span>                                                   |
| <span data-ttu-id="fe23b-360">Device Stage</span><span class="sxs-lookup"><span data-stu-id="fe23b-360">Device Stage</span></span>                   | <span data-ttu-id="fe23b-361">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-361">Yes</span></span>       | <span data-ttu-id="fe23b-362">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-362">No</span></span>            | <span data-ttu-id="fe23b-363">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-363">No</span></span>                                                   |
| <span data-ttu-id="fe23b-364">Piattaforma di sincronizzazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="fe23b-364">Device Sync Platform</span></span>           | <span data-ttu-id="fe23b-365">Sì</span><span class="sxs-lookup"><span data-stu-id="fe23b-365">Yes</span></span>       | <span data-ttu-id="fe23b-366">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-366">No</span></span>            | <span data-ttu-id="fe23b-367">No</span><span class="sxs-lookup"><span data-stu-id="fe23b-367">No</span></span>                                                   |



 

<span data-ttu-id="fe23b-368">Per le edizioni di Windows 7 e Windows Vista in cui non è installato Microsoft Windows Media Player per impostazione predefinita (le edizioni N e KN), è necessario installare [Windows Media Format 11 SDK]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) per abilitare la funzionalità WPD.</span><span class="sxs-lookup"><span data-stu-id="fe23b-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="fe23b-369">Per ulteriori informazioni, vedere l' [articolo della Knowledge base](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , originariamente pubblicato come risoluzione per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe23b-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe23b-370">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe23b-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe23b-371">Aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="fe23b-372">**Cenni preliminari**</span><span class="sxs-lookup"><span data-stu-id="fe23b-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="fe23b-373">Informazioni sull'aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe23b-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="fe23b-374">Articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="fe23b-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 