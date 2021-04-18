---
title: Informazioni sugli archivi online di tipo 1
description: Informazioni sugli archivi online di tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online Stores, digitare 1 Store online
- negozi online, digitare 1 negozi online
- digitare 1 Store online, informazioni
- Windows Media Player, digitare 1 negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299428"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="376a6-107">Informazioni sugli archivi online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="376a6-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="376a6-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="376a6-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="376a6-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="376a6-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="376a6-110">Microsoft Windows Media Player 11 supporta due tipi di negozi online: tipo 1 e tipo 2.</span><span class="sxs-lookup"><span data-stu-id="376a6-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="376a6-111">Gli archivi di tipo 1 sono più profondamente integrati in Windows Media Player rispetto ai negozi di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="376a6-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="376a6-112">Un archivio online di tipo 1 fornisce un catalogo musicale scaricabile, in modo che Windows Media Player possa rendere disponibile il contenuto del negozio all'utente come se il contenuto si trovasse nel Catalogo multimediale locale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="376a6-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="376a6-113">Un archivio online di tipo 1 deve fornire un plug-in che implementi l'interfaccia [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="376a6-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="376a6-114">Quando l'utente naviga nell'interfaccia utente di Windows Media Player, il lettore chiama il plug-in in modo che lo Store online possa migliorare l'esperienza dell'utente fornendo pagine Web visualizzate nel lettore.</span><span class="sxs-lookup"><span data-stu-id="376a6-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="376a6-115">Di seguito sono riportate le funzionalità dei negozi in linea di tipo 1 che li distinguono da quelli di tipo 2:</span><span class="sxs-lookup"><span data-stu-id="376a6-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="376a6-116">**Semplicità d'uso.**</span><span class="sxs-lookup"><span data-stu-id="376a6-116">**Ease of use.**</span></span> <span data-ttu-id="376a6-117">Gli utenti possono cercare musica dal catalogo online Store usando la stessa interfaccia utente Windows Media Player familiare che attualmente usano per gestire la propria libreria personale.</span><span class="sxs-lookup"><span data-stu-id="376a6-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="376a6-118">Gli utenti possono visualizzare solo un singolo catalogo di Store online nella funzionalità di ricerca in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="376a6-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="376a6-119">**Convenienza.**</span><span class="sxs-lookup"><span data-stu-id="376a6-119">**Convenience.**</span></span> <span data-ttu-id="376a6-120">Gli utenti possono campionare o acquistare musica senza passare dalla funzionalità di esplorazione a un'altra parte dell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="376a6-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="376a6-121">**Funzionalità avanzate.**</span><span class="sxs-lookup"><span data-stu-id="376a6-121">**Rich features.**</span></span> <span data-ttu-id="376a6-122">Poiché il catalogo dei negozi online viene archiviato in modo analogo alla libreria dell'utente, molte delle funzionalità della libreria Media Player di Windows possono essere applicate al catalogo.</span><span class="sxs-lookup"><span data-stu-id="376a6-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="376a6-123">Ad esempio, gli utenti possono utilizzare la rotellina della funzionalità Sfoglia per filtrare il catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="376a6-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="376a6-124">Per un provider di negozio online, i vantaggi derivanti dalla fornitura di un archivio di tipo 1 anziché di un archivio di tipo 2 includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="376a6-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="376a6-125">Nodo personalizzato a visibilità elevata nell'albero della libreria Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="376a6-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="376a6-126">Sistema progettato per gli acquisti di musica.</span><span class="sxs-lookup"><span data-stu-id="376a6-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="376a6-127">Connessioni migliorate ai processi dei giocatori.</span><span class="sxs-lookup"><span data-stu-id="376a6-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="376a6-128">Gestione download migliore e più facile da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="376a6-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="376a6-129">Possibilità di spostarsi tra le varie funzionalità del lettore, inclusa l'apertura di nodi dell'albero della libreria specifici.</span><span class="sxs-lookup"><span data-stu-id="376a6-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="376a6-130">Notifiche relative alla scadenza delle licenze per il contenuto della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="376a6-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="376a6-131">Notifiche per l'uso di lettori musicali portatili connessi.</span><span class="sxs-lookup"><span data-stu-id="376a6-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="376a6-132">Nelle sezioni seguenti vengono fornite informazioni generali sugli archivi online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="376a6-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="376a6-133">Sezione</span><span class="sxs-lookup"><span data-stu-id="376a6-133">Section</span></span>                                                                                              | <span data-ttu-id="376a6-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="376a6-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="376a6-135">Catalogo musica</span><span class="sxs-lookup"><span data-stu-id="376a6-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="376a6-136">Descrive il catalogo musicale fornito dallo Store online.</span><span class="sxs-lookup"><span data-stu-id="376a6-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="376a6-137">Viene descritto il compilatore del catalogo fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="376a6-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="376a6-138">Contenitori di contenuto</span><span class="sxs-lookup"><span data-stu-id="376a6-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="376a6-139">Viene descritta l'interfaccia del contenitore di contenuti ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), che viene utilizzata per rappresentare una raccolta di elementi multimediali da acquistare o scaricare.</span><span class="sxs-lookup"><span data-stu-id="376a6-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="376a6-140">Integrazione della libreria</span><span class="sxs-lookup"><span data-stu-id="376a6-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="376a6-141">Descrive il modo in cui il catalogo musicale del negozio online è integrato nella visualizzazione libreria del lettore.</span><span class="sxs-lookup"><span data-stu-id="376a6-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="376a6-142">Pagine di individuazione</span><span class="sxs-lookup"><span data-stu-id="376a6-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="376a6-143">Viene descritta l'interazione tra Media Player Windows e le pagine Web fornite dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="376a6-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="376a6-144">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="376a6-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="376a6-145">Viene descritto in che modo l'archivio online può fornire menu di scelta rapida quando l'utente naviga nell'interfaccia utente del lettore.</span><span class="sxs-lookup"><span data-stu-id="376a6-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="376a6-146">Flussi audio</span><span class="sxs-lookup"><span data-stu-id="376a6-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="376a6-147">Viene descritto in che modo l'archivio online fornisce Windows Media Player con l'URL per lo streaming di contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="376a6-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="376a6-148">Documento ServiceInfo per un negozio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="376a6-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="376a6-149">Viene descritto il documento XML ServiceInfo fornito da un archivio online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="376a6-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="376a6-150">Digitare 1 plug-in di archivio online</span><span class="sxs-lookup"><span data-stu-id="376a6-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="376a6-151">Descrive il plug-in che deve essere fornito da un archivio online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="376a6-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="376a6-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="376a6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="376a6-153">**Digitare 1 negozi online**</span><span class="sxs-lookup"><span data-stu-id="376a6-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




