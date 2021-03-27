---
title: Metodo ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Ottiene un puntatore a una variabile che contiene lo stato rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058664"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a><span data-ttu-id="66f1f-106">Metodo ID3DX11EffectRasterizerVariable:: GetBackingStore</span><span class="sxs-lookup"><span data-stu-id="66f1f-106">ID3DX11EffectRasterizerVariable::GetBackingStore method</span></span>

<span data-ttu-id="66f1f-107">Ottiene un puntatore a una variabile che contiene lo stato rasteriser.</span><span class="sxs-lookup"><span data-stu-id="66f1f-107">Get a pointer to a variable that contains rasteriser state.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f1f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66f1f-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="66f1f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="66f1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f1f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="66f1f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="66f1f-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="66f1f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="66f1f-112">Indicizzare in una matrice di descrizioni dello stato rasteriser.</span><span class="sxs-lookup"><span data-stu-id="66f1f-112">Index into an array of rasteriser-state descriptions.</span></span> <span data-ttu-id="66f1f-113">Se è presente una sola variabile rasteriser nell'effetto, usare 0.</span><span class="sxs-lookup"><span data-stu-id="66f1f-113">If there is only one rasteriser variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="66f1f-114">*pRasterizerDesc*</span><span class="sxs-lookup"><span data-stu-id="66f1f-114">*pRasterizerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="66f1f-115">Tipo: **[ **d3d11 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span><span class="sxs-lookup"><span data-stu-id="66f1f-115">Type: **[**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span></span>

<span data-ttu-id="66f1f-116">Un puntatore a una descrizione dello stato rasteriser (vedere la pagina relativa al [**\_ rasterizzatore d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span><span class="sxs-lookup"><span data-stu-id="66f1f-116">A pointer to a rasteriser-state description (see [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f1f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66f1f-117">Return value</span></span>

<span data-ttu-id="66f1f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66f1f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66f1f-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="66f1f-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66f1f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="66f1f-120">Remarks</span></span>

<span data-ttu-id="66f1f-121">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f1f-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="66f1f-122">Quando necessario, è possibile utilizzare i dati dell'archivio di backup per ricreare la variabile.</span><span class="sxs-lookup"><span data-stu-id="66f1f-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="66f1f-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="66f1f-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="66f1f-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="66f1f-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="66f1f-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="66f1f-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66f1f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66f1f-126">Requirements</span></span>



| <span data-ttu-id="66f1f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f1f-127">Requirement</span></span> | <span data-ttu-id="66f1f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="66f1f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f1f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66f1f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="66f1f-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f1f-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="66f1f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="66f1f-131">Library</span></span><br/> | <dl> <span data-ttu-id="66f1f-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="66f1f-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f1f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66f1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f1f-134">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="66f1f-134">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

