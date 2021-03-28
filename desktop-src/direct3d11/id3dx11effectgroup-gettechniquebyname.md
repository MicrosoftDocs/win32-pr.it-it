---
title: Metodo ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Ottenere una tecnica in base al nome. | Metodo ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Metodo GetTechniqueByName Direct3D 11
- Metodo GetTechniqueByName Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982292"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="ca710-107">Metodo ID3DX11EffectGroup:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="ca710-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="ca710-108">Ottenere una tecnica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ca710-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca710-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca710-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="ca710-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca710-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca710-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="ca710-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ca710-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca710-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ca710-113">Nome della tecnica.</span><span class="sxs-lookup"><span data-stu-id="ca710-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca710-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca710-114">Return value</span></span>

<span data-ttu-id="ca710-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca710-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="ca710-116">Puntatore a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)o **null** se la tecnica non viene trovata.</span><span class="sxs-lookup"><span data-stu-id="ca710-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca710-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca710-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ca710-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="ca710-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ca710-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ca710-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ca710-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ca710-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca710-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca710-121">Requirements</span></span>



| <span data-ttu-id="ca710-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca710-122">Requirement</span></span> | <span data-ttu-id="ca710-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ca710-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca710-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca710-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ca710-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca710-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ca710-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca710-126">Library</span></span><br/> | <dl> <span data-ttu-id="ca710-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="ca710-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca710-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca710-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca710-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="ca710-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

