---
title: Oggetti Internet-Aware
description: Oggetti Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963503"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="0428f-103">Oggetti Internet-Aware</span><span class="sxs-lookup"><span data-stu-id="0428f-103">Internet-Aware Objects</span></span>

<span data-ttu-id="0428f-104">Sono state identificate determinate categorie per coprire le interfacce persistenza. Questi sono stati identificati come risultato della definizione del modo in cui i controlli funzionano in Internet.</span><span class="sxs-lookup"><span data-stu-id="0428f-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="0428f-105">Un contenitore che non supporta l'intera gamma di interfacce persistenza deve garantire che non venga ospitato un controllo che richiede una combinazione di interfacce che non supporta.</span><span class="sxs-lookup"><span data-stu-id="0428f-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="0428f-106">Le tabelle seguenti descrivono il significato per le varie categorie sia come implementate che come categorie obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="0428f-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="0428f-107">Categorie obbligatorie</span><span class="sxs-lookup"><span data-stu-id="0428f-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="0428f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0428f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0428f-109">CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0428f-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0428f-110">Ognuna di queste categorie si escludono a vicenda e viene usata solo quando un oggetto supporta solo un meccanismo di persistenza, da cui l'esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="0428f-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="0428f-111">I contenitori che non supportano il meccanismo di persistenza descritto da una di queste categorie devono impedire la creazione di oggetti di classi così contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="0428f-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="0428f-112">RequiresDataPathHost CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="0428f-113">L'oggetto richiede la possibilità di salvare i dati in uno o più percorsi e richiede il coinvolgimento del contenitore e pertanto richiede il supporto dei contenitori per [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0428f-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="0428f-114">Categorie implementate</span><span class="sxs-lookup"><span data-stu-id="0428f-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="0428f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0428f-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0428f-116">CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0428f-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0428f-117">L'oggetto supporta il meccanismo IPersist corrispondente \* per la categoria.</span><span class="sxs-lookup"><span data-stu-id="0428f-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="0428f-118">La tabella seguente fornisce il CATID esatto assegnato a ogni categoria:</span><span class="sxs-lookup"><span data-stu-id="0428f-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="0428f-119">Category</span><span class="sxs-lookup"><span data-stu-id="0428f-119">Category</span></span>                                | <span data-ttu-id="0428f-120">CATID</span><span class="sxs-lookup"><span data-stu-id="0428f-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="0428f-121">RequiresDataPathHost CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="0428f-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-123">PersistsToMoniker CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="0428f-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-125">PersistsToStorage CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="0428f-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-127">PersistsToStreamInit CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="0428f-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-129">PersistsToStream CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="0428f-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-131">PersistsToMemory CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="0428f-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-133">PersistsToFile CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="0428f-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0428f-135">PersistsToPropertyBag CATId \_</span><span class="sxs-lookup"><span data-stu-id="0428f-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0428f-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0428f-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0428f-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0428f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0428f-138">Categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="0428f-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

