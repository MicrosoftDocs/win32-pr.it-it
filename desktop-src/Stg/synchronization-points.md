---
title: Punti di sincronizzazione
description: Quando i set di proprietà sono supportati nello stesso oggetto di IStorage, è importante tenere presente i punti di sincronizzazione tra l'archiviazione di base e l'archiviazione delle proprietà.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714566"
---
# <a name="synchronization-points"></a><span data-ttu-id="85b43-103">Punti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="85b43-103">Synchronization Points</span></span>

<span data-ttu-id="85b43-104">Quando i set di proprietà sono supportati nello stesso oggetto di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), è importante tenere presente i punti di sincronizzazione tra l'archiviazione di base e l'archiviazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="85b43-104">When property sets are supported on the same object as [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), it is important to be aware of synchronization points between the base storage and the property storage.</span></span>

<span data-ttu-id="85b43-105">La risorsa di archiviazione del set di proprietà include il flusso del set di proprietà in un buffer interno finché non viene eseguito il commit del buffer tramite il metodo [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="85b43-105">The property set storage holds the property set stream in an internal buffer until that buffer is committed through the [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) method.</span></span> <span data-ttu-id="85b43-106">Questo vale se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) è stato aperto in modalità transazionale o in modalità diretta.</span><span class="sxs-lookup"><span data-stu-id="85b43-106">This is true whether [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) was opened in transacted mode or in direct mode.</span></span>

 

 




