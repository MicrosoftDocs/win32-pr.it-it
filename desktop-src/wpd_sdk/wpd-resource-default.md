---
description: Specifica l'intero file sottostante l'oggetto. È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non inclusi in altri tipi di risorse dei dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529892"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="0a4b8-104">\_impostazione predefinita della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="0a4b8-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="0a4b8-105">Specifica l'intero file sottostante l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="0a4b8-106">È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non inclusi in altri tipi di risorse dei dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="0a4b8-107">Verranno incluse tutte le risorse incorporate all'interno della risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="0a4b8-108">Ad esempio, la risorsa predefinita di una cartella radice di contatti può includere tutti i contatti annidati.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="0a4b8-109">Tuttavia, le risorse figlio semplicemente *collegate* da metadati o riferimenti non sono incluse.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="0a4b8-110">Un esempio è costituito da una playlist, che può essere collegata solo a file audio tramite riferimenti ai metadati o riferimenti al percorso testuale nel file.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="0a4b8-111">L'unico valore *PID* consentito per questo **PropertyKey** è zero.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="0a4b8-112">Questo tipo di risorsa deve supportare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="0a4b8-113">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="0a4b8-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="0a4b8-114">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="0a4b8-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0a4b8-115">\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a4b8-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="0a4b8-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-116">Required.</span></span>                                              |
| [<span data-ttu-id="0a4b8-117">l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere</span><span class="sxs-lookup"><span data-stu-id="0a4b8-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="0a4b8-118">Obbligatorio se i client possono leggere questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="0a4b8-119">l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere</span><span class="sxs-lookup"><span data-stu-id="0a4b8-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="0a4b8-120">Obbligatorio se i client possono scrivere in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="0a4b8-121">l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="0a4b8-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="0a4b8-122">Obbligatorio se i client possono eliminare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="0a4b8-123">\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD</span><span class="sxs-lookup"><span data-stu-id="0a4b8-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="0a4b8-124">Obbligatorio se i client hanno accesso in lettura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="0a4b8-125">\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="0a4b8-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="0a4b8-126">Obbligatorio se i client hanno accesso in scrittura alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="0a4b8-127">\_formato dell' \_ attributo della risorsa WPD \_</span><span class="sxs-lookup"><span data-stu-id="0a4b8-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="0a4b8-128">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-128">Required.</span></span>                                              |
| [<span data-ttu-id="0a4b8-129">\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a4b8-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="0a4b8-130">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="0a4b8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a4b8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4b8-132">**Requisiti per le risorse**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



