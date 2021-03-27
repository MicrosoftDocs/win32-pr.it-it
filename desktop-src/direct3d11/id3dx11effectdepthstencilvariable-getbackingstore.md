---
title: Metodo ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect. h)
description: Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982307"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a><span data-ttu-id="13f5e-106">Metodo ID3DX11EffectDepthStencilVariable:: GetBackingStore</span><span class="sxs-lookup"><span data-stu-id="13f5e-106">ID3DX11EffectDepthStencilVariable::GetBackingStore method</span></span>

<span data-ttu-id="13f5e-107">Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="13f5e-107">Get a pointer to a variable that contains depth-stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f5e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13f5e-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a><span data-ttu-id="13f5e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13f5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f5e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="13f5e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="13f5e-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="13f5e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="13f5e-112">Indicizzare in una matrice di descrizioni dello stato di depth-stencil.</span><span class="sxs-lookup"><span data-stu-id="13f5e-112">Index into an array of depth-stencil-state descriptions.</span></span> <span data-ttu-id="13f5e-113">Se è presente una sola variabile di stencil Depth nell'effetto, usare 0.</span><span class="sxs-lookup"><span data-stu-id="13f5e-113">If there is only one depth-stencil variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="13f5e-114">*pDepthStencilDesc*</span><span class="sxs-lookup"><span data-stu-id="13f5e-114">*pDepthStencilDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="13f5e-115">Tipo: **[ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span><span class="sxs-lookup"><span data-stu-id="13f5e-115">Type: **[**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span></span>

<span data-ttu-id="13f5e-116">Puntatore a una descrizione dello stato di depth-stencil (vedere [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="13f5e-116">A pointer to a depth-stencil-state description (see [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f5e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13f5e-117">Return value</span></span>

<span data-ttu-id="13f5e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13f5e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13f5e-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="13f5e-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="13f5e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="13f5e-120">Remarks</span></span>

<span data-ttu-id="13f5e-121">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f5e-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="13f5e-122">Quando necessario, è possibile utilizzare i dati dell'archivio di backup per ricreare la variabile.</span><span class="sxs-lookup"><span data-stu-id="13f5e-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="13f5e-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="13f5e-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="13f5e-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="13f5e-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="13f5e-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="13f5e-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13f5e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13f5e-126">Requirements</span></span>



| <span data-ttu-id="13f5e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f5e-127">Requirement</span></span> | <span data-ttu-id="13f5e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="13f5e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f5e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13f5e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="13f5e-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="13f5e-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="13f5e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="13f5e-131">Library</span></span><br/> | <dl> <span data-ttu-id="13f5e-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="13f5e-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f5e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13f5e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f5e-134">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="13f5e-134">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

