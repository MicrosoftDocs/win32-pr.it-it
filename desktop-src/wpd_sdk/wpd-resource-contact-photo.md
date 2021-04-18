---
description: Specifica un'immagine che rappresenta una foto dell'utente a cui si fa riferimento nell'oggetto contatto.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306646"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="5e141-103">\_ \_ Foto contatto risorse \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5e141-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="5e141-104">Specifica un'immagine che rappresenta una foto dell'utente a cui si fa riferimento nell'oggetto contatto.</span><span class="sxs-lookup"><span data-stu-id="5e141-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="5e141-105">Questo tipo di risorsa deve supportare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e141-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="5e141-106">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="5e141-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="5e141-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="5e141-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5e141-108">\_Larghezza supporto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5e141-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="5e141-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e141-109">Required.</span></span>                                              |
| [<span data-ttu-id="5e141-110">\_altezza supporto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5e141-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="5e141-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e141-111">Required.</span></span>                                              |
| [<span data-ttu-id="5e141-112">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="5e141-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="5e141-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e141-113">Required.</span></span>                                              |
| [<span data-ttu-id="5e141-114">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="5e141-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="5e141-115">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e141-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="5e141-116">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="5e141-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="5e141-117">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e141-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="5e141-118">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="5e141-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="5e141-119">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e141-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="5e141-120">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="5e141-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="5e141-121">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e141-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="5e141-122">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="5e141-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="5e141-123">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e141-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="5e141-124">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="5e141-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="5e141-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e141-125">Required.</span></span>                                              |
| [<span data-ttu-id="5e141-126">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="5e141-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="5e141-127">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="5e141-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="5e141-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e141-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e141-129">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="5e141-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



