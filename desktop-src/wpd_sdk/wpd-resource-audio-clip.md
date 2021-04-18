---
description: Specifica un clip audio per l'oggetto.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316798"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="dde5c-103">\_ \_ clip audio della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="dde5c-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="dde5c-104">Specifica un clip audio per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dde5c-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="dde5c-105">Questo tipo di risorsa deve supportare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="dde5c-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="dde5c-106">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="dde5c-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="dde5c-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="dde5c-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dde5c-108">\_velocità in \_ bit audio WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="dde5c-109">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="dde5c-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="dde5c-110">\_numero di \_ canali \_ audio WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="dde5c-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dde5c-111">Optional.</span></span>                                              |
| [<span data-ttu-id="dde5c-112">\_codice del \_ formato \_ audio WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="dde5c-113">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dde5c-113">Optional.</span></span>                                              |
| [<span data-ttu-id="dde5c-114">\_ \_ profondità bit audio \_ WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="dde5c-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dde5c-115">Optional.</span></span>                                              |
| [<span data-ttu-id="dde5c-116">\_ \_ allineamento blocchi audio \_ WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="dde5c-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dde5c-117">Optional.</span></span>                                              |
| [<span data-ttu-id="dde5c-118">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="dde5c-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="dde5c-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dde5c-119">Required.</span></span>                                              |
| [<span data-ttu-id="dde5c-120">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="dde5c-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="dde5c-121">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde5c-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="dde5c-122">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="dde5c-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="dde5c-123">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde5c-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="dde5c-124">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="dde5c-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="dde5c-125">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde5c-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="dde5c-126">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="dde5c-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="dde5c-127">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde5c-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="dde5c-128">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="dde5c-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="dde5c-129">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde5c-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="dde5c-130">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="dde5c-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="dde5c-131">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dde5c-131">Required.</span></span>                                              |
| [<span data-ttu-id="dde5c-132">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="dde5c-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="dde5c-133">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="dde5c-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="dde5c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dde5c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde5c-135">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="dde5c-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



