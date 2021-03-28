---
title: Metodo ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
description: Ottenere un'annotazione in base all'indice. | Metodo ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Metodo GetAnnotationByIndex Direct3D 11
- Metodo GetAnnotationByIndex Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235106"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a><span data-ttu-id="7b1af-107">Metodo ID3DX11EffectGroup:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="7b1af-107">ID3DX11EffectGroup::GetAnnotationByIndex method</span></span>

<span data-ttu-id="7b1af-108">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="7b1af-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1af-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b1af-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="7b1af-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b1af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1af-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="7b1af-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1af-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7b1af-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7b1af-113">Indice dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="7b1af-113">Index of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1af-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b1af-114">Return value</span></span>

<span data-ttu-id="7b1af-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b1af-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="7b1af-116">Puntatore a un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1af-116">Pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b1af-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b1af-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b1af-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7b1af-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7b1af-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7b1af-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7b1af-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7b1af-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b1af-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b1af-121">Requirements</span></span>



| <span data-ttu-id="7b1af-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b1af-122">Requirement</span></span> | <span data-ttu-id="7b1af-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7b1af-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1af-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b1af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7b1af-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1af-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7b1af-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b1af-126">Library</span></span><br/> | <dl> <span data-ttu-id="7b1af-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7b1af-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b1af-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b1af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1af-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="7b1af-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

