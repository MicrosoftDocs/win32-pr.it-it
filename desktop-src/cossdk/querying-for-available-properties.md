---
description: Esecuzione di query per le proprietà disponibili
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Esecuzione di query per le proprietà disponibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127402"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="d456b-103">Esecuzione di query per le proprietà disponibili</span><span class="sxs-lookup"><span data-stu-id="d456b-103">Querying for Available Properties</span></span>

<span data-ttu-id="d456b-104">Se si sta scrivendo uno strumento di amministrazione di uso generico, è molto probabile che sia necessario scrivere routine per l'impostazione delle proprietà in generale.</span><span class="sxs-lookup"><span data-stu-id="d456b-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="d456b-105">Per supportare questa operazione, esiste una funzionalità che consente di eseguire query in modo dinamico per le proprietà disponibili per gli elementi in una raccolta specifica.</span><span class="sxs-lookup"><span data-stu-id="d456b-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="d456b-106">La raccolta [**PropertyInfo**](propertyinfo.md) è disponibile da qualsiasi raccolta che potrebbe essere in attesa.</span><span class="sxs-lookup"><span data-stu-id="d456b-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="d456b-107">La raccolta **PropertyInfo** contiene un elemento per ogni proprietà disponibile.</span><span class="sxs-lookup"><span data-stu-id="d456b-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="d456b-108">È possibile enumerare questi elementi per determinare se una determinata proprietà è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d456b-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="d456b-109">È possibile ottenere la raccolta [**PropertyInfo**](propertyinfo.md) da qualsiasi raccolta che si sta tenendo usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d456b-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d456b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d456b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d456b-111">Recupero e impostazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d456b-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="d456b-112">Interdipendenze tra proprietà</span><span class="sxs-lookup"><span data-stu-id="d456b-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="d456b-113">Salvataggio o eliminazione di modifiche</span><span class="sxs-lookup"><span data-stu-id="d456b-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



