---
description: '\_ \_ Calendario tipo di contenuto WPD \_'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316356"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="edcd4-103">\_ \_ Calendario tipo di contenuto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="edcd4-104">Un oggetto che descrive il tipo come \_ calendario del tipo di contenuto WPD \_ \_ rappresenta un calendario.</span><span class="sxs-lookup"><span data-stu-id="edcd4-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="edcd4-105">L'oggetto può essere un file che contiene informazioni sul calendario o una cartella che contiene altri oggetti correlati al calendario, ad esempio attività, appuntamenti e così via.</span><span class="sxs-lookup"><span data-stu-id="edcd4-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="edcd4-106">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="edcd4-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="edcd4-107">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="edcd4-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="edcd4-108">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="edcd4-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="edcd4-109">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="edcd4-110">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="edcd4-110">Required.</span></span>                                                             |
| [<span data-ttu-id="edcd4-111">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="edcd4-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="edcd4-112">Required.</span></span>                                                             |
| [<span data-ttu-id="edcd4-113">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="edcd4-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="edcd4-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="edcd4-115">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="edcd4-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="edcd4-116">Required.</span></span>                                                             |
| [<span data-ttu-id="edcd4-117">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="edcd4-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="edcd4-118">Required.</span></span>                                                             |
| [<span data-ttu-id="edcd4-119">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="edcd4-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="edcd4-120">Required.</span></span>                                                             |
| [<span data-ttu-id="edcd4-121">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="edcd4-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="edcd4-122">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="edcd4-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="edcd4-123">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="edcd4-124">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="edcd4-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="edcd4-125">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="edcd4-126">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="edcd4-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="edcd4-127">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="edcd4-128">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="edcd4-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="edcd4-129">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="edcd4-130">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="edcd4-131">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="edcd4-132">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="edcd4-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="edcd4-133">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="edcd4-134">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-135">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="edcd4-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-137">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="edcd4-138">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="edcd4-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="edcd4-139">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="edcd4-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="edcd4-140">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-141">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="edcd4-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="edcd4-142">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="edcd4-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="edcd4-143">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="edcd4-144">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-145">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="edcd4-146">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="edcd4-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="edcd4-147">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="edcd4-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="edcd4-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-149">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="edcd4-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="edcd4-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="edcd4-151">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="edcd4-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="edcd4-152">Obbligatorio se l'oggetto può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="edcd4-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="edcd4-153">\_ \_ impostazioni locali della lingua dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="edcd4-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="edcd4-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edcd4-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="edcd4-155">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="edcd4-155">Typical Resources</span></span>

<span data-ttu-id="edcd4-156">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="edcd4-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="edcd4-157">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="edcd4-157">Resource Name</span></span>                                          | <span data-ttu-id="edcd4-158">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="edcd4-158">Required or Optional</span></span>                             | <span data-ttu-id="edcd4-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edcd4-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="edcd4-160">**\_impostazione predefinita della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="edcd4-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="edcd4-161">Obbligatorio se l'oggetto è supportato da dati binari.</span><span class="sxs-lookup"><span data-stu-id="edcd4-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="edcd4-162">Contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="edcd4-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="edcd4-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edcd4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edcd4-164">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="edcd4-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



