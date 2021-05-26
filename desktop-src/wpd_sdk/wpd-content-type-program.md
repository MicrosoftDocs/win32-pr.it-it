---
description: PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423771"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="84069-103">PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="84069-104">Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE PROGRAM rappresenta un programma \_ \_ eseguibile.</span><span class="sxs-lookup"><span data-stu-id="84069-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="84069-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="84069-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="84069-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="84069-106">Property Name</span></span>     | <span data-ttu-id="84069-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="84069-107">Required or Optional</span></span>      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="84069-108">ID OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="84069-109">Obbligatorio, ma di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="84069-109">Required, but read-only.</span></span> <span data-ttu-id="84069-110">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="84069-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="84069-111">ID PADRE \_ DELL'OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="84069-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84069-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="84069-113">NOME OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="84069-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="84069-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="84069-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="84069-115">\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="84069-116">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="84069-116">Required, read-only.</span></span> <span data-ttu-id="84069-117">Un client non può impostare questa proprietà anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="84069-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="84069-118">FORMATO OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="84069-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84069-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="84069-120">TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="84069-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="84069-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84069-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="84069-122">\_ISHIDDEN DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="84069-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="84069-123">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="84069-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="84069-124">ISSYSTEM \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="84069-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="84069-125">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="84069-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="84069-126">DIMENSIONI DEGLI OGGETTI \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="84069-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="84069-127">Obbligatorio se l'oggetto ha almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="84069-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="84069-128">NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_</span><span class="sxs-lookup"><span data-stu-id="84069-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="84069-129">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="84069-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="84069-130">OGGETTO WPD \_ \_ NON \_ UTILIZZABILE</span><span class="sxs-lookup"><span data-stu-id="84069-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="84069-131">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84069-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="84069-132">RIFERIMENTI AGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="84069-133">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="84069-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="84069-134">PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="84069-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-136">ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="84069-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-138">L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="84069-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="84069-139">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="84069-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="84069-140">DATA CREAZIONE OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="84069-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-142">DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="84069-143">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="84069-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="84069-144">DATA CREAZIONE OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="84069-145">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-146">RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="84069-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="84069-147">Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="84069-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="84069-148">ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD</span><span class="sxs-lookup"><span data-stu-id="84069-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="84069-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-150">OGGETTO WPD \_ \_ CHE GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA</span><span class="sxs-lookup"><span data-stu-id="84069-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="84069-151">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="84069-152">L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO</span><span class="sxs-lookup"><span data-stu-id="84069-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="84069-153">Obbligatorio se l'oggetto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="84069-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="84069-154">IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_</span><span class="sxs-lookup"><span data-stu-id="84069-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="84069-155">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84069-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="84069-156">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="84069-156">Typical Resources</span></span>

<span data-ttu-id="84069-157">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="84069-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="84069-158">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="84069-158">Resource Name</span></span>                                          | <span data-ttu-id="84069-159">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="84069-159">Required or Optional</span></span> | <span data-ttu-id="84069-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84069-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="84069-161">**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84069-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="84069-162">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84069-162">Required.</span></span>            | <span data-ttu-id="84069-163">Contiene il file di programma.</span><span class="sxs-lookup"><span data-stu-id="84069-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="84069-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84069-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84069-165">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="84069-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



