---
description: Specifica se l'acquisizione vocale DSP esegue il ritaglio al centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Proprietà MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226543"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="a3048-103">\_Proprietà clip MFPKEY WMAAECMA \_ featr \_ Center \_</span><span class="sxs-lookup"><span data-stu-id="a3048-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="a3048-104">Specifica se l'acquisizione vocale DSP esegue il ritaglio al centro.</span><span class="sxs-lookup"><span data-stu-id="a3048-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a3048-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a3048-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a3048-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a3048-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a3048-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a3048-107">Data Type</span></span>

<span data-ttu-id="a3048-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="a3048-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="a3048-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a3048-109">Default Value</span></span>

<span data-ttu-id="a3048-110">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="a3048-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="a3048-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="a3048-111">Applies To</span></span>

-   [<span data-ttu-id="a3048-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="a3048-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="a3048-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3048-113">Remarks</span></span>

<span data-ttu-id="a3048-114">Il ritaglio al centro è un processo che rimuove i residui di eco piccoli che rimangono dopo l'elaborazione AEC, in situazioni di sola conversazione (quando il discorso si verifica solo su un'estremità della riga).</span><span class="sxs-lookup"><span data-stu-id="a3048-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="a3048-115">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3048-115">This property can have the following values.</span></span>



| <span data-ttu-id="a3048-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a3048-116">Value</span></span>          | <span data-ttu-id="a3048-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3048-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="a3048-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="a3048-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="a3048-119">Disabilitare il ritaglio al centro.</span><span class="sxs-lookup"><span data-stu-id="a3048-119">Disable center clipping.</span></span> |
| <span data-ttu-id="a3048-120">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="a3048-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="a3048-121">Abilita ritaglio al centro.</span><span class="sxs-lookup"><span data-stu-id="a3048-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="a3048-122">Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="a3048-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="a3048-123">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="a3048-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="a3048-124">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.</span><span class="sxs-lookup"><span data-stu-id="a3048-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3048-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3048-125">Requirements</span></span>



| <span data-ttu-id="a3048-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3048-126">Requirement</span></span> | <span data-ttu-id="a3048-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a3048-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3048-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3048-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3048-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3048-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a3048-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3048-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3048-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3048-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3048-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3048-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3048-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3048-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3048-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3048-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3048-135">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3048-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a3048-136">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="a3048-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
