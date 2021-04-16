---
description: Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Metodo ID3DX10Mesh:: GenerateAdjacencyAndPointReps (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530991"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="9c961-103">Metodo ID3DX10Mesh:: GenerateAdjacencyAndPointReps</span><span class="sxs-lookup"><span data-stu-id="9c961-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="9c961-104">Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.</span><span class="sxs-lookup"><span data-stu-id="9c961-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c961-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c961-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="9c961-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c961-107">*Epsilon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c961-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c961-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c961-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c961-109">Specifica che i vertici che differiscono dalla posizione minore di Epsilon devono essere considerati coincidenti.</span><span class="sxs-lookup"><span data-stu-id="9c961-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c961-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c961-110">Return value</span></span>

<span data-ttu-id="9c961-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c961-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c961-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9c961-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c961-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c961-113">Remarks</span></span>

<span data-ttu-id="9c961-114">Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="9c961-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="9c961-115">L'ordine delle voci nel buffer adiacenza è determinato dall'ordine degli indici dei vertici nel buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="9c961-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="9c961-116">Il triangolo adiacente 0 corrisponde sempre al bordo tra gli indici degli angoli 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="9c961-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="9c961-117">Il triangolo adiacente 1 corrisponde sempre al bordo tra gli indici degli angoli 1 e 2, mentre il triangolo adiacente 2 corrisponde al bordo tra gli indici degli angoli 2 e 0.</span><span class="sxs-lookup"><span data-stu-id="9c961-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c961-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c961-118">Requirements</span></span>



| <span data-ttu-id="9c961-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c961-119">Requirement</span></span> | <span data-ttu-id="9c961-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9c961-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c961-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c961-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9c961-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c961-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c961-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9c961-123">Library</span></span><br/> | <dl> <span data-ttu-id="9c961-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c961-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c961-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c961-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c961-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="9c961-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="9c961-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="9c961-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
