---
title: Metodo ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Ottenere una tecnica in base all'indice. | Metodo ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Metodo GetTechniqueByIndex Direct3D 11
- Metodo GetTechniqueByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969458"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="cd27c-107">Metodo ID3DX11Effect:: GetTechniqueByIndex</span><span class="sxs-lookup"><span data-stu-id="cd27c-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="cd27c-108">Ottenere una tecnica in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="cd27c-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd27c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd27c-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="cd27c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd27c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd27c-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="cd27c-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="cd27c-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cd27c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cd27c-113">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="cd27c-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd27c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd27c-114">Return value</span></span>

<span data-ttu-id="cd27c-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd27c-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="cd27c-116">Puntatore a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="cd27c-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd27c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd27c-117">Remarks</span></span>

<span data-ttu-id="cd27c-118">Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="cd27c-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="cd27c-119">È possibile accedere a una tecnica usando il nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="cd27c-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="cd27c-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="cd27c-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cd27c-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="cd27c-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cd27c-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cd27c-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd27c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd27c-123">Requirements</span></span>



| <span data-ttu-id="cd27c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd27c-124">Requirement</span></span> | <span data-ttu-id="cd27c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cd27c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd27c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd27c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cd27c-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd27c-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cd27c-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd27c-128">Library</span></span><br/> | <dl> <span data-ttu-id="cd27c-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="cd27c-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd27c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd27c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd27c-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="cd27c-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

