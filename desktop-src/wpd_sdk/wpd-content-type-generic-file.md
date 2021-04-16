---
description: '\_ \_ messaggio generico di tipo di contenuto WPD \_ \_'
ms.assetid: 8e58d15f-ee51-42c2-9d8b-6c3b9c730ff4
title: WPD_CONTENT_TYPE_GENERIC_MESSAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febde68787366dc0f84b1b187f1393017ceb9c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347396"
---
# <a name="wpd_content_type_generic_message"></a><span data-ttu-id="ebf5a-103">\_ \_ messaggio generico di tipo di contenuto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-103">WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE</span></span>

<span data-ttu-id="ebf5a-104">Un oggetto che descrive il tipo come \_ messaggio generico del tipo di contenuto WPD \_ \_ \_ rappresenta un messaggio, ad esempio SMS, posta elettronica e così via.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-104">An object that describes its type as WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE represents a message, for example, SMS, e-mail, and so on.</span></span>

<span data-ttu-id="ebf5a-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="ebf5a-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="ebf5a-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="ebf5a-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="ebf5a-107">Required or Optional</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ebf5a-108">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="ebf5a-109">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-109">Required, read-only.</span></span> <span data-ttu-id="ebf5a-110">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="ebf5a-111">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="ebf5a-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-113">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="ebf5a-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="ebf5a-115">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="ebf5a-116">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-116">Required, read-only.</span></span> <span data-ttu-id="ebf5a-117">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="ebf5a-118">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="ebf5a-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-119">Required.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-120">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="ebf5a-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-121">Required.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-122">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="ebf5a-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="ebf5a-123">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-123">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="ebf5a-124">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="ebf5a-125">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="ebf5a-125">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="ebf5a-126">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="ebf5a-127">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-127">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="ebf5a-128">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="ebf5a-129">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-129">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="ebf5a-130">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="ebf5a-131">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-131">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="ebf5a-132">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="ebf5a-133">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-133">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="ebf5a-134">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="ebf5a-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-135">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-136">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="ebf5a-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-137">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-138">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="ebf5a-139">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-139">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="ebf5a-140">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="ebf5a-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="ebf5a-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-141">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-142">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="ebf5a-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="ebf5a-143">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-143">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="ebf5a-144">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="ebf5a-145">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-145">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-146">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="ebf5a-147">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-147">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="ebf5a-148">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ebf5a-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="ebf5a-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-149">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-150">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="ebf5a-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="ebf5a-151">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-151">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ebf5a-152">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="ebf5a-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="ebf5a-153">Obbligatorio se l'oggetto può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-153">Required if the object can be deleted.</span></span>                                         |
| [<span data-ttu-id="ebf5a-154">\_ \_ impostazioni locali della lingua dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="ebf5a-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="ebf5a-155">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-155">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="ebf5a-156">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="ebf5a-156">Typical Resources</span></span>

<span data-ttu-id="ebf5a-157">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="ebf5a-158">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ebf5a-158">Resource Name</span></span>                                          | <span data-ttu-id="ebf5a-159">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="ebf5a-159">Required or Optional</span></span>                                  | <span data-ttu-id="ebf5a-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebf5a-160">Description</span></span>        |
|--------------------------------------------------------|-------------------------------------------------------|--------------------|
| [<span data-ttu-id="ebf5a-161">**\_impostazione predefinita della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ebf5a-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="ebf5a-162">Obbligatorio se l'oggetto è supportato con dati binari.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-162">Required if the object is supported with binary data.</span></span> | <span data-ttu-id="ebf5a-163">Contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-163">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ebf5a-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebf5a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf5a-165">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="ebf5a-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



