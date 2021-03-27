---
title: Metodo ID3DX11EffectShaderVariable GetInputSignatureElementDesc (D3dx11effect. h)
description: Ottenere una descrizione della firma di input.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- Metodo GetInputSignatureElementDesc Direct3D 11
- Metodo GetInputSignatureElementDesc Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetInputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132422"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a><span data-ttu-id="1f5a5-106">Metodo ID3DX11EffectShaderVariable:: GetInputSignatureElementDesc</span><span class="sxs-lookup"><span data-stu-id="1f5a5-106">ID3DX11EffectShaderVariable::GetInputSignatureElementDesc method</span></span>

<span data-ttu-id="1f5a5-107">Ottenere una descrizione della firma di input.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-107">Get an input-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f5a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f5a5-108">Syntax</span></span>


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="1f5a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f5a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f5a5-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="1f5a5-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="1f5a5-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1f5a5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1f5a5-112">Indice dello shader in base zero.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="1f5a5-113">*elemento*</span><span class="sxs-lookup"><span data-stu-id="1f5a5-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="1f5a5-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1f5a5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1f5a5-115">Indice in base zero dell'elemento shader.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-115">A zero-based shader-element index.</span></span>

</dd> <dt>

<span data-ttu-id="1f5a5-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="1f5a5-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="1f5a5-117">Tipo: **[ **\_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="1f5a5-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="1f5a5-118">Puntatore a una descrizione del parametro (vedere [**il \_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="1f5a5-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f5a5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f5a5-119">Return value</span></span>

<span data-ttu-id="1f5a5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f5a5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f5a5-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1f5a5-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f5a5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f5a5-122">Remarks</span></span>

<span data-ttu-id="1f5a5-123">Un effetto contiene uno o più shader; ogni shader ha una firma di input e di output. ogni firma contiene uno o più elementi (o parametri).</span><span class="sxs-lookup"><span data-stu-id="1f5a5-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="1f5a5-124">L'indice dello shader identifica lo shader e l'indice dell'elemento identifica l'elemento (o parametro) nella firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="1f5a5-125">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1f5a5-126">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="1f5a5-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1f5a5-127">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1f5a5-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f5a5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f5a5-128">Requirements</span></span>



| <span data-ttu-id="1f5a5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f5a5-129">Requirement</span></span> | <span data-ttu-id="1f5a5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1f5a5-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5a5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f5a5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1f5a5-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f5a5-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1f5a5-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f5a5-133">Library</span></span><br/> | <dl> <span data-ttu-id="1f5a5-134"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="1f5a5-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f5a5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f5a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f5a5-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="1f5a5-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

