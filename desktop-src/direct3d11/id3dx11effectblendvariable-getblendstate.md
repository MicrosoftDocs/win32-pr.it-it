---
title: Metodo ID3DX11EffectBlendVariable GetBlendState (D3dx11effect. h)
description: Ottenere un puntatore a un'interfaccia di stato di Blend.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Metodo GetBlendState Direct3D 11
- Metodo GetBlendState Direct3D 11, interfaccia ID3DX11EffectBlendVariable
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11, metodo GetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355524"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a><span data-ttu-id="7aa43-106">Metodo ID3DX11EffectBlendVariable:: GetBlendState</span><span class="sxs-lookup"><span data-stu-id="7aa43-106">ID3DX11EffectBlendVariable::GetBlendState method</span></span>

<span data-ttu-id="7aa43-107">Ottenere un puntatore a un'interfaccia di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="7aa43-107">Get a pointer to a blend-state interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa43-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aa43-108">Syntax</span></span>


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="7aa43-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7aa43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa43-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="7aa43-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7aa43-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7aa43-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7aa43-112">Indicizzare in una matrice di interfacce di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="7aa43-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="7aa43-113">Se è presente una sola interfaccia di stato di Blend, usare 0.</span><span class="sxs-lookup"><span data-stu-id="7aa43-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="7aa43-114">*ppBlendState*</span><span class="sxs-lookup"><span data-stu-id="7aa43-114">*ppBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="7aa43-115">Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="7aa43-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span></span>

<span data-ttu-id="7aa43-116">Indirizzo di un puntatore a un'interfaccia di stato di Blend (vedere [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span><span class="sxs-lookup"><span data-stu-id="7aa43-116">The address of a pointer to a blend-state interface (see [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa43-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7aa43-117">Return value</span></span>

<span data-ttu-id="7aa43-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7aa43-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7aa43-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7aa43-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa43-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7aa43-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7aa43-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7aa43-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7aa43-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7aa43-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7aa43-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7aa43-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7aa43-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aa43-124">Requirements</span></span>



| <span data-ttu-id="7aa43-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa43-125">Requirement</span></span> | <span data-ttu-id="7aa43-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7aa43-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa43-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aa43-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7aa43-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa43-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7aa43-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="7aa43-129">Library</span></span><br/> | <dl> <span data-ttu-id="7aa43-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7aa43-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aa43-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7aa43-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa43-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="7aa43-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

