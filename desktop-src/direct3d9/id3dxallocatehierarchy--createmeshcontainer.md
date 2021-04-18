---
description: Richiede l'allocazione di un oggetto contenitore mesh.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'Metodo ID3DXAllocateHierarchy:: CreateMeshContainer (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322148"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="18166-103">Metodo ID3DXAllocateHierarchy:: CreateMeshContainer</span><span class="sxs-lookup"><span data-stu-id="18166-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="18166-104">Richiede l'allocazione di un oggetto contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="18166-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="18166-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18166-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="18166-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18166-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18166-107">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18166-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18166-109">Nome della mesh.</span><span class="sxs-lookup"><span data-stu-id="18166-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="18166-110">*pMeshData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-111">Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="18166-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="18166-112">Puntatore alla struttura dei dati mesh.</span><span class="sxs-lookup"><span data-stu-id="18166-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="18166-113">Vedere [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="18166-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="18166-114">*pMaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-115">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="18166-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="18166-116">Matrice di materiali usati nella rete.</span><span class="sxs-lookup"><span data-stu-id="18166-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="18166-117">*pEffectInstances* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-118">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="18166-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="18166-119">Matrice delle istanze degli effetti utilizzate nella rete.</span><span class="sxs-lookup"><span data-stu-id="18166-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="18166-120">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="18166-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="18166-121">*NumMaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18166-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18166-123">Numero di materiali nella matrice di materiali.</span><span class="sxs-lookup"><span data-stu-id="18166-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="18166-124">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="18166-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18166-126">Matrice adiacenza per la mesh.</span><span class="sxs-lookup"><span data-stu-id="18166-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="18166-127">*pSkinInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18166-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-128">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="18166-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="18166-129">Puntatore all'oggetto mesh dell'interfaccia se vengono trovati dati dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="18166-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="18166-130">Vedere [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="18166-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="18166-131">*ppNewMeshContainer* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="18166-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="18166-132">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="18166-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="18166-133">Restituisce il contenitore mesh creato.</span><span class="sxs-lookup"><span data-stu-id="18166-133">Returns the created mesh container.</span></span> <span data-ttu-id="18166-134">Vedere [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="18166-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18166-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18166-135">Return value</span></span>

<span data-ttu-id="18166-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18166-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18166-137">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="18166-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="18166-138">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18166-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="18166-139">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="18166-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="18166-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18166-140">Requirements</span></span>



| <span data-ttu-id="18166-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="18166-141">Requirement</span></span> | <span data-ttu-id="18166-142">Valore</span><span class="sxs-lookup"><span data-stu-id="18166-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18166-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18166-143">Header</span></span><br/>  | <dl> <span data-ttu-id="18166-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="18166-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="18166-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="18166-145">Library</span></span><br/> | <dl> <span data-ttu-id="18166-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18166-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18166-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18166-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18166-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="18166-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
