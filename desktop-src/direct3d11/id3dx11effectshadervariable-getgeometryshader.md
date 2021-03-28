---
title: Metodo ID3DX11EffectShaderVariable GetGeometryShader (D3dx11effect. h)
description: Ottenere un geometry shader.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- Metodo GetGeometryShader Direct3D 11
- Metodo GetGeometryShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetGeometryShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30478d84e0048ff7a56e5bd8faee8d50548417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355734"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a><span data-ttu-id="27263-106">Metodo ID3DX11EffectShaderVariable:: GetGeometryShader</span><span class="sxs-lookup"><span data-stu-id="27263-106">ID3DX11EffectShaderVariable::GetGeometryShader method</span></span>

<span data-ttu-id="27263-107">Ottenere un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="27263-107">Get a geometry shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="27263-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27263-108">Syntax</span></span>


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a><span data-ttu-id="27263-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27263-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27263-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="27263-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="27263-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="27263-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="27263-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="27263-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="27263-113">*ppGS*</span><span class="sxs-lookup"><span data-stu-id="27263-113">*ppGS*</span></span> 
</dt> <dd>

<span data-ttu-id="27263-114">Tipo: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="27263-114">Type: **[**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span></span>

<span data-ttu-id="27263-115">Puntatore a un puntatore [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) che verrà impostato sulla geometria dello shader al ritorno.</span><span class="sxs-lookup"><span data-stu-id="27263-115">A pointer to an [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) pointer that will be set to the geometry shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27263-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27263-116">Return value</span></span>

<span data-ttu-id="27263-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27263-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27263-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="27263-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27263-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="27263-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27263-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="27263-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="27263-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="27263-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="27263-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="27263-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27263-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27263-123">Requirements</span></span>



| <span data-ttu-id="27263-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27263-124">Requirement</span></span> | <span data-ttu-id="27263-125">Valore</span><span class="sxs-lookup"><span data-stu-id="27263-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27263-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27263-126">Header</span></span><br/>  | <dl> <span data-ttu-id="27263-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="27263-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="27263-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="27263-128">Library</span></span><br/> | <dl> <span data-ttu-id="27263-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="27263-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27263-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27263-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27263-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="27263-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

