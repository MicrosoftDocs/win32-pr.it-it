---
description: Ottiene la semantica per tutti gli elementi di output dello shader.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Funzione D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530901"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="90db3-103">D3DXGetShaderOutputSemantics (funzione)</span><span class="sxs-lookup"><span data-stu-id="90db3-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="90db3-104">Ottiene la semantica per tutti gli elementi di output dello shader.</span><span class="sxs-lookup"><span data-stu-id="90db3-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="90db3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90db3-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="90db3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90db3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90db3-107">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90db3-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90db3-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="90db3-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90db3-109">Puntatore al flusso DWORD della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="90db3-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="90db3-110">*pSemantics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90db3-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90db3-111">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="90db3-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="90db3-112">Puntatore a una matrice di strutture [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="90db3-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="90db3-113">La funzione riempirà questa matrice con la semantica per ogni elemento di output a cui fa riferimento lo shader.</span><span class="sxs-lookup"><span data-stu-id="90db3-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="90db3-114">Si presuppone che questa matrice contenga almeno gli elementi MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="90db3-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="90db3-115">Tuttavia, la chiamata a **D3DXGetShaderOutputSemantics** con PSemantics = **null** restituirà il numero di elementi necessari per pcount.</span><span class="sxs-lookup"><span data-stu-id="90db3-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="90db3-116">*pcount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90db3-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90db3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90db3-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90db3-118">Restituisce il numero di elementi in pSemantics.</span><span class="sxs-lookup"><span data-stu-id="90db3-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90db3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90db3-119">Return value</span></span>

<span data-ttu-id="90db3-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90db3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90db3-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90db3-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="90db3-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="90db3-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="90db3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90db3-123">Requirements</span></span>



| <span data-ttu-id="90db3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="90db3-124">Requirement</span></span> | <span data-ttu-id="90db3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="90db3-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90db3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90db3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="90db3-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="90db3-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="90db3-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="90db3-128">Library</span></span><br/> | <dl> <span data-ttu-id="90db3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90db3-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="90db3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90db3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90db3-131">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="90db3-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
