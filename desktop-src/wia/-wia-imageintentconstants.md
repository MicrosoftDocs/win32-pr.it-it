---
description: Le costanti per finalità di immagine specificano il tipo di dati che l'immagine deve rappresentare.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Costanti per finalità di immagine (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966843"
---
# <a name="image-intent-constants"></a><span data-ttu-id="f42f2-103">Costanti per finalità di immagine</span><span class="sxs-lookup"><span data-stu-id="f42f2-103">Image Intent Constants</span></span>

<span data-ttu-id="f42f2-104">Le costanti per finalità di immagine specificano il tipo di dati che l'immagine deve rappresentare.</span><span class="sxs-lookup"><span data-stu-id="f42f2-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="f42f2-105">La proprietà [**WIA \_ IPS \_ cur \_ Intent**](-wia-wiaitempropscanneritem.md) scanner utilizza questi flag.</span><span class="sxs-lookup"><span data-stu-id="f42f2-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="f42f2-106">Per fornire uno scopo, combinare un flag di tipo di immagine previsto con un flag di dimensioni/qualità previsto usando l'operatore OR.</span><span class="sxs-lookup"><span data-stu-id="f42f2-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="f42f2-107">\_La finalità WIA \_ None non deve essere combinata con altri flag.</span><span class="sxs-lookup"><span data-stu-id="f42f2-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="f42f2-108">Si noti che un'immagine non può essere sia di scala di grigi che di colore.</span><span class="sxs-lookup"><span data-stu-id="f42f2-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="f42f2-109">Di seguito sono riportate costanti per finalità di immagine valide:</span><span class="sxs-lookup"><span data-stu-id="f42f2-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="f42f2-110">Flag del tipo di immagine previsto</span><span class="sxs-lookup"><span data-stu-id="f42f2-110">Intended image type flags</span></span>           | <span data-ttu-id="f42f2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f42f2-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="f42f2-112">\_nessuna finalità \_ WIA</span><span class="sxs-lookup"><span data-stu-id="f42f2-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="f42f2-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f42f2-113">Default value.</span></span> <span data-ttu-id="f42f2-114">Non impostare alcuna proprietà.</span><span class="sxs-lookup"><span data-stu-id="f42f2-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="f42f2-115">\_colore del \_ tipo di immagine preventivo \_ per WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="f42f2-116">Proprietà predefinite per il contenuto del colore.</span><span class="sxs-lookup"><span data-stu-id="f42f2-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="f42f2-117">\_tipo di \_ immagine per finalità \_ WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="f42f2-118">Proprietà predefinite per il contenuto in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="f42f2-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="f42f2-119">\_ \_ testo tipo di immagine finalità \_ WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="f42f2-120">Proprietà predefinite per il contenuto di testo.</span><span class="sxs-lookup"><span data-stu-id="f42f2-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="f42f2-121">\_maschera del \_ tipo di immagine preventivo \_ WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="f42f2-122">Maschera per tutti i flag del tipo di immagine.</span><span class="sxs-lookup"><span data-stu-id="f42f2-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="f42f2-123">Flag di qualità/dimensioni immagine previsti</span><span class="sxs-lookup"><span data-stu-id="f42f2-123">Intended image size/quality flags</span></span> | <span data-ttu-id="f42f2-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f42f2-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="f42f2-125">\_ \_ dimensioni minime della finalità WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="f42f2-126">Proprietà predefinite per ridurre al minimo le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f42f2-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="f42f2-127">\_finalità WIA \_ massimizza la \_ qualità</span><span class="sxs-lookup"><span data-stu-id="f42f2-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="f42f2-128">Proprietà predefinite per ottimizzare la qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f42f2-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="f42f2-129">\_ \_ maschera dimensioni finalità \_ WIA</span><span class="sxs-lookup"><span data-stu-id="f42f2-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="f42f2-130">Maschera per tutti i flag di dimensione/qualità.</span><span class="sxs-lookup"><span data-stu-id="f42f2-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="f42f2-131">\_Anteprima finalità \_ WIA \_</span><span class="sxs-lookup"><span data-stu-id="f42f2-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="f42f2-132">Specifica l'anteprima della qualità migliore.</span><span class="sxs-lookup"><span data-stu-id="f42f2-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="f42f2-133">Nell'elenco seguente viene illustrato il nome della costante C/C++ seguito dal nome corrispondente tra parentesi utilizzate nello scripting.</span><span class="sxs-lookup"><span data-stu-id="f42f2-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="f42f2-134">I nomi di script sono dal tipo enumerato WiaIntent.</span><span class="sxs-lookup"><span data-stu-id="f42f2-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="f42f2-135">Si noti che non tutte le costanti sono disponibili tramite script.</span><span class="sxs-lookup"><span data-stu-id="f42f2-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="f42f2-136">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="f42f2-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="f42f2-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f42f2-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="f42f2-138"><dt>**WIA \_ Tipo di immagine Intent \_ \_ \_ color**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="f42f2-139">Proprietà predefinite per il contenuto del colore.</span><span class="sxs-lookup"><span data-stu-id="f42f2-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="f42f2-140"><dt>**WIA \_ Tipo di immagine Intent in \_ \_ scala di \_ grigi**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="f42f2-141">Proprietà predefinite per il contenuto in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="f42f2-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="f42f2-142"><dt>**WIA \_ Tipo di immagine preventivo 0x00000004 \_ \_ \_ testo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="f42f2-143">Proprietà predefinite per il contenuto di testo.</span><span class="sxs-lookup"><span data-stu-id="f42f2-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="f42f2-144"><dt>**WIA \_ \_ \_ Dimensioni minime Intent**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="f42f2-145">Proprietà predefinite per ridurre al minimo le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f42f2-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="f42f2-146"><dt>**WIA \_ Intent \_ massimizza la \_ qualità**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="f42f2-147">Proprietà predefinite per ottimizzare la qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f42f2-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="f42f2-148"><dt>**WIA \_ Intent \_ Best \_ Preview**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="f42f2-149">Specifica l'anteprima della qualità migliore.</span><span class="sxs-lookup"><span data-stu-id="f42f2-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="f42f2-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f42f2-150">Requirements</span></span>



| <span data-ttu-id="f42f2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f42f2-151">Requirement</span></span> | <span data-ttu-id="f42f2-152">Valore</span><span class="sxs-lookup"><span data-stu-id="f42f2-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f42f2-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42f2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f42f2-154">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f42f2-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f42f2-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42f2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f42f2-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f42f2-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f42f2-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f42f2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42f2-158"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42f2-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




