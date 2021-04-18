---
description: Converte i dati rappresentativi del punto in informazioni adiacenza mesh.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Metodo ID3DXBaseMesh:: ConvertPointRepsToAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322554"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="fea7b-103">Metodo ID3DXBaseMesh:: ConvertPointRepsToAdjacency</span><span class="sxs-lookup"><span data-stu-id="fea7b-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="fea7b-104">Converte i dati rappresentativi del punto in informazioni adiacenza mesh.</span><span class="sxs-lookup"><span data-stu-id="fea7b-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fea7b-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="fea7b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fea7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea7b-107">*pPRep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fea7b-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea7b-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fea7b-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fea7b-109">Puntatore a una matrice di un valore DWORD per vertice della mesh che contiene i dati rappresentativi del punto.</span><span class="sxs-lookup"><span data-stu-id="fea7b-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="fea7b-110">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fea7b-110">This parameter is optional.</span></span> <span data-ttu-id="fea7b-111">Se si specifica un valore **null** , questo parametro verrà interpretato come una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="fea7b-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="fea7b-112">*pAdjacency* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fea7b-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea7b-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fea7b-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fea7b-114">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="fea7b-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="fea7b-115">Il numero di byte in questa matrice deve essere almeno 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="fea7b-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea7b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fea7b-116">Return value</span></span>

<span data-ttu-id="fea7b-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fea7b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fea7b-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fea7b-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fea7b-119">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="fea7b-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea7b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fea7b-120">Requirements</span></span>



| <span data-ttu-id="fea7b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea7b-121">Requirement</span></span> | <span data-ttu-id="fea7b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fea7b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fea7b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fea7b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fea7b-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea7b-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fea7b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="fea7b-125">Library</span></span><br/> | <dl> <span data-ttu-id="fea7b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fea7b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fea7b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fea7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea7b-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="fea7b-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
