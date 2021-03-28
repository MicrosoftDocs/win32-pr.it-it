---
title: Metodo ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Ripristina uno stato di depth stencil impostato in precedenza.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Metodo UndoSetDepthStencilState Direct3D 11
- Metodo UndoSetDepthStencilState Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996145"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="f42e9-106">Metodo ID3DX11EffectDepthStencilVariable:: UndoSetDepthStencilState</span><span class="sxs-lookup"><span data-stu-id="f42e9-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="f42e9-107">Ripristina uno stato di depth stencil impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f42e9-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f42e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f42e9-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f42e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f42e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42e9-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f42e9-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f42e9-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f42e9-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f42e9-112">Indicizzare in una matrice di interfacce di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="f42e9-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="f42e9-113">Se è presente una sola interfaccia di stencil Depth, usare 0.</span><span class="sxs-lookup"><span data-stu-id="f42e9-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42e9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f42e9-114">Return value</span></span>

<span data-ttu-id="f42e9-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f42e9-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f42e9-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f42e9-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f42e9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f42e9-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f42e9-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f42e9-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f42e9-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f42e9-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f42e9-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f42e9-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f42e9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f42e9-121">Requirements</span></span>



| <span data-ttu-id="f42e9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f42e9-122">Requirement</span></span> | <span data-ttu-id="f42e9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f42e9-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42e9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f42e9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f42e9-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42e9-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f42e9-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f42e9-126">Library</span></span><br/> | <dl> <span data-ttu-id="f42e9-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f42e9-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42e9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f42e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f42e9-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="f42e9-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

