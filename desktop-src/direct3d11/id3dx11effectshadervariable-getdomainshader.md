---
title: Metodo ID3DX11EffectShaderVariable GetDomainShader (D3dx11effect. h)
description: Ottenere un Domain shader.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Metodo GetDomainShader Direct3D 11
- Metodo GetDomainShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetDomainShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235223"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a><span data-ttu-id="a2c93-106">Metodo ID3DX11EffectShaderVariable:: GetDomainShader</span><span class="sxs-lookup"><span data-stu-id="a2c93-106">ID3DX11EffectShaderVariable::GetDomainShader method</span></span>

<span data-ttu-id="a2c93-107">Ottenere un Domain shader.</span><span class="sxs-lookup"><span data-stu-id="a2c93-107">Get a domain shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c93-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2c93-108">Syntax</span></span>


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="a2c93-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2c93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c93-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="a2c93-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c93-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2c93-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2c93-112">Indice dello shader del dominio.</span><span class="sxs-lookup"><span data-stu-id="a2c93-112">Index of the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2c93-113">*PPP*</span><span class="sxs-lookup"><span data-stu-id="a2c93-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c93-114">Tipo: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="a2c93-114">Type: **[**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span></span>

<span data-ttu-id="a2c93-115">Puntatore a un puntatore [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) che verrà impostato sullo shader del dominio al ritorno.</span><span class="sxs-lookup"><span data-stu-id="a2c93-115">Pointer to an [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) pointer that will be set to the domain shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c93-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2c93-116">Return value</span></span>

<span data-ttu-id="a2c93-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2c93-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2c93-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a2c93-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c93-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2c93-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2c93-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a2c93-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a2c93-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a2c93-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a2c93-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a2c93-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2c93-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2c93-123">Requirements</span></span>



| <span data-ttu-id="a2c93-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c93-124">Requirement</span></span> | <span data-ttu-id="a2c93-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a2c93-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c93-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2c93-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a2c93-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2c93-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a2c93-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2c93-128">Library</span></span><br/> | <dl> <span data-ttu-id="a2c93-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a2c93-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c93-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2c93-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c93-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="a2c93-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

