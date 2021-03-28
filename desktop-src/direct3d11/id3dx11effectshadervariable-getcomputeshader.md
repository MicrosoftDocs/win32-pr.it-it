---
title: Metodo ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect. h)
description: Ottenere un compute shader.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Metodo GetComputeShader Direct3D 11
- Metodo GetComputeShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235224"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a><span data-ttu-id="1c85b-106">Metodo ID3DX11EffectShaderVariable:: GetComputeShader</span><span class="sxs-lookup"><span data-stu-id="1c85b-106">ID3DX11EffectShaderVariable::GetComputeShader method</span></span>

<span data-ttu-id="1c85b-107">Ottenere un compute shader.</span><span class="sxs-lookup"><span data-stu-id="1c85b-107">Get a compute shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c85b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c85b-108">Syntax</span></span>


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="1c85b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c85b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c85b-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="1c85b-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="1c85b-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c85b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c85b-112">Indice del compute shader.</span><span class="sxs-lookup"><span data-stu-id="1c85b-112">Index of the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="1c85b-113">*PPP*</span><span class="sxs-lookup"><span data-stu-id="1c85b-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="1c85b-114">Tipo: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="1c85b-114">Type: **[**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span></span>

<span data-ttu-id="1c85b-115">Puntatore a un puntatore [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) che verrà impostato su compute shader al ritorno.</span><span class="sxs-lookup"><span data-stu-id="1c85b-115">Pointer to an [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) pointer that will be set to the compute shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c85b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c85b-116">Return value</span></span>

<span data-ttu-id="1c85b-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c85b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c85b-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1c85b-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c85b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c85b-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c85b-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="1c85b-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1c85b-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="1c85b-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1c85b-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1c85b-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c85b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c85b-123">Requirements</span></span>



| <span data-ttu-id="1c85b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c85b-124">Requirement</span></span> | <span data-ttu-id="1c85b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1c85b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c85b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c85b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1c85b-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c85b-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1c85b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c85b-128">Library</span></span><br/> | <dl> <span data-ttu-id="1c85b-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="1c85b-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c85b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c85b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c85b-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="1c85b-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

