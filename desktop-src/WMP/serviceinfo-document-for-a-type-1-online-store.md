---
title: Documento ServiceInfo per un negozio online di tipo 1
description: Documento ServiceInfo per un negozio online di tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044861"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="b26b1-107">Documento ServiceInfo per un negozio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="b26b1-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="b26b1-108">Gli archivi online di tipo 1 devono fornire a Microsoft l'URL di un documento XML che descrive l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="b26b1-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="b26b1-109">Windows Media Player 11 utilizza questo documento per determinare come configurare l'interfaccia utente per ospitare lo Store online.</span><span class="sxs-lookup"><span data-stu-id="b26b1-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="b26b1-110">Il documento ServiceInfo per un archivio di tipo 1 fornisce le informazioni seguenti a Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="b26b1-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="b26b1-111">Informazioni utilizzate per configurare il pulsante **Store online** (chiamato anche scheda), ad esempio il testo del pulsante, il colore del pulsante e la descrizione comando per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="b26b1-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="b26b1-112">URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.</span><span class="sxs-lookup"><span data-stu-id="b26b1-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="b26b1-113">URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b26b1-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="b26b1-114">URL in cui Windows Media Player può recuperare il plug-in del negozio online, in modo che sia possibile installare il plug-in nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b26b1-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="b26b1-115">Quando Windows Media Player Recupera il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL.</span><span class="sxs-lookup"><span data-stu-id="b26b1-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="b26b1-116">La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali e sulla posizione geografica dell'utente e sulla versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b26b1-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b26b1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b26b1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b26b1-118">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b26b1-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b26b1-119">**Creazione dinamica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b26b1-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="b26b1-120">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b26b1-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b26b1-121">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b26b1-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




