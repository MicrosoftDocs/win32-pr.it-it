---
title: Metodo ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Ottenere una variabile in base alla semantica.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Metodo GetVariableBySemantic Direct3D 11
- Metodo GetVariableBySemantic Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235148"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a><span data-ttu-id="ab61d-106">Metodo ID3DX11Effect:: GetVariableBySemantic</span><span class="sxs-lookup"><span data-stu-id="ab61d-106">ID3DX11Effect::GetVariableBySemantic method</span></span>

<span data-ttu-id="ab61d-107">Ottenere una variabile in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="ab61d-107">Get a variable by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab61d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab61d-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="ab61d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab61d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab61d-110">*Semantica*</span><span class="sxs-lookup"><span data-stu-id="ab61d-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="ab61d-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab61d-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab61d-112">Nome semantico.</span><span class="sxs-lookup"><span data-stu-id="ab61d-112">The semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab61d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab61d-113">Return value</span></span>

<span data-ttu-id="ab61d-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab61d-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="ab61d-115">Puntatore alla variabile Effect indicata dalla semantica.</span><span class="sxs-lookup"><span data-stu-id="ab61d-115">A pointer to the effect variable indicated by the Semantic.</span></span> <span data-ttu-id="ab61d-116">Vedere [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="ab61d-116">See [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab61d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab61d-117">Remarks</span></span>

<span data-ttu-id="ab61d-118">Ogni variabile Effect può avere una semantica collegata, ovvero una stringa di metadati definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ab61d-118">Each effect variable can have a semantic attached, which is a user defined metadata string.</span></span> <span data-ttu-id="ab61d-119">Alcune [semantiche dei valori di sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) sono parole riservate che attivano funzionalità predefinite per fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab61d-119">Some [system-value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) are reserved words that trigger built in functionality by pipeline stages.</span></span>

<span data-ttu-id="ab61d-120">Il metodo restituisce un puntatore a un' [**interfaccia di variabile di effetto**](id3dx11effectvariable.md) se non viene trovata una variabile. è possibile chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se la semantica esiste o meno.</span><span class="sxs-lookup"><span data-stu-id="ab61d-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the semantic exists.</span></span>

> [!Note]  
> <span data-ttu-id="ab61d-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="ab61d-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ab61d-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ab61d-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ab61d-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ab61d-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab61d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab61d-124">Requirements</span></span>



| <span data-ttu-id="ab61d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab61d-125">Requirement</span></span> | <span data-ttu-id="ab61d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ab61d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab61d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab61d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ab61d-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab61d-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ab61d-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab61d-129">Library</span></span><br/> | <dl> <span data-ttu-id="ab61d-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="ab61d-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab61d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab61d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab61d-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="ab61d-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

