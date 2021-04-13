---
description: Specifica se il DSP di acquisizione vocale usa la modalità di origine o filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Proprietà MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226544"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="3f277-103">\_ \_ \_ Proprietà modalità origine MFPKEY WMAAECMA DMO \_</span><span class="sxs-lookup"><span data-stu-id="3f277-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="3f277-104">Specifica se il DSP di acquisizione vocale usa la modalità di origine o filtro.</span><span class="sxs-lookup"><span data-stu-id="3f277-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3f277-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3f277-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3f277-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="3f277-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3f277-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3f277-107">Data Type</span></span>

<span data-ttu-id="3f277-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="3f277-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="3f277-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3f277-109">Default Value</span></span>

<span data-ttu-id="3f277-110">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="3f277-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="3f277-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3f277-111">Applies To</span></span>

-   [<span data-ttu-id="3f277-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="3f277-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="3f277-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f277-113">Remarks</span></span>

<span data-ttu-id="3f277-114">In modalità origine, l'applicazione non deve inviare dati di input al DSP, perché il DSP estrae automaticamente i dati dai dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="3f277-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="3f277-115">In modalità filtro, l'applicazione deve inviare i dati di input al DSP.</span><span class="sxs-lookup"><span data-stu-id="3f277-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="3f277-116">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f277-116">This property can have the following values.</span></span>



| <span data-ttu-id="3f277-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3f277-117">Value</span></span>          | <span data-ttu-id="3f277-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f277-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="3f277-119">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="3f277-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="3f277-120">Modalità filtro.</span><span class="sxs-lookup"><span data-stu-id="3f277-120">Filter mode.</span></span> |
| <span data-ttu-id="3f277-121">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="3f277-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="3f277-122">Modalità di origine.</span><span class="sxs-lookup"><span data-stu-id="3f277-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="3f277-123">Quando DMO è in modalità origine, è necessario chiamare [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il formato del flusso di output e non chiamare [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) per impostare i formati del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="3f277-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="3f277-124">In caso contrario, l'inizializzazione DMO non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="3f277-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="3f277-125">Se il valore di questa proprietà è VARIANT \_ true, il DSP ha zero input.</span><span class="sxs-lookup"><span data-stu-id="3f277-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="3f277-126">Se il valore è VARIANT \_ false, il DSP dispone di uno o due input, a seconda del valore della proprietà [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md) , come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3f277-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="3f277-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3f277-127">Value</span></span>                     | <span data-ttu-id="3f277-128">Numero di input</span><span class="sxs-lookup"><span data-stu-id="3f277-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="3f277-129">OPTIBEAM \_ array \_ e \_ AEC</span><span class="sxs-lookup"><span data-stu-id="3f277-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="3f277-130">2</span><span class="sxs-lookup"><span data-stu-id="3f277-130">2</span></span>                |
| <span data-ttu-id="3f277-131">\_solo matrice \_ OPTIBEAM</span><span class="sxs-lookup"><span data-stu-id="3f277-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="3f277-132">1</span><span class="sxs-lookup"><span data-stu-id="3f277-132">1</span></span>                |
| <span data-ttu-id="3f277-133">\_AEC canale \_ singolo</span><span class="sxs-lookup"><span data-stu-id="3f277-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="3f277-134">2</span><span class="sxs-lookup"><span data-stu-id="3f277-134">2</span></span>                |
| <span data-ttu-id="3f277-135">\_NSAGC a canale singolo \_</span><span class="sxs-lookup"><span data-stu-id="3f277-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="3f277-136">1</span><span class="sxs-lookup"><span data-stu-id="3f277-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="3f277-137">Solo le modalità con un singolo input funzioneranno con il filtro del wrapper DMO dall'API DirectShow 9,0.</span><span class="sxs-lookup"><span data-stu-id="3f277-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f277-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f277-138">Requirements</span></span>



| <span data-ttu-id="3f277-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f277-139">Requirement</span></span> | <span data-ttu-id="3f277-140">Valore</span><span class="sxs-lookup"><span data-stu-id="3f277-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f277-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f277-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3f277-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f277-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f277-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f277-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3f277-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f277-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f277-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f277-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f277-146"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f277-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f277-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f277-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f277-148">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f277-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3f277-149">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="3f277-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
