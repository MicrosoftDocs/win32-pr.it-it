---
title: Metodo ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Impostare una destinazione di rendering.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Metodo SetRenderTarget Direct3D 11
- Metodo SetRenderTarget Direct3D 11, interfaccia ID3DX11EffectRenderTargetViewVariable
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, metodo SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886332"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="dce26-106">Metodo ID3DX11EffectRenderTargetViewVariable:: SetRenderTarget</span><span class="sxs-lookup"><span data-stu-id="dce26-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="dce26-107">Impostare una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="dce26-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce26-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dce26-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="dce26-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dce26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce26-110">*pResource*</span><span class="sxs-lookup"><span data-stu-id="dce26-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="dce26-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="dce26-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="dce26-112">Puntatore a un'interfaccia di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="dce26-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="dce26-113">Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="dce26-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce26-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dce26-114">Return value</span></span>

<span data-ttu-id="dce26-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dce26-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dce26-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dce26-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dce26-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dce26-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dce26-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="dce26-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="dce26-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="dce26-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="dce26-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="dce26-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dce26-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dce26-121">Requirements</span></span>



| <span data-ttu-id="dce26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce26-122">Requirement</span></span> | <span data-ttu-id="dce26-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dce26-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce26-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dce26-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dce26-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce26-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dce26-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="dce26-126">Library</span></span><br/> | <dl> <span data-ttu-id="dce26-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="dce26-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce26-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dce26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce26-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="dce26-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





