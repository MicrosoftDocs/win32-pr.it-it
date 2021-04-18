---
description: '\_certificato del \_ tipo di contenuto WPD \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316355"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="2bbed-103">\_certificato del \_ tipo di contenuto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="2bbed-104">Un oggetto che descrive il tipo come \_ \_ certificato del tipo di contenuto WPD \_ rappresenta un certificato utilizzato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="2bbed-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="2bbed-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bbed-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="2bbed-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="2bbed-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="2bbed-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="2bbed-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="2bbed-108">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="2bbed-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-109">Required.</span></span>                                                             |
| [<span data-ttu-id="2bbed-110">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="2bbed-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-111">Required.</span></span>                                                             |
| [<span data-ttu-id="2bbed-112">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="2bbed-113">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="2bbed-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="2bbed-114">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="2bbed-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-115">Required.</span></span>                                                             |
| [<span data-ttu-id="2bbed-116">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="2bbed-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-117">Required.</span></span>                                                             |
| [<span data-ttu-id="2bbed-118">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="2bbed-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-119">Required.</span></span>                                                             |
| [<span data-ttu-id="2bbed-120">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="2bbed-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="2bbed-121">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="2bbed-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="2bbed-122">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="2bbed-123">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="2bbed-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="2bbed-124">\_dimensioni dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="2bbed-125">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="2bbed-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="2bbed-126">\_ \_ \_ nome file originale oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="2bbed-127">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="2bbed-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="2bbed-128">\_oggetto WPD \_ non utilizzabile \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="2bbed-129">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="2bbed-130">\_riferimenti a oggetti WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="2bbed-131">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="2bbed-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="2bbed-132">\_parole chiave dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="2bbed-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-134">\_ \_ ID sincronizzazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="2bbed-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-136">\_oggetto WPD \_ \_ protetto da DRM \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="2bbed-137">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="2bbed-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="2bbed-138">\_data dell'oggetto WPD \_ \_ creata</span><span class="sxs-lookup"><span data-stu-id="2bbed-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="2bbed-139">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-140">\_data dell'oggetto WPD \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="2bbed-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="2bbed-141">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="2bbed-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="2bbed-142">\_ \_ Data creazione oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="2bbed-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-144">\_riferimenti all'oggetto WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="2bbed-145">Consigliato se un altro oggetto fa riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2bbed-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="2bbed-146">\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2bbed-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="2bbed-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-148">oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa</span><span class="sxs-lookup"><span data-stu-id="2bbed-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="2bbed-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="2bbed-150">l' \_ oggetto WPD \_ può essere \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="2bbed-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="2bbed-151">Obbligatorio se l'oggetto può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="2bbed-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="2bbed-152">\_ \_ impostazioni locali della lingua dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="2bbed-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="2bbed-153">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2bbed-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="2bbed-154">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="2bbed-154">Typical Resources</span></span>

<span data-ttu-id="2bbed-155">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bbed-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="2bbed-156">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="2bbed-156">Resource Name</span></span>                                          | <span data-ttu-id="2bbed-157">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="2bbed-157">Required or Optional</span></span> | <span data-ttu-id="2bbed-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bbed-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="2bbed-159">**\_impostazione predefinita della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2bbed-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="2bbed-160">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bbed-160">Required.</span></span>            | <span data-ttu-id="2bbed-161">Contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="2bbed-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2bbed-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bbed-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bbed-163">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="2bbed-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



