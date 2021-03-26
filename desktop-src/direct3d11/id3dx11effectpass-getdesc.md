---
title: Metodo getdesc ID3DX11EffectPass (D3dx11effect. h)
description: Ottenere una descrizione del passaggio.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355244"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="7e817-106">Metodo ID3DX11EffectPass:: getdesc</span><span class="sxs-lookup"><span data-stu-id="7e817-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="7e817-107">Ottenere una descrizione del passaggio.</span><span class="sxs-lookup"><span data-stu-id="7e817-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e817-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e817-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7e817-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e817-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e817-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="7e817-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="7e817-111">Tipo: **[ **D3DX11 \_ pass \_ desc**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e817-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="7e817-112">Un puntatore a una descrizione Pass (vedere [**D3DX11 \_ pass \_ desc**](d3dx11-pass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="7e817-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e817-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e817-113">Return value</span></span>

<span data-ttu-id="7e817-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e817-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e817-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7e817-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e817-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e817-116">Remarks</span></span>

<span data-ttu-id="7e817-117">Un passaggio è un blocco di codice che imposta lo stato di rendering e gli shader, che a sua volta imposta buffer costanti, sampler e trame.</span><span class="sxs-lookup"><span data-stu-id="7e817-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="7e817-118">Una tecnica degli effetti contiene uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="7e817-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="7e817-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7e817-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7e817-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7e817-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7e817-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7e817-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e817-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e817-122">Requirements</span></span>



| <span data-ttu-id="7e817-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e817-123">Requirement</span></span> | <span data-ttu-id="7e817-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7e817-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e817-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e817-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7e817-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e817-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7e817-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e817-127">Library</span></span><br/> | <dl> <span data-ttu-id="7e817-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7e817-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e817-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e817-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e817-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="7e817-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





