---
title: Metodo ID3DX11EffectType GetMemberTypeByIndex (D3dx11effect. h)
description: Ottenere un tipo di membro in base all'indice.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Metodo GetMemberTypeByIndex Direct3D 11
- Metodo GetMemberTypeByIndex Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo GetMemberTypeByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530967"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="bd5b9-106">Metodo ID3DX11EffectType:: GetMemberTypeByIndex</span><span class="sxs-lookup"><span data-stu-id="bd5b9-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="bd5b9-107">Ottenere un tipo di membro in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5b9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd5b9-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="bd5b9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd5b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5b9-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="bd5b9-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="bd5b9-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd5b9-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd5b9-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5b9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd5b9-113">Return value</span></span>

<span data-ttu-id="bd5b9-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd5b9-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="bd5b9-115">Puntatore a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd5b9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd5b9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd5b9-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bd5b9-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bd5b9-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd5b9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd5b9-120">Requirements</span></span>



| <span data-ttu-id="bd5b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd5b9-121">Requirement</span></span> | <span data-ttu-id="bd5b9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bd5b9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5b9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd5b9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bd5b9-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd5b9-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bd5b9-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd5b9-125">Library</span></span><br/> | <dl> <span data-ttu-id="bd5b9-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="bd5b9-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5b9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd5b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5b9-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="bd5b9-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

