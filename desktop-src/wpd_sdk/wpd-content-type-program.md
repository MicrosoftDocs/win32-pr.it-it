---
description: '\_ \_ programma tipo di contenuto WPD \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758438"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="d7665-103">\_ \_ programma tipo di contenuto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="d7665-104">Un oggetto che descrive il tipo come WPD \_ Content \_ Type \_ Program rappresenta un programma eseguibile.</span><span class="sxs-lookup"><span data-stu-id="d7665-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="d7665-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7665-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7665-106">**Nome della proprietà**</span><span class="sxs-lookup"><span data-stu-id="d7665-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="d7665-107">**Obbligatorio o facoltativo**</span><span class="sxs-lookup"><span data-stu-id="d7665-107">**Required or Optional**</span></span>                                                           |
| [<span data-ttu-id="d7665-108">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d7665-109">Obbligatorio, ma di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d7665-109">Required, but read-only.</span></span> <span data-ttu-id="d7665-110">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="d7665-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="d7665-111">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d7665-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7665-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="d7665-113">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d7665-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="d7665-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="d7665-115">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d7665-116">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d7665-116">Required, read-only.</span></span> <span data-ttu-id="d7665-117">Un client non può impostare questa proprietà anche al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="d7665-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="d7665-118">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d7665-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7665-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="d7665-120">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d7665-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7665-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="d7665-122">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="d7665-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d7665-123">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="d7665-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="d7665-124">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d7665-125">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="d7665-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="d7665-126">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d7665-127">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7665-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="d7665-128">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d7665-129">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="d7665-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="d7665-130">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="d7665-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d7665-131">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7665-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="d7665-132">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d7665-133">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="d7665-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="d7665-134">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d7665-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-136">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d7665-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-138">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="d7665-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d7665-139">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="d7665-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="d7665-140">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="d7665-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d7665-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-142">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="d7665-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d7665-143">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="d7665-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="d7665-144">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d7665-145">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-146">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7665-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="d7665-147">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7665-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="d7665-148">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7665-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d7665-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-150">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="d7665-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d7665-151">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="d7665-152">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="d7665-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="d7665-153">Obbligatorio se l'oggetto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="d7665-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="d7665-154">\_ \_ impostazioni locali della lingua dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d7665-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d7665-155">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7665-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="d7665-156">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="d7665-156">Typical Resources</span></span>

<span data-ttu-id="d7665-157">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7665-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="d7665-158">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="d7665-158">Resource Name</span></span>                                          | <span data-ttu-id="d7665-159">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="d7665-159">Required or Optional</span></span> | <span data-ttu-id="d7665-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7665-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="d7665-161">**\_impostazione predefinita della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d7665-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="d7665-162">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7665-162">Required.</span></span>            | <span data-ttu-id="d7665-163">Contiene il file di programma.</span><span class="sxs-lookup"><span data-stu-id="d7665-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d7665-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7665-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7665-165">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="d7665-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



