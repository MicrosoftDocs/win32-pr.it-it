---
title: Metodo ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect. h)
description: Ottenere una descrizione della firma di output.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Metodo GetOutputSignatureElementDesc Direct3D 11
- Metodo GetOutputSignatureElementDesc Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetOutputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996164"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a><span data-ttu-id="d0975-106">Metodo ID3DX11EffectShaderVariable:: GetOutputSignatureElementDesc</span><span class="sxs-lookup"><span data-stu-id="d0975-106">ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc method</span></span>

<span data-ttu-id="d0975-107">Ottenere una descrizione della firma di output.</span><span class="sxs-lookup"><span data-stu-id="d0975-107">Get an output-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0975-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0975-108">Syntax</span></span>


```C++
HRESULT GetOutputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d0975-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0975-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0975-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="d0975-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="d0975-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0975-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0975-112">Indice dello shader in base zero.</span><span class="sxs-lookup"><span data-stu-id="d0975-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="d0975-113">*elemento*</span><span class="sxs-lookup"><span data-stu-id="d0975-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="d0975-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0975-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0975-115">Indice di elemento in base zero.</span><span class="sxs-lookup"><span data-stu-id="d0975-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="d0975-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="d0975-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d0975-117">Tipo: **[ **\_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="d0975-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="d0975-118">Puntatore a una descrizione del parametro (vedere [**il \_ parametro della firma d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="d0975-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0975-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0975-119">Return value</span></span>

<span data-ttu-id="d0975-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0975-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0975-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d0975-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0975-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0975-122">Remarks</span></span>

<span data-ttu-id="d0975-123">Un effetto contiene uno o più shader; ogni shader ha una firma di input e di output. ogni firma contiene uno o più elementi (o parametri).</span><span class="sxs-lookup"><span data-stu-id="d0975-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="d0975-124">L'indice dello shader identifica lo shader e l'indice dell'elemento identifica l'elemento (o parametro) nella firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="d0975-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="d0975-125">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="d0975-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d0975-126">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d0975-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d0975-127">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d0975-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0975-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0975-128">Requirements</span></span>



| <span data-ttu-id="d0975-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0975-129">Requirement</span></span> | <span data-ttu-id="d0975-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d0975-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0975-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0975-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d0975-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0975-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d0975-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0975-133">Library</span></span><br/> | <dl> <span data-ttu-id="d0975-134"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="d0975-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0975-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0975-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0975-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="d0975-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

