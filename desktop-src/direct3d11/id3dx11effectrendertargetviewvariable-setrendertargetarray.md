---
title: Metodo ID3DX11EffectRenderTargetViewVariable SetRenderTargetArray (D3dx11effect. h)
description: Impostare una matrice di destinazioni di rendering.
ms.assetid: 03e1c4ea-292c-439f-a647-070b9e91a044
keywords:
- Metodo SetRenderTargetArray Direct3D 11
- Metodo SetRenderTargetArray Direct3D 11, interfaccia ID3DX11EffectRenderTargetViewVariable
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, metodo SetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ff8a1931e95df4fd78d67a3a71d53150875400
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982166"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertargetarray-method"></a><span data-ttu-id="9a9f1-106">Metodo ID3DX11EffectRenderTargetViewVariable:: SetRenderTargetArray</span><span class="sxs-lookup"><span data-stu-id="9a9f1-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTargetArray method</span></span>

<span data-ttu-id="9a9f1-107">Impostare una matrice di destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-107">Set an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a9f1-108">Syntax</span></span>


```C++
HRESULT SetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="9a9f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a9f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9f1-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="9a9f1-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="9a9f1-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a9f1-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="9a9f1-112">Impostare una matrice di interfacce di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-112">Set an array of render-target-view interfaces.</span></span> <span data-ttu-id="9a9f1-113">Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="9a9f1-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="9a9f1-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="9a9f1-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="9a9f1-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a9f1-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a9f1-116">Indice della matrice in base zero in cui archiviare la prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-116">The zero-based array index to store the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="9a9f1-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="9a9f1-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="9a9f1-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a9f1-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a9f1-119">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9f1-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a9f1-120">Return value</span></span>

<span data-ttu-id="9a9f1-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a9f1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a9f1-122">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9a9f1-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a9f1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a9f1-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a9f1-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a9f1-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9a9f1-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a9f1-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a9f1-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a9f1-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a9f1-127">Requirements</span></span>



| <span data-ttu-id="9a9f1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a9f1-128">Requirement</span></span> | <span data-ttu-id="9a9f1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9a9f1-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9f1-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a9f1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9a9f1-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f1-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a9f1-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a9f1-132">Library</span></span><br/> | <dl> <span data-ttu-id="9a9f1-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f1-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a9f1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a9f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9f1-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="9a9f1-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

