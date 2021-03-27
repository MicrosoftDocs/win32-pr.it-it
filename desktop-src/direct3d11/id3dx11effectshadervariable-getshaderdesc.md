---
title: Metodo ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione dello shader.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Metodo GetShaderDesc Direct3D 11
- Metodo GetShaderDesc Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982430"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a><span data-ttu-id="9f799-106">Metodo ID3DX11EffectShaderVariable:: GetShaderDesc</span><span class="sxs-lookup"><span data-stu-id="9f799-106">ID3DX11EffectShaderVariable::GetShaderDesc method</span></span>

<span data-ttu-id="9f799-107">Ottenere una descrizione dello shader.</span><span class="sxs-lookup"><span data-stu-id="9f799-107">Get a shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f799-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f799-108">Syntax</span></span>


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9f799-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f799-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f799-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="9f799-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="9f799-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9f799-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9f799-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="9f799-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="9f799-113">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="9f799-113">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="9f799-114">Tipo: **[ **D3DX11 \_ Effect \_ shader \_ desc**](d3dx11-effect-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f799-114">Type: **[**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)\***</span></span>

<span data-ttu-id="9f799-115">Puntatore a una descrizione dello shader (vedere [**D3DX11 \_ Effect \_ shader \_ desc**](d3dx11-effect-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="9f799-115">A pointer to a shader description (see [**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f799-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f799-116">Return value</span></span>

<span data-ttu-id="9f799-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f799-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f799-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9f799-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f799-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f799-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f799-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="9f799-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9f799-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9f799-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9f799-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9f799-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f799-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f799-123">Requirements</span></span>



| <span data-ttu-id="9f799-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f799-124">Requirement</span></span> | <span data-ttu-id="9f799-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9f799-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f799-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f799-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9f799-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f799-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9f799-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f799-128">Library</span></span><br/> | <dl> <span data-ttu-id="9f799-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="9f799-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f799-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f799-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f799-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="9f799-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

