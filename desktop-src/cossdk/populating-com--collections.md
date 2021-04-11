---
description: Popolamento di raccolte COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Popolamento di raccolte COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342251"
---
# <a name="populating-com-collections"></a><span data-ttu-id="71f2b-103">Popolamento di raccolte COM+</span><span class="sxs-lookup"><span data-stu-id="71f2b-103">Populating COM+ Collections</span></span>

<span data-ttu-id="71f2b-104">Dopo aver recuperato una raccolta e prima di poter usare direttamente gli elementi in esso contenuti, è necessario popolare la raccolta usando il metodo [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="71f2b-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="71f2b-105">Recupera i dati per il contenuto della raccolta dal catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="71f2b-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="71f2b-106">È importante tenere presente che ogni volta che si utilizzano gli oggetti COMAdmin per modificare gli elementi o i dati nelle raccolte, si sta effettivamente lavorando sui dati memorizzati temporaneamente nella cache. non si sta lavorando direttamente con il catalogo permanente.</span><span class="sxs-lookup"><span data-stu-id="71f2b-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="71f2b-107">Non viene eseguita alcuna operazione con una raccolta o con i relativi elementi nel catalogo fino a quando non si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="71f2b-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="71f2b-108">Per informazioni dettagliate, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="71f2b-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="71f2b-109">Tutte le chiamate successive a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prima di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), hanno l'effetto di ignorare le modifiche in sospeso in tutti gli elementi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="71f2b-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="71f2b-110">**Popola** popola sempre la cache con cui si sta lavorando con i dati salvati in modalità permanente nell'archivio dati del catalogo sottostante.</span><span class="sxs-lookup"><span data-stu-id="71f2b-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71f2b-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71f2b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f2b-112">Esplorazione della gerarchia della raccolta COM+</span><span class="sxs-lookup"><span data-stu-id="71f2b-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="71f2b-113">Esecuzione di query per le raccolte correlate disponibili</span><span class="sxs-lookup"><span data-stu-id="71f2b-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="71f2b-114">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="71f2b-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



