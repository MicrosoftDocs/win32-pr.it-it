---
description: Specifica un'icona per l'oggetto.
ms.assetid: 7abf0f9a-795b-4650-af7a-44aee4d3dd91
title: WPD_RESOURCE_ICON
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca008b22700869327c3bb432dd9c591affcea22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317847"
---
# <a name="wpd_resource_icon"></a><span data-ttu-id="c0a07-103">\_icona della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="c0a07-103">WPD\_RESOURCE\_ICON</span></span>

<span data-ttu-id="c0a07-104">Specifica un'icona per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0a07-104">Specifies an icon for the object.</span></span>

<span data-ttu-id="c0a07-105">Questo tipo di risorsa deve supportare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0a07-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="c0a07-106">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="c0a07-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="c0a07-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="c0a07-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c0a07-108">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c0a07-108">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="c0a07-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0a07-109">Required.</span></span>                                              |
| [<span data-ttu-id="c0a07-110">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="c0a07-110">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="c0a07-111">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0a07-111">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="c0a07-112">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="c0a07-112">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="c0a07-113">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0a07-113">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="c0a07-114">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="c0a07-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="c0a07-115">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0a07-115">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="c0a07-116">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="c0a07-116">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="c0a07-117">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0a07-117">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="c0a07-118">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="c0a07-118">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="c0a07-119">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0a07-119">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="c0a07-120">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="c0a07-120">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="c0a07-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0a07-121">Required.</span></span>                                              |
| [<span data-ttu-id="c0a07-122">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c0a07-122">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="c0a07-123">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="c0a07-123">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="c0a07-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0a07-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a07-125">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="c0a07-125">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



