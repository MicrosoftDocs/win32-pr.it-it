---
title: Metodo ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
description: Ottenere un'annotazione in base all'indice. | Metodo ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Metodo GetAnnotationByIndex Direct3D 11
- Metodo GetAnnotationByIndex Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e30712ba38f1360a992a8e409c249a746cca036
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996220"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a><span data-ttu-id="c1bd9-107">Metodo ID3DX11EffectTechnique:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="c1bd9-107">ID3DX11EffectTechnique::GetAnnotationByIndex method</span></span>

<span data-ttu-id="c1bd9-108">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="c1bd9-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1bd9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1bd9-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c1bd9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1bd9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1bd9-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="c1bd9-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bd9-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c1bd9-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c1bd9-113">Indice in base zero del puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c1bd9-113">The zero-based index of the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1bd9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1bd9-114">Return value</span></span>

<span data-ttu-id="c1bd9-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1bd9-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c1bd9-116">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c1bd9-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1bd9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1bd9-117">Remarks</span></span>

<span data-ttu-id="c1bd9-118">Usare un'annotazione per alleghi una parte di metadati a una tecnica.</span><span class="sxs-lookup"><span data-stu-id="c1bd9-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="c1bd9-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c1bd9-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c1bd9-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c1bd9-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c1bd9-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c1bd9-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1bd9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1bd9-122">Requirements</span></span>



| <span data-ttu-id="c1bd9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bd9-123">Requirement</span></span> | <span data-ttu-id="c1bd9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c1bd9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bd9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1bd9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c1bd9-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1bd9-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c1bd9-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c1bd9-127">Library</span></span><br/> | <dl> <span data-ttu-id="c1bd9-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c1bd9-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1bd9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1bd9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bd9-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="c1bd9-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

