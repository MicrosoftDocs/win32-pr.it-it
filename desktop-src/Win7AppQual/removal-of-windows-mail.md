---
description: Rimozione di Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Rimozione di Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116279"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="c8537-103">Rimozione di Windows Mail</span><span class="sxs-lookup"><span data-stu-id="c8537-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c8537-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="c8537-104">Affected Platforms</span></span>

<span data-ttu-id="c8537-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8537-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="c8537-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8537-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="c8537-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="c8537-107">Feature Impact</span></span>

<span data-ttu-id="c8537-108">**Gravità** - Alta</span><span class="sxs-lookup"><span data-stu-id="c8537-108">**Severity** - High</span></span>  
<span data-ttu-id="c8537-109">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="c8537-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="c8537-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8537-110">Description</span></span>

<span data-ttu-id="c8537-111">Microsoft sta deprecando l'utilità Windows Mail e disabilitando l'API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="c8537-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="c8537-112">Le altre API di posta elettronica sono state contrassegnate come deprecate e sono programmate per la rimozione in una versione successiva di Windows.</span><span class="sxs-lookup"><span data-stu-id="c8537-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="c8537-113">Tuttavia, le API documentate pubblicamente che non sono contrassegnate come deprecate o obsolete continueranno a funzionare in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8537-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="c8537-114">I file binari rimarranno nei sistemi degli utenti e continueranno a essere accessibili tramite le API, in particolare nei casi indicati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c8537-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="c8537-115">Inoltre, i file di posta elettronica (.eml) e di notizie (con estensione nws) degli utenti rimarranno nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c8537-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="c8537-116">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="c8537-116">Manifestation of Impact</span></span>

<span data-ttu-id="c8537-117">La rimozione di Windows Mail comporta quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c8537-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="c8537-118">Tutti i punti di ingresso a Windows Mail e Ai contatti (ad esempio, Menu Start, Collegamenti creati dall'utente, Avvia -> Esegui e così via) vengono rimossi o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="c8537-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="c8537-119">Alcune di queste vengono rimosse completamente, altre avranno esito negativo durante il tentativo di avvio.</span><span class="sxs-lookup"><span data-stu-id="c8537-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="c8537-120">Tutte le DLL vengono spedite nella casella</span><span class="sxs-lookup"><span data-stu-id="c8537-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="c8537-121">Le API documentate pubblicamente continuano a funzionare come in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8537-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="c8537-122">Tutte le API che tentano di avviare l'interfaccia utente principale del browser sono state modificate per creare un errore invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="c8537-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="c8537-123">La funzione restituirà l'esito positivo, ma non mostrerà l'interfaccia utente all'utente.</span><span class="sxs-lookup"><span data-stu-id="c8537-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="c8537-124">Le API che chiamano altre finestre di dialogo, ad esempio lo Spooler o la finestra di dialogo Account, continuano a mostrare tale interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c8537-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="c8537-125">I gestori di protocollo (mailto, ldap, news, snews, nntp) non verranno associati a Windows Mail o Contatti.</span><span class="sxs-lookup"><span data-stu-id="c8537-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="c8537-126">Quando tentano di avviarli, i clienti visualizzano una finestra di dialogo di errore che li indica alla posizione in cui possono impostare queste associazioni su un altro programma</span><span class="sxs-lookup"><span data-stu-id="c8537-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="c8537-127">Le associazioni di file (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sono interrotte o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="c8537-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="c8537-128">Quando tentano di aprire un file con queste estensioni, i clienti otterrà una finestra di dialogo che offre loro altre app installate che possono usare e che puntano a una pagina Web che offre soluzioni</span><span class="sxs-lookup"><span data-stu-id="c8537-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="c8537-129">Tutti i file utente (ad esempio, i file di contatto o i messaggi) rimangono nel sistema nello scenario di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c8537-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="c8537-130">La cartella Contatti è nascosta per impostazione predefinita, quindi i clienti non la visualizzano</span><span class="sxs-lookup"><span data-stu-id="c8537-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="c8537-131">Le API sono contrassegnate come deprecate in MSDN</span><span class="sxs-lookup"><span data-stu-id="c8537-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="c8537-132">La funzione di anteprima del file è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="c8537-132">The file preview function is removed</span></span>
-   <span data-ttu-id="c8537-133">Gli hook della shell nel menu di scelta rapida vengono rimossi</span><span class="sxs-lookup"><span data-stu-id="c8537-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="c8537-134">La funzione di ricerca file è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="c8537-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="c8537-135">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="c8537-135">Mitigation</span></span>

<span data-ttu-id="c8537-136">Gli utenti devono installare Windows Live Mail o qualsiasi altro prodotto di posta elettronica in grado di leggere i file con estensione eml e nws.</span><span class="sxs-lookup"><span data-stu-id="c8537-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="c8537-137">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c8537-137">Solution</span></span>

<span data-ttu-id="c8537-138">Rilevare se è installato un gestore di posta elettronica predefinito.</span><span class="sxs-lookup"><span data-stu-id="c8537-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="c8537-139">In caso contrario, consigliare all'utente di installare Windows Live Mail o qualsiasi altro prodotto in grado di leggere i file con estensione eml e nws.</span><span class="sxs-lookup"><span data-stu-id="c8537-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="c8537-140">Non progettare codice che chiama l'API dell'interfaccia utente di Windows Mail, perché non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="c8537-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="c8537-141">È necessario trovare altri modi per accedere ai file con estensione eml e nws.</span><span class="sxs-lookup"><span data-stu-id="c8537-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="c8537-142">Inoltre, non appena è possibile, interrompere l'affidamento su tutte le altre API di Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="c8537-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="c8537-143">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="c8537-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="c8537-144">Eseguire l'applicazione in un ambiente Windows 7 per assicurarsi che l'applicazione non tuffi a chiamare l'API dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c8537-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="c8537-145">In alternativa, è possibile eseguire Application Compatibility Toolkit (ACT) usando Windows Compatibility Evaluator (WCE) per individuare eventuali problemi potenziali dovuti alla deprecazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c8537-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c8537-146">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="c8537-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="c8537-147">Application Compatibility Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="c8537-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
