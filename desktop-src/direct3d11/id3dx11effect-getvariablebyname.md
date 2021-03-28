---
title: Metodo ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Ottenere una variabile in base al nome.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Metodo GetVariableByName Direct3D 11
- Metodo GetVariableByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996095"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="0e47c-106">Metodo ID3DX11Effect:: GetVariableByName</span><span class="sxs-lookup"><span data-stu-id="0e47c-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="0e47c-107">Ottenere una variabile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="0e47c-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e47c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e47c-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="0e47c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e47c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e47c-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="0e47c-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="0e47c-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e47c-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0e47c-112">Nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="0e47c-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e47c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e47c-113">Return value</span></span>

<span data-ttu-id="0e47c-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e47c-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="0e47c-115">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0e47c-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="0e47c-116">Restituisce una variabile non valida se non è possibile trovare il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="0e47c-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e47c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e47c-117">Remarks</span></span>

<span data-ttu-id="0e47c-118">Un effetto può contenere una o più variabili.</span><span class="sxs-lookup"><span data-stu-id="0e47c-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="0e47c-119">Le variabili al di fuori di una tecnica sono considerate globali per tutti gli effetti, quelle situate all'interno di una tecnica sono locali a tale tecnica.</span><span class="sxs-lookup"><span data-stu-id="0e47c-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="0e47c-120">È possibile accedere a una variabile Effect usando il nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="0e47c-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="0e47c-121">Il metodo restituisce un puntatore a un' [**interfaccia della variabile di effetto**](id3dx11effectvariable.md) indipendentemente dal fatto che venga trovata o meno una variabile.</span><span class="sxs-lookup"><span data-stu-id="0e47c-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="0e47c-122">È necessario chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se il nome esiste o meno.</span><span class="sxs-lookup"><span data-stu-id="0e47c-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="0e47c-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="0e47c-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0e47c-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0e47c-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0e47c-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0e47c-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e47c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e47c-126">Requirements</span></span>



| <span data-ttu-id="0e47c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e47c-127">Requirement</span></span> | <span data-ttu-id="0e47c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0e47c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e47c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e47c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0e47c-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e47c-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0e47c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e47c-131">Library</span></span><br/> | <dl> <span data-ttu-id="0e47c-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="0e47c-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e47c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e47c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e47c-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="0e47c-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

