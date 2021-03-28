---
title: Metodo ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect. h)
description: Ottenere un pixel shader.
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- Metodo GetPixelShader Direct3D 11
- Metodo GetPixelShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetPixelShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531026"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a><span data-ttu-id="32ea6-106">Metodo ID3DX11EffectShaderVariable:: GetPixelShader</span><span class="sxs-lookup"><span data-stu-id="32ea6-106">ID3DX11EffectShaderVariable::GetPixelShader method</span></span>

<span data-ttu-id="32ea6-107">Ottenere un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="32ea6-107">Get a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ea6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32ea6-108">Syntax</span></span>


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="32ea6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="32ea6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ea6-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="32ea6-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="32ea6-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="32ea6-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="32ea6-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="32ea6-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="32ea6-113">*PPP*</span><span class="sxs-lookup"><span data-stu-id="32ea6-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="32ea6-114">Tipo: **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="32ea6-114">Type: **[**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span></span>

<span data-ttu-id="32ea6-115">Puntatore a un puntatore [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) che verrà impostato sulla pixel shader alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="32ea6-115">A pointer to an [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) pointer that will be set to the pixel shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ea6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32ea6-116">Return value</span></span>

<span data-ttu-id="32ea6-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32ea6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32ea6-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="32ea6-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32ea6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="32ea6-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32ea6-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="32ea6-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="32ea6-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="32ea6-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="32ea6-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="32ea6-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32ea6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32ea6-123">Requirements</span></span>



| <span data-ttu-id="32ea6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ea6-124">Requirement</span></span> | <span data-ttu-id="32ea6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="32ea6-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ea6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32ea6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="32ea6-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ea6-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="32ea6-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="32ea6-128">Library</span></span><br/> | <dl> <span data-ttu-id="32ea6-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="32ea6-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ea6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32ea6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ea6-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="32ea6-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

