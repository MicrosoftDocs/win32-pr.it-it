---
description: Genera una dichiarazione del vertice di output dalla dichiarazione di input. La dichiarazione di output è destinata all'uso da parte delle funzioni a mosaico mesh.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Funzione D3DXGenerateOutputDecl (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322674"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="efc18-104">D3DXGenerateOutputDecl (funzione)</span><span class="sxs-lookup"><span data-stu-id="efc18-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="efc18-105">Genera una dichiarazione del vertice di output dalla dichiarazione di input.</span><span class="sxs-lookup"><span data-stu-id="efc18-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="efc18-106">La dichiarazione di output è destinata all'uso da parte delle funzioni a mosaico mesh.</span><span class="sxs-lookup"><span data-stu-id="efc18-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc18-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efc18-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="efc18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efc18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc18-109">*pOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efc18-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efc18-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="efc18-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="efc18-111">Puntatore alla dichiarazione del vertice di output.</span><span class="sxs-lookup"><span data-stu-id="efc18-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="efc18-112">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="efc18-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc18-113">*Pinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efc18-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc18-114">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="efc18-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="efc18-115">Puntatore alla dichiarazione del vertice di input.</span><span class="sxs-lookup"><span data-stu-id="efc18-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="efc18-116">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="efc18-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc18-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efc18-117">Return value</span></span>

<span data-ttu-id="efc18-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efc18-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efc18-119">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efc18-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="efc18-120">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="efc18-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc18-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efc18-121">Requirements</span></span>



| <span data-ttu-id="efc18-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc18-122">Requirement</span></span> | <span data-ttu-id="efc18-123">Valore</span><span class="sxs-lookup"><span data-stu-id="efc18-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efc18-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efc18-124">Header</span></span><br/>  | <dl> <span data-ttu-id="efc18-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc18-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="efc18-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="efc18-126">Library</span></span><br/> | <dl> <span data-ttu-id="efc18-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efc18-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efc18-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc18-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc18-129">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="efc18-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




