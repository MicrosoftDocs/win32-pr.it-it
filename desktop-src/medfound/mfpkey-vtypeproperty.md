---
description: Specifica la logica che il codec userà per rilevare il video di origine interlacciato.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Proprietà MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880085"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="0937e-103">\_Proprietà VTYPE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0937e-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="0937e-104">Specifica la logica che il codec userà per rilevare il video di origine interlacciato.</span><span class="sxs-lookup"><span data-stu-id="0937e-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0937e-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0937e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0937e-106">g \_ wszWMVCVType</span><span class="sxs-lookup"><span data-stu-id="0937e-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="0937e-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0937e-107">Data Type</span></span>

<span data-ttu-id="0937e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0937e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0937e-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0937e-109">Default Value</span></span>

<span data-ttu-id="0937e-110">0</span><span class="sxs-lookup"><span data-stu-id="0937e-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0937e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0937e-111">Remarks</span></span>

<span data-ttu-id="0937e-112">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0937e-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="0937e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0937e-113">Value</span></span> | <span data-ttu-id="0937e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0937e-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0937e-115">0</span><span class="sxs-lookup"><span data-stu-id="0937e-115">0</span></span>     | <span data-ttu-id="0937e-116">Il codec userà la logica di rilevamento dei tipi di frame standard.</span><span class="sxs-lookup"><span data-stu-id="0937e-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="0937e-117">1</span><span class="sxs-lookup"><span data-stu-id="0937e-117">1</span></span>     | <span data-ttu-id="0937e-118">Il codec considererà tutti i fotogrammi video di origine come frame interlacciati.</span><span class="sxs-lookup"><span data-stu-id="0937e-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="0937e-119">2</span><span class="sxs-lookup"><span data-stu-id="0937e-119">2</span></span>     | <span data-ttu-id="0937e-120">Il codec considererà tutti i frame video di origine come campi di video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="0937e-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="0937e-121">3</span><span class="sxs-lookup"><span data-stu-id="0937e-121">3</span></span>     | <span data-ttu-id="0937e-122">Il codec determina automaticamente se i fotogrammi video di input sono frame o campi interlacciati di video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="0937e-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="0937e-123">4</span><span class="sxs-lookup"><span data-stu-id="0937e-123">4</span></span>     | <span data-ttu-id="0937e-124">Il codec determina automaticamente se i fotogrammi video di input sono frame progressivi, frame interlacciati o campi di video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="0937e-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="0937e-125">Questa proprietà determina il metodo di codifica immagine usato per la codifica video progressiva o interlacciata.</span><span class="sxs-lookup"><span data-stu-id="0937e-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="0937e-126">Se non viene specificato alcun tipo di video, il codec userà la codifica del frame progressiva per le sessioni di codifica progressiva e la codifica interlacciata del campo per le sessioni di codifica interlacciate.</span><span class="sxs-lookup"><span data-stu-id="0937e-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="0937e-127">Il tipo di sessione di codifica video (progressivo o interlacciato) viene impostato tramite la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0937e-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="0937e-128">La [proprietà \_ INTERLACEDCODINGENABLED di MFPKEY](mfpkey-interlacedcodingenabledproperty.md) deve essere impostata su Variant \_ true per produrre output interlacciato. in caso contrario, l'impostazione della proprietà VTYPE di MPFKEY non avrà \_ alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0937e-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="0937e-129">Quando si codifica il video interlacciato, è possibile specificare diversi metodi di codifica dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0937e-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="0937e-130">In genere, il modo più efficiente per codificare video interlacciato consiste nell'usare il metodo interlacciato del campo (2).</span><span class="sxs-lookup"><span data-stu-id="0937e-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="0937e-131">Se il video di origine contiene un movimento molto ridotto, il metodo interlacciato del frame (1) o il metodo di frame/campo automatico (2) potrebbe essere più appropriato.</span><span class="sxs-lookup"><span data-stu-id="0937e-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="0937e-132">Quando si codificano contenuti misti (contenenti frame progressivi e interlacciati), è preferibile usare il valore auto frame/Field/progressive Method (4).</span><span class="sxs-lookup"><span data-stu-id="0937e-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="0937e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0937e-133">Requirements</span></span>



| <span data-ttu-id="0937e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0937e-134">Requirement</span></span> | <span data-ttu-id="0937e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0937e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0937e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0937e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0937e-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0937e-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0937e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0937e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0937e-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0937e-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0937e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0937e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0937e-141"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0937e-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0937e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0937e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0937e-143">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0937e-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




