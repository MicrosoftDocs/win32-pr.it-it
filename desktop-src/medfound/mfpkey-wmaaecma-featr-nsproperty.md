---
description: Specifica se il DSP di acquisizione vocale esegue l'eliminazione del rumore.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Proprietà MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309121"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="07a79-103">\_ \_ Proprietà NS MFPKEY WMAAECMA featr \_</span><span class="sxs-lookup"><span data-stu-id="07a79-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="07a79-104">Specifica se il DSP di acquisizione vocale esegue l'eliminazione del rumore.</span><span class="sxs-lookup"><span data-stu-id="07a79-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="07a79-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="07a79-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="07a79-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="07a79-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="07a79-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="07a79-107">Data Type</span></span>

<span data-ttu-id="07a79-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="07a79-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="07a79-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="07a79-109">Default Value</span></span>

<span data-ttu-id="07a79-110">1</span><span class="sxs-lookup"><span data-stu-id="07a79-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="07a79-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="07a79-111">Applies To</span></span>

-   [<span data-ttu-id="07a79-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="07a79-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="07a79-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="07a79-113">Remarks</span></span>

<span data-ttu-id="07a79-114">L'eliminazione del rumore è un componente DSP (Digital Signal Processing) che elimina o riduce i rumori di fondo fissi nel segnale audio.</span><span class="sxs-lookup"><span data-stu-id="07a79-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="07a79-115">L'eliminazione del rumore viene applicata dopo l'elaborazione di annullamenti acustici (AEC) e della matrice microfonica.</span><span class="sxs-lookup"><span data-stu-id="07a79-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="07a79-116">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="07a79-116">This property can have the following values.</span></span>



| <span data-ttu-id="07a79-117">Valore</span><span class="sxs-lookup"><span data-stu-id="07a79-117">Value</span></span> | <span data-ttu-id="07a79-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a79-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="07a79-119">0</span><span class="sxs-lookup"><span data-stu-id="07a79-119">0</span></span>     | <span data-ttu-id="07a79-120">Disabilitare l'eliminazione del rumore.</span><span class="sxs-lookup"><span data-stu-id="07a79-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="07a79-121">1</span><span class="sxs-lookup"><span data-stu-id="07a79-121">1</span></span>     | <span data-ttu-id="07a79-122">Abilitare l'eliminazione del rumore.</span><span class="sxs-lookup"><span data-stu-id="07a79-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="07a79-123">Il valore predefinito di questa proprietà è 1 (abilitato).</span><span class="sxs-lookup"><span data-stu-id="07a79-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="07a79-124">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="07a79-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a79-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07a79-125">Requirements</span></span>



| <span data-ttu-id="07a79-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a79-126">Requirement</span></span> | <span data-ttu-id="07a79-127">Valore</span><span class="sxs-lookup"><span data-stu-id="07a79-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a79-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a79-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07a79-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07a79-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="07a79-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a79-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07a79-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07a79-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07a79-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07a79-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a79-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a79-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a79-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07a79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a79-135">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07a79-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="07a79-136">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="07a79-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
