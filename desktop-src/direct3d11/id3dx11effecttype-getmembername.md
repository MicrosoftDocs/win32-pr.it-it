---
title: Metodo GetMemberName di ID3DX11EffectType (D3dx11effect. h)
description: Ottiene il nome di un membro.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Metodo GetMemberName Direct3D 11
- Metodo GetMemberName Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, Metodo GetMemberName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355169"
---
# <a name="id3dx11effecttypegetmembername-method"></a><span data-ttu-id="db7ff-106">Metodo ID3DX11EffectType:: GetMemberName</span><span class="sxs-lookup"><span data-stu-id="db7ff-106">ID3DX11EffectType::GetMemberName method</span></span>

<span data-ttu-id="db7ff-107">Ottiene il nome di un membro.</span><span class="sxs-lookup"><span data-stu-id="db7ff-107">Get the name of a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db7ff-108">Syntax</span></span>


```C++
LPCSTR GetMemberName(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="db7ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="db7ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7ff-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="db7ff-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="db7ff-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db7ff-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db7ff-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="db7ff-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db7ff-113">Return value</span></span>

<span data-ttu-id="db7ff-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db7ff-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db7ff-115">Nome del membro.</span><span class="sxs-lookup"><span data-stu-id="db7ff-115">The name of the member.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7ff-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="db7ff-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="db7ff-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="db7ff-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db7ff-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="db7ff-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db7ff-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="db7ff-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db7ff-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db7ff-120">Requirements</span></span>



| <span data-ttu-id="db7ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7ff-121">Requirement</span></span> | <span data-ttu-id="db7ff-122">Valore</span><span class="sxs-lookup"><span data-stu-id="db7ff-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7ff-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db7ff-123">Header</span></span><br/>  | <dl> <span data-ttu-id="db7ff-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7ff-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db7ff-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="db7ff-125">Library</span></span><br/> | <dl> <span data-ttu-id="db7ff-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="db7ff-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7ff-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db7ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7ff-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="db7ff-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

