---
description: 'Metodo ID3DX10Mesh::Optimize: genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: Metodo ID3DX10Mesh::Optimize (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108049"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="de31f-103">Metodo ID3DX10Mesh::Optimize</span><span class="sxs-lookup"><span data-stu-id="de31f-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="de31f-104">Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="de31f-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="de31f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de31f-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="de31f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de31f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de31f-107">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de31f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de31f-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de31f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de31f-109">Specifica il tipo di ottimizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="de31f-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="de31f-110">Questo parametro può essere impostato su una combinazione di uno o più flag di D3DXMESHOPT e D3DXMESH (ad eccezione di D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="de31f-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="de31f-111">*pFaceRemap* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de31f-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de31f-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="de31f-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="de31f-113">Matrice di UINT, uno per viso, che identifica il viso della mesh originale che corrisponde a ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="de31f-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="de31f-114">Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="de31f-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="de31f-115">*ppVertexRemap* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="de31f-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de31f-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="de31f-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="de31f-117">Indirizzo di un puntatore a [**un'interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi.</span><span class="sxs-lookup"><span data-stu-id="de31f-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="de31f-118">Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="de31f-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de31f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de31f-119">Return value</span></span>

<span data-ttu-id="de31f-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de31f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de31f-121">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="de31f-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de31f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="de31f-122">Remarks</span></span>

<span data-ttu-id="de31f-123">Questo metodo genera una nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="de31f-123">This method generates a new mesh.</span></span> <span data-ttu-id="de31f-124">Prima di eseguire Optimize, un'applicazione deve generare un buffer di adiacenza chiamando [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="de31f-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="de31f-125">Il buffer di adienze contiene dati di adizia, ad esempio un elenco di bordi e le facce adiacenti l'una all'altra.</span><span class="sxs-lookup"><span data-stu-id="de31f-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="de31f-126">Questo metodo è molto simile al metodo [**ID3DX10Mesh::CloneMesh,**](id3dx10mesh-clonemesh.md) ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh.</span><span class="sxs-lookup"><span data-stu-id="de31f-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="de31f-127">La mesh di output eredita tutti i parametri di creazione della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="de31f-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="de31f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de31f-128">Requirements</span></span>



| <span data-ttu-id="de31f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="de31f-129">Requirement</span></span> | <span data-ttu-id="de31f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="de31f-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de31f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de31f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="de31f-132"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="de31f-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="de31f-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="de31f-133">Library</span></span><br/> | <dl> <span data-ttu-id="de31f-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="de31f-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de31f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de31f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de31f-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="de31f-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="de31f-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="de31f-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
