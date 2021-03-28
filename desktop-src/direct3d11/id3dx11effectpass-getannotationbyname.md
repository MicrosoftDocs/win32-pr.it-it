---
title: Metodo ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969440"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="c1da8-107">Metodo ID3DX11EffectPass:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="c1da8-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="c1da8-108">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c1da8-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1da8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1da8-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="c1da8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1da8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1da8-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="c1da8-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="c1da8-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c1da8-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c1da8-113">Nome dell'elemento Annotation.</span><span class="sxs-lookup"><span data-stu-id="c1da8-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1da8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1da8-114">Return value</span></span>

<span data-ttu-id="c1da8-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1da8-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c1da8-116">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c1da8-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1da8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1da8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1da8-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c1da8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c1da8-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c1da8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c1da8-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c1da8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1da8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1da8-121">Requirements</span></span>



| <span data-ttu-id="c1da8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1da8-122">Requirement</span></span> | <span data-ttu-id="c1da8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c1da8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1da8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c1da8-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c1da8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c1da8-126">Library</span></span><br/> | <dl> <span data-ttu-id="c1da8-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1da8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1da8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1da8-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="c1da8-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

