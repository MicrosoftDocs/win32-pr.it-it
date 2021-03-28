---
title: Metodo ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect. h)
description: Consente di calcolare una maschera a blocchi di stato per consentire o impedire modifiche di stato.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Metodo ComputeStateBlockMask Direct3D 11
- Metodo ComputeStateBlockMask Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234963"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a><span data-ttu-id="f268c-106">Metodo ID3DX11EffectTechnique:: ComputeStateBlockMask</span><span class="sxs-lookup"><span data-stu-id="f268c-106">ID3DX11EffectTechnique::ComputeStateBlockMask method</span></span>

<span data-ttu-id="f268c-107">Consente di calcolare una maschera a blocchi di stato per consentire o impedire modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="f268c-107">Compute a state-block mask to allow/prevent state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f268c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f268c-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="f268c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f268c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f268c-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="f268c-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="f268c-111">Tipo: **[ **D3DX11 \_ state \_ Block \_ mask**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="f268c-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="f268c-112">Puntatore a una maschera a blocchi di stato (vedere [**D3DX11 \_ state \_ Block \_ mask**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="f268c-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f268c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f268c-113">Return value</span></span>

<span data-ttu-id="f268c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f268c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f268c-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f268c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f268c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f268c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f268c-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f268c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f268c-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f268c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f268c-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f268c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f268c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f268c-120">Requirements</span></span>



| <span data-ttu-id="f268c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f268c-121">Requirement</span></span> | <span data-ttu-id="f268c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f268c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f268c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f268c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f268c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f268c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f268c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f268c-125">Library</span></span><br/> | <dl> <span data-ttu-id="f268c-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f268c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f268c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f268c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f268c-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="f268c-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





