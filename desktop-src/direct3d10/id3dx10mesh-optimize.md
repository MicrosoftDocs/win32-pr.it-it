---
description: Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Metodo ID3DX10Mesh:: Optimize (D3DX10. h)'
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
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355274"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="69bff-103">Metodo ID3DX10Mesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="69bff-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="69bff-104">Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="69bff-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69bff-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="69bff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69bff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bff-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69bff-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bff-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69bff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69bff-109">Specifica il tipo di ottimizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="69bff-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="69bff-110">Questo parametro può essere impostato su una combinazione di uno o più flag di D3DXMESHOPT e D3DXMESH (eccetto D3DXMESH a \_ 32 bit, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="69bff-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="69bff-111">*pFaceRemap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69bff-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bff-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69bff-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69bff-113">Matrice di UINTs, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="69bff-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="69bff-114">Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.</span><span class="sxs-lookup"><span data-stu-id="69bff-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="69bff-115">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69bff-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69bff-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="69bff-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="69bff-117">Indirizzo di un puntatore a un' [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="69bff-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="69bff-118">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="69bff-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bff-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69bff-119">Return value</span></span>

<span data-ttu-id="69bff-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69bff-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69bff-121">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="69bff-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69bff-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="69bff-122">Remarks</span></span>

<span data-ttu-id="69bff-123">Questo metodo genera una nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="69bff-123">This method generates a new mesh.</span></span> <span data-ttu-id="69bff-124">Prima di eseguire l'ottimizzazione, un'applicazione deve generare un buffer adiacenza chiamando [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="69bff-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="69bff-125">Il buffer adiacenza contiene dati adiacenza, ad esempio un elenco di bordi e i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="69bff-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="69bff-126">Questo metodo è molto simile al metodo [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh.</span><span class="sxs-lookup"><span data-stu-id="69bff-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="69bff-127">La mesh di output eredita tutti i parametri di creazione della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="69bff-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bff-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69bff-128">Requirements</span></span>



| <span data-ttu-id="69bff-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bff-129">Requirement</span></span> | <span data-ttu-id="69bff-130">Valore</span><span class="sxs-lookup"><span data-stu-id="69bff-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69bff-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69bff-131">Header</span></span><br/>  | <dl> <span data-ttu-id="69bff-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bff-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69bff-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="69bff-133">Library</span></span><br/> | <dl> <span data-ttu-id="69bff-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69bff-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69bff-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69bff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bff-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="69bff-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="69bff-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="69bff-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
