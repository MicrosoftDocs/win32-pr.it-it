---
description: Esecuzione di query per le raccolte correlate disponibili
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Esecuzione di query per le raccolte correlate disponibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342321"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="50dd8-103">Esecuzione di query per le raccolte correlate disponibili</span><span class="sxs-lookup"><span data-stu-id="50dd8-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="50dd8-104">Se si scrive uno strumento di amministrazione di uso generico, è probabile che sia necessario scrivere routine per spostarsi nell'intera gerarchia di raccolta.</span><span class="sxs-lookup"><span data-stu-id="50dd8-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="50dd8-105">Per supportare questa operazione, COM+ dispone di una funzionalità che consente di eseguire query in modo dinamico per le raccolte correlate disponibili in una raccolta specifica.</span><span class="sxs-lookup"><span data-stu-id="50dd8-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="50dd8-106">La raccolta [**RelatedCollectionInfo**](relatedcollectioninfo.md) è disponibile da qualsiasi raccolta che è possibile mantenere e contiene un elemento per ogni raccolta correlata disponibile.</span><span class="sxs-lookup"><span data-stu-id="50dd8-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="50dd8-107">È possibile enumerare questi elementi per determinare se una determinata raccolta è disponibile.</span><span class="sxs-lookup"><span data-stu-id="50dd8-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="50dd8-108">È possibile ottenere la raccolta [**RelatedCollectionInfo**](relatedcollectioninfo.md) da qualsiasi raccolta che si sta tenendo usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="50dd8-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50dd8-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50dd8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50dd8-110">Esplorazione della gerarchia della raccolta COM+</span><span class="sxs-lookup"><span data-stu-id="50dd8-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="50dd8-111">Popolamento di raccolte COM+</span><span class="sxs-lookup"><span data-stu-id="50dd8-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="50dd8-112">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="50dd8-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



