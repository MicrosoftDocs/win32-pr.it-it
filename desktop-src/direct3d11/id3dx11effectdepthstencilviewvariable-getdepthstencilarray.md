---
title: Metodo ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect. h)
description: Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Metodo GetDepthStencilArray Direct3D 11
- Metodo GetDepthStencilArray Direct3D 11, interfaccia ID3DX11EffectDepthStencilViewVariable
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, metodo GetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982445"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a><span data-ttu-id="6602a-106">Metodo ID3DX11EffectDepthStencilViewVariable:: GetDepthStencilArray</span><span class="sxs-lookup"><span data-stu-id="6602a-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray method</span></span>

<span data-ttu-id="6602a-107">Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="6602a-107">Get an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6602a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6602a-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="6602a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6602a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6602a-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="6602a-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="6602a-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="6602a-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="6602a-112">Puntatore a una matrice di interfacce di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="6602a-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="6602a-113">Vedere [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="6602a-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="6602a-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="6602a-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="6602a-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6602a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6602a-116">Indice della matrice in base zero per ottenere la prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6602a-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="6602a-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="6602a-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="6602a-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6602a-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6602a-119">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6602a-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6602a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6602a-120">Return value</span></span>

<span data-ttu-id="6602a-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6602a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6602a-122">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6602a-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6602a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6602a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6602a-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6602a-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6602a-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6602a-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6602a-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6602a-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6602a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6602a-127">Requirements</span></span>



| <span data-ttu-id="6602a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6602a-128">Requirement</span></span> | <span data-ttu-id="6602a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6602a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6602a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6602a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6602a-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6602a-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6602a-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6602a-132">Library</span></span><br/> | <dl> <span data-ttu-id="6602a-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6602a-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6602a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6602a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6602a-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="6602a-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

