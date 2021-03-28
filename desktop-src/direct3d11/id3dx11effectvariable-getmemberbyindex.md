---
title: Metodo ID3DX11EffectVariable GetMemberByIndex (D3dx11effect. h)
description: Ottiene un membro della struttura in base all'indice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Metodo GetMemberByIndex Direct3D 11
- Metodo GetMemberByIndex Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetMemberByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995978"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a><span data-ttu-id="5fc80-106">Metodo ID3DX11EffectVariable:: GetMemberByIndex</span><span class="sxs-lookup"><span data-stu-id="5fc80-106">ID3DX11EffectVariable::GetMemberByIndex method</span></span>

<span data-ttu-id="5fc80-107">Ottiene un membro della struttura in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="5fc80-107">Get a structure member by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc80-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fc80-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5fc80-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fc80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc80-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5fc80-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc80-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fc80-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fc80-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="5fc80-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fc80-113">Return value</span></span>

<span data-ttu-id="5fc80-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="5fc80-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="5fc80-115">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="5fc80-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc80-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fc80-116">Remarks</span></span>

<span data-ttu-id="5fc80-117">Se la variabile Effect è una struttura, usare questo metodo per cercare un membro in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="5fc80-117">If the effect variable is an structure, use this method to look up a member by index.</span></span>

> [!Note]  
> <span data-ttu-id="5fc80-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="5fc80-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5fc80-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5fc80-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5fc80-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5fc80-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5fc80-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fc80-121">Requirements</span></span>



| <span data-ttu-id="5fc80-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc80-122">Requirement</span></span> | <span data-ttu-id="5fc80-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5fc80-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc80-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fc80-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5fc80-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc80-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5fc80-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fc80-126">Library</span></span><br/> | <dl> <span data-ttu-id="5fc80-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="5fc80-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc80-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fc80-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc80-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="5fc80-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

