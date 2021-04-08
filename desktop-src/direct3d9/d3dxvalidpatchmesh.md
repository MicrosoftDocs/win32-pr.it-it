---
description: Convalida una mesh patch, restituendo il numero di vertici e patch degenerati.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Funzione D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969335"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="8b637-103">D3DXValidPatchMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b637-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="8b637-104">Convalida una mesh patch, restituendo il numero di vertici e patch degenerati.</span><span class="sxs-lookup"><span data-stu-id="8b637-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b637-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b637-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="8b637-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b637-107">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b637-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b637-108">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8b637-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="8b637-109">Puntatore a un'interfaccia [**ID3DXPatchMesh**](id3dxpatchmesh.md) , che rappresenta la mesh della patch da testare.</span><span class="sxs-lookup"><span data-stu-id="8b637-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="8b637-110">*pNumDegenerateVertices* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b637-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b637-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b637-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8b637-112">Restituisce il numero di vertici degenerati nella mesh della patch.</span><span class="sxs-lookup"><span data-stu-id="8b637-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8b637-113">*pNumDegeneratePatches* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b637-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b637-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b637-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8b637-115">Restituisce il numero di patch degenerate nella mesh patch.</span><span class="sxs-lookup"><span data-stu-id="8b637-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8b637-116">*ppErrorsAndWarnings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b637-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b637-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b637-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8b637-118">Restituisce un puntatore a un buffer contenente una stringa di errori e avvisi che illustrano i problemi rilevati nella mesh della patch.</span><span class="sxs-lookup"><span data-stu-id="8b637-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b637-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b637-119">Return value</span></span>

<span data-ttu-id="8b637-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b637-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b637-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b637-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8b637-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8b637-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b637-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b637-123">Remarks</span></span>

<span data-ttu-id="8b637-124">Questo metodo convalida la mesh controllando la presenza di indici non validi.</span><span class="sxs-lookup"><span data-stu-id="8b637-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="8b637-125">Le informazioni sull'errore sono disponibili nell'output del debugger.</span><span class="sxs-lookup"><span data-stu-id="8b637-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b637-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b637-126">Requirements</span></span>



| <span data-ttu-id="8b637-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b637-127">Requirement</span></span> | <span data-ttu-id="8b637-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8b637-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b637-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b637-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8b637-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b637-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8b637-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b637-131">Library</span></span><br/> | <dl> <span data-ttu-id="8b637-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b637-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b637-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b637-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b637-134">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8b637-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
