---
description: Disegnare diverse istanze dello stesso subset di una mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: Metodo ID3DX10Mesh::D rawSubsetInstanced (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335635"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="e2e2d-103">Metodo ID3DX10Mesh::D rawSubsetInstanced</span><span class="sxs-lookup"><span data-stu-id="e2e2d-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="e2e2d-104">Disegnare diverse istanze dello stesso subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e2d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2e2d-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="e2e2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2e2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e2d-107">*AttribId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e2e2d-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e2d-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2e2d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2e2d-109">Specifica il subset della mesh da disegnare.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="e2e2d-110">Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="e2e2d-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e2e2d-112">*InstanceCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e2e2d-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e2d-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2e2d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2e2d-114">Numero di istanze di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="e2e2d-115">*StartInstanceLocation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e2e2d-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e2d-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2e2d-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2e2d-117">Istanza da cui iniziare il recupero in ogni buffer contrassegnato come dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e2d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2e2d-118">Return value</span></span>

<span data-ttu-id="e2e2d-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2e2d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2e2d-120">Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="e2e2d-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e2d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2e2d-121">Remarks</span></span>

<span data-ttu-id="e2e2d-122">Una mesh contiene una tabella di attributi.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="e2e2d-123">La tabella degli attributi può dividere una mesh in subset, in cui ogni subset viene identificato con un ID attributo.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="e2e2d-124">Ad esempio, una mesh con 200 visi, suddivisa in tre subset, potrebbe avere una tabella di attributi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="e2e2d-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="e2e2d-125">Subset</span><span class="sxs-lookup"><span data-stu-id="e2e2d-125">Subset</span></span>     | <span data-ttu-id="e2e2d-126">Smile</span><span class="sxs-lookup"><span data-stu-id="e2e2d-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="e2e2d-127">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="e2e2d-127">AttribID 0</span></span> | <span data-ttu-id="e2e2d-128">Visi 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="e2e2d-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="e2e2d-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="e2e2d-129">AttribID 1</span></span> | <span data-ttu-id="e2e2d-130">Visi 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="e2e2d-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="e2e2d-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="e2e2d-131">AttribID 2</span></span> | <span data-ttu-id="e2e2d-132">Visi 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="e2e2d-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="e2e2d-133">Le istanze possono estendere le prestazioni riutilizzando la stessa geometria per disegnare più oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="e2e2d-134">Un esempio di istanze può essere quello di disegnare lo stesso oggetto con posizioni e colori diversi.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="e2e2d-135">L'indicizzazione richiede più buffer dei vertici: almeno uno per i dati per vertice e un secondo buffer per i dati per istanza.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="e2e2d-136">Il disegno di istanze con DrawSubsetInstanced è molto simile al processo usato con [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) descritto in [Esempio](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)di istanze.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="e2e2d-137">La differenza principale quando si usa DrawSubsetInstanced è che i buffer dei vertici e degli indici devono essere estratti dall'oggetto interfaccia [**ID3DX10Mesh**](id3dx10mesh.md) prima di poter combinare i dati di istanza.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="e2e2d-138">Il codice seguente illustra l'estrazione dei buffer dei vertici e degli indici dall'oggetto mesh.</span><span class="sxs-lookup"><span data-stu-id="e2e2d-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="e2e2d-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2e2d-139">Requirements</span></span>



| <span data-ttu-id="e2e2d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2e2d-140">Requirement</span></span> | <span data-ttu-id="e2e2d-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e2e2d-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e2d-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2e2d-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e2e2d-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e2d-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2e2d-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2e2d-144">Library</span></span><br/> | <dl> <span data-ttu-id="e2e2d-145"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2e2d-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e2d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2e2d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e2d-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e2e2d-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e2e2d-148">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e2e2d-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
