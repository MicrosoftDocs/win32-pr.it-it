---
title: Metodo ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect. h)
description: Ottenere un membro della struttura in base alla semantica.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Metodo GetMemberBySemantic Direct3D 11
- Metodo GetMemberBySemantic Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996217"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="c16f0-106">Metodo ID3DX11EffectVariable:: GetMemberBySemantic</span><span class="sxs-lookup"><span data-stu-id="c16f0-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="c16f0-107">Ottenere un membro della struttura in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="c16f0-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c16f0-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="c16f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c16f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c16f0-110">*Semantica*</span><span class="sxs-lookup"><span data-stu-id="c16f0-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="c16f0-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c16f0-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c16f0-112">Semantica.</span><span class="sxs-lookup"><span data-stu-id="c16f0-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c16f0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c16f0-113">Return value</span></span>

<span data-ttu-id="c16f0-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c16f0-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c16f0-115">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c16f0-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c16f0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c16f0-116">Remarks</span></span>

<span data-ttu-id="c16f0-117">Se la variabile Effect è una struttura, usare questo metodo per cercare un membro in base alla semantica associata.</span><span class="sxs-lookup"><span data-stu-id="c16f0-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="c16f0-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c16f0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c16f0-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c16f0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c16f0-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c16f0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c16f0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c16f0-121">Requirements</span></span>



| <span data-ttu-id="c16f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c16f0-122">Requirement</span></span> | <span data-ttu-id="c16f0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c16f0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16f0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c16f0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c16f0-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c16f0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c16f0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c16f0-126">Library</span></span><br/> | <dl> <span data-ttu-id="c16f0-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c16f0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c16f0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c16f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16f0-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c16f0-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

