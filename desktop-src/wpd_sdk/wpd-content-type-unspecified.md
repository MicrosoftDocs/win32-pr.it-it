---
description: TIPO DI \_ CONTENUTO WPD NON \_ \_ SPECIFICATO
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423681"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="c9246-103">TIPO DI \_ CONTENUTO WPD NON \_ \_ SPECIFICATO</span><span class="sxs-lookup"><span data-stu-id="c9246-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="c9246-104">Un oggetto che descrive il tipo come WPD \_ CONTENT \_ TYPE UNSPECIFIED rappresenta un oggetto generico che può avere o meno \_ un file fisico sottostante.</span><span class="sxs-lookup"><span data-stu-id="c9246-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="c9246-105">La differenza tra questo tipo e WPD CONTENT TYPE GENERIC FILE è che gli oggetti \_ \_ \_ \_ WPD \_ CONTENT TYPE GENERIC FILE devono avere un file fisico \_ \_ \_ sottostante.</span><span class="sxs-lookup"><span data-stu-id="c9246-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="c9246-106">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9246-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="c9246-107">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="c9246-107">Property Name</span></span>       | <span data-ttu-id="c9246-108">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="c9246-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="c9246-109">ID OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="c9246-110">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c9246-110">Required, read-only.</span></span> <span data-ttu-id="c9246-111">Un client non può impostare questa proprietà anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="c9246-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="c9246-112">ID PADRE \_ DELL'OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="c9246-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9246-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="c9246-114">NOME OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="c9246-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="c9246-115">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="c9246-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="c9246-116">\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="c9246-117">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c9246-117">Required, read-only.</span></span> <span data-ttu-id="c9246-118">Un client non può impostare questa proprietà anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="c9246-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="c9246-119">FORMATO OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="c9246-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="c9246-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9246-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="c9246-121">TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="c9246-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9246-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="c9246-123">OGGETTO WPD \_ \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="c9246-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="c9246-124">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="c9246-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="c9246-125">ISSYSTEM \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="c9246-126">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="c9246-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="c9246-127">DIMENSIONI \_ DELL'OGGETTO WPD \_</span><span class="sxs-lookup"><span data-stu-id="c9246-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="c9246-128">Obbligatorio se l'oggetto dispone di almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9246-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="c9246-129">NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="c9246-130">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="c9246-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="c9246-131">OGGETTO WPD \_ \_ NON \_ CONSUMABILE</span><span class="sxs-lookup"><span data-stu-id="c9246-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="c9246-132">Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9246-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="c9246-133">RIFERIMENTI AGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="c9246-134">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="c9246-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="c9246-135">PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="c9246-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-137">ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="c9246-138">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-139">L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="c9246-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="c9246-140">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="c9246-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="c9246-141">DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="c9246-142">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-143">DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="c9246-144">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="c9246-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="c9246-145">DATA DELL'OGGETTO WPD \_ \_ \_ CREATO</span><span class="sxs-lookup"><span data-stu-id="c9246-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="c9246-146">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-147">RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c9246-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="c9246-148">Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="c9246-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="c9246-149">ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="c9246-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-151">OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA</span><span class="sxs-lookup"><span data-stu-id="c9246-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="c9246-152">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="c9246-153">L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO</span><span class="sxs-lookup"><span data-stu-id="c9246-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="c9246-154">Obbligatorio se l'oggetto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="c9246-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="c9246-155">IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c9246-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="c9246-156">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9246-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="c9246-157">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="c9246-157">Typical Resources</span></span>

<span data-ttu-id="c9246-158">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9246-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="c9246-159">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="c9246-159">Resource Name</span></span>                                          | <span data-ttu-id="c9246-160">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="c9246-160">Required or Optional</span></span>                             | <span data-ttu-id="c9246-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9246-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="c9246-162">**RISORSA WPD \_ \_ PREDEFINITA**</span><span class="sxs-lookup"><span data-stu-id="c9246-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="c9246-163">Obbligatorio se l'oggetto è supportato da dati binari.</span><span class="sxs-lookup"><span data-stu-id="c9246-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="c9246-164">Contiene i dati binari.</span><span class="sxs-lookup"><span data-stu-id="c9246-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9246-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9246-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9246-166">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="c9246-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



