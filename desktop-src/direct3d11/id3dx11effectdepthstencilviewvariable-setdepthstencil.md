---
title: Metodo ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect. h)
description: Impostare una risorsa di visualizzazione stencil profondità.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Metodo SetDepthStencil Direct3D 11
- Metodo SetDepthStencil Direct3D 11, interfaccia ID3DX11EffectDepthStencilViewVariable
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, metodo SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995963"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="e8a8d-106">Metodo ID3DX11EffectDepthStencilViewVariable:: SetDepthStencil</span><span class="sxs-lookup"><span data-stu-id="e8a8d-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="e8a8d-107">Impostare una risorsa di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="e8a8d-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a8d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8a8d-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="e8a8d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8a8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a8d-110">*pResource*</span><span class="sxs-lookup"><span data-stu-id="e8a8d-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a8d-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="e8a8d-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="e8a8d-112">Puntatore a un'interfaccia di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="e8a8d-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="e8a8d-113">Vedere [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="e8a8d-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a8d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8a8d-114">Return value</span></span>

<span data-ttu-id="e8a8d-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8a8d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8a8d-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e8a8d-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8a8d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8a8d-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8a8d-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e8a8d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8a8d-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e8a8d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8a8d-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e8a8d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8a8d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8a8d-121">Requirements</span></span>



| <span data-ttu-id="e8a8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a8d-122">Requirement</span></span> | <span data-ttu-id="e8a8d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e8a8d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a8d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8a8d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8a8d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a8d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8a8d-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8a8d-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8a8d-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e8a8d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a8d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8a8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a8d-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="e8a8d-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





