---
description: Un oggetto che descrive il tipo come \_ tipo di contenuto WPD \_ \_ Television rappresenta una registrazione TV.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347381"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="e13ba-103">\_televisione del \_ tipo di contenuto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="e13ba-104">Un oggetto che descrive il tipo come \_ tipo di contenuto WPD \_ \_ Television rappresenta una registrazione TV.</span><span class="sxs-lookup"><span data-stu-id="e13ba-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="e13ba-105">Questo tipo di oggetto deve ospitare le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="e13ba-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="e13ba-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="e13ba-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="e13ba-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="e13ba-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e13ba-108">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="e13ba-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ba-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-110">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="e13ba-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ba-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-112">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="e13ba-113">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="e13ba-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="e13ba-114">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="e13ba-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ba-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-116">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="e13ba-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ba-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-118">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="e13ba-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e13ba-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-120">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="e13ba-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="e13ba-121">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="e13ba-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="e13ba-122">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="e13ba-123">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="e13ba-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="e13ba-124">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="e13ba-125">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e13ba-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="e13ba-126">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="e13ba-127">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="e13ba-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="e13ba-128">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="e13ba-129">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="e13ba-130">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="e13ba-131">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="e13ba-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="e13ba-132">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="e13ba-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-134">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="e13ba-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-136">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="e13ba-137">Obbligatorio se l'oggetto è protetto da Digital Rights Management Technology.</span><span class="sxs-lookup"><span data-stu-id="e13ba-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="e13ba-138">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="e13ba-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="e13ba-139">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-140">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="e13ba-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="e13ba-141">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="e13ba-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="e13ba-142">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="e13ba-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-144">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="e13ba-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="e13ba-145">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e13ba-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="e13ba-146">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="e13ba-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-148">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e13ba-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="e13ba-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-150">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="e13ba-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="e13ba-151">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e13ba-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="e13ba-152">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="e13ba-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="e13ba-153">Obbligatorio se l'oggetto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="e13ba-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="e13ba-154">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="e13ba-154">Typical Resources</span></span>

<span data-ttu-id="e13ba-155">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e13ba-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="e13ba-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e13ba-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13ba-157">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="e13ba-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



