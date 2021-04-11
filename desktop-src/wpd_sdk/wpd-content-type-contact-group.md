---
description: '\_gruppo di \_ contatti del tipo di contenuto WPD \_ \_'
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233000"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="19028-103">\_gruppo di \_ contatti del tipo di contenuto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="19028-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="19028-104">Un oggetto che descrive il tipo come \_ \_ \_ gruppo di contatti del tipo di contenuto WPD \_ rappresenta un gruppo di contatti.</span><span class="sxs-lookup"><span data-stu-id="19028-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="19028-105">\_I riferimenti all'oggetto WPD di questo oggetto \_ contengono un elenco di ID oggetto per \_ vari \_ oggetti contatto del tipo di contenuto WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="19028-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="19028-106">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="19028-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="19028-107">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="19028-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="19028-108">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="19028-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="19028-109">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="19028-110">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19028-110">Required.</span></span>                                                             |
| [<span data-ttu-id="19028-111">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="19028-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19028-112">Required.</span></span>                                                             |
| [<span data-ttu-id="19028-113">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="19028-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="19028-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="19028-115">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="19028-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19028-116">Required.</span></span>                                                             |
| [<span data-ttu-id="19028-117">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="19028-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19028-118">Required.</span></span>                                                             |
| [<span data-ttu-id="19028-119">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="19028-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19028-120">Required.</span></span>                                                             |
| [<span data-ttu-id="19028-121">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="19028-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="19028-122">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="19028-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="19028-123">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="19028-124">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="19028-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="19028-125">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="19028-126">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="19028-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="19028-127">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="19028-128">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="19028-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="19028-129">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="19028-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="19028-130">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19028-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="19028-131">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="19028-132">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="19028-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="19028-133">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="19028-134">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="19028-135">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="19028-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="19028-137">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="19028-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="19028-138">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="19028-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="19028-139">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="19028-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="19028-140">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="19028-141">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="19028-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="19028-142">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="19028-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="19028-143">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="19028-144">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="19028-145">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="19028-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="19028-146">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="19028-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="19028-147">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="19028-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="19028-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="19028-149">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="19028-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="19028-150">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="19028-150">Optional</span></span>                                                              |
| [<span data-ttu-id="19028-151">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="19028-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="19028-152">Obbligatorio se l'oggetto può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="19028-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="19028-153">\_ \_ impostazioni locali della lingua dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="19028-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="19028-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19028-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="19028-155">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="19028-155">Typical Resources</span></span>

<span data-ttu-id="19028-156">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="19028-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19028-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19028-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19028-158">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="19028-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



