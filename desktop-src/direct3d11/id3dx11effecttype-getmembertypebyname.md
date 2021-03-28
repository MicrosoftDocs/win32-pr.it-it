---
title: Metodo ID3DX11EffectType GetMemberTypeByName (D3dx11effect. h)
description: Ottenere un tipo di membro in base al nome.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Metodo GetMemberTypeByName Direct3D 11
- Metodo GetMemberTypeByName Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995852"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="95592-106">Metodo ID3DX11EffectType:: GetMemberTypeByName</span><span class="sxs-lookup"><span data-stu-id="95592-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="95592-107">Ottenere un tipo di membro in base al nome.</span><span class="sxs-lookup"><span data-stu-id="95592-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="95592-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95592-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="95592-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95592-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95592-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="95592-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="95592-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95592-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95592-112">Nome di un membro.</span><span class="sxs-lookup"><span data-stu-id="95592-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95592-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95592-113">Return value</span></span>

<span data-ttu-id="95592-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="95592-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="95592-115">Puntatore a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="95592-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95592-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="95592-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95592-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="95592-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95592-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="95592-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95592-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95592-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95592-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95592-120">Requirements</span></span>



| <span data-ttu-id="95592-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="95592-121">Requirement</span></span> | <span data-ttu-id="95592-122">Valore</span><span class="sxs-lookup"><span data-stu-id="95592-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95592-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95592-123">Header</span></span><br/>  | <dl> <span data-ttu-id="95592-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95592-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95592-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="95592-125">Library</span></span><br/> | <dl> <span data-ttu-id="95592-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="95592-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95592-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95592-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95592-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="95592-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

