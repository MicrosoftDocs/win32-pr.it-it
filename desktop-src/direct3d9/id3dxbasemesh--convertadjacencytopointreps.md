---
description: Converte le informazioni adiacenza mesh in una matrice di rappresentanti punto.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'Metodo ID3DXBaseMesh:: ConvertAdjacencyToPointReps (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234993"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="b9595-103">Metodo ID3DXBaseMesh:: ConvertAdjacencyToPointReps</span><span class="sxs-lookup"><span data-stu-id="b9595-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="b9595-104">Converte le informazioni adiacenza mesh in una matrice di rappresentanti punto.</span><span class="sxs-lookup"><span data-stu-id="b9595-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9595-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9595-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="b9595-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9595-107">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9595-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9595-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9595-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9595-109">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="b9595-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="b9595-110">Il numero di byte in questa matrice deve essere almeno 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="b9595-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="b9595-111">*pPRep* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b9595-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9595-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9595-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9595-113">Puntatore a una matrice di un valore DWORD per vertice della mesh che verrà riempito con dati rappresentativi del punto.</span><span class="sxs-lookup"><span data-stu-id="b9595-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9595-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9595-114">Return value</span></span>

<span data-ttu-id="b9595-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9595-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9595-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b9595-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b9595-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b9595-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9595-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9595-118">Requirements</span></span>



| <span data-ttu-id="b9595-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9595-119">Requirement</span></span> | <span data-ttu-id="b9595-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b9595-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9595-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9595-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b9595-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9595-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b9595-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9595-123">Library</span></span><br/> | <dl> <span data-ttu-id="b9595-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9595-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9595-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9595-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9595-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b9595-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
