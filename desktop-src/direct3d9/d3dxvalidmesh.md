---
description: Convalida una mesh.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Funzione D3DXValidMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354609"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="113dd-103">D3DXValidMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="113dd-103">D3DXValidMesh function</span></span>

<span data-ttu-id="113dd-104">Convalida una mesh.</span><span class="sxs-lookup"><span data-stu-id="113dd-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="113dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="113dd-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="113dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="113dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113dd-107">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="113dd-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113dd-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="113dd-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="113dd-109">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh da testare.</span><span class="sxs-lookup"><span data-stu-id="113dd-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="113dd-110">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="113dd-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113dd-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="113dd-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="113dd-112">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh da testare.</span><span class="sxs-lookup"><span data-stu-id="113dd-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="113dd-113">*ppErrorsAndWarnings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="113dd-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="113dd-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="113dd-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="113dd-115">Restituisce un buffer contenente una stringa di errori e avvisi che illustra i problemi rilevati nella mesh.</span><span class="sxs-lookup"><span data-stu-id="113dd-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113dd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="113dd-116">Return value</span></span>

<span data-ttu-id="113dd-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="113dd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="113dd-118">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="113dd-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="113dd-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="113dd-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="113dd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="113dd-120">Remarks</span></span>

<span data-ttu-id="113dd-121">Questo metodo convalida la mesh controllando la presenza di indici non validi.</span><span class="sxs-lookup"><span data-stu-id="113dd-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="113dd-122">Le informazioni sull'errore sono disponibili nell'output del debugger.</span><span class="sxs-lookup"><span data-stu-id="113dd-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="113dd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113dd-123">Requirements</span></span>



| <span data-ttu-id="113dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="113dd-124">Requirement</span></span> | <span data-ttu-id="113dd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="113dd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="113dd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="113dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="113dd-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="113dd-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="113dd-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="113dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="113dd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="113dd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="113dd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113dd-131">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="113dd-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
