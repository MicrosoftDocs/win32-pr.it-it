---
title: FMA (Corecrt \_ Math. h)
description: Restituisce l'aggiunta a due volte con doppia precisione di un oggetto \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL FMA
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400599"
---
# <a name="fma"></a><span data-ttu-id="755a6-104">fma</span><span class="sxs-lookup"><span data-stu-id="755a6-104">fma</span></span>

<span data-ttu-id="755a6-105">Restituisce l'aggiunta di un oggetto \* b + c a precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="755a6-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="755a6-106">*ret* FMA (Double *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="755a6-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="755a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="755a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755a6-108"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="755a6-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="755a6-109">\[nel \] primo valore dell'aggiunta di moltiplicazione fusa.</span><span class="sxs-lookup"><span data-stu-id="755a6-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="755a6-110"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="755a6-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="755a6-111">\[nel \] secondo valore nell'addizione di moltiplicazione fusa.</span><span class="sxs-lookup"><span data-stu-id="755a6-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="755a6-112"><span id="c"></span><span id="C"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="755a6-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="755a6-113">\[nel \] terzo valore nell'addizione di moltiplicazione fusa.</span><span class="sxs-lookup"><span data-stu-id="755a6-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755a6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="755a6-114">Return Value</span></span>

<span data-ttu-id="755a6-115">L'aggiunta di *un parametro a* \* *b*  +  *c* da parte della doppia precisione.</span><span class="sxs-lookup"><span data-stu-id="755a6-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="755a6-116">Il valore restituito deve essere accurato per 0,5 unità di precisione minima (ULP rispetto).</span><span class="sxs-lookup"><span data-stu-id="755a6-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="755a6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="755a6-117">Remarks</span></span>

<span data-ttu-id="755a6-118">La funzione intrinseca **FMA** deve supportare Nans, infs e denorms.</span><span class="sxs-lookup"><span data-stu-id="755a6-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="755a6-119">Per usare la funzione intrinseca **FMA** nel codice dello shader, chiamare il metodo [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ Opzioni d3d11 della funzionalità d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) per verificare che il dispositivo Direct3D supporti l'opzione della funzionalità [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="755a6-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="755a6-120">La funzione intrinseca **FMA** richiede un driver di visualizzazione WDDM 1,2 e tutti i driver di visualizzazione WDDM 1,2 devono supportare **FMA**.</span><span class="sxs-lookup"><span data-stu-id="755a6-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="755a6-121">Se l'app crea un dispositivo di rendering con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 e la destinazione di compilazione è il modello di shader 5 o versione successiva, il codice sorgente di HLSL può usare l'intrinseco **FMA** .</span><span class="sxs-lookup"><span data-stu-id="755a6-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="755a6-122">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="755a6-122">Type Description</span></span>



| <span data-ttu-id="755a6-123">Nome</span><span class="sxs-lookup"><span data-stu-id="755a6-123">Name</span></span>  | [<span data-ttu-id="755a6-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="755a6-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="755a6-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="755a6-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="755a6-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="755a6-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="755a6-127">*un*</span><span class="sxs-lookup"><span data-stu-id="755a6-127">*a*</span></span>   | <span data-ttu-id="755a6-128">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="755a6-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="755a6-129">**doppio**</span><span class="sxs-lookup"><span data-stu-id="755a6-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="755a6-130">any</span><span class="sxs-lookup"><span data-stu-id="755a6-130">any</span></span>                          |
| <span data-ttu-id="755a6-131">*b*</span><span class="sxs-lookup"><span data-stu-id="755a6-131">*b*</span></span>   | <span data-ttu-id="755a6-132">uguale all'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="755a6-133">**doppio**</span><span class="sxs-lookup"><span data-stu-id="755a6-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="755a6-134">stesse dimensioni dell'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="755a6-135">*c*</span><span class="sxs-lookup"><span data-stu-id="755a6-135">*c*</span></span>   | <span data-ttu-id="755a6-136">uguale all'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="755a6-137">**doppio**</span><span class="sxs-lookup"><span data-stu-id="755a6-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="755a6-138">stesse dimensioni dell'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="755a6-139">*RET*</span><span class="sxs-lookup"><span data-stu-id="755a6-139">*ret*</span></span> | <span data-ttu-id="755a6-140">uguale all'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="755a6-141">**doppio**</span><span class="sxs-lookup"><span data-stu-id="755a6-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="755a6-142">stesse dimensioni dell'input *a*</span><span class="sxs-lookup"><span data-stu-id="755a6-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="755a6-143">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="755a6-143">Minimum Shader Model</span></span>

<span data-ttu-id="755a6-144">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="755a6-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="755a6-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="755a6-145">Shader Model</span></span>                                                | <span data-ttu-id="755a6-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="755a6-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="755a6-147">Shader Model 5 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="755a6-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="755a6-148">sì</span><span class="sxs-lookup"><span data-stu-id="755a6-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="755a6-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="755a6-149">Requirements</span></span>



| <span data-ttu-id="755a6-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="755a6-150">Requirement</span></span> | <span data-ttu-id="755a6-151">Valore</span><span class="sxs-lookup"><span data-stu-id="755a6-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="755a6-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755a6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="755a6-153">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="755a6-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="755a6-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755a6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="755a6-155">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="755a6-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="755a6-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="755a6-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="755a6-157"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="755a6-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755a6-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="755a6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755a6-159">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="755a6-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

