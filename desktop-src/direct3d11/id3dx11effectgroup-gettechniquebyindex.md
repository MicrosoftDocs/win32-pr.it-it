---
title: Metodo ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Ottenere una tecnica in base all'indice. | Metodo ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Metodo GetTechniqueByIndex Direct3D 11
- Metodo GetTechniqueByIndex Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969422"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="68398-107">Metodo ID3DX11EffectGroup:: GetTechniqueByIndex</span><span class="sxs-lookup"><span data-stu-id="68398-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="68398-108">Ottenere una tecnica in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="68398-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="68398-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68398-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="68398-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="68398-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68398-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="68398-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="68398-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68398-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="68398-113">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="68398-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68398-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68398-114">Return value</span></span>

<span data-ttu-id="68398-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="68398-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="68398-116">Puntatore a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="68398-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68398-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="68398-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68398-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="68398-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="68398-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="68398-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="68398-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="68398-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68398-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68398-121">Requirements</span></span>



| <span data-ttu-id="68398-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="68398-122">Requirement</span></span> | <span data-ttu-id="68398-123">Valore</span><span class="sxs-lookup"><span data-stu-id="68398-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68398-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68398-124">Header</span></span><br/>  | <dl> <span data-ttu-id="68398-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="68398-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="68398-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="68398-126">Library</span></span><br/> | <dl> <span data-ttu-id="68398-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="68398-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68398-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68398-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68398-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="68398-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

