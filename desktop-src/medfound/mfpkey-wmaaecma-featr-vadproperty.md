---
description: Specifica il tipo di rilevamento dell'attività vocale eseguita dal DSP di acquisizione voce.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Proprietà MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309120"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="ee174-103">MFPKEY \_ WMAAECMA \_ featr \_ Proprietà VAD</span><span class="sxs-lookup"><span data-stu-id="ee174-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="ee174-104">Specifica il tipo di rilevamento dell'attività vocale eseguita dal DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="ee174-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ee174-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ee174-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ee174-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ee174-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ee174-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ee174-107">Data Type</span></span>

<span data-ttu-id="ee174-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ee174-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ee174-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ee174-109">Default Value</span></span>

<span data-ttu-id="ee174-110">0</span><span class="sxs-lookup"><span data-stu-id="ee174-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="ee174-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ee174-111">Applies To</span></span>

-   [<span data-ttu-id="ee174-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="ee174-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ee174-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee174-113">Remarks</span></span>

<span data-ttu-id="ee174-114">Il valore di questa proprietà è un membro dell'enumerazione [della \_ \_ modalità VAD AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) .</span><span class="sxs-lookup"><span data-stu-id="ee174-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="ee174-115">L'output del rilevamento dell'attività vocale è un numero compreso tra 0 e 3, calcolato per ogni fotogramma audio.</span><span class="sxs-lookup"><span data-stu-id="ee174-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="ee174-116">Il DSP codifica il risultato nel bit più basso dei primi due esempi audio in ogni frame audio.</span><span class="sxs-lookup"><span data-stu-id="ee174-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="ee174-117">Il significato del valore dipende dalla modalità specificata.</span><span class="sxs-lookup"><span data-stu-id="ee174-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="ee174-118">Il codice seguente mostra come estrarre i risultati dai dati audio.</span><span class="sxs-lookup"><span data-stu-id="ee174-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="ee174-119">In questo esempio, *pOutput* è un puntatore all'inizio di un frame audio nei dati di output.</span><span class="sxs-lookup"><span data-stu-id="ee174-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="ee174-120">Il valore predefinito di questa proprietà è 0 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="ee174-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="ee174-121">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="ee174-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee174-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee174-122">Requirements</span></span>



| <span data-ttu-id="ee174-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee174-123">Requirement</span></span> | <span data-ttu-id="ee174-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ee174-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee174-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee174-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ee174-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ee174-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee174-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee174-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ee174-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee174-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee174-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee174-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee174-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee174-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee174-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee174-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee174-132">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee174-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
