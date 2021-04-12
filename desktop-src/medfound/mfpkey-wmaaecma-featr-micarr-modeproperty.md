---
description: Specifica il modo in cui il DSP di acquisizione vocale esegue l'elaborazione della matrice microfonica.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Proprietà MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226541"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="48429-103">\_Proprietà Mode MFPKEY WMAAECMA \_ featr \_ MICARR \_</span><span class="sxs-lookup"><span data-stu-id="48429-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="48429-104">Specifica il modo in cui il DSP di acquisizione vocale esegue l'elaborazione della matrice microfonica.</span><span class="sxs-lookup"><span data-stu-id="48429-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="48429-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="48429-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="48429-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="48429-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="48429-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="48429-107">Data Type</span></span>

<span data-ttu-id="48429-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="48429-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="48429-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="48429-109">Default Value</span></span>

<span data-ttu-id="48429-110">MICARRAY \_ a \_ fascio singolo</span><span class="sxs-lookup"><span data-stu-id="48429-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="48429-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="48429-111">Applies To</span></span>

-   [<span data-ttu-id="48429-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="48429-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="48429-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="48429-113">Remarks</span></span>

<span data-ttu-id="48429-114">Il valore di questa proprietà è un membro dell'enumerazione [della \_ \_ modalità matrice MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) .</span><span class="sxs-lookup"><span data-stu-id="48429-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="48429-115">Il valore predefinito è MICARRAY \_ Single \_ Beam.</span><span class="sxs-lookup"><span data-stu-id="48429-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="48429-116">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="48429-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="48429-117">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione della matrice microfonica.</span><span class="sxs-lookup"><span data-stu-id="48429-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="48429-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48429-118">Requirements</span></span>



| <span data-ttu-id="48429-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48429-119">Requirement</span></span> | <span data-ttu-id="48429-120">Valore</span><span class="sxs-lookup"><span data-stu-id="48429-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48429-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48429-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48429-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48429-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="48429-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48429-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48429-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48429-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48429-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48429-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="48429-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48429-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48429-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48429-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48429-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48429-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="48429-129">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="48429-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
