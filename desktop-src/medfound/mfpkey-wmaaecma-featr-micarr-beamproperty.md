---
description: Specifica il fascio utilizzato dal DSP di acquisizione vocale per l'elaborazione di matrici di microfoni.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Proprietà MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309131"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="94d58-103">MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ Beam proprietà</span><span class="sxs-lookup"><span data-stu-id="94d58-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="94d58-104">Specifica il fascio utilizzato dal DSP di acquisizione vocale per l'elaborazione di matrici di microfoni.</span><span class="sxs-lookup"><span data-stu-id="94d58-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="94d58-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="94d58-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="94d58-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="94d58-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="94d58-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="94d58-107">Data Type</span></span>

<span data-ttu-id="94d58-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="94d58-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="94d58-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="94d58-109">Applies To</span></span>

-   [<span data-ttu-id="94d58-110">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="94d58-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="94d58-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94d58-111">Remarks</span></span>

<span data-ttu-id="94d58-112">Impostare questa proprietà se il valore della proprietà [MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ extern \_ Beam.</span><span class="sxs-lookup"><span data-stu-id="94d58-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="94d58-113">Se il valore di [**MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ Single \_ Beam, è possibile leggere questa proprietà per eseguire una query su quale Beam è stato selezionato dal DSP.</span><span class="sxs-lookup"><span data-stu-id="94d58-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="94d58-114">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="94d58-114">This property can have the following values.</span></span> <span data-ttu-id="94d58-115">I valori sono in gradi orizzontali.</span><span class="sxs-lookup"><span data-stu-id="94d58-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="94d58-116">Valore</span><span class="sxs-lookup"><span data-stu-id="94d58-116">Value</span></span> | <span data-ttu-id="94d58-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94d58-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="94d58-118">0</span><span class="sxs-lookup"><span data-stu-id="94d58-118">0</span></span>     | <span data-ttu-id="94d58-119">-50 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-119">-50 degrees.</span></span>             |
| <span data-ttu-id="94d58-120">1</span><span class="sxs-lookup"><span data-stu-id="94d58-120">1</span></span>     | <span data-ttu-id="94d58-121">-40 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-121">-40 degrees.</span></span>             |
| <span data-ttu-id="94d58-122">2</span><span class="sxs-lookup"><span data-stu-id="94d58-122">2</span></span>     | <span data-ttu-id="94d58-123">-30 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-123">-30 degrees.</span></span>             |
| <span data-ttu-id="94d58-124">3</span><span class="sxs-lookup"><span data-stu-id="94d58-124">3</span></span>     | <span data-ttu-id="94d58-125">-20 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-125">-20 degrees.</span></span>             |
| <span data-ttu-id="94d58-126">4</span><span class="sxs-lookup"><span data-stu-id="94d58-126">4</span></span>     | <span data-ttu-id="94d58-127">-10 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-127">-10 degrees.</span></span>             |
| <span data-ttu-id="94d58-128">5</span><span class="sxs-lookup"><span data-stu-id="94d58-128">5</span></span>     | <span data-ttu-id="94d58-129">0 gradi (raggio centrale).</span><span class="sxs-lookup"><span data-stu-id="94d58-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="94d58-130">6</span><span class="sxs-lookup"><span data-stu-id="94d58-130">6</span></span>     | <span data-ttu-id="94d58-131">10 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-131">10 degrees.</span></span>              |
| <span data-ttu-id="94d58-132">7</span><span class="sxs-lookup"><span data-stu-id="94d58-132">7</span></span>     | <span data-ttu-id="94d58-133">20 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-133">20 degrees.</span></span>              |
| <span data-ttu-id="94d58-134">8</span><span class="sxs-lookup"><span data-stu-id="94d58-134">8</span></span>     | <span data-ttu-id="94d58-135">30 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-135">30 degrees.</span></span>              |
| <span data-ttu-id="94d58-136">9</span><span class="sxs-lookup"><span data-stu-id="94d58-136">9</span></span>     | <span data-ttu-id="94d58-137">40 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-137">40 degrees.</span></span>              |
| <span data-ttu-id="94d58-138">10</span><span class="sxs-lookup"><span data-stu-id="94d58-138">10</span></span>    | <span data-ttu-id="94d58-139">50 gradi.</span><span class="sxs-lookup"><span data-stu-id="94d58-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="94d58-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94d58-140">Requirements</span></span>



| <span data-ttu-id="94d58-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d58-141">Requirement</span></span> | <span data-ttu-id="94d58-142">Valore</span><span class="sxs-lookup"><span data-stu-id="94d58-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d58-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d58-143">Minimum supported client</span></span><br/> | <span data-ttu-id="94d58-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94d58-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="94d58-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d58-145">Minimum supported server</span></span><br/> | <span data-ttu-id="94d58-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94d58-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94d58-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94d58-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d58-148"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d58-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d58-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94d58-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d58-150">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94d58-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="94d58-151">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="94d58-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
