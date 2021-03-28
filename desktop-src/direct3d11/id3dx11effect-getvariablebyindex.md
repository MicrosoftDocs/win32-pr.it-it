---
title: Metodo ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Ottiene una variabile in base all'indice.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Metodo GetVariableByIndex Direct3D 11
- Metodo GetVariableByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996101"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="72822-106">Metodo ID3DX11Effect:: GetVariableByIndex</span><span class="sxs-lookup"><span data-stu-id="72822-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="72822-107">Ottiene una variabile in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="72822-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="72822-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72822-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="72822-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="72822-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72822-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="72822-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="72822-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="72822-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="72822-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="72822-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72822-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72822-113">Return value</span></span>

<span data-ttu-id="72822-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="72822-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="72822-115">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="72822-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="72822-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="72822-116">Remarks</span></span>

<span data-ttu-id="72822-117">Un effetto può contenere una o più variabili.</span><span class="sxs-lookup"><span data-stu-id="72822-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="72822-118">Le variabili al di fuori di una tecnica sono considerate globali per tutti gli effetti, quelle situate all'interno di una tecnica sono locali a tale tecnica.</span><span class="sxs-lookup"><span data-stu-id="72822-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="72822-119">È possibile accedere a qualsiasi variabile locale di effetto non statico usando il nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="72822-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="72822-120">Il metodo restituisce un puntatore a un' [**interfaccia di variabile di effetto**](id3dx11effectvariable.md) se non viene trovata una variabile. è possibile chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se l'indice esiste o meno.</span><span class="sxs-lookup"><span data-stu-id="72822-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="72822-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="72822-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="72822-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="72822-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="72822-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="72822-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72822-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72822-124">Requirements</span></span>



| <span data-ttu-id="72822-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="72822-125">Requirement</span></span> | <span data-ttu-id="72822-126">Valore</span><span class="sxs-lookup"><span data-stu-id="72822-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72822-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72822-127">Header</span></span><br/>  | <dl> <span data-ttu-id="72822-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="72822-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="72822-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="72822-129">Library</span></span><br/> | <dl> <span data-ttu-id="72822-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="72822-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72822-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72822-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72822-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="72822-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

