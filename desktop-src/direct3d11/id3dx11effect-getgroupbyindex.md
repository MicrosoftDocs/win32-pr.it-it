---
title: Metodo ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
description: Ottiene un effetto Group by index.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Metodo GetGroupByIndex Direct3D 11
- Metodo GetGroupByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetGroupByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969459"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="8923b-106">Metodo ID3DX11Effect:: GetGroupByIndex</span><span class="sxs-lookup"><span data-stu-id="8923b-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="8923b-107">Ottiene un effetto Group by index.</span><span class="sxs-lookup"><span data-stu-id="8923b-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8923b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8923b-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="8923b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8923b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8923b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="8923b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8923b-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8923b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8923b-112">Indice del gruppo di effetti.</span><span class="sxs-lookup"><span data-stu-id="8923b-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8923b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8923b-113">Return value</span></span>

<span data-ttu-id="8923b-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="8923b-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="8923b-115">Puntatore a un'interfaccia [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="8923b-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="8923b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8923b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8923b-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="8923b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8923b-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8923b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8923b-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8923b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8923b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8923b-120">Requirements</span></span>



| <span data-ttu-id="8923b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8923b-121">Requirement</span></span> | <span data-ttu-id="8923b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8923b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8923b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8923b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8923b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8923b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8923b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8923b-125">Library</span></span><br/> | <dl> <span data-ttu-id="8923b-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="8923b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8923b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8923b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8923b-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="8923b-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

