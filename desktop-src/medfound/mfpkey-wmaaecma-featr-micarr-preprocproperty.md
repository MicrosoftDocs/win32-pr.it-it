---
description: Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione della matrice di microfoni.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Proprietà MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309126"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="58ed5-103">\_ \_ \_ Proprietà Preproc di MFPKEY WMAAECMA featr MICARR \_</span><span class="sxs-lookup"><span data-stu-id="58ed5-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="58ed5-104">Specifica se il DSP di acquisizione vocale esegue la pre-elaborazione della matrice di microfoni.</span><span class="sxs-lookup"><span data-stu-id="58ed5-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="58ed5-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="58ed5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="58ed5-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="58ed5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="58ed5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="58ed5-107">Data Type</span></span>

<span data-ttu-id="58ed5-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="58ed5-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="58ed5-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="58ed5-109">Default Value</span></span>

<span data-ttu-id="58ed5-110">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="58ed5-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="58ed5-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="58ed5-111">Applies To</span></span>

-   [<span data-ttu-id="58ed5-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="58ed5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="58ed5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58ed5-113">Remarks</span></span>

<span data-ttu-id="58ed5-114">La pre-elaborazione può rimuovere i toni stazionari che interferiscono con l'elaborazione, ad esempio un tono con un passo fisso.</span><span class="sxs-lookup"><span data-stu-id="58ed5-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="58ed5-115">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="58ed5-115">This property can have the following values.</span></span>



| <span data-ttu-id="58ed5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="58ed5-116">Value</span></span>          | <span data-ttu-id="58ed5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58ed5-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="58ed5-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="58ed5-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="58ed5-119">Disabilitare la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="58ed5-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="58ed5-120">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="58ed5-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="58ed5-121">Abilitare la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="58ed5-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="58ed5-122">Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="58ed5-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="58ed5-123">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="58ed5-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="58ed5-124">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione della matrice microfonica.</span><span class="sxs-lookup"><span data-stu-id="58ed5-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ed5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ed5-125">Requirements</span></span>



| <span data-ttu-id="58ed5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ed5-126">Requirement</span></span> | <span data-ttu-id="58ed5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="58ed5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ed5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ed5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="58ed5-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58ed5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58ed5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ed5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="58ed5-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58ed5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58ed5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ed5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ed5-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ed5-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ed5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ed5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ed5-135">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58ed5-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="58ed5-136">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="58ed5-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
