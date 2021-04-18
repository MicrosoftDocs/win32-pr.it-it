---
description: L'API dell'agente di Windows Update (WUA) può essere usata da un utente in un computer remoto o da un'applicazione in esecuzione in un computer remoto. Tuttavia, l'utente remoto o l'applicazione deve disporre di privilegi di amministratore.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Uso di WUA da un computer remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305829"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="b67b3-104">Uso di WUA da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="b67b3-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="b67b3-105">L'API dell'agente di Windows Update (WUA) può essere usata da un utente in un computer remoto o da un'applicazione in esecuzione in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b67b3-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="b67b3-106">Tuttavia, l'utente remoto o l'applicazione deve disporre di privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b67b3-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="b67b3-107">L'elenco seguente contiene le interfacce disponibili per gli utenti e le applicazioni remote:</span><span class="sxs-lookup"><span data-stu-id="b67b3-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="b67b3-108">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="b67b3-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="b67b3-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="b67b3-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="b67b3-110">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="b67b3-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="b67b3-111">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="b67b3-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="b67b3-112">**ISearchResult**</span><span class="sxs-lookup"><span data-stu-id="b67b3-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="b67b3-113">**IUpdateCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="b67b3-114">**IUpdate**</span><span class="sxs-lookup"><span data-stu-id="b67b3-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="b67b3-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="b67b3-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="b67b3-116">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="b67b3-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="b67b3-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="b67b3-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="b67b3-118">**IUpdateIdentity**</span><span class="sxs-lookup"><span data-stu-id="b67b3-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="b67b3-119">**IImageInformation**</span><span class="sxs-lookup"><span data-stu-id="b67b3-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="b67b3-120">**IInstallationBehavior**</span><span class="sxs-lookup"><span data-stu-id="b67b3-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="b67b3-121">**Tringcollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="b67b3-122">**IUpdateHistoryEntryCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="b67b3-123">**IUpdateHistoryEntry**</span><span class="sxs-lookup"><span data-stu-id="b67b3-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="b67b3-124">**ICategoryCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="b67b3-125">**ICategory**</span><span class="sxs-lookup"><span data-stu-id="b67b3-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="b67b3-126">**IUpdateExceptionCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="b67b3-127">**IUpdateException**</span><span class="sxs-lookup"><span data-stu-id="b67b3-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="b67b3-128">**IUpdateDownloadContentCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="b67b3-129">**IUpdateDownloadContent**</span><span class="sxs-lookup"><span data-stu-id="b67b3-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="b67b3-130">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="b67b3-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="b67b3-131">**IUpdateServiceCollection**</span><span class="sxs-lookup"><span data-stu-id="b67b3-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="b67b3-132">**IUpdateService**</span><span class="sxs-lookup"><span data-stu-id="b67b3-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="b67b3-133">**IWindowsUpdateAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="b67b3-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="b67b3-134">L'elenco seguente contiene le interfacce e le proprietà che non sono disponibili per gli utenti e le applicazioni remote:</span><span class="sxs-lookup"><span data-stu-id="b67b3-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="b67b3-135">**IUpdateSession::CreateUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="b67b3-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="b67b3-136">**IUpdateSession::CreateUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="b67b3-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="b67b3-137">**Proprietà WebProxy di IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="b67b3-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="b67b3-138">**IUpdateSearcher::BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="b67b3-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="b67b3-139">**IUpdateSearcher::EndSearch**</span><span class="sxs-lookup"><span data-stu-id="b67b3-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="b67b3-140">La [**Proprietà IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) **(nascosto** è di sola lettura quando viene chiamata in modalità remota).</span><span class="sxs-lookup"><span data-stu-id="b67b3-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="b67b3-141">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="b67b3-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="b67b3-142">**IUpdate:: CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="b67b3-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="b67b3-143">**IUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="b67b3-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="b67b3-144">**IWindowsDriverUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="b67b3-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="b67b3-145">**IUpdateServiceManager:: AddService**</span><span class="sxs-lookup"><span data-stu-id="b67b3-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="b67b3-146">**IUpdateServiceManager::RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="b67b3-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="b67b3-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="b67b3-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="b67b3-148">**IAutomaticUpdate::P ause**</span><span class="sxs-lookup"><span data-stu-id="b67b3-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="b67b3-149">**IAutomaticUpdates:: Resume**</span><span class="sxs-lookup"><span data-stu-id="b67b3-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="b67b3-150">**IAutomaticUpdates::ShowSettingsDialog**</span><span class="sxs-lookup"><span data-stu-id="b67b3-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="b67b3-151">**Proprietà Settings di IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="b67b3-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="b67b3-152">**Proprietà ServiceEnabled di IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="b67b3-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="b67b3-153">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="b67b3-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="b67b3-154">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="b67b3-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="b67b3-155">È necessario aggiungere le seguenti porte ed eccezioni alle impostazioni di Windows Firewall per Windows Vista e Windows Server 2008 affinché l'API WUA venga chiamata in remoto.</span><span class="sxs-lookup"><span data-stu-id="b67b3-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="b67b3-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Eccezione 1</span><span class="sxs-lookup"><span data-stu-id="b67b3-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="b67b3-157">Porta locale: 135</span><span class="sxs-lookup"><span data-stu-id="b67b3-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="b67b3-158">Porta remota: tutti</span><span class="sxs-lookup"><span data-stu-id="b67b3-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="b67b3-159">Numero di protocollo: 6</span><span class="sxs-lookup"><span data-stu-id="b67b3-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="b67b3-160">Eseguibile:% windir% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b67b3-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="b67b3-161">Servizio: RPCSS</span><span class="sxs-lookup"><span data-stu-id="b67b3-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="b67b3-162">Privilegio remoto: amministratore</span><span class="sxs-lookup"><span data-stu-id="b67b3-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="b67b3-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Eccezione 2</span><span class="sxs-lookup"><span data-stu-id="b67b3-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="b67b3-164">Porta locale: RPC dinamica</span><span class="sxs-lookup"><span data-stu-id="b67b3-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="b67b3-165">Porta remota: tutti</span><span class="sxs-lookup"><span data-stu-id="b67b3-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="b67b3-166">Numero di protocollo: 6</span><span class="sxs-lookup"><span data-stu-id="b67b3-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="b67b3-167">Eseguibile:% windir% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="b67b3-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="b67b3-168">Privilegio remoto: amministratore</span><span class="sxs-lookup"><span data-stu-id="b67b3-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="b67b3-169">L'elenco seguente contiene gli strumenti che è possibile usare per configurare le impostazioni di Windows Firewall:</span><span class="sxs-lookup"><span data-stu-id="b67b3-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="b67b3-170">Windows Firewall con snap-in Windows Firewall con protezione avanzata</span><span class="sxs-lookup"><span data-stu-id="b67b3-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="b67b3-171">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="b67b3-171">Group Policy</span></span>
-   <span data-ttu-id="b67b3-172">Strumento da riga di comando netsh advfirewall</span><span class="sxs-lookup"><span data-stu-id="b67b3-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="b67b3-173">Per ulteriori informazioni su come utilizzare gli strumenti di per configurare le impostazioni di Windows Firewall, vedere [Introduzione con Windows Firewall con sicurezza avanzata](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b67b3-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
