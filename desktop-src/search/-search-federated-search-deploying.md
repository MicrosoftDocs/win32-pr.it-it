---
description: In questo argomento viene illustrato come un utente registra un nuovo archivio dati remoto con ricerca federata aprendo un file di descrizione OpenSearch (con estensione osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del servizio OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Distribuire i connettori di ricerca nella ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484437"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="a1c78-103">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="a1c78-104">In questo argomento viene illustrato come un utente registra un nuovo archivio dati remoto con ricerca federata aprendo un file di descrizione OpenSearch (con estensione osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del servizio [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="a1c78-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="a1c78-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a1c78-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a1c78-106">File. searchconnector-ms (connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="a1c78-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="a1c78-107">Metodi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a1c78-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="a1c78-108">Distribuzione pull</span><span class="sxs-lookup"><span data-stu-id="a1c78-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="a1c78-109">Distribuzione push</span><span class="sxs-lookup"><span data-stu-id="a1c78-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="a1c78-110">Rilevamento dell'utilizzo</span><span class="sxs-lookup"><span data-stu-id="a1c78-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="a1c78-111">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a1c78-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a1c78-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1c78-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="a1c78-113">File. searchconnector-ms (connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="a1c78-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="a1c78-114">È sufficiente aprire il file con estensione osdx che descrive come connettersi al servizio Web e come eseguire il mapping di eventuali elementi personalizzati nel codice XML RSS o Atom per la registrazione del nuovo archivio dati remoto con la ricerca federata.</span><span class="sxs-lookup"><span data-stu-id="a1c78-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="a1c78-115">Un archivio dati che dispone già di un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) compatibile con la ricerca federata può essere aggiunto a Esplora risorse quando un utente apre un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="a1c78-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="a1c78-116">Dopo aver assegnato il file. osdx all'utente e l'utente apre il file con estensione osdx, si verificano gli eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1c78-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="a1c78-117">Viene creato un file con estensione searchconnector-ms nella cartella **ricerche di Windows** (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="a1c78-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="a1c78-118">Viene creato un collegamento al file. searchconnector-ms nella cartella **Links** (% USERPROFILE%/Links).</span><span class="sxs-lookup"><span data-stu-id="a1c78-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="a1c78-119">Viene visualizzato un collegamento nel riquadro **Preferiti** di esplorazione di Esplora risorse, che consente all'utente di spostarsi nel nuovo archivio dati ed eseguire query sul servizio Web.</span><span class="sxs-lookup"><span data-stu-id="a1c78-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="a1c78-120">Metodi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a1c78-120">Deployment Methods</span></span>

<span data-ttu-id="a1c78-121">Esistono due modi per distribuire i connettori di ricerca, la distribuzione pull e la distribuzione push.</span><span class="sxs-lookup"><span data-stu-id="a1c78-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="a1c78-122">Distribuzione pull</span><span class="sxs-lookup"><span data-stu-id="a1c78-122">Pull Deployment</span></span>

<span data-ttu-id="a1c78-123">Distribuzione pull descrive qualsiasi tipo di distribuzione in cui l'utente finale intraprende l'iniziativa di installare i connettori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1c78-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="a1c78-124">I metodi comuni di distribuzione pull sono:</span><span class="sxs-lookup"><span data-stu-id="a1c78-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="a1c78-125">Il file con estensione osdx viene collegato in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a1c78-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="a1c78-126">Pubblicazione del file in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="a1c78-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="a1c78-127">Fornire un collegamento dinamico nel sito Intranet. ad esempio, uno che genera file con estensione osdx personalizzati in base alle scelte utente o all'ambito corrente all'interno del sito.</span><span class="sxs-lookup"><span data-stu-id="a1c78-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="a1c78-128">Per il download del file quando l'utente fa clic sul collegamento nel browser, il server Web che ospita il servizio Web deve essere configurato in modo da recapitare il file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="a1c78-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="a1c78-129">Pertanto, è necessario configurare i tipi MIME nel server Web per trattare i file. osdx come `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="a1c78-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="a1c78-130">Facoltativamente, è possibile usare l'icona fornita da Microsoft per identificare il collegamento al connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1c78-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="a1c78-131">Distribuzione push</span><span class="sxs-lookup"><span data-stu-id="a1c78-131">Push Deployment</span></span>

<span data-ttu-id="a1c78-132">Distribuzione push descrive tutti i tipi di distribuzione che non dipendono dall'iniziativa utente per installare i connettori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1c78-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="a1c78-133">I metodi comuni di distribuzione push sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c78-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="a1c78-134">Preferenze Criteri di gruppo (GPP)</span><span class="sxs-lookup"><span data-stu-id="a1c78-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="a1c78-135">Script di accesso</span><span class="sxs-lookup"><span data-stu-id="a1c78-135">Logon script</span></span>
-   <span data-ttu-id="a1c78-136">Profili mobili</span><span class="sxs-lookup"><span data-stu-id="a1c78-136">Roaming profiles</span></span>
-   <span data-ttu-id="a1c78-137">Creazione delle immagini</span><span class="sxs-lookup"><span data-stu-id="a1c78-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="a1c78-138">Rilevamento dell'utilizzo</span><span class="sxs-lookup"><span data-stu-id="a1c78-138">Tracking Usage</span></span>

<span data-ttu-id="a1c78-139">Per tenere traccia dell'utilizzo del servizio [OpenSearch](https://github.com/dewitt/opensearch) da parte degli utenti che eseguono ricerche da Esplora risorse, filtrare i file di log del server Web per la stringa dell'agente utente: `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="a1c78-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1c78-140">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a1c78-140">Additional Resources</span></span>

<span data-ttu-id="a1c78-141">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1c78-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c78-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1c78-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c78-143">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="a1c78-144">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="a1c78-145">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="a1c78-146">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="a1c78-147">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="a1c78-148">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c78-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
