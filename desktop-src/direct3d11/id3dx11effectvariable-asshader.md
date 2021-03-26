---
title: Metodo ID3DX11EffectVariable AsShader (D3dx11effect. h)
description: Ottiene una variabile shader.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Metodo AsShader Direct3D 11
- Metodo AsShader Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsShader
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996074"
---
# <a name="id3dx11effectvariableasshader-method"></a><span data-ttu-id="492cc-106">Metodo ID3DX11EffectVariable:: AsShader</span><span class="sxs-lookup"><span data-stu-id="492cc-106">ID3DX11EffectVariable::AsShader method</span></span>

<span data-ttu-id="492cc-107">Ottiene una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="492cc-107">Get a shader variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="492cc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="492cc-108">Syntax</span></span>


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a><span data-ttu-id="492cc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="492cc-109">Parameters</span></span>

<span data-ttu-id="492cc-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="492cc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="492cc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="492cc-111">Return value</span></span>

<span data-ttu-id="492cc-112">Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="492cc-112">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

<span data-ttu-id="492cc-113">Puntatore a una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="492cc-113">A pointer to a shader variable.</span></span> <span data-ttu-id="492cc-114">Vedere [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span><span class="sxs-lookup"><span data-stu-id="492cc-114">See [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="492cc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="492cc-115">Remarks</span></span>

<span data-ttu-id="492cc-116">AsShader restituisce una versione della variabile Effect specializzata in una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="492cc-116">AsShader returns a version of the effect variable that has been specialized to a shader variable.</span></span> <span data-ttu-id="492cc-117">Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati shader.</span><span class="sxs-lookup"><span data-stu-id="492cc-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.</span></span>

<span data-ttu-id="492cc-118">Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="492cc-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="492cc-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="492cc-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="492cc-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="492cc-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="492cc-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="492cc-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="492cc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="492cc-122">Requirements</span></span>



| <span data-ttu-id="492cc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="492cc-123">Requirement</span></span> | <span data-ttu-id="492cc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="492cc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="492cc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="492cc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="492cc-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="492cc-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="492cc-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="492cc-127">Library</span></span><br/> | <dl> <span data-ttu-id="492cc-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="492cc-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="492cc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="492cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="492cc-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="492cc-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





