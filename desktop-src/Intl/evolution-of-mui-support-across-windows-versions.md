---
description: Evoluzione del supporto MUI nelle versioni di Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evoluzione del supporto MUI nelle versioni di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313835"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="6f742-103">Evoluzione del supporto MUI nelle versioni di Windows</span><span class="sxs-lookup"><span data-stu-id="6f742-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="6f742-104">Prima di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f742-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="6f742-105">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="6f742-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="6f742-106">Sistema operativo indipendente dalla lingua/MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="6f742-107">Gli scenari di distribuzione sono completamente basati su MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="6f742-108">Distribuzione con immagine singola</span><span class="sxs-lookup"><span data-stu-id="6f742-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="6f742-109">Modello di manutenzione migliorato</span><span class="sxs-lookup"><span data-stu-id="6f742-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="6f742-110">Infrastruttura MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="6f742-111">Gestione della lingua</span><span class="sxs-lookup"><span data-stu-id="6f742-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="6f742-112">Gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6f742-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="6f742-113">Prima di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f742-113">Before Windows Vista</span></span>

<span data-ttu-id="6f742-114">Prima della versione di Windows Vista, Windows veniva fornito con immagini in linguaggio singolo, il che significava che ogni versione localizzata di Windows conteneva una sola lingua per la relativa interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6f742-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="6f742-115">MUI era un componente aggiuntivo della versione in lingua inglese del sistema operativo e i pacchetti dell'interfaccia utente multilingue potevano essere aggiunti solo a determinate versioni in lingua inglese di Windows.</span><span class="sxs-lookup"><span data-stu-id="6f742-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="6f742-116">Quando è installato nella versione inglese di Windows, MUI ha consentito la modifica della lingua dell'interfaccia utente del sistema operativo in base alle preferenze dei singoli utenti a una delle lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="6f742-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="6f742-117">Il modello di MUI Pack non ha esposto il supporto MUI per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6f742-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="6f742-118">Sebbene gli sviluppatori potessero creare applicazioni multilingue, avrebbero dovuto creare i propri meccanismi a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="6f742-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="6f742-119">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="6f742-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="6f742-120">Con Windows Vista, Microsoft ha realizzato un investimento significativo in MUI.</span><span class="sxs-lookup"><span data-stu-id="6f742-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="6f742-121">Windows Vista è stato creato in base a una piattaforma MUI.</span><span class="sxs-lookup"><span data-stu-id="6f742-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="6f742-122">Sebbene questo rappresenti un importante progresso nella strategia di localizzazione di Windows, poiché si tratta di una chiave fondamentale per Microsoft per fornire Windows in più lingue, è prima di tutto un ottimo progresso per utenti e clienti di Windows.</span><span class="sxs-lookup"><span data-stu-id="6f742-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="6f742-123">Sistema operativo indipendente dalla lingua/MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="6f742-124">La maggior parte dei file binari di Windows Vista sono conformi a MUI e i relativi dati localizzabili vengono archiviati separatamente dal codice.</span><span class="sxs-lookup"><span data-stu-id="6f742-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="6f742-125">Questo offre flessibilità, in quanto è possibile aggiungere dati di lingua diversi in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="6f742-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="6f742-126">Gli scenari di distribuzione sono completamente basati su MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="6f742-127">La progettazione per la creazione di pacchetti e l'installazione di Windows Vista è basata su MUI e tutti i dati localizzabili sono inclusi in pacchetti specifici della lingua e ogni Language Pack può essere distribuito in scenari diversi.</span><span class="sxs-lookup"><span data-stu-id="6f742-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="6f742-128">Ad esempio, anche se i DVD finali di Windows Vista contengono versioni in linguaggio singolo, gli utenti dell'edizione Ultimate possono scaricare Language Pack MUI aggiuntivi e possono cambiare lingua dell'interfaccia utente dal pannello di controllo **Opzioni internazionali e della lingua** .</span><span class="sxs-lookup"><span data-stu-id="6f742-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="6f742-129">I licenziatari di Enterprise Edition ottengono tutte le lingue e possono distribuirli.</span><span class="sxs-lookup"><span data-stu-id="6f742-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="6f742-130">Distribuzione con immagine singola</span><span class="sxs-lookup"><span data-stu-id="6f742-130">Single image deployment</span></span>

<span data-ttu-id="6f742-131">I clienti aziendali e gli OEM possono ora ridurre il numero di immagini che è necessario gestire per distribuire Windows e le applicazioni nei computer in diverse impostazioni locali tramite la distribuzione di un'immagine singola.</span><span class="sxs-lookup"><span data-stu-id="6f742-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="6f742-132">Con MUI in Windows Vista, un'immagine contenente più lingue può essere distribuita a tutti gli utenti del linguaggio e gli utenti possono determinare le proprie lingue preferite (entro i criteri) durante l'installazione o l'esperienza iniziale "predefinita" con il computer.</span><span class="sxs-lookup"><span data-stu-id="6f742-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="6f742-133">In particolare, gli OEM possono inserire molte lingue dell'interfaccia utente nei nuovi computer per consentire agli utenti di selezionarne una dal centro di benvenuto.</span><span class="sxs-lookup"><span data-stu-id="6f742-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="6f742-134">Quindi, da un'immagine con più Language Pack, il programma di installazione visualizzerà un elenco di lingue disponibili e consentirà agli utenti di selezionarne uno.</span><span class="sxs-lookup"><span data-stu-id="6f742-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="6f742-135">Tutte le impostazioni internazionali vengono quindi impostate in base alla lingua o alle impostazioni locali selezionate.</span><span class="sxs-lookup"><span data-stu-id="6f742-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="6f742-136">Modello di manutenzione migliorato</span><span class="sxs-lookup"><span data-stu-id="6f742-136">Improved servicing model</span></span>

<span data-ttu-id="6f742-137">È ora possibile installare lo stesso QFE o il pacchetto di correzione della sicurezza in qualsiasi sistema di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="6f742-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="6f742-138">Questo è fondamentale perché consente un ritorno più rapido delle correzioni di sicurezza in particolare e consente a tutti gli utenti internazionali di trarre vantaggio dalla stessa disponibilità di tutte le correzioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6f742-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="6f742-139">Infrastruttura MUI</span><span class="sxs-lookup"><span data-stu-id="6f742-139">MUI infrastructure</span></span>

<span data-ttu-id="6f742-140">A partire da Windows Vista, le API MUI sono disponibili per consentire agli sviluppatori di sfruttare i meccanismi MUI per le proprie applicazioni, senza dover creare logica personalizzata per la gestione delle risorse e la gestione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="6f742-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="6f742-141">Gestione della lingua</span><span class="sxs-lookup"><span data-stu-id="6f742-141">Language management</span></span>

<span data-ttu-id="6f742-142">Le API MUI di base che forniscono funzionalità di gestione della lingua dell'interfaccia utente sono disponibili come parte dell'infrastruttura MUI.</span><span class="sxs-lookup"><span data-stu-id="6f742-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="6f742-143">Per semplificare la gestione delle diverse impostazioni della lingua dell'interfaccia utente a livello di sistema, utente e applicazione, MUI li combina internamente in un unico elenco con priorità.</span><span class="sxs-lookup"><span data-stu-id="6f742-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="6f742-144">MUI implementa quindi un meccanismo di fallback basato su questo elenco in ordine di priorità, consentendo soluzioni di localizzazione parziali offrendo agli utenti un'esperienza di lingua dell'interfaccia utente appropriata, se non preferita.</span><span class="sxs-lookup"><span data-stu-id="6f742-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="6f742-145">Ad esempio, un sistema che esegue la versione spagnola di Windows Vista con un LIP (Language Interface Pack) Catalano installato sul sistema operativo di base può supportare il comportamento seguente: il sistema tenterà e visualizzerà prima le risorse in catalano e, se queste risorse non sono disponibili in Catalano, fornire all'utente risorse per lo spagnolo.</span><span class="sxs-lookup"><span data-stu-id="6f742-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="6f742-146">Gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6f742-146">Resource handling</span></span>

<span data-ttu-id="6f742-147">Con l'infrastruttura MUI migliorata disponibile a partire da Windows Vista, la maggior parte delle tecnologie delle risorse comuni è abilitata per MUI.</span><span class="sxs-lookup"><span data-stu-id="6f742-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="6f742-148">Nella tabella seguente vengono forniti ulteriori dettagli sul supporto per la gestione delle risorse disponibile in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f742-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f742-149">Category</span><span class="sxs-lookup"><span data-stu-id="6f742-149">Category</span></span></th>
<th><span data-ttu-id="6f742-150">Supporto</span><span class="sxs-lookup"><span data-stu-id="6f742-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f742-151">Tipi di risorsa supportati</span><span class="sxs-lookup"><span data-stu-id="6f742-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="6f742-152">Risorsa Win32/non gestita:. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="6f742-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="6f742-153">Registrazioni correlate alla shell</span><span class="sxs-lookup"><span data-stu-id="6f742-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="6f742-154">Risorse correlate alla gestione: log eventi, file di snap-in/MSC</span><span class="sxs-lookup"><span data-stu-id="6f742-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="6f742-155">WMI: MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="6f742-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="6f742-156">Criteri di gruppo: ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="6f742-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="6f742-157">Resources.dll gestite</span><span class="sxs-lookup"><span data-stu-id="6f742-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f742-158">Strumenti di sviluppo</span><span class="sxs-lookup"><span data-stu-id="6f742-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="6f742-159">Per Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="6f742-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f742-160">Supporto per tipi di risorse limitati</span><span class="sxs-lookup"><span data-stu-id="6f742-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="6f742-161">file della guida \*. chm</span><span class="sxs-lookup"><span data-stu-id="6f742-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



