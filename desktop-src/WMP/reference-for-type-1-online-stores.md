---
title: Riferimento per negozi online di tipo 1
description: Riferimento per negozi online di tipo 1
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Windows Media Player Online Stores, informazioni di riferimento
- negozi online, informazioni di riferimento
- digitare 1 negozi online, informazioni di riferimento
- informazioni di riferimento sui negozi online di tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398757"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="99cfc-107">Riferimento per negozi online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="99cfc-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="99cfc-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="99cfc-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="99cfc-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="99cfc-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="99cfc-110">Windows Media Player 11 fornisce un compilatore di catalogo, un oggetto e diverse interfacce che supportano i negozi online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="99cfc-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="99cfc-111">Le sezioni seguenti illustrano in dettaglio questi argomenti.</span><span class="sxs-lookup"><span data-stu-id="99cfc-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="99cfc-112">Sezione</span><span class="sxs-lookup"><span data-stu-id="99cfc-112">Section</span></span>                                                                                    | <span data-ttu-id="99cfc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99cfc-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99cfc-114">Compilatore del catalogo per i negozi di tipo 1 online</span><span class="sxs-lookup"><span data-stu-id="99cfc-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="99cfc-115">Fornisce materiale di riferimento per il compilatore utilizzato da un archivio online per compilare il catalogo musicale.</span><span class="sxs-lookup"><span data-stu-id="99cfc-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="99cfc-116">Interfaccia IWMPContentContainer</span><span class="sxs-lookup"><span data-stu-id="99cfc-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="99cfc-117">Fornisce pagine di riferimento per i metodi che il plug-in del negozio online chiama per esaminare un contenitore di contenuti.</span><span class="sxs-lookup"><span data-stu-id="99cfc-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="99cfc-118">Un contenitore di contenuti rappresenta un set di elementi multimediali da scaricare o acquistare.</span><span class="sxs-lookup"><span data-stu-id="99cfc-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="99cfc-119">Implementato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="99cfc-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="99cfc-120">Interfaccia IWMPContentContainerList</span><span class="sxs-lookup"><span data-stu-id="99cfc-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="99cfc-121">Fornisce pagine di riferimento per i metodi che il plug-in del negozio online chiama per esaminare un elenco di contenitori di contenuto.</span><span class="sxs-lookup"><span data-stu-id="99cfc-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="99cfc-122">Implementato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="99cfc-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="99cfc-123">Interfaccia IWMPContentPartner</span><span class="sxs-lookup"><span data-stu-id="99cfc-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="99cfc-124">Fornisce pagine di riferimento per i metodi che Windows Media Player chiama per ottenere informazioni dallo Store online e per notificare all'archivio online le azioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99cfc-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="99cfc-125">Implementato dal plug-in Online Store.</span><span class="sxs-lookup"><span data-stu-id="99cfc-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="99cfc-126">Interfaccia IWMPContentPartnerCallback</span><span class="sxs-lookup"><span data-stu-id="99cfc-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="99cfc-127">Fornisce pagine di riferimento per i metodi che il plug-in del negozio online chiama per notificare a Windows Media Player il completamento delle operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="99cfc-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="99cfc-128">Implementato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="99cfc-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="99cfc-129">Oggetto esterno per i negozi di tipo 1 online</span><span class="sxs-lookup"><span data-stu-id="99cfc-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="99cfc-130">Fornisce pagine di riferimento per le proprietà, i metodi e gli eventi usati dallo script nelle pagine Web fornite dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="99cfc-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="99cfc-131">Enumerazioni per i negozi di tipo 1 online</span><span class="sxs-lookup"><span data-stu-id="99cfc-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="99cfc-132">Fornisce pagine di riferimento per le enumerazioni utilizzate nella comunicazione tra Media Player di Windows e il plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="99cfc-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="99cfc-133">Strutture per i negozi di tipo 1 online</span><span class="sxs-lookup"><span data-stu-id="99cfc-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="99cfc-134">Fornisce pagine di riferimento per le strutture utilizzate nella comunicazione tra Media Player Windows e il plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="99cfc-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="99cfc-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99cfc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99cfc-136">**Digitare 1 negozi online**</span><span class="sxs-lookup"><span data-stu-id="99cfc-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




