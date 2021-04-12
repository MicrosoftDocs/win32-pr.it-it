---
title: D3D11Reflect (funzione)
description: Ottiene un puntatore a un'interfaccia di Reflection.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Funzione D3D11Reflect HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132398"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="45f37-104">D3D11Reflect (funzione)</span><span class="sxs-lookup"><span data-stu-id="45f37-104">D3D11Reflect function</span></span>

<span data-ttu-id="45f37-105">Ottiene un puntatore a un'interfaccia di Reflection.</span><span class="sxs-lookup"><span data-stu-id="45f37-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f37-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45f37-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="45f37-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="45f37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f37-108">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45f37-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f37-109">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45f37-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45f37-110">Puntatore ai dati di origine come codice HLSL compilato.</span><span class="sxs-lookup"><span data-stu-id="45f37-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="45f37-111">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45f37-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f37-112">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45f37-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45f37-113">Lunghezza di *pSrcData*.</span><span class="sxs-lookup"><span data-stu-id="45f37-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="45f37-114">*ppReflector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="45f37-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45f37-115">Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="45f37-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="45f37-116">Indirizzo di un puntatore all'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .</span><span class="sxs-lookup"><span data-stu-id="45f37-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f37-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45f37-117">Return value</span></span>

<span data-ttu-id="45f37-118">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45f37-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45f37-119">Restituisce uno dei codici restituiti descritti nell'argomento [codici restituiti Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span><span class="sxs-lookup"><span data-stu-id="45f37-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="45f37-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="45f37-120">Remarks</span></span>

<span data-ttu-id="45f37-121">La funzione inline del compilatore **D3D11Reflect** è un wrapper per la funzione del compilatore [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="45f37-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="45f37-122">**D3D11Reflect** può recuperare solo un'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) da uno shader.</span><span class="sxs-lookup"><span data-stu-id="45f37-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="45f37-123">**D3DReflect** può recuperare un'interfaccia **ID3D11ShaderReflection** o un'interfaccia di Reflection direct3d 10 o Direct3D 10,1, ad esempio [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="45f37-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="45f37-124">Il codice dello shader contiene metadati che possono essere controllati tramite le API di Reflection.</span><span class="sxs-lookup"><span data-stu-id="45f37-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="45f37-125">Nel codice seguente viene illustrato come recuperare un'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) da uno shader.</span><span class="sxs-lookup"><span data-stu-id="45f37-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="45f37-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45f37-126">Requirements</span></span>



| <span data-ttu-id="45f37-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f37-127">Requirement</span></span> | <span data-ttu-id="45f37-128">Valore</span><span class="sxs-lookup"><span data-stu-id="45f37-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f37-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45f37-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45f37-130"><dt>D3DCompiler. inl</dt></span><span class="sxs-lookup"><span data-stu-id="45f37-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="45f37-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="45f37-131">Library</span></span><br/> | <dl> <span data-ttu-id="45f37-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45f37-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="45f37-133">DLL</span><span class="sxs-lookup"><span data-stu-id="45f37-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="45f37-134"><dt>\_47.dllD3dcompiler</dt></span><span class="sxs-lookup"><span data-stu-id="45f37-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f37-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45f37-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f37-136">Funzioni</span><span class="sxs-lookup"><span data-stu-id="45f37-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

