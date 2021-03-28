---
title: Metodo ID3DX11EffectType GetMemberTypeBySemantic (D3dx11effect. h)
description: Ottenere un tipo di membro in base alla semantica.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Metodo GetMemberTypeBySemantic Direct3D 11
- Metodo GetMemberTypeBySemantic Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo GetMemberTypeBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996188"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a><span data-ttu-id="e5c37-106">Metodo ID3DX11EffectType:: GetMemberTypeBySemantic</span><span class="sxs-lookup"><span data-stu-id="e5c37-106">ID3DX11EffectType::GetMemberTypeBySemantic method</span></span>

<span data-ttu-id="e5c37-107">Ottenere un tipo di membro in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="e5c37-107">Get a member type by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5c37-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="e5c37-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5c37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c37-110">*Semantica*</span><span class="sxs-lookup"><span data-stu-id="e5c37-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c37-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e5c37-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e5c37-112">Semantica.</span><span class="sxs-lookup"><span data-stu-id="e5c37-112">A semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c37-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5c37-113">Return value</span></span>

<span data-ttu-id="e5c37-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5c37-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="e5c37-115">Puntatore a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="e5c37-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c37-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5c37-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5c37-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e5c37-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e5c37-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e5c37-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e5c37-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e5c37-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5c37-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c37-120">Requirements</span></span>



| <span data-ttu-id="e5c37-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c37-121">Requirement</span></span> | <span data-ttu-id="e5c37-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c37-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c37-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c37-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c37-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c37-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e5c37-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5c37-125">Library</span></span><br/> | <dl> <span data-ttu-id="e5c37-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e5c37-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c37-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c37-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="e5c37-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

