---
title: Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows
description: Usare questi suggerimenti per risolvere i problemi riscontrati durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto dell'app.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2021
ms.locfileid: "106333997"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="87df0-103">Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows</span><span class="sxs-lookup"><span data-stu-id="87df0-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="87df0-104">Usare questi suggerimenti per la risoluzione dei problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto di app Windows (con estensione msix/appx) come sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="87df0-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="87df0-105">Questo articolo è destinato agli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="87df0-105">This article is intended for developers.</span></span> <span data-ttu-id="87df0-106">Se non si è uno sviluppatore e si sta cercando assistenza per un errore di installazione dell'app Windows, vedere [supporto di Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="87df0-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="87df0-107">Ottenere informazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="87df0-107">Get diagnostic information</span></span>

<span data-ttu-id="87df0-108">Quando un'API ha esito negativo, restituisce un codice di errore che descrive il problema.</span><span class="sxs-lookup"><span data-stu-id="87df0-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="87df0-109">Se il codice di errore non fornisce informazioni sufficienti, si trovano altre informazioni di diagnostica nei registri eventi dettagliati.</span><span class="sxs-lookup"><span data-stu-id="87df0-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="87df0-110">Per accedere ai registri eventi di creazione pacchetti e distribuzione tramite **Visualizzatore eventi**, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="87df0-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="87df0-111">Effettuare uno dei passaggi indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="87df0-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="87df0-112">Fare clic su **Start** nel menu Windows, digitare **Visualizzatore eventi** e **premere invio**.</span><span class="sxs-lookup"><span data-stu-id="87df0-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="87df0-113">Eseguire **eventvwr. msc**.</span><span class="sxs-lookup"><span data-stu-id="87df0-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="87df0-114">Nella pagina a sinistra espandere **Visualizzatore eventi (local)**  >  **registri applicazioni e servizi**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="87df0-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="87df0-115">Verificare la presenza di log disponibili in queste categorie:</span><span class="sxs-lookup"><span data-stu-id="87df0-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="87df0-116">**AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**</span><span class="sxs-lookup"><span data-stu-id="87df0-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="87df0-117">**AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**</span><span class="sxs-lookup"><span data-stu-id="87df0-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="87df0-118">Per iniziare, esaminare i log in **AppXDeployment-Server**.</span><span class="sxs-lookup"><span data-stu-id="87df0-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="87df0-119">Se l'errore è stato causato da **0x80073CF0** o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, i dettagli aggiuntivi possono essere presenti nei log di **AppxpackagingOM** .</span><span class="sxs-lookup"><span data-stu-id="87df0-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="87df0-120">È anche possibile usare il comando [Get-AppxLog](/powershell/module/appx/get-appxlog) in PowerShell per ottenere i primi eventi registrati.</span><span class="sxs-lookup"><span data-stu-id="87df0-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="87df0-121">Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente.</span><span class="sxs-lookup"><span data-stu-id="87df0-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="87df0-122">Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente in una tabella interattiva in una finestra separata.</span><span class="sxs-lookup"><span data-stu-id="87df0-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="87df0-123">Codici di errore comuni</span><span class="sxs-lookup"><span data-stu-id="87df0-123">Common error codes</span></span>

<span data-ttu-id="87df0-124">In questa tabella sono elencati alcuni dei codici di errore più comuni.</span><span class="sxs-lookup"><span data-stu-id="87df0-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="87df0-125">Se è necessaria ulteriore assistenza per uno di questi errori o se si sta riscontrando un codice di errore non presente nell'elenco, vedere [Opzioni della guida aggiuntive](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="87df0-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87df0-126">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="87df0-126">Error code</span></span></th>
<th><span data-ttu-id="87df0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87df0-127">Value</span></span></th>
<th><span data-ttu-id="87df0-128">Descrizione e possibili cause</span><span class="sxs-lookup"><span data-stu-id="87df0-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="87df0-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="87df0-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="87df0-130">0x80070002</span></span></td>
<td><span data-ttu-id="87df0-131">Il file o il percorso non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="87df0-131">File or path is not found.</span></span> <span data-ttu-id="87df0-132">Questo problema può verificarsi durante la convalida di un TypeLib COM richiede che il percorso della directory esista effettivamente all'interno del pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="87df0-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="87df0-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="87df0-134">0x8007000B</span></span></td>
<td><span data-ttu-id="87df0-135">Il pacchetto non è formattato correttamente ed è necessario ricompilarlo o firmarlo nuovamente.</span><span class="sxs-lookup"><span data-stu-id="87df0-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="87df0-136">Questo errore può verificarsi in caso di mancata corrispondenza tra il nome del soggetto del certificato di firma e il nome del server di pubblicazione AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="87df0-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="87df0-137">Vedere <a href="how-to-sign-a-package-using-signtool.md">come firmare un pacchetto dell'app usando SignTool</a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="87df0-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="87df0-139">0x80070057</span></span></td>
<td><span data-ttu-id="87df0-140">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="87df0-140">One or more arguments are not valid.</span></span> <span data-ttu-id="87df0-141">Se si seleziona il registro eventi AppXDeployment-Server e viene visualizzato l'evento seguente: "durante l'installazione del pacchetto, il sistema non è riuscito a registrare l'estensione Windows. repositoryExtension a causa dell'errore seguente: il parametro non è corretto".</span><span class="sxs-lookup"><span data-stu-id="87df0-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="87df0-142">Questo errore può verificarsi se gli elementi del manifesto DisplayName o Description contengono caratteri non consentiti da Windows Firewall. nome |  e tutti, a causa del quale Windows non è in grado di creare il profilo AppContainer per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="87df0-143">Rimuovere questi caratteri dal manifesto e provare a installare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="87df0-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="87df0-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="87df0-147">Non è stato possibile aprire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="87df0-148">Cause possibili:</span><span class="sxs-lookup"><span data-stu-id="87df0-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="87df0-149">Il pacchetto non è firmato.</span><span class="sxs-lookup"><span data-stu-id="87df0-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="87df0-150">Il nome dell'autore non corrisponde al soggetto del certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="87df0-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="87df0-151">Il prefisso file://è mancante oppure il pacchetto non è stato trovato nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="87df0-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="87df0-152">Per ulteriori informazioni, controllare il registro eventi di <strong>AppxPackagingOM</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="87df0-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="87df0-156">Impossibile trovare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="87df0-157">Questo errore può verificarsi durante la rimozione di un pacchetto non installato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="87df0-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-159"><strong>PACCHETTO</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="87df0-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="87df0-161">I dati del pacchetto non sono validi.</span><span class="sxs-lookup"><span data-stu-id="87df0-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="87df0-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="87df0-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="87df0-165">Non è stato possibile completare la convalida dell'aggiornamento, delle dipendenze o dei conflitti per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="87df0-166">Cause possibili:</span><span class="sxs-lookup"><span data-stu-id="87df0-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="87df0-167">Il pacchetto in arrivo è in conflitto con un pacchetto installato.</span><span class="sxs-lookup"><span data-stu-id="87df0-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="87df0-168">Impossibile trovare una dipendenza del pacchetto specificata.</span><span class="sxs-lookup"><span data-stu-id="87df0-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="87df0-169">Il pacchetto non supporta l'architettura del processore corretta.</span><span class="sxs-lookup"><span data-stu-id="87df0-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="87df0-170">Per altre informazioni, vedere il registro eventi di <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="87df0-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="87df0-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="87df0-174">Spazio su disco insufficiente nel computer.</span><span class="sxs-lookup"><span data-stu-id="87df0-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="87df0-175">Liberare spazio e riprovare.</span><span class="sxs-lookup"><span data-stu-id="87df0-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="87df0-177"><strong>ERRORE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="87df0-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="87df0-179">Non è possibile scaricare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="87df0-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="87df0-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="87df0-183">Il pacchetto non può essere registrato.</span><span class="sxs-lookup"><span data-stu-id="87df0-183">The package can't be registered.</span></span><br/> <span data-ttu-id="87df0-184">Per ulteriori informazioni, controllare il registro eventi di <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="87df0-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="87df0-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="87df0-188">Non è possibile annullare la registrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="87df0-189">Questo errore può verificarsi durante la rimozione di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="87df0-190">Per ulteriori informazioni, controllare il registro eventi di <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="87df0-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="87df0-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="87df0-193">L'utente ha annullato la richiesta di installazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="87df0-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="87df0-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="87df0-196">Installazione pacchetto non riuscita.</span><span class="sxs-lookup"><span data-stu-id="87df0-196">Package install failed.</span></span> <span data-ttu-id="87df0-197">Contattare il fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="87df0-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="87df0-198">Per ulteriori informazioni, controllare il registro eventi di <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="87df0-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="87df0-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="87df0-201">Rimozione pacchetto non riuscita.</span><span class="sxs-lookup"><span data-stu-id="87df0-201">Package removal failed.</span></span><br/> <span data-ttu-id="87df0-202">Questo errore può verificarsi se si verificano errori durante la disinstallazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="87df0-203">Per ulteriori informazioni, vedere <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="87df0-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="87df0-207">Il pacchetto fornito è già installato, pertanto la reinstallazione del pacchetto è stata bloccata.</span><span class="sxs-lookup"><span data-stu-id="87df0-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="87df0-208">Questo errore può verificarsi se si installa un pacchetto che non è un bit per bit identico al pacchetto già installato.</span><span class="sxs-lookup"><span data-stu-id="87df0-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="87df0-209">Si noti che anche la firma digitale fa parte del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="87df0-210">Di conseguenza, se un pacchetto viene ricompilato o firmato, non è più bit per bit del pacchetto installato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="87df0-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="87df0-211">Due opzioni possibili per correggere l'errore sono: (1) incrementare il numero di versione dell'app, quindi ricompilare e firmare nuovamente il pacchetto (2) rimuovere il pacchetto precedente per ogni utente del sistema prima di installare il nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="87df0-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="87df0-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="87df0-214">Non è possibile avviare l'app.</span><span class="sxs-lookup"><span data-stu-id="87df0-214">The app can't be started.</span></span> <span data-ttu-id="87df0-215">Provare a reinstallare l'app.</span><span class="sxs-lookup"><span data-stu-id="87df0-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="87df0-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="87df0-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="87df0-219">Non è stato possibile soddisfare un prerequisito di installazione specificato.</span><span class="sxs-lookup"><span data-stu-id="87df0-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="87df0-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="87df0-223">Il repository del pacchetto è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="87df0-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="87df0-224">Questo errore può verificarsi se la cartella a cui fa riferimento la chiave del registro di sistema non esiste o è danneggiata:</span><span class="sxs-lookup"><span data-stu-id="87df0-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="87df0-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="87df0-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="87df0-227">Per eseguire il ripristino da questo stato, aggiornare il PC.</span><span class="sxs-lookup"><span data-stu-id="87df0-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="87df0-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="87df0-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="87df0-231">Per installare questa app, è necessaria una licenza per sviluppatori o un sistema abilitato per sideload.</span><span class="sxs-lookup"><span data-stu-id="87df0-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="87df0-232">Questo errore può verificarsi se il pacchetto non soddisfa uno dei requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="87df0-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="87df0-233">L'app viene distribuita con F5 in Visual Studio in un computer con una licenza per sviluppatori Windows.</span><span class="sxs-lookup"><span data-stu-id="87df0-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="87df0-234">Il pacchetto è firmato con una firma Microsoft e distribuito come parte di Windows o dal Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="87df0-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="87df0-235">Il pacchetto è firmato con una firma attendibile e installato in un computer con una licenza per sviluppatori, un computer aggiunto a un dominio con il criterio AllowAllTrustedApps abilitato oppure un computer con una licenza Windows sideload con il criterio AllowAllTrustedApps abilitato.</span><span class="sxs-lookup"><span data-stu-id="87df0-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="87df0-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="87df0-237">0x80073D00</span></span></td>
<td><span data-ttu-id="87df0-238">Non è possibile avviare l'app perché è attualmente in fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="87df0-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="87df0-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="87df0-241">0x80073D01</span></span></td>
<td><span data-ttu-id="87df0-242">L'operazione di distribuzione del pacchetto è bloccata dai criteri.</span><span class="sxs-lookup"><span data-stu-id="87df0-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="87df0-243">Contattare l'amministratore del sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="87df0-244">Cause possibili:</span><span class="sxs-lookup"><span data-stu-id="87df0-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="87df0-245">La distribuzione del pacchetto è bloccata dai criteri di controllo delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="87df0-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="87df0-246">La distribuzione del pacchetto è bloccata dal &quot; criterio Consenti operazioni di distribuzione in profili speciali &quot; .</span><span class="sxs-lookup"><span data-stu-id="87df0-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="87df0-247">Una delle possibili cause è la necessità di un profilo mobile.</span><span class="sxs-lookup"><span data-stu-id="87df0-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="87df0-248">Per informazioni sulla configurazione dei profili utente mobili sugli account utente, vedere <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">deploy Mobile User Profiles</a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="87df0-249">Se nel sistema non sono configurati criteri e questo errore viene comunque visualizzato, probabilmente si è connessi con un profilo temporaneo.</span><span class="sxs-lookup"><span data-stu-id="87df0-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="87df0-250">Disconnettersi e accedere di nuovo, quindi ripetere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="87df0-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="87df0-252">0x80073D02</span></span></td>
<td><span data-ttu-id="87df0-253">Non è stato possibile installare il pacchetto perché le risorse modificate sono attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="87df0-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="87df0-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="87df0-256">0x80073D03</span></span></td>
<td><span data-ttu-id="87df0-257">Non è stato possibile recuperare il pacchetto perché i dati necessari per il ripristino sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="87df0-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="87df0-260">0x80073D04</span></span></td>
<td><span data-ttu-id="87df0-261">La firma non è valida.</span><span class="sxs-lookup"><span data-stu-id="87df0-261">The signature isn't valid.</span></span> <span data-ttu-id="87df0-262">Per eseguire la registrazione in modalità sviluppatore, AppxSignature. p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="87df0-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="87df0-263">Per gli sviluppatori che usano F5 con Visual Studio, assicurarsi che la directory del progetto compilata non contenga i file della firma o del blocco della mappa da versioni precedenti del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="87df0-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="87df0-266">0x80073D05</span></span></td>
<td><span data-ttu-id="87df0-267">Si è verificato un errore durante l'eliminazione dei dati dell'applicazione precedentemente esistenti del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="87df0-268">È possibile ottenere questo errore se il <a href="/previous-versions/hh441475(v=vs.110)">simulatore</a> è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87df0-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="87df0-269">Chiudere il simulatore.</span><span class="sxs-lookup"><span data-stu-id="87df0-269">Close the simulator.</span></span> <span data-ttu-id="87df0-270">Questo errore può essere visualizzato anche se sono presenti file aperti nei dati dell'app, ad esempio se si dispone di un file di log aperto in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="87df0-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="87df0-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="87df0-273">0x80073D06</span></span></td>
<td><span data-ttu-id="87df0-274">Non è stato possibile installare il pacchetto perché è già installata una versione più recente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="87df0-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="87df0-277">0x80073D07</span></span></td>
<td><span data-ttu-id="87df0-278">È stato rilevato un errore in un file binario di sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-278">An error in a system binary was detected.</span></span> <span data-ttu-id="87df0-279">Per risolvere il problema, provare ad aggiornare il PC.</span><span class="sxs-lookup"><span data-stu-id="87df0-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="87df0-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="87df0-282">0x80073D08</span></span></td>
<td><span data-ttu-id="87df0-283">Un file binario non Windows danneggiato è stato rilevato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="87df0-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="87df0-286">0x80073D09</span></span></td>
<td><span data-ttu-id="87df0-287">Non è stato possibile riprendere l'operazione perché i dati necessari per il ripristino sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="87df0-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="87df0-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="87df0-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="87df0-291">Non è stato possibile installare il pacchetto perché il servizio Windows Firewall non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87df0-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="87df0-292">Abilitare il servizio Windows Firewall e riprovare.</span><span class="sxs-lookup"><span data-stu-id="87df0-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="87df0-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="87df0-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="87df0-295">Operazione di spostamento del pacchetto non riuscita.</span><span class="sxs-lookup"><span data-stu-id="87df0-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="87df0-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="87df0-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="87df0-299">L'operazione di distribuzione non è riuscita perché il volume non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="87df0-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="87df0-301"><strong>OFFLINE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="87df0-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="87df0-303">L'operazione di distribuzione non è riuscita perché il volume è offline.</span><span class="sxs-lookup"><span data-stu-id="87df0-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="87df0-304">Per un aggiornamento del pacchetto, il volume fa riferimento al volume installato di tutte le versioni dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="87df0-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="87df0-306"><strong>DANNEGGIATO</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="87df0-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="87df0-308">L'operazione di distribuzione non è riuscita perché il volume specificato è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="87df0-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="87df0-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="87df0-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="87df0-311">L'operazione di distribuzione non è riuscita perché è necessario registrare prima l'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="87df0-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="87df0-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="87df0-314">0x80073D10</span></span></td>
<td><span data-ttu-id="87df0-315">L'operazione di distribuzione non è riuscita perché il pacchetto è destinato all'architettura del processore non corretta.</span><span class="sxs-lookup"><span data-stu-id="87df0-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="87df0-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="87df0-318">0x80073D11</span></span></td>
<td><span data-ttu-id="87df0-319">È stato raggiunto il numero massimo di pacchetti sideload per sviluppatori consentiti in questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87df0-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="87df0-320">Disinstallare un pacchetto sideload e riprovare.</span><span class="sxs-lookup"><span data-stu-id="87df0-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="87df0-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="87df0-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="87df0-324">0x80073D12</span></span></td>
<td><span data-ttu-id="87df0-325">Per installare questo pacchetto facoltativo, è necessario un pacchetto dell'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="87df0-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="87df0-326">Installare prima il pacchetto principale e riprovare.</span><span class="sxs-lookup"><span data-stu-id="87df0-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="87df0-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="87df0-329">0x80073D13</span></span></td>
<td><span data-ttu-id="87df0-330">Questo tipo di pacchetto dell'app non è supportato in questo file System.</span><span class="sxs-lookup"><span data-stu-id="87df0-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="87df0-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="87df0-333">0x80073D14</span></span></td>
<td><span data-ttu-id="87df0-334">L'operazione di spostamento del pacchetto è bloccata fino al termine dello streaming dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="87df0-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="87df0-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="87df0-338">0x80073D15</span></span></td>
<td><span data-ttu-id="87df0-339">Un pacchetto dell'applicazione principale o un altro pacchetto facoltativo ha lo stesso ID applicazione di questo pacchetto facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87df0-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="87df0-340">Modificare l'ID applicazione per il pacchetto facoltativo per evitare conflitti.</span><span class="sxs-lookup"><span data-stu-id="87df0-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="87df0-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="87df0-343">0x80073D16</span></span></td>
<td><span data-ttu-id="87df0-344">Questa sessione di staging è stata mantenuta per consentire l'assegnazione delle priorità a un'altra operazione di gestione temporanea.</span><span class="sxs-lookup"><span data-stu-id="87df0-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="87df0-347">0x80073D17</span></span></td>
<td><span data-ttu-id="87df0-348">Non è possibile aggiornare un set correlato perché il set aggiornato non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="87df0-349">Tutti i pacchetti nel set correlato devono essere aggiornati nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="87df0-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="87df0-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="87df0-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="87df0-353">0x80073D18</span></span></td>
<td><span data-ttu-id="87df0-354">Per un pacchetto facoltativo con un punto di ingresso FullTrust è necessario che il pacchetto principale disponga della funzionalità <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="87df0-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="87df0-357">0x80073D19</span></span></td>
<td><span data-ttu-id="87df0-358">Si è verificato un errore perché un utente è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="87df0-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="87df0-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="87df0-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="87df0-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="87df0-363">Per un provisioning di pacchetti facoltativo è necessario eseguire il provisioning anche del pacchetto principale di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="87df0-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="87df0-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="87df0-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="87df0-367">I pacchetti non hanno superato il <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">controllo della reputazione SmartScreen</a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="87df0-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="87df0-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="87df0-371">Timeout dell'operazione di <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">controllo della reputazione SmartScreen</a> .</span><span class="sxs-lookup"><span data-stu-id="87df0-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="87df0-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="87df0-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="87df0-375">L'opzione di distribuzione corrente non è supportata.</span><span class="sxs-lookup"><span data-stu-id="87df0-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="87df0-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="87df0-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="87df0-379">L'attivazione è bloccata a causa delle impostazioni di aggiornamento. AppInstaller per questa app.</span><span class="sxs-lookup"><span data-stu-id="87df0-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="87df0-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="87df0-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="87df0-383">Le unità remote non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="87df0-383">Remote drives are not supported.</span></span> <span data-ttu-id="87df0-384">Usare <strong> \\ server\share.</strong> per registrare un pacchetto remoto.</span><span class="sxs-lookup"><span data-stu-id="87df0-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="87df0-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="87df0-387">0x80073D20</span></span></td>
<td><span data-ttu-id="87df0-388">Non è stato possibile elaborare e scrivere i dati del pacchetto scaricato su disco.</span><span class="sxs-lookup"><span data-stu-id="87df0-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="87df0-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="87df0-391">0x80073D21</span></span></td>
<td><span data-ttu-id="87df0-392">L'operazione di distribuzione è stata bloccata a causa di un criterio della famiglia per pacchetto che limita le distribuzioni in un volume non di sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="87df0-393">Per criterio, l'app deve essere installata nell'unità di sistema, ma non è impostata come predefinita.</span><span class="sxs-lookup"><span data-stu-id="87df0-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="87df0-394">In impostazioni di archiviazione fare in modo che il sistema Guidi il percorso predefinito per salvare nuovo contenuto, quindi ripetere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="87df0-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="87df0-397">0x80073D22</span></span></td>
<td><span data-ttu-id="87df0-398">L'operazione di distribuzione è stata bloccata a causa di criteri a livello di computer che limitano le distribuzioni in un volume non di sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="87df0-399">Per criterio, l'app deve essere installata nell'unità di sistema, ma non è impostata come predefinita.</span><span class="sxs-lookup"><span data-stu-id="87df0-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="87df0-400">In impostazioni di archiviazione fare in modo che il sistema Guidi il percorso predefinito per salvare nuovo contenuto, quindi ripetere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="87df0-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="87df0-403">0x80073D23</span></span></td>
<td><span data-ttu-id="87df0-404">L'operazione di distribuzione è stata bloccata perché la distribuzione del profilo speciale non è consentita (i profili speciali sono profili utente in cui le modifiche vengono scartate dopo la disinstallazione dell'utente).</span><span class="sxs-lookup"><span data-stu-id="87df0-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="87df0-405">Provare ad accedere a un account che non è un profilo speciale.</span><span class="sxs-lookup"><span data-stu-id="87df0-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="87df0-406">È possibile provare a disconnettersi e accedere di nuovo all'account corrente oppure provare ad accedere a un account diverso.</span><span class="sxs-lookup"><span data-stu-id="87df0-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="87df0-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-409"><strong>DIRECTORY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="87df0-410">0x80073D24</span></span></td>
<td><span data-ttu-id="87df0-411">Operazione di distribuzione non riuscita a causa di una directory del <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">pacchetto mutevole</a>del pacchetto in conflitto.</span><span class="sxs-lookup"><span data-stu-id="87df0-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="87df0-412">Per installare questo pacchetto, rimuovere il pacchetto esistente con la directory del pacchetto modificabile in conflitto.</span><span class="sxs-lookup"><span data-stu-id="87df0-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="87df0-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="87df0-415">0x80073D25</span></span></td>
<td><span data-ttu-id="87df0-416">L'installazione del pacchetto non è riuscita perché è stata specificata una risorsa singleton e è stato eseguito l'accesso a un altro utente con il pacchetto installato.</span><span class="sxs-lookup"><span data-stu-id="87df0-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="87df0-417">Verificare che tutti gli utenti attivi con il pacchetto installato siano disconnessi e riprovare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="87df0-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="87df0-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="87df0-420">0x80073D26</span></span></td>
<td><span data-ttu-id="87df0-421">L'installazione del pacchetto non è riuscita perché è installata una versione diversa del servizio.</span><span class="sxs-lookup"><span data-stu-id="87df0-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="87df0-422">Provare a installare una versione più recente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="87df0-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="87df0-425">0x80073D27</span></span></td>
<td><span data-ttu-id="87df0-426">L'installazione del pacchetto non è riuscita perché esiste una versione del servizio all'esterno di un pacchetto con estensione msix/appx.</span><span class="sxs-lookup"><span data-stu-id="87df0-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="87df0-427">Contattare il fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="87df0-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="87df0-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="87df0-430">0x80073D28</span></span></td>
<td><span data-ttu-id="87df0-431">L'installazione del pacchetto non è riuscita perché sono necessari i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="87df0-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="87df0-432">Contattare un amministratore per installare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="87df0-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="87df0-435">0x80073D29</span></span></td>
<td><span data-ttu-id="87df0-436">La distribuzione del pacchetto non è riuscita perché l'operazione è stata reindirizzata all'account predefinito, quando il chiamante non lo ha fatto.</span><span class="sxs-lookup"><span data-stu-id="87df0-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="87df0-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="87df0-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="87df0-440">La distribuzione del pacchetto non è riuscita perché il pacchetto richiede una funzionalità per la destinazione nativa di questo host.</span><span class="sxs-lookup"><span data-stu-id="87df0-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="87df0-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="87df0-444">La distribuzione del pacchetto non è riuscita perché il relativo contenuto non è valido per un pacchetto non firmato.</span><span class="sxs-lookup"><span data-stu-id="87df0-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="87df0-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="87df0-448">La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non è nello spazio dei nomi senza segno.</span><span class="sxs-lookup"><span data-stu-id="87df0-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="87df0-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="87df0-452">La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non è nello spazio dei nomi firmato.</span><span class="sxs-lookup"><span data-stu-id="87df0-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="87df0-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="87df0-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="87df0-456">La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non è nello spazio dei nomi firmato.</span><span class="sxs-lookup"><span data-stu-id="87df0-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="87df0-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="87df0-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="87df0-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="87df0-461">Una dipendenza di runtime host che si risolve in un pacchetto con contenuto completamente attendibile richiede che il pacchetto principale disponga della funzionalità <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="87df0-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="87df0-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="87df0-463">0x80080200</span></span></td>
<td><span data-ttu-id="87df0-464">Si è verificato un errore interno nell'API per la creazione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="87df0-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="87df0-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="87df0-467">0x80080201</span></span></td>
<td><span data-ttu-id="87df0-468">Il pacchetto non è valido perché il relativo contenuto è con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="87df0-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="87df0-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="87df0-471">0x80080202</span></span></td>
<td><span data-ttu-id="87df0-472">Il pacchetto non è valido perché contiene relazioni OPC.</span><span class="sxs-lookup"><span data-stu-id="87df0-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="87df0-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="87df0-475">0x80080203</span></span></td>
<td><span data-ttu-id="87df0-476">Il pacchetto non è valido perché manca un manifesto o una mappa dei blocchi oppure un file di integrità del codice è presente ma manca un file di firma.</span><span class="sxs-lookup"><span data-stu-id="87df0-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="87df0-477">Verificare che nel pacchetto non mancano uno o più file necessari:</span><span class="sxs-lookup"><span data-stu-id="87df0-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="87df0-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="87df0-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="87df0-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="87df0-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="87df0-480">Se il pacchetto contiene \AppxMetadata\CodeIntegrity.cat, deve anche contenere \AppxSignature.p7x.</span><span class="sxs-lookup"><span data-stu-id="87df0-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="87df0-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="87df0-482">0x80080204</span></span></td>
<td><span data-ttu-id="87df0-483">Il file di AppxManifest.xml del pacchetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="87df0-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="87df0-485">0x80080205</span></span></td>
<td><span data-ttu-id="87df0-486">Il file di AppxBlockMap.xml del pacchetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="87df0-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="87df0-488">0x80080206</span></span></td>
<td><span data-ttu-id="87df0-489">Non è possibile leggere il contenuto del pacchetto perché è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="87df0-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="87df0-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="87df0-492">0x80080207</span></span></td>
<td><span data-ttu-id="87df0-493">Il valore hash calcolato del blocco non corrisponde al valore dell'oggetto archiviato nella mappa dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="87df0-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="87df0-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="87df0-496">0x80080208</span></span></td>
<td><span data-ttu-id="87df0-497">L'intervallo di byte richiesto è superiore a 4 GB se convertito in un intervallo di byte di blocchi.</span><span class="sxs-lookup"><span data-stu-id="87df0-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="87df0-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="87df0-499">0x800B0100</span></span></td>
<td><span data-ttu-id="87df0-500">Nessuna firma presente nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="87df0-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="87df0-501">Questo errore può verificarsi se il pacchetto non è firmato o se la firma non è valida.</span><span class="sxs-lookup"><span data-stu-id="87df0-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="87df0-502">Il pacchetto deve essere firmato per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="87df0-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="87df0-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="87df0-504">0x800B0109</span></span></td>
<td><span data-ttu-id="87df0-505">Una catena di certificati elaborata, ma terminata in un certificato radice non attendibile dal provider di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="87df0-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="87df0-506">Vedere <a href="/previous-versions/br230260(v=vs.110)">firma di un pacchetto</a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="87df0-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="87df0-508">0x800B010A</span></span></td>
<td><span data-ttu-id="87df0-509">Non è stato possibile compilare una catena di certificati per un'autorità di certificazione radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="87df0-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="87df0-510">Vedere <a href="/previous-versions/br230260(v=vs.110)">firma di un pacchetto</a>.</span><span class="sxs-lookup"><span data-stu-id="87df0-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="87df0-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="87df0-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="87df0-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="87df0-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="87df0-513">0x80080209</span></span></td>
<td><span data-ttu-id="87df0-514">La struttura di <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilizzata per firmare il pacchetto non contiene i dati necessari</span><span class="sxs-lookup"><span data-stu-id="87df0-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="87df0-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="87df0-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="87df0-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="87df0-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="87df0-517">0x8008020A</span></span></td>
<td><span data-ttu-id="87df0-518">La struttura <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilizzata per crittografare o decrittografare il pacchetto contiene dati non validi.</span><span class="sxs-lookup"><span data-stu-id="87df0-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-520"><strong>CONTENTGROUPMAP</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="87df0-521">0x8008020B</span></span></td>
<td><span data-ttu-id="87df0-522">La mappa del gruppo di contenuti del pacchetto. msix/. appx non è valida.</span><span class="sxs-lookup"><span data-stu-id="87df0-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="87df0-525">0x8008020C</span></span></td>
<td><span data-ttu-id="87df0-526">Il <a href="/windows/msix/app-installer/app-installer-root">file con estensione AppInstaller</a> per il pacchetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="87df0-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="87df0-529">0x8008020D</span></span></td>
<td><span data-ttu-id="87df0-530">La versione del pacchetto di base nel pacchetto Delta non corrisponde a quella del pacchetto di base da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="87df0-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="87df0-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="87df0-533">0x8008020E</span></span></td>
<td><span data-ttu-id="87df0-534">Nel pacchetto Delta manca un file dal pacchetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="87df0-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="87df0-537">0x8008020F</span></span></td>
<td><span data-ttu-id="87df0-538">Il pacchetto Delta non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="87df0-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="87df0-541">0x80080210</span></span></td>
<td><span data-ttu-id="87df0-542">Il pacchetto Delta aggiunto non è consentito per l'operazione corrente.</span><span class="sxs-lookup"><span data-stu-id="87df0-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="87df0-545">0x80080211</span></span></td>
<td><span data-ttu-id="87df0-546">Il file di layout del pacchetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-548"><strong>PACKAGESIGNCONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="87df0-549">0x80080212</span></span></td>
<td><span data-ttu-id="87df0-550">Il file packageSignConfig non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="87df0-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="87df0-553">0x80080213</span></span></td>
<td><span data-ttu-id="87df0-554">Il file resources. pri non è consentito quando nel manifesto del pacchetto non sono presenti elementi di risorsa.</span><span class="sxs-lookup"><span data-stu-id="87df0-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="87df0-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="87df0-557">0x80080214</span></span></td>
<td><span data-ttu-id="87df0-558">Lo stato di compressione del file nella linea di base e il pacchetto aggiornato non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="87df0-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87df0-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="87df0-561">0x80080215</span></span></td>
<td><span data-ttu-id="87df0-562">Non sono consentite estensioni appx per i pacchetti di payload destinati a piattaforme precedenti.</span><span class="sxs-lookup"><span data-stu-id="87df0-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87df0-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="87df0-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="87df0-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="87df0-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="87df0-565">0x80080216</span></span></td>
<td><span data-ttu-id="87df0-566">Il file encryptionExclusionFileList non è valido.</span><span class="sxs-lookup"><span data-stu-id="87df0-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="87df0-567">Le applicazioni non vengono avviate e i nomi sono visualizzati in grigio</span><span class="sxs-lookup"><span data-stu-id="87df0-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="87df0-568">In un computer basato su Windows 10 non è possibile avviare alcune applicazioni e i nomi delle applicazioni vengono visualizzati in grigio.</span><span class="sxs-lookup"><span data-stu-id="87df0-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Alcuni nomi di applicazione vengono visualizzati in grigio nel menu Start](./images/app-names-dimmed.png)

<span data-ttu-id="87df0-570">Quando si tenta di aprire un'applicazione selezionando il nome visualizzato in grigio, è possibile che venga visualizzato uno dei messaggi di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="87df0-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="87df0-571">Si è verificato un problema con \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="87df0-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="87df0-572">Contattare l'amministratore di sistema per informazioni su come ripristinarlo o reinstallarlo</span><span class="sxs-lookup"><span data-stu-id="87df0-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="87df0-573">Errore: non è possibile aprire l'app</span><span class="sxs-lookup"><span data-stu-id="87df0-573">Error: This app can't open</span></span>

<span data-ttu-id="87df0-574">Inoltre, le voci di evento seguenti vengono registrate nel registro "Microsoft-Windows-TWinUI/Operational" in **Applications e Services\Microsoft\Windows\Apps**:</span><span class="sxs-lookup"><span data-stu-id="87df0-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="87df0-575">Nome registro: Microsoft-Windows-TWinUI/Operational</span><span class="sxs-lookup"><span data-stu-id="87df0-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="87df0-576">Origine: Microsoft-Windows-Immersiv-Shell</span><span class="sxs-lookup"><span data-stu-id="87df0-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="87df0-577">Data: <*Data*></span><span class="sxs-lookup"><span data-stu-id="87df0-577">Date: <*date*></span></span>  
> <span data-ttu-id="87df0-578">ID evento: 5960</span><span class="sxs-lookup"><span data-stu-id="87df0-578">Event ID: 5960</span></span>  
> <span data-ttu-id="87df0-579">Categoria attività: (5960)</span><span class="sxs-lookup"><span data-stu-id="87df0-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="87df0-580">Level: Error</span><span class="sxs-lookup"><span data-stu-id="87df0-580">Level: Error</span></span>  
> <span data-ttu-id="87df0-581">Parole chiave:</span><span class="sxs-lookup"><span data-stu-id="87df0-581">Keywords:</span></span>  
> <span data-ttu-id="87df0-582">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87df0-582">Description:</span></span>  
> <span data-ttu-id="87df0-583">Attivazione dell'app Microsoft.BingNews_8wekyb3d8bbwe. AppexNews per Windows.</span><span class="sxs-lookup"><span data-stu-id="87df0-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="87df0-584">Il contratto di avvio è stato bloccato con errore 0x80073CFC perché il relativo pacchetto si trova in stato: modificato.</span><span class="sxs-lookup"><span data-stu-id="87df0-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="87df0-585">Causa</span><span class="sxs-lookup"><span data-stu-id="87df0-585">Cause</span></span>

<span data-ttu-id="87df0-586">Questo problema si verifica perché la voce del registro di sistema per il valore di stato del pacchetto corrispondente dell'applicazione è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="87df0-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="87df0-587">Soluzione</span><span class="sxs-lookup"><span data-stu-id="87df0-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="87df0-588">Se si modifica il registro di sistema in modo non corretto utilizzando l'Editor del Registro di sistema o un altro metodo, si possono causare gravi problemi.</span><span class="sxs-lookup"><span data-stu-id="87df0-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="87df0-589">che per essere risolti potrebbero richiedere la reinstallazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87df0-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="87df0-590">Microsoft non garantisce la possibilità di risolvere questi problemi.</span><span class="sxs-lookup"><span data-stu-id="87df0-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="87df0-591">La modifica del Registro di sistema è a rischio e pericolo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="87df0-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="87df0-592">Per risolvere il problema:</span><span class="sxs-lookup"><span data-stu-id="87df0-592">To fix this issue:</span></span>

1. <span data-ttu-id="87df0-593">Avviare l'editor del registro di sistema e individuare la sottochiave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .</span><span class="sxs-lookup"><span data-stu-id="87df0-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="87df0-594">Per eseguire il backup dei dati della sottochiave, fare clic con il pulsante destro del mouse su **pacchetti**, scegliere **Esporta**, quindi salvare i dati come file del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="87df0-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="87df0-595">Per ognuna delle applicazioni elencate nelle voci di log dell'ID evento 5960, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="87df0-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="87df0-596">Individuare la voce **PackageStatus** .</span><span class="sxs-lookup"><span data-stu-id="87df0-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="87df0-597">Impostare il valore di **PackageStatus** su zero (**0**).</span><span class="sxs-lookup"><span data-stu-id="87df0-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="87df0-598">Se non sono presenti voci per l'applicazione in **Package**, il problema ha un'altra causa.</span><span class="sxs-lookup"><span data-stu-id="87df0-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="87df0-599">Nel caso dell'evento di esempio in questo articolo, la sottochiave completa è **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="87df0-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="87df0-600">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="87df0-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="87df0-601">Ottenere altre informazioni</span><span class="sxs-lookup"><span data-stu-id="87df0-601">Get additional help</span></span>

<span data-ttu-id="87df0-602">Per ulteriori informazioni sulla risoluzione di un problema riscontrato durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto di app Windows (con estensione msix/appx) come sviluppatore, fare riferimento a queste risorse aggiuntive per il supporto tecnico per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="87df0-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="87df0-603">[Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) offre risposte rilevanti e tempestive ai problemi tecnici di una community di esperti e tecnici Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87df0-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="87df0-604">Per assistenza della community con domande sullo sviluppo, sono disponibili i [Forum](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)e [StackOverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="87df0-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="87df0-605">Il sito del [supporto tecnico per sviluppatori di Windows](https://developer.microsoft.com/windows/support) illustra altre opzioni di supporto.</span><span class="sxs-lookup"><span data-stu-id="87df0-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87df0-606">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87df0-606">Related topics</span></span>

- [<span data-ttu-id="87df0-607">Come firmare un pacchetto di app con SignTool</span><span class="sxs-lookup"><span data-stu-id="87df0-607">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
- [<span data-ttu-id="87df0-608">Come risolvere gli errori di firma del pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="87df0-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
