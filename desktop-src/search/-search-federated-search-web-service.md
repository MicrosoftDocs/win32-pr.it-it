---
description: In questo argomento vengono descritti i passaggi necessari per connettere un servizio Web tra l'archivio dati e la ricerca federata di Windows e come inviare query e restituire i risultati della ricerca in formato RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Connessione del servizio Web in ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128578"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="94dfb-103">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="94dfb-104">In questo argomento vengono descritti i passaggi necessari per connettere un servizio Web tra l'archivio dati e la ricerca federata di Windows e come inviare query e restituire i risultati della ricerca in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="94dfb-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="94dfb-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="94dfb-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="94dfb-106">Connettere il servizio Web</span><span class="sxs-lookup"><span data-stu-id="94dfb-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="94dfb-107">Registrare un archivio dati remoto esistente</span><span class="sxs-lookup"><span data-stu-id="94dfb-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="94dfb-108">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="94dfb-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="94dfb-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94dfb-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="94dfb-110">Connettere il servizio Web</span><span class="sxs-lookup"><span data-stu-id="94dfb-110">Connect Your web Service</span></span>

<span data-ttu-id="94dfb-111">**Per connettere il servizio Web dell'archivio dati alla ricerca federata, seguire questa procedura:**</span><span class="sxs-lookup"><span data-stu-id="94dfb-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="94dfb-112">Creare un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="94dfb-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="94dfb-113">Fornire il file. osdx agli utenti in modo che possano aggiungere il servizio su richiesta aprendo il file. osdx.</span><span class="sxs-lookup"><span data-stu-id="94dfb-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="94dfb-114">Generare un connettore di ricerca e distribuirlo attivamente nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="94dfb-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="94dfb-115">Registrare un archivio dati remoto esistente</span><span class="sxs-lookup"><span data-stu-id="94dfb-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="94dfb-116">Un utente registra un nuovo archivio dati remoto con ricerca federata di Windows aprendo un file di descrizione OpenSearch (con estensione osdx).</span><span class="sxs-lookup"><span data-stu-id="94dfb-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="94dfb-117">Quando l'utente esegue questa operazione, si verificano gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="94dfb-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="94dfb-118">Un file. searchconnector-ms (connettore di ricerca) viene creato nella cartella ricerche di Windows (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="94dfb-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="94dfb-119">Viene creato un collegamento al file. searchconnector-ms nella cartella Links (% USERPROFILE%/Links).</span><span class="sxs-lookup"><span data-stu-id="94dfb-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="94dfb-120">Viene visualizzato un collegamento nel riquadro **Preferiti** di esplorazione di Esplora risorse, che consente all'utente di spostarsi nel nuovo archivio dati ed eseguire query sul servizio Web.</span><span class="sxs-lookup"><span data-stu-id="94dfb-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="94dfb-121">Un archivio dati che dispone già di un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) compatibile con la ricerca federata di Windows può essere aggiunto a Esplora risorse quando un utente apre un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="94dfb-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="94dfb-122">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="94dfb-122">Additional Resources</span></span>

<span data-ttu-id="94dfb-123">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94dfb-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94dfb-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94dfb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94dfb-125">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="94dfb-126">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="94dfb-127">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="94dfb-128">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="94dfb-129">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="94dfb-130">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="94dfb-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
