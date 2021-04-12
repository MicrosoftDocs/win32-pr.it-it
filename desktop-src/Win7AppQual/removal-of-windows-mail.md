---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Rimozione di Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233485"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="7e01c-103">Rimozione di Windows Mail</span><span class="sxs-lookup"><span data-stu-id="7e01c-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7e01c-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="7e01c-104">Affected Platforms</span></span>

<span data-ttu-id="7e01c-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e01c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7e01c-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e01c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="7e01c-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="7e01c-107">Feature Impact</span></span>

<span data-ttu-id="7e01c-108">**Gravità** -alta</span><span class="sxs-lookup"><span data-stu-id="7e01c-108">**Severity** - High</span></span>  
<span data-ttu-id="7e01c-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="7e01c-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="7e01c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e01c-110">Description</span></span>

<span data-ttu-id="7e01c-111">Microsoft sta deprecando l'utilità Windows Mail e disabilitando l'API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="7e01c-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="7e01c-112">Le altre API di posta elettronica sono state contrassegnate come deprecate e vengono rimosse in una versione successiva di Windows.</span><span class="sxs-lookup"><span data-stu-id="7e01c-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="7e01c-113">Tuttavia, le API documentate pubblicamente non contrassegnate come deprecate o obsolete continueranno a funzionare in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e01c-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="7e01c-114">I file binari resteranno nei sistemi degli utenti e continueranno a essere accessibili tramite le API, in particolare nei casi indicati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7e01c-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="7e01c-115">Inoltre, i file di posta elettronica (. eml) e le notizie (. NWS) degli utenti rimarranno nel sistema.</span><span class="sxs-lookup"><span data-stu-id="7e01c-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7e01c-116">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="7e01c-116">Manifestation of Impact</span></span>

<span data-ttu-id="7e01c-117">La rimozione di Windows Mail comporta le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="7e01c-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="7e01c-118">Tutti i punti di ingresso di Windows Mail e i contatti, ad esempio menu Start, scelte rapide create dall'utente, avvio > esecuzione e così via, vengono rimossi o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="7e01c-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="7e01c-119">Alcune di queste sono completamente rimosse, altre avranno esito negativo durante il tentativo di avvio.</span><span class="sxs-lookup"><span data-stu-id="7e01c-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="7e01c-120">Tutte le dll vengono fornite nella casella</span><span class="sxs-lookup"><span data-stu-id="7e01c-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="7e01c-121">Le API documentate pubblicamente continuano a funzionare come in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e01c-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="7e01c-122">Tutte le API che tentano di avviare l'interfaccia utente principale del browser sono state modificate per creare un errore invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="7e01c-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="7e01c-123">La funzione restituirà l'esito positivo, ma non visualizzerà l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e01c-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="7e01c-124">Le API che chiamano altre finestre di dialogo, ad esempio la finestra di dialogo spooler o accounts, continuano a mostrare tale interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7e01c-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="7e01c-125">I gestori del protocollo (mailto, LDAP, News, SNEWS, NNTP) non verranno associati a Windows Mail o ai contatti.</span><span class="sxs-lookup"><span data-stu-id="7e01c-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="7e01c-126">Quando si tenta di avviarli, i clienti visualizzeranno una finestra di dialogo di errore che punta alla posizione in cui possono impostare queste associazioni in un altro programma</span><span class="sxs-lookup"><span data-stu-id="7e01c-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="7e01c-127">Le associazioni di file (. eml,. NWS,. Contact,. Group,. wab,. p7c,. VFC) sono interrotte o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="7e01c-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="7e01c-128">Quando si tenta di aprire un file con queste estensioni, i clienti riceveranno una finestra di dialogo che offre altre app installate che possono usare e che puntano a una pagina Web che offre soluzioni</span><span class="sxs-lookup"><span data-stu-id="7e01c-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="7e01c-129">Tutti i file utente (ad esempio, file di contatto o messaggi) rimangono nel sistema nello scenario di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7e01c-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="7e01c-130">La cartella contatti è nascosta per impostazione predefinita, quindi i clienti non visualizzeranno la cartella</span><span class="sxs-lookup"><span data-stu-id="7e01c-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="7e01c-131">Le API sono contrassegnate come deprecate in MSDN</span><span class="sxs-lookup"><span data-stu-id="7e01c-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="7e01c-132">La funzione di anteprima file è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="7e01c-132">The file preview function is removed</span></span>
-   <span data-ttu-id="7e01c-133">Gli hook della shell nel menu di scelta rapida vengono rimossi</span><span class="sxs-lookup"><span data-stu-id="7e01c-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="7e01c-134">La funzione di ricerca file è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="7e01c-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="7e01c-135">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="7e01c-135">Mitigation</span></span>

<span data-ttu-id="7e01c-136">Gli utenti devono installare Windows Live Mail o qualsiasi altro prodotto di posta elettronica in grado di leggere file con estensione eml e NWS.</span><span class="sxs-lookup"><span data-stu-id="7e01c-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="7e01c-137">Soluzione</span><span class="sxs-lookup"><span data-stu-id="7e01c-137">Solution</span></span>

<span data-ttu-id="7e01c-138">Rilevare se è installato un gestore di posta predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e01c-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="7e01c-139">In caso contrario, consigliare all'utente di installare Windows Live Mail o qualsiasi altro prodotto in grado di leggere file con estensione eml e NWS.</span><span class="sxs-lookup"><span data-stu-id="7e01c-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="7e01c-140">Non progettare codice che chiama l'API dell'interfaccia utente di Windows Mail, perché non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="7e01c-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="7e01c-141">È necessario trovare altri modi per accedere ai file con estensione. eml e. NWS.</span><span class="sxs-lookup"><span data-stu-id="7e01c-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="7e01c-142">Inoltre, non appena è possibile, interrompere la dipendenza da tutte le altre API di Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="7e01c-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="7e01c-143">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="7e01c-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="7e01c-144">Eseguire l'applicazione in un ambiente Windows 7 per assicurarsi che l'applicazione non tenti di chiamare l'API dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e01c-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="7e01c-145">In alternativa, è possibile eseguire Application Compatibility Toolkit (ACT) utilizzando Windows Compatibility Evaluator (WCE) per individuare eventuali problemi causati dalla deprecazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7e01c-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7e01c-146">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="7e01c-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="7e01c-147">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="7e01c-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
