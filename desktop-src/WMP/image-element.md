---
title: Elemento Image (WMP SDK)
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento Image (WMP SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Finestra elemento immagine Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330893"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="299f4-105">Elemento Image (WMP SDK)</span><span class="sxs-lookup"><span data-stu-id="299f4-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="299f4-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="299f4-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="299f4-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="299f4-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="299f4-108">L'elemento **Image** specifica le immagini che Windows Media Player visualizza all'utente per rappresentare l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="299f4-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="299f4-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="299f4-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="299f4-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (obbligatorio per gli archivi di tipo 1, ignorato per il tipo 2)</span><span class="sxs-lookup"><span data-stu-id="299f4-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="299f4-111">URL del logo visualizzato da Windows Media Player nella finestra di dialogo contratto di licenza con l'utente finale (EULA).</span><span class="sxs-lookup"><span data-stu-id="299f4-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="299f4-112">Deve essere un'immagine PNG di 80 x 80 pixel.</span><span class="sxs-lookup"><span data-stu-id="299f4-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="299f4-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="299f4-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="299f4-114">URL dell'immagine visualizzata da Windows Media Player nel menu servizi.</span><span class="sxs-lookup"><span data-stu-id="299f4-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="299f4-115">Questa immagine deve essere di 15 x 15 pixel.</span><span class="sxs-lookup"><span data-stu-id="299f4-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="299f4-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="299f4-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="299f4-117">Per un archivio online di tipo 1, questo è l'URL dell'immagine visualizzata da Windows Media Player nella scheda **Store online** . Per Windows Media Player 11, questa immagine deve essere di 45 pixel di larghezza per 13 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="299f4-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="299f4-118">Per Windows Media Player 12, questa immagine deve essere di 45 pixel di larghezza per 30 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="299f4-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="299f4-119">Per supportare entrambe le versioni 11 e 12 di Windows Media Player, è necessario fornire due documenti ServiceInfo.xml distinti, ognuno dei quali fa riferimento all'immagine di dimensioni appropriate per ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="299f4-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="299f4-120">Per un archivio di tipo 2 online, questo è l'URL dell'immagine visualizzata da Windows Media Player accanto alla scheda **Store online** o accanto ai pulsanti del riquadro attività.</span><span class="sxs-lookup"><span data-stu-id="299f4-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="299f4-121">Questa immagine deve essere di 30 x 30 pixel.</span><span class="sxs-lookup"><span data-stu-id="299f4-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="299f4-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="299f4-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="299f4-123">URL per il logo visualizzato insieme alla descrizione di marketing specificata nell'elemento **Description** .</span><span class="sxs-lookup"><span data-stu-id="299f4-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="299f4-124">Se non viene specificato, sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="299f4-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="299f4-125">(Tutti i tipi, facoltativo) Deve essere un'immagine PNG di 45 pixel di larghezza e 13 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="299f4-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="299f4-126">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="299f4-126">Parent/Child Elements</span></span>



| <span data-ttu-id="299f4-127">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="299f4-127">Hierarchy</span></span>       | <span data-ttu-id="299f4-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="299f4-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="299f4-129">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="299f4-129">Parent elements</span></span> | <span data-ttu-id="299f4-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="299f4-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="299f4-131">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="299f4-131">Child elements</span></span>  | <span data-ttu-id="299f4-132">nessuno</span><span class="sxs-lookup"><span data-stu-id="299f4-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="299f4-133">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="299f4-133">Remarks</span></span>

<span data-ttu-id="299f4-134">I formati di immagine supportati sono. gif,. jpg,. bmp e. png (il formato consigliato).</span><span class="sxs-lookup"><span data-stu-id="299f4-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="299f4-135">L'uso della trasparenza web è supportato e consigliato.</span><span class="sxs-lookup"><span data-stu-id="299f4-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="299f4-136">I file GIF animati non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="299f4-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="299f4-137">Se non si specifica un valore per **MenuURL**, Windows Media Player non visualizza alcun grafico nel menu per il negozio online.</span><span class="sxs-lookup"><span data-stu-id="299f4-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="299f4-138">È possibile specificare un'immagine animata per ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="299f4-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="299f4-139">In Windows Media Player 10 o 11, l'immagine viene animata.</span><span class="sxs-lookup"><span data-stu-id="299f4-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="299f4-140">In Windows Media Player 12, viene visualizzato solo il primo frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="299f4-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="299f4-141">Per fornire un'immagine animata, creare un singolo file di immagine che contiene i frame successivi dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="299f4-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="299f4-142">Ad esempio, per un'immagine con una larghezza di 30 pixel e 30 pixel di altezza, è possibile fornire 20 immagini successive affiancate in un'immagine di 600 pixel di larghezza e 30 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="299f4-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="299f4-143">Windows Media Player eseguirà automaticamente l'animazione di tale immagine mostrando 20 immagini singole una dopo l'altra.</span><span class="sxs-lookup"><span data-stu-id="299f4-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="299f4-144">Questa animazione viene eseguita una sola volta quando si apre l'archivio online; non si ripete.</span><span class="sxs-lookup"><span data-stu-id="299f4-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="299f4-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="299f4-145">Requirements</span></span>



| <span data-ttu-id="299f4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="299f4-146">Requirement</span></span> | <span data-ttu-id="299f4-147">Valore</span><span class="sxs-lookup"><span data-stu-id="299f4-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="299f4-148">Versione</span><span class="sxs-lookup"><span data-stu-id="299f4-148">Version</span></span><br/> | <span data-ttu-id="299f4-149">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="299f4-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="299f4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="299f4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299f4-151">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="299f4-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="299f4-152">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="299f4-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="299f4-153">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="299f4-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





