---
description: Restituisce la versione shader dello shader compilato.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Funzione D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132338"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="96ecc-103">D3DXGetShaderVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="96ecc-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="96ecc-104">Restituisce la versione shader dello shader compilato.</span><span class="sxs-lookup"><span data-stu-id="96ecc-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ecc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96ecc-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="96ecc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96ecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ecc-107">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96ecc-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ecc-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96ecc-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96ecc-109">Puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="96ecc-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ecc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96ecc-110">Return value</span></span>

<span data-ttu-id="96ecc-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96ecc-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96ecc-112">Restituisce la versione shader dello shader specificato oppure zero se la funzione shader è **null**.</span><span class="sxs-lookup"><span data-stu-id="96ecc-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ecc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96ecc-113">Requirements</span></span>



| <span data-ttu-id="96ecc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ecc-114">Requirement</span></span> | <span data-ttu-id="96ecc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="96ecc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ecc-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96ecc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="96ecc-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ecc-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="96ecc-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="96ecc-118">Library</span></span><br/> | <dl> <span data-ttu-id="96ecc-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96ecc-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="96ecc-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ecc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ecc-121">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="96ecc-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
