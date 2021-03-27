---
title: Metodo ID3DX11EffectDepthStencilVariable SetDepthStencilState (D3dx11effect. h)
description: Imposta lo stato del depth stencil.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Metodo SetDepthStencilState Direct3D 11
- Metodo SetDepthStencilState Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo SetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982454"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a><span data-ttu-id="c674b-106">Metodo ID3DX11EffectDepthStencilVariable:: SetDepthStencilState</span><span class="sxs-lookup"><span data-stu-id="c674b-106">ID3DX11EffectDepthStencilVariable::SetDepthStencilState method</span></span>

<span data-ttu-id="c674b-107">Imposta lo stato del depth stencil.</span><span class="sxs-lookup"><span data-stu-id="c674b-107">Sets the depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c674b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c674b-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="c674b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c674b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c674b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c674b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c674b-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c674b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c674b-112">Indicizzare in una matrice di interfacce di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="c674b-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="c674b-113">Se è presente una sola interfaccia di stencil Depth, usare 0.</span><span class="sxs-lookup"><span data-stu-id="c674b-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="c674b-114">*pDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="c674b-114">*pDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="c674b-115">Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span><span class="sxs-lookup"><span data-stu-id="c674b-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span></span>

<span data-ttu-id="c674b-116">Puntatore a un'interfaccia [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) contenente il nuovo stato depth stencil.</span><span class="sxs-lookup"><span data-stu-id="c674b-116">Pointer to an [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) interface containing the new depth stencil state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c674b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c674b-117">Return value</span></span>

<span data-ttu-id="c674b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c674b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c674b-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c674b-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c674b-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c674b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c674b-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c674b-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c674b-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c674b-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c674b-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c674b-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c674b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c674b-124">Requirements</span></span>



| <span data-ttu-id="c674b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c674b-125">Requirement</span></span> | <span data-ttu-id="c674b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c674b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c674b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c674b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c674b-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c674b-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c674b-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c674b-129">Library</span></span><br/> | <dl> <span data-ttu-id="c674b-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c674b-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c674b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c674b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c674b-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="c674b-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

