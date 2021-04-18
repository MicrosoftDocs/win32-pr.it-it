---
description: Disassembla uno shader.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Funzione D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322711"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="b3a0b-103">D3DXDisassembleShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="b3a0b-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="b3a0b-104">Disassembla uno shader.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="b3a0b-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="b3a0b-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b3a0b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3a0b-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="b3a0b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3a0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a0b-108">*pShader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a0b-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a0b-109">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3a0b-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3a0b-110">Puntatore a un buffer di memoria che contiene i dati dello shader.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="b3a0b-111">*EnableColorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a0b-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a0b-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3a0b-113">Abilitare il codice colore per semplificare la lettura del Disassembly.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="b3a0b-114">*pComments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a0b-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a0b-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3a0b-116">Stringa di commento facoltativa con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="b3a0b-117">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3a0b-118">*ppDisassembly* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3a0b-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a0b-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3a0b-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b3a0b-120">Restituisce un buffer contenente lo shader disassemblato.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="b3a0b-121">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b3a0b-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a0b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3a0b-122">Return value</span></span>

<span data-ttu-id="b3a0b-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3a0b-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3a0b-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a0b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3a0b-126">Requirements</span></span>



| <span data-ttu-id="b3a0b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a0b-127">Requirement</span></span> | <span data-ttu-id="b3a0b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b3a0b-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a0b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3a0b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a0b-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a0b-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3a0b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3a0b-131">Library</span></span><br/> | <dl> <span data-ttu-id="b3a0b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3a0b-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3a0b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3a0b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a0b-134">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="b3a0b-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
