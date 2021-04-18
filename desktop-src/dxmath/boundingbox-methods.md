---
description: Metodi BoundingBox
ms.assetid: 68db5936-f0f8-4dbd-a183-b6c3089af0f0
title: Metodi BoundingBox
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b58c79f202304a289bf1e30447b76ba9ad6dc83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309427"
---
# <a name="boundingbox-methods"></a><span data-ttu-id="44cc1-103">Metodi BoundingBox</span><span class="sxs-lookup"><span data-stu-id="44cc1-103">BoundingBox Methods</span></span>



| <span data-ttu-id="44cc1-104">Metodo</span><span class="sxs-lookup"><span data-stu-id="44cc1-104">Method</span></span>                                                              | <span data-ttu-id="44cc1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44cc1-105">Description</span></span>                                                                                            |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44cc1-106">**Contiene**</span><span class="sxs-lookup"><span data-stu-id="44cc1-106">**Contains**</span></span>](boundingbox-contains.md)<br/>                 | <span data-ttu-id="44cc1-107">Verifica se il BoundingBox contiene un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="44cc1-107">Tests whether the BoundingBox contains a specified object.</span></span><br/>                                  |
| [<span data-ttu-id="44cc1-108">**CreateFromPoints**</span><span class="sxs-lookup"><span data-stu-id="44cc1-108">**CreateFromPoints**</span></span>](boundingbox-createfrompoints.md)<br/> | <span data-ttu-id="44cc1-109">Crea un BoundingBox da punti.</span><span class="sxs-lookup"><span data-stu-id="44cc1-109">Creates a BoundingBox from points.</span></span><br/>                                                          |
| [<span data-ttu-id="44cc1-110">**Interseca**</span><span class="sxs-lookup"><span data-stu-id="44cc1-110">**Intersects**</span></span>](boundingbox-intersects.md)<br/>             | <span data-ttu-id="44cc1-111">Verifica il BoundingBox per l'intersezione con un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="44cc1-111">Tests the BoundingBox for intersection with another object.</span></span><br/>                                 |
| [<span data-ttu-id="44cc1-112">**Transform**</span><span class="sxs-lookup"><span data-stu-id="44cc1-112">**Transform**</span></span>](boundingbox-transform.md)<br/>               | <span data-ttu-id="44cc1-113">Trasforma l'oggetto BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="44cc1-113">Transforms the BoundingBox.</span></span><br/>                                                                 |
| [<span data-ttu-id="44cc1-114">**ContainedBy**</span><span class="sxs-lookup"><span data-stu-id="44cc1-114">**ContainedBy**</span></span>](/windows/desktop/api/DirectXCollision/nf-directxcollision-boundingbox-containedby)<br/>           | <span data-ttu-id="44cc1-115">Verifica se il [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) è contenuto nel tronco specificato.</span><span class="sxs-lookup"><span data-stu-id="44cc1-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) is contained by the specified frustum.</span></span><br/> |
| [<span data-ttu-id="44cc1-116">**CreateFromSphere**</span><span class="sxs-lookup"><span data-stu-id="44cc1-116">**CreateFromSphere**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfromsphere)<br/> | <span data-ttu-id="44cc1-117">Crea un oggetto BoundingBox sufficientemente grande da contenere la BoundingSphere specificata.</span><span class="sxs-lookup"><span data-stu-id="44cc1-117">Creates a BoundingBox large enough to contain the a specified BoundingSphere.</span></span><br/>               |
| [<span data-ttu-id="44cc1-118">**CreateMerged**</span><span class="sxs-lookup"><span data-stu-id="44cc1-118">**CreateMerged**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createmerged)<br/>         | <span data-ttu-id="44cc1-119">Crea un oggetto BoundingBox sufficientemente grande da contenere due istanze BoundBox specificati.</span><span class="sxs-lookup"><span data-stu-id="44cc1-119">Creates a BoundingBox large enough to contains two specified BoundBox intances.</span></span><br/>             |
| [<span data-ttu-id="44cc1-120">**Getangoli**</span><span class="sxs-lookup"><span data-stu-id="44cc1-120">**GetCorners**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-getcorners)<br/>             | <span data-ttu-id="44cc1-121">Recupera gli angoli dell'oggetto BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="44cc1-121">Retrieves the corners of the BoundingBox.</span></span><br/>                                                   |
| [<span data-ttu-id="44cc1-122">**\_assegnazione op**</span><span class="sxs-lookup"><span data-stu-id="44cc1-122">**op\_Assignment**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-operator-assign)<br/>      | <span data-ttu-id="44cc1-123">Copia i valori da un altro BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="44cc1-123">Copies values from another BoundingBox.</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="44cc1-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44cc1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44cc1-125">BoundingBox</span><span class="sxs-lookup"><span data-stu-id="44cc1-125">BoundingBox</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
