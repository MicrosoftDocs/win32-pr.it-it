---
description: PROFILO WIRELESS \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423701"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="f1d91-103">PROFILO WIRELESS \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="f1d91-104">Un oggetto che ne descrive il tipo come WPD CONTENT TYPE WIRELESS PROFILE rappresenta le \_ informazioni usate per accedere a una rete \_ \_ \_ wireless.</span><span class="sxs-lookup"><span data-stu-id="f1d91-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="f1d91-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1d91-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="f1d91-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="f1d91-106">Property Name</span></span>             | <span data-ttu-id="f1d91-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="f1d91-107">Required or Optional</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f1d91-108">ID OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="f1d91-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1d91-109">Required.</span></span>                                                             |
| [<span data-ttu-id="f1d91-110">ID PADRE \_ DELL'OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="f1d91-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1d91-111">Required.</span></span>                                                             |
| [<span data-ttu-id="f1d91-112">NOME OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="f1d91-113">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="f1d91-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="f1d91-114">\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="f1d91-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1d91-115">Required.</span></span>                                                             |
| [<span data-ttu-id="f1d91-116">FORMATO \_ DELL'OGGETTO WPD \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="f1d91-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1d91-117">Required.</span></span>                                                             |
| [<span data-ttu-id="f1d91-118">TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="f1d91-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1d91-119">Required.</span></span>                                                             |
| [<span data-ttu-id="f1d91-120">\_ISHIDDEN DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="f1d91-121">Obbligatorio se l'oggetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="f1d91-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="f1d91-122">ISSYSTEM \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="f1d91-123">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="f1d91-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="f1d91-124">DIMENSIONI \_ DELL'OGGETTO WPD \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="f1d91-125">Obbligatorio se l'oggetto dispone di almeno una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f1d91-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="f1d91-126">NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="f1d91-127">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="f1d91-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="f1d91-128">OGGETTO WPD \_ \_ NON \_ UTILIZZABILE</span><span class="sxs-lookup"><span data-stu-id="f1d91-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="f1d91-129">Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="f1d91-130">RIFERIMENTI AGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="f1d91-131">Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="f1d91-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="f1d91-132">PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="f1d91-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-134">ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="f1d91-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-136">L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="f1d91-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="f1d91-137">Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="f1d91-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="f1d91-138">DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="f1d91-139">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-140">DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="f1d91-141">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="f1d91-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="f1d91-142">DATA DI \_ CREAZIONE \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="f1d91-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-144">RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d91-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="f1d91-145">Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1d91-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="f1d91-146">ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="f1d91-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-148">OGGETTO WPD \_ \_ CHE GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA</span><span class="sxs-lookup"><span data-stu-id="f1d91-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="f1d91-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="f1d91-150">L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO</span><span class="sxs-lookup"><span data-stu-id="f1d91-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="f1d91-151">Obbligatorio se l'oggetto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="f1d91-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="f1d91-152">IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD</span><span class="sxs-lookup"><span data-stu-id="f1d91-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="f1d91-153">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1d91-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="f1d91-154">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="f1d91-154">Typical Resources</span></span>

<span data-ttu-id="f1d91-155">Questi oggetti includono in genere le risorse seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1d91-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="f1d91-156">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="f1d91-156">Resource Name</span></span>                                          | <span data-ttu-id="f1d91-157">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="f1d91-157">Required or Optional</span></span>                                  | <span data-ttu-id="f1d91-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1d91-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="f1d91-159">**IMPOSTAZIONE PREDEFINITA \_ DELLA RISORSA WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f1d91-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="f1d91-160">Obbligatorio se l'oggetto è rappresentato da dati binari.</span><span class="sxs-lookup"><span data-stu-id="f1d91-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="f1d91-161">Contiene i dati binari.</span><span class="sxs-lookup"><span data-stu-id="f1d91-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f1d91-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1d91-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d91-163">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="f1d91-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



