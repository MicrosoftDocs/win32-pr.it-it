---
title: Metodo ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Ottenere un indice pass-by.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Metodo GetPassByIndex Direct3D 11
- Metodo GetPassByIndex Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969471"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="f4bd8-106">Metodo ID3DX11EffectTechnique:: GetPassByIndex</span><span class="sxs-lookup"><span data-stu-id="f4bd8-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="f4bd8-107">Ottenere un indice pass-by.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4bd8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4bd8-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f4bd8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4bd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4bd8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f4bd8-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f4bd8-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f4bd8-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f4bd8-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4bd8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4bd8-113">Return value</span></span>

<span data-ttu-id="f4bd8-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4bd8-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="f4bd8-115">Puntatore a un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="f4bd8-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4bd8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4bd8-116">Remarks</span></span>

<span data-ttu-id="f4bd8-117">Una tecnica contiene uno o più passaggi. ottenere un pass usando un nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="f4bd8-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f4bd8-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f4bd8-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f4bd8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4bd8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4bd8-121">Requirements</span></span>



| <span data-ttu-id="f4bd8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4bd8-122">Requirement</span></span> | <span data-ttu-id="f4bd8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f4bd8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bd8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4bd8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f4bd8-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4bd8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f4bd8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4bd8-126">Library</span></span><br/> | <dl> <span data-ttu-id="f4bd8-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f4bd8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4bd8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4bd8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4bd8-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="f4bd8-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

