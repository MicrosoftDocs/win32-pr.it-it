---
title: msad4
description: Confronta un valore di riferimento di 4 byte e un valore di origine a 8 byte e accumula un vettore di 4 somme. Ogni somma corrisponde alla somma mascherata delle differenze assolute di un diverso allineamento dei byte tra il valore di riferimento e il valore di origine.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104976967"
---
# <a name="msad4"></a><span data-ttu-id="0de09-105">msad4</span><span class="sxs-lookup"><span data-stu-id="0de09-105">msad4</span></span>

<span data-ttu-id="0de09-106">Confronta un valore di riferimento di 4 byte e un valore di origine a 8 byte e accumula un vettore di 4 somme.</span><span class="sxs-lookup"><span data-stu-id="0de09-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="0de09-107">Ogni somma corrisponde alla somma mascherata delle differenze assolute di un diverso allineamento dei byte tra il valore di riferimento e il valore di origine.</span><span class="sxs-lookup"><span data-stu-id="0de09-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="0de09-108">risultato di uint4 = msad4 (riferimento a uint, origine uint2, uint4 di accuratezza);</span><span class="sxs-lookup"><span data-stu-id="0de09-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0de09-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0de09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de09-110"><span id="reference"></span><span id="REFERENCE"></span>*riferimento*</span><span class="sxs-lookup"><span data-stu-id="0de09-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="0de09-111">\[nella \] matrice di riferimento di 4 byte in un valore **uint** .</span><span class="sxs-lookup"><span data-stu-id="0de09-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="0de09-112"><span id="source"></span><span id="SOURCE"></span>*origine*</span><span class="sxs-lookup"><span data-stu-id="0de09-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="0de09-113">\[nella \] matrice di origine di 8 byte in due valori **uint2** .</span><span class="sxs-lookup"><span data-stu-id="0de09-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="0de09-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span><span class="sxs-lookup"><span data-stu-id="0de09-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="0de09-115">\[in \] un vettore di 4 valori.</span><span class="sxs-lookup"><span data-stu-id="0de09-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="0de09-116">**msad4** aggiunge questo vettore alla somma mascherata delle differenze assolute dei diversi allineamenti di byte tra il valore di riferimento e il valore di origine.</span><span class="sxs-lookup"><span data-stu-id="0de09-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de09-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0de09-117">Return Value</span></span>

<span data-ttu-id="0de09-118">Vettore di 4 somme.</span><span class="sxs-lookup"><span data-stu-id="0de09-118">A vector of 4 sums.</span></span> <span data-ttu-id="0de09-119">Ogni somma corrisponde alla somma mascherata delle differenze assolute degli allineamenti di byte diversi tra il valore di riferimento e il valore di origine.</span><span class="sxs-lookup"><span data-stu-id="0de09-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="0de09-120">**msad4** non include una differenza nella somma se tale differenza è nascosta (ovvero, il byte di riferimento è 0).</span><span class="sxs-lookup"><span data-stu-id="0de09-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="0de09-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0de09-121">Remarks</span></span>

<span data-ttu-id="0de09-122">Per usare la funzione intrinseca **msad4** nel codice dello shader, chiamare il metodo [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ Opzioni d3d11 della funzionalità d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) per verificare che il dispositivo Direct3D supporti l'opzione della funzionalità [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="0de09-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="0de09-123">Per la funzione intrinseca **msad4** è necessario un driver di visualizzazione WDDM 1,2 e tutti i driver di visualizzazione WDDM 1,2 devono supportare **msad4**.</span><span class="sxs-lookup"><span data-stu-id="0de09-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="0de09-124">Se l'app crea un dispositivo di rendering con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 e la destinazione di compilazione è Shader Model 5 o versione successiva, il codice sorgente di HLSL può usare il **msad4** intrinseco.</span><span class="sxs-lookup"><span data-stu-id="0de09-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="0de09-125">I valori restituiti sono accurati solo fino a 65535.</span><span class="sxs-lookup"><span data-stu-id="0de09-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="0de09-126">Se si chiama la funzione intrinseca **msad4** con input che potrebbero restituire valori restituiti maggiori di 65535, **msad4** genera risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="0de09-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="0de09-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0de09-127">Minimum Shader Model</span></span>

<span data-ttu-id="0de09-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0de09-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0de09-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0de09-129">Shader Model</span></span>                                                | <span data-ttu-id="0de09-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="0de09-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="0de09-131">Shader Model 5 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0de09-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="0de09-132">sì</span><span class="sxs-lookup"><span data-stu-id="0de09-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="0de09-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="0de09-133">Examples</span></span>

<span data-ttu-id="0de09-134">Di seguito è riportato un esempio di calcolo dei risultati per **msad4**:</span><span class="sxs-lookup"><span data-stu-id="0de09-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="0de09-135">Di seguito è riportato un esempio di come è possibile usare **msad4** per cercare un modello di riferimento all'interno di un buffer:</span><span class="sxs-lookup"><span data-stu-id="0de09-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="0de09-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0de09-136">Requirements</span></span>



| <span data-ttu-id="0de09-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0de09-137">Requirement</span></span> | <span data-ttu-id="0de09-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0de09-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0de09-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0de09-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0de09-140">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0de09-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="0de09-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0de09-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0de09-142">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0de09-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0de09-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0de09-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de09-144">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="0de09-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

