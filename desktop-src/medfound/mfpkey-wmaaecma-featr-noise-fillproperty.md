---
description: Specifica se l'acquisizione vocale DSP esegue il riempimento del rumore.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Proprietà MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309122"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="54c44-103">\_ \_ \_ Proprietà riempimento rumore MFPKEY WMAAECMA featr \_</span><span class="sxs-lookup"><span data-stu-id="54c44-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="54c44-104">Specifica se l'acquisizione vocale DSP esegue il riempimento del rumore.</span><span class="sxs-lookup"><span data-stu-id="54c44-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="54c44-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="54c44-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="54c44-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="54c44-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="54c44-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="54c44-107">Data Type</span></span>

<span data-ttu-id="54c44-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="54c44-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="54c44-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="54c44-109">Default Value</span></span>

<span data-ttu-id="54c44-110">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="54c44-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="54c44-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="54c44-111">Applies To</span></span>

-   [<span data-ttu-id="54c44-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="54c44-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="54c44-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="54c44-113">Remarks</span></span>

<span data-ttu-id="54c44-114">Il riempimento del rumore aggiunge una piccola quantità di rumore alle parti del segnale in cui il ritaglio al centro ha rimosso gli echi residui.</span><span class="sxs-lookup"><span data-stu-id="54c44-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="54c44-115">In questo modo si ottiene un'esperienza migliore per l'utente rispetto alla mancata presenza di gap nel segnale.</span><span class="sxs-lookup"><span data-stu-id="54c44-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="54c44-116">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="54c44-116">This property can have the following values.</span></span>



| <span data-ttu-id="54c44-117">Valore</span><span class="sxs-lookup"><span data-stu-id="54c44-117">Value</span></span>          | <span data-ttu-id="54c44-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54c44-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="54c44-119">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="54c44-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="54c44-120">Abilita riempimento rumore.</span><span class="sxs-lookup"><span data-stu-id="54c44-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="54c44-121">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="54c44-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="54c44-122">Disabilitare il riempimento del rumore.</span><span class="sxs-lookup"><span data-stu-id="54c44-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="54c44-123">Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="54c44-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="54c44-124">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="54c44-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="54c44-125">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.</span><span class="sxs-lookup"><span data-stu-id="54c44-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c44-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54c44-126">Requirements</span></span>



| <span data-ttu-id="54c44-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="54c44-127">Requirement</span></span> | <span data-ttu-id="54c44-128">Valore</span><span class="sxs-lookup"><span data-stu-id="54c44-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54c44-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c44-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54c44-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54c44-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54c44-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c44-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54c44-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54c44-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54c44-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54c44-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c44-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54c44-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c44-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54c44-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c44-136">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54c44-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="54c44-137">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="54c44-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
