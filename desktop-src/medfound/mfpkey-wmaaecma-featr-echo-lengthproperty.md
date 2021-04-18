---
description: Specifica la durata di ECHO che l'algoritmo AEC (Acoustic Echo Cancel) può gestire, in millisecondi.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Proprietà MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309133"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="392ce-103">\_ \_ \_ Proprietà lunghezza Echo MFPKEY WMAAECMA featr \_</span><span class="sxs-lookup"><span data-stu-id="392ce-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="392ce-104">Specifica la durata di ECHO che l'algoritmo AEC (Acoustic Echo Cancel) può gestire, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="392ce-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="392ce-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="392ce-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="392ce-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="392ce-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="392ce-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="392ce-107">Data Type</span></span>

<span data-ttu-id="392ce-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="392ce-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="392ce-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="392ce-109">Default Value</span></span>

<span data-ttu-id="392ce-110">256</span><span class="sxs-lookup"><span data-stu-id="392ce-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="392ce-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="392ce-111">Applies To</span></span>

-   [<span data-ttu-id="392ce-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="392ce-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="392ce-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="392ce-113">Remarks</span></span>

<span data-ttu-id="392ce-114">L'algoritmo AEC utilizza un filtro adattivo la cui lunghezza è determinata dalla durata dell'eco.</span><span class="sxs-lookup"><span data-stu-id="392ce-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="392ce-115">È consigliabile che le applicazioni usino uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="392ce-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="392ce-116">128</span><span class="sxs-lookup"><span data-stu-id="392ce-116">128</span></span>
-   <span data-ttu-id="392ce-117">256</span><span class="sxs-lookup"><span data-stu-id="392ce-117">256</span></span>
-   <span data-ttu-id="392ce-118">512</span><span class="sxs-lookup"><span data-stu-id="392ce-118">512</span></span>
-   <span data-ttu-id="392ce-119">1024</span><span class="sxs-lookup"><span data-stu-id="392ce-119">1024</span></span>

<span data-ttu-id="392ce-120">Il valore predefinito è 256 millisecondi, che è sufficiente per la maggior parte degli ambienti Office e Home.</span><span class="sxs-lookup"><span data-stu-id="392ce-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="392ce-121">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="392ce-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="392ce-122">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.</span><span class="sxs-lookup"><span data-stu-id="392ce-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="392ce-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="392ce-123">Requirements</span></span>



| <span data-ttu-id="392ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="392ce-124">Requirement</span></span> | <span data-ttu-id="392ce-125">Valore</span><span class="sxs-lookup"><span data-stu-id="392ce-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="392ce-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="392ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="392ce-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="392ce-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="392ce-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="392ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="392ce-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="392ce-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="392ce-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="392ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="392ce-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="392ce-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="392ce-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="392ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392ce-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="392ce-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="392ce-134">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="392ce-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
