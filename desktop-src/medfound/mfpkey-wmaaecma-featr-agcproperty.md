---
description: Specifica se il DSP di acquisizione vocale esegue il controllo di guadagno automatico.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Proprietà MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309135"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="0765a-103">\_Proprietà MFPKEY WMAAECMA \_ featr \_ AGC</span><span class="sxs-lookup"><span data-stu-id="0765a-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="0765a-104">Specifica se il DSP di acquisizione vocale esegue il controllo di guadagno automatico.</span><span class="sxs-lookup"><span data-stu-id="0765a-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0765a-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0765a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0765a-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="0765a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0765a-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0765a-107">Data Type</span></span>

<span data-ttu-id="0765a-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="0765a-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="0765a-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0765a-109">Default Value</span></span>

<span data-ttu-id="0765a-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="0765a-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="0765a-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="0765a-111">Applies To</span></span>

-   [<span data-ttu-id="0765a-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="0765a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="0765a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0765a-113">Remarks</span></span>

<span data-ttu-id="0765a-114">Il controllo del guadagno automatico è un componente DSP (Digital Signal Processing) che regola il guadagno in modo che il livello di output del segnale rimanga entro lo stesso intervallo approssimativo.</span><span class="sxs-lookup"><span data-stu-id="0765a-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="0765a-115">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0765a-115">This property can have the following values.</span></span>



| <span data-ttu-id="0765a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0765a-116">Value</span></span>          | <span data-ttu-id="0765a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0765a-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="0765a-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="0765a-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="0765a-119">Disabilitare il controllo di guadagno automatico.</span><span class="sxs-lookup"><span data-stu-id="0765a-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="0765a-120">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="0765a-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="0765a-121">Abilitare il controllo di guadagno automatico.</span><span class="sxs-lookup"><span data-stu-id="0765a-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="0765a-122">Il valore predefinito di questa proprietà è VARIANT \_ false (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="0765a-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="0765a-123">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="0765a-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0765a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0765a-124">Requirements</span></span>



| <span data-ttu-id="0765a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0765a-125">Requirement</span></span> | <span data-ttu-id="0765a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0765a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0765a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0765a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0765a-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0765a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0765a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0765a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0765a-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0765a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0765a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0765a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0765a-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0765a-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0765a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0765a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0765a-134">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0765a-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0765a-135">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="0765a-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
