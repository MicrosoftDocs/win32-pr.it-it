---
description: Cerca uno shader per un commento specifico. Il commento è identificato da un codice di quattro caratteri (FOURCC) nel primo valore DWORD del commento.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Funzione D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322693"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="984f7-104">D3DXFindShaderComment (funzione)</span><span class="sxs-lookup"><span data-stu-id="984f7-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="984f7-105">Cerca uno shader per un commento specifico.</span><span class="sxs-lookup"><span data-stu-id="984f7-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="984f7-106">Il commento è identificato da un codice di quattro caratteri (FOURCC) nel primo valore DWORD del commento.</span><span class="sxs-lookup"><span data-stu-id="984f7-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="984f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="984f7-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="984f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="984f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="984f7-109">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984f7-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984f7-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="984f7-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="984f7-111">Puntatore al flusso DWORD della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="984f7-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="984f7-112">*Fourcc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984f7-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984f7-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984f7-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984f7-114">Codice FOURCC che identifica il blocco di commento.</span><span class="sxs-lookup"><span data-stu-id="984f7-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="984f7-115">Vedere [formati FourCC](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="984f7-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="984f7-116">*ppData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984f7-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984f7-117">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="984f7-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="984f7-118">Restituisce un puntatore ai dati di commento, escluso il token di commento e il codice FOURCC.</span><span class="sxs-lookup"><span data-stu-id="984f7-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="984f7-119">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="984f7-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984f7-120">*pSizeInBytes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="984f7-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="984f7-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="984f7-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="984f7-122">Restituisce le dimensioni in byte dei dati di commento.</span><span class="sxs-lookup"><span data-stu-id="984f7-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="984f7-123">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="984f7-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="984f7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="984f7-124">Return value</span></span>

<span data-ttu-id="984f7-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="984f7-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="984f7-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="984f7-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="984f7-127">Se il commento non viene trovato e non si sono verificati altri errori, \_ viene restituito S false.</span><span class="sxs-lookup"><span data-stu-id="984f7-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="984f7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="984f7-128">Requirements</span></span>



| <span data-ttu-id="984f7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="984f7-129">Requirement</span></span> | <span data-ttu-id="984f7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="984f7-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="984f7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="984f7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="984f7-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="984f7-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="984f7-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="984f7-133">Library</span></span><br/> | <dl> <span data-ttu-id="984f7-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="984f7-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="984f7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="984f7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984f7-136">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="984f7-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
