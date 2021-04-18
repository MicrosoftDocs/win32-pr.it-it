---
description: Restituisce le dimensioni in byte del codice byte dello shader.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Funzione D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322655"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="aa428-103">D3DXGetShaderSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="aa428-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="aa428-104">Restituisce le dimensioni in byte del codice byte dello shader.</span><span class="sxs-lookup"><span data-stu-id="aa428-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa428-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa428-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="aa428-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa428-107">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa428-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa428-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aa428-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aa428-109">Puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="aa428-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa428-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa428-110">Return value</span></span>

<span data-ttu-id="aa428-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa428-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa428-112">Restituisce le dimensioni in byte del codice byte dello shader.</span><span class="sxs-lookup"><span data-stu-id="aa428-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa428-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa428-113">Requirements</span></span>



| <span data-ttu-id="aa428-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa428-114">Requirement</span></span> | <span data-ttu-id="aa428-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aa428-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa428-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa428-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aa428-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa428-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="aa428-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa428-118">Library</span></span><br/> | <dl> <span data-ttu-id="aa428-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa428-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aa428-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa428-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa428-121">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="aa428-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
