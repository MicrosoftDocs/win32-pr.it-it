---
title: Metodo ID3DX11EffectRenderTargetViewVariable GetRenderTargetArray (D3dx11effect. h)
description: Ottenere una matrice di destinazioni di rendering.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- Metodo GetRenderTargetArray Direct3D 11
- Metodo GetRenderTargetArray Direct3D 11, interfaccia ID3DX11EffectRenderTargetViewVariable
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, metodo GetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996252"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a><span data-ttu-id="6d596-106">Metodo ID3DX11EffectRenderTargetViewVariable:: GetRenderTargetArray</span><span class="sxs-lookup"><span data-stu-id="6d596-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTargetArray method</span></span>

<span data-ttu-id="6d596-107">Ottenere una matrice di destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="6d596-107">Get an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d596-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d596-108">Syntax</span></span>


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="6d596-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d596-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d596-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="6d596-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="6d596-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="6d596-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="6d596-112">Puntatore a una matrice di interfacce di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="6d596-112">A pointer to an array of render-target-view interfaces.</span></span> <span data-ttu-id="6d596-113">Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="6d596-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="6d596-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="6d596-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="6d596-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d596-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d596-116">Indice della matrice in base zero per ottenere la prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6d596-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="6d596-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="6d596-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="6d596-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d596-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d596-119">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6d596-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d596-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d596-120">Return value</span></span>

<span data-ttu-id="6d596-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d596-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d596-122">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6d596-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d596-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d596-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d596-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6d596-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6d596-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6d596-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6d596-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6d596-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d596-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d596-127">Requirements</span></span>



| <span data-ttu-id="6d596-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d596-128">Requirement</span></span> | <span data-ttu-id="6d596-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6d596-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d596-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d596-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6d596-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d596-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6d596-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d596-132">Library</span></span><br/> | <dl> <span data-ttu-id="6d596-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6d596-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d596-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d596-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d596-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="6d596-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

