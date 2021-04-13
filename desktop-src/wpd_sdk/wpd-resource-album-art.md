---
description: Specifica un'immagine che rappresenta la grafica dell'album per l'oggetto.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525903"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="1df07-103">\_Art album delle risorse WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1df07-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="1df07-104">Specifica un'immagine che rappresenta la grafica dell'album per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1df07-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="1df07-105">Questo tipo di risorsa deve supportare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1df07-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="1df07-106">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="1df07-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="1df07-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="1df07-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="1df07-108">\_Larghezza supporto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="1df07-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="1df07-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1df07-109">Required.</span></span>                                              |
| [<span data-ttu-id="1df07-110">\_altezza supporto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="1df07-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="1df07-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1df07-111">Required.</span></span>                                              |
| [<span data-ttu-id="1df07-112">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1df07-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="1df07-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1df07-113">Required.</span></span>                                              |
| [<span data-ttu-id="1df07-114">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="1df07-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="1df07-115">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df07-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="1df07-116">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="1df07-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="1df07-117">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df07-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="1df07-118">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="1df07-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="1df07-119">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df07-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="1df07-120">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="1df07-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="1df07-121">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df07-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="1df07-122">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="1df07-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="1df07-123">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df07-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="1df07-124">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="1df07-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="1df07-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1df07-125">Required.</span></span>                                              |
| [<span data-ttu-id="1df07-126">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1df07-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="1df07-127">Consigliato</span><span class="sxs-lookup"><span data-stu-id="1df07-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="1df07-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1df07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df07-129">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="1df07-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



