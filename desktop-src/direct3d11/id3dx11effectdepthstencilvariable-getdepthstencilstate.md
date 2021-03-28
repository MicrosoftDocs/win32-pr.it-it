---
title: Metodo ID3DX11EffectDepthStencilVariable GetDepthStencilState (D3dx11effect. h)
description: Ottenere un puntatore a un'interfaccia di stencil profondità.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Metodo GetDepthStencilState Direct3D 11
- Metodo GetDepthStencilState Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo GetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982457"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="c49a5-106">Metodo ID3DX11EffectDepthStencilVariable:: GetDepthStencilState</span><span class="sxs-lookup"><span data-stu-id="c49a5-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="c49a5-107">Ottenere un puntatore a un'interfaccia di stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="c49a5-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c49a5-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="c49a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c49a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49a5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c49a5-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c49a5-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c49a5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c49a5-112">Indicizzare in una matrice di interfacce di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="c49a5-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="c49a5-113">Se è presente una sola interfaccia di stencil Depth, usare 0.</span><span class="sxs-lookup"><span data-stu-id="c49a5-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="c49a5-114">*ppDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="c49a5-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="c49a5-115">Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="c49a5-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="c49a5-116">Indirizzo di un puntatore a un'interfaccia di stato di Blend (vedere [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="c49a5-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49a5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c49a5-117">Return value</span></span>

<span data-ttu-id="c49a5-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c49a5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c49a5-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c49a5-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c49a5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c49a5-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c49a5-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c49a5-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c49a5-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c49a5-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c49a5-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c49a5-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c49a5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c49a5-124">Requirements</span></span>



| <span data-ttu-id="c49a5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c49a5-125">Requirement</span></span> | <span data-ttu-id="c49a5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c49a5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49a5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c49a5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c49a5-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49a5-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c49a5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c49a5-129">Library</span></span><br/> | <dl> <span data-ttu-id="c49a5-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c49a5-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49a5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c49a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49a5-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="c49a5-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

