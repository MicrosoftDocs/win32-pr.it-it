---
title: Metodo ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect. h)
description: Ottenere una descrizione della firma costante della patch.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Metodo GetPatchConstantSignatureElementDesc Direct3D 11
- Metodo GetPatchConstantSignatureElementDesc Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetPatchConstantSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996161"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="e00bc-106">Metodo ID3DX11EffectShaderVariable:: GetPatchConstantSignatureElementDesc</span><span class="sxs-lookup"><span data-stu-id="e00bc-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="e00bc-107">Ottenere una descrizione della firma costante della patch.</span><span class="sxs-lookup"><span data-stu-id="e00bc-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e00bc-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="e00bc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e00bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00bc-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="e00bc-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e00bc-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e00bc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e00bc-112">Indice dello shader in base zero.</span><span class="sxs-lookup"><span data-stu-id="e00bc-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="e00bc-113">*elemento*</span><span class="sxs-lookup"><span data-stu-id="e00bc-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="e00bc-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e00bc-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e00bc-115">Indice di elemento in base zero.</span><span class="sxs-lookup"><span data-stu-id="e00bc-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="e00bc-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="e00bc-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="e00bc-117">Tipo: **[ **\_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="e00bc-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="e00bc-118">Puntatore a una descrizione del parametro (vedere [**il \_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="e00bc-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00bc-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e00bc-119">Return value</span></span>

<span data-ttu-id="e00bc-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e00bc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e00bc-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e00bc-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e00bc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e00bc-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e00bc-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e00bc-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e00bc-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e00bc-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e00bc-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e00bc-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e00bc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e00bc-126">Requirements</span></span>



| <span data-ttu-id="e00bc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00bc-127">Requirement</span></span> | <span data-ttu-id="e00bc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e00bc-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e00bc-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e00bc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e00bc-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00bc-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e00bc-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e00bc-131">Library</span></span><br/> | <dl> <span data-ttu-id="e00bc-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e00bc-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00bc-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e00bc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00bc-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="e00bc-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

