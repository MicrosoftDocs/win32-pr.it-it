---
description: Specifica la dimensione del frame audio utilizzata dal DSP di acquisizione voce.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Proprietà MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309132"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="b18c5-103">\_ \_ \_ Proprietà dimensioni frame feat MFPKEY \_ WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="b18c5-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="b18c5-104">Specifica la dimensione del frame audio utilizzata dal DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="b18c5-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b18c5-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b18c5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b18c5-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b18c5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b18c5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b18c5-107">Data Type</span></span>

<span data-ttu-id="b18c5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b18c5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b18c5-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b18c5-109">Default Value</span></span>

<span data-ttu-id="b18c5-110">0</span><span class="sxs-lookup"><span data-stu-id="b18c5-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="b18c5-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b18c5-111">Applies To</span></span>

-   [<span data-ttu-id="b18c5-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="b18c5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="b18c5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b18c5-113">Remarks</span></span>

<span data-ttu-id="b18c5-114">L'algoritmo Acoustic Echo Cancel (AEC) elabora i campioni audio PCM un frame alla volta.</span><span class="sxs-lookup"><span data-stu-id="b18c5-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="b18c5-115">Il valore di questa proprietà corrisponde alla dimensione del frame audio, in esempi.</span><span class="sxs-lookup"><span data-stu-id="b18c5-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="b18c5-116">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="b18c5-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="b18c5-117">Il DSP di acquisizione vocale supporta le seguenti dimensioni dei frame:</span><span class="sxs-lookup"><span data-stu-id="b18c5-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="b18c5-118">80</span><span class="sxs-lookup"><span data-stu-id="b18c5-118">80</span></span>
-   <span data-ttu-id="b18c5-119">128</span><span class="sxs-lookup"><span data-stu-id="b18c5-119">128</span></span>
-   <span data-ttu-id="b18c5-120">160</span><span class="sxs-lookup"><span data-stu-id="b18c5-120">160</span></span>
-   <span data-ttu-id="b18c5-121">240</span><span class="sxs-lookup"><span data-stu-id="b18c5-121">240</span></span>
-   <span data-ttu-id="b18c5-122">256</span><span class="sxs-lookup"><span data-stu-id="b18c5-122">256</span></span>
-   <span data-ttu-id="b18c5-123">320</span><span class="sxs-lookup"><span data-stu-id="b18c5-123">320</span></span>

<span data-ttu-id="b18c5-124">Se il valore di questa proprietà è zero, il DSP seleziona le dimensioni del frame in base alla modalità di sistema e al formato di output.</span><span class="sxs-lookup"><span data-stu-id="b18c5-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="b18c5-125">Per prestazioni ottimali, tuttavia, è consigliabile usare il valore predefinito per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b18c5-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="b18c5-126">Se la modalità di elaborazione è solo una matrice di microfoni, il valore predefinito è 320 esempi.</span><span class="sxs-lookup"><span data-stu-id="b18c5-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="b18c5-127">Per tutte le altre modalità di elaborazione, il valore predefinito è 160 esempi.</span><span class="sxs-lookup"><span data-stu-id="b18c5-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="b18c5-128">Per altre informazioni sulle modalità di elaborazione del DSP di acquisizione vocale, vedere [ \_ modalità di \_ sistema \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b18c5-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="b18c5-129">Dopo la prima chiamata a [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), è possibile leggere questa proprietà per ottenere le dimensioni effettive del frame in uso, anche quando la [**\_ modalità della \_ funzionalità \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) è false.</span><span class="sxs-lookup"><span data-stu-id="b18c5-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b18c5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b18c5-130">Requirements</span></span>



| <span data-ttu-id="b18c5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18c5-131">Requirement</span></span> | <span data-ttu-id="b18c5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b18c5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b18c5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b18c5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b18c5-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b18c5-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b18c5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b18c5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b18c5-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b18c5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b18c5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b18c5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b18c5-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b18c5-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18c5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b18c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18c5-140">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b18c5-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b18c5-141">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="b18c5-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
