---
title: Metodo getdesc ID3DX11EffectVariable (D3dx11effect. h)
description: Ottenere una descrizione.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996284"
---
# <a name="id3dx11effectvariablegetdesc-method"></a><span data-ttu-id="3184c-106">Metodo ID3DX11EffectVariable:: getdesc</span><span class="sxs-lookup"><span data-stu-id="3184c-106">ID3DX11EffectVariable::GetDesc method</span></span>

<span data-ttu-id="3184c-107">Ottenere una descrizione.</span><span class="sxs-lookup"><span data-stu-id="3184c-107">Get a description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3184c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3184c-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3184c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3184c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3184c-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="3184c-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="3184c-111">Tipo: **[ **D3DX11 \_ Effect \_ variabile \_ desc**](d3dx11-effect-variable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3184c-111">Type: **[**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)\***</span></span>

<span data-ttu-id="3184c-112">Un puntatore a una descrizione della variabile di effetto ( [**vedere \_ variabile effetto D3DX11 \_ \_ desc**](d3dx11-effect-variable-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="3184c-112">A pointer to an effect-variable description (see [**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3184c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3184c-113">Return value</span></span>

<span data-ttu-id="3184c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3184c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3184c-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3184c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3184c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3184c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3184c-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3184c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3184c-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3184c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3184c-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3184c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3184c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3184c-120">Requirements</span></span>



| <span data-ttu-id="3184c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3184c-121">Requirement</span></span> | <span data-ttu-id="3184c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3184c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3184c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3184c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3184c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3184c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3184c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3184c-125">Library</span></span><br/> | <dl> <span data-ttu-id="3184c-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3184c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3184c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3184c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3184c-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="3184c-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





