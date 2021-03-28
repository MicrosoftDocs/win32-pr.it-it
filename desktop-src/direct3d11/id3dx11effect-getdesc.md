---
title: Metodo getdesc ID3DX11Effect (D3dx11effect. h)
description: Ottenere una descrizione dell'effetto.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996124"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="d6806-106">Metodo ID3DX11Effect:: getdesc</span><span class="sxs-lookup"><span data-stu-id="d6806-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="d6806-107">Ottenere una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="d6806-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6806-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6806-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d6806-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6806-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6806-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="d6806-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d6806-111">Tipo: **[ **D3DX11 \_ Effect \_ desc**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6806-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="d6806-112">Puntatore a una descrizione dell'effetto (vedere [**D3DX11 \_ Effect \_ desc**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="d6806-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6806-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6806-113">Return value</span></span>

<span data-ttu-id="d6806-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6806-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6806-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d6806-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6806-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6806-116">Remarks</span></span>

<span data-ttu-id="d6806-117">Una descrizione dell'effetto contiene informazioni di base su un effetto, ad esempio le tecniche che contiene e le risorse del buffer costante richieste.</span><span class="sxs-lookup"><span data-stu-id="d6806-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="d6806-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="d6806-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d6806-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d6806-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d6806-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d6806-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6806-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6806-121">Requirements</span></span>



| <span data-ttu-id="d6806-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6806-122">Requirement</span></span> | <span data-ttu-id="d6806-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d6806-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6806-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6806-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d6806-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6806-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d6806-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6806-126">Library</span></span><br/> | <dl> <span data-ttu-id="d6806-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="d6806-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6806-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6806-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6806-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="d6806-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





