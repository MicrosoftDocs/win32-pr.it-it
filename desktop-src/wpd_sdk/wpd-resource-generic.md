---
description: Specifica un tipo di risorsa non definito diversamente dai dispositivi portatili Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128947"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="63f5f-103">\_risorsa WPD \_ generica</span><span class="sxs-lookup"><span data-stu-id="63f5f-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="63f5f-104">Specifica un tipo di risorsa non definito diversamente dai dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="63f5f-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="63f5f-105">È possibile definire risorse personalizzate che supportano qualsiasi attributo definito da dispositivi portatili o di Windows.</span><span class="sxs-lookup"><span data-stu-id="63f5f-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="63f5f-106">Tutte le risorse create devono tuttavia supportare i seguenti attributi.</span><span class="sxs-lookup"><span data-stu-id="63f5f-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="63f5f-107">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="63f5f-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="63f5f-108">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="63f5f-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="63f5f-109">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="63f5f-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="63f5f-110">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="63f5f-110">Required.</span></span>                                              |
| [<span data-ttu-id="63f5f-111">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="63f5f-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="63f5f-112">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f5f-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="63f5f-113">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="63f5f-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="63f5f-114">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f5f-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="63f5f-115">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="63f5f-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="63f5f-116">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f5f-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="63f5f-117">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="63f5f-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="63f5f-118">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f5f-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="63f5f-119">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="63f5f-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="63f5f-120">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f5f-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="63f5f-121">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="63f5f-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="63f5f-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="63f5f-122">Required.</span></span>                                              |
| [<span data-ttu-id="63f5f-123">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="63f5f-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="63f5f-124">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="63f5f-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="63f5f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63f5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f5f-126">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="63f5f-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



