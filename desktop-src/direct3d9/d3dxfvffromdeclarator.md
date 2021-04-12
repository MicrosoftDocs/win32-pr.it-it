---
description: Restituisce un codice FVF (Flexible Vertex Format) da un dichiaratore.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Funzione D3DXFVFFromDeclarator (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354839"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="f5314-103">D3DXFVFFromDeclarator (funzione)</span><span class="sxs-lookup"><span data-stu-id="f5314-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="f5314-104">Restituisce un codice FVF (Flexible Vertex Format) da un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="f5314-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5314-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5314-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="f5314-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5314-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5314-107">*pDeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5314-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5314-108">Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5314-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="f5314-109">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il codice FVF.</span><span class="sxs-lookup"><span data-stu-id="f5314-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="f5314-110">*pFVF* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f5314-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5314-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5314-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f5314-112">Puntatore a un valore DWORD che rappresenta la combinazione restituita di [D3DFVF](d3dfvf.md) che descrive il formato del vertice restituito dal dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="f5314-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5314-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5314-113">Return value</span></span>

<span data-ttu-id="f5314-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f5314-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f5314-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f5314-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f5314-116">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f5314-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5314-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5314-117">Remarks</span></span>

<span data-ttu-id="f5314-118">Questa funzione avrà esito negativo per qualsiasi dichiaratore che non esegue il mapping direttamente a un FVF.</span><span class="sxs-lookup"><span data-stu-id="f5314-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5314-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5314-119">Requirements</span></span>



| <span data-ttu-id="f5314-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5314-120">Requirement</span></span> | <span data-ttu-id="f5314-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f5314-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5314-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5314-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f5314-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5314-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f5314-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5314-124">Library</span></span><br/> | <dl> <span data-ttu-id="f5314-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5314-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5314-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5314-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5314-127">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="f5314-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f5314-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="f5314-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
