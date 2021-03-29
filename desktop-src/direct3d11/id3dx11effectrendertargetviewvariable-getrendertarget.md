---
title: Metodo ID3DX11EffectRenderTargetViewVariable GetRenderTarget (D3dx11effect. h)
description: Ottenere una destinazione di rendering.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Metodo GetRenderTarget Direct3D 11
- Metodo GetRenderTarget Direct3D 11, interfaccia ID3DX11EffectRenderTargetViewVariable
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, metodo GetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa86dd3a5c950e18ae97ba1987ee0f44b9f658c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996257"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a><span data-ttu-id="e964f-106">Metodo ID3DX11EffectRenderTargetViewVariable:: GetRenderTarget</span><span class="sxs-lookup"><span data-stu-id="e964f-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTarget method</span></span>

<span data-ttu-id="e964f-107">Ottenere una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e964f-107">Get a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="e964f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e964f-108">Syntax</span></span>


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="e964f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e964f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e964f-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="e964f-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="e964f-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="e964f-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="e964f-112">Indirizzo di un puntatore a un'interfaccia di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e964f-112">The address of a pointer to a render-target-view interface.</span></span> <span data-ttu-id="e964f-113">Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="e964f-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e964f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e964f-114">Return value</span></span>

<span data-ttu-id="e964f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e964f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e964f-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e964f-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e964f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e964f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e964f-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e964f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e964f-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e964f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e964f-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e964f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e964f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e964f-121">Requirements</span></span>



| <span data-ttu-id="e964f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e964f-122">Requirement</span></span> | <span data-ttu-id="e964f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e964f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e964f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e964f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e964f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e964f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e964f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e964f-126">Library</span></span><br/> | <dl> <span data-ttu-id="e964f-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e964f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e964f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e964f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e964f-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="e964f-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





