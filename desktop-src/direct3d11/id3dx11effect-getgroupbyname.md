---
title: Metodo GetGroupByName di ID3DX11Effect (D3dx11effect. h)
description: Ottiene un gruppo di effetti per nome.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Metodo GetGroupByName Direct3D 11
- Metodo GetGroupByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetGroupByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996116"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="73801-106">Metodo ID3DX11Effect:: GetGroupByName</span><span class="sxs-lookup"><span data-stu-id="73801-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="73801-107">Ottiene un gruppo di effetti per nome.</span><span class="sxs-lookup"><span data-stu-id="73801-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="73801-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73801-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="73801-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="73801-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73801-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="73801-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="73801-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73801-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="73801-112">Nome del gruppo di effetti.</span><span class="sxs-lookup"><span data-stu-id="73801-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73801-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73801-113">Return value</span></span>

<span data-ttu-id="73801-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="73801-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="73801-115">Puntatore a un'interfaccia [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="73801-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="73801-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="73801-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73801-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="73801-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="73801-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="73801-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="73801-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="73801-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73801-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73801-120">Requirements</span></span>



| <span data-ttu-id="73801-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="73801-121">Requirement</span></span> | <span data-ttu-id="73801-122">Valore</span><span class="sxs-lookup"><span data-stu-id="73801-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73801-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73801-123">Header</span></span><br/>  | <dl> <span data-ttu-id="73801-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="73801-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="73801-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="73801-125">Library</span></span><br/> | <dl> <span data-ttu-id="73801-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="73801-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73801-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73801-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73801-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="73801-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

