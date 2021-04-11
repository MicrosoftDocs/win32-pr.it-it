---
description: Crea un oggetto shader di trama dallo shader compilato.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Funzione D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354904"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="e9a1c-103">D3DXCreateTextureShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9a1c-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="e9a1c-104">Crea un oggetto shader di trama dallo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a1c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9a1c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="e9a1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a1c-107">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a1c-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a1c-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9a1c-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9a1c-109">Puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="e9a1c-110">*ppTextureShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9a1c-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a1c-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9a1c-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="e9a1c-112">Restituisce un oggetto [**ID3DXTextureShader**](id3dxtextureshader.md) che può essere usato per compilare in modo procedurale il contenuto di una trama usando le funzioni [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a1c-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a1c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9a1c-113">Return value</span></span>

<span data-ttu-id="e9a1c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9a1c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9a1c-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9a1c-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a1c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9a1c-117">Requirements</span></span>



| <span data-ttu-id="e9a1c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a1c-118">Requirement</span></span> | <span data-ttu-id="e9a1c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e9a1c-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a1c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9a1c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e9a1c-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9a1c-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e9a1c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9a1c-122">Library</span></span><br/> | <dl> <span data-ttu-id="e9a1c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9a1c-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e9a1c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9a1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a1c-125">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="e9a1c-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
