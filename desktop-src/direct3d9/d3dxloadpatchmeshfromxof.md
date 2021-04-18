---
description: Carica una mesh patch da un oggetto ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Funzione D3DXLoadPatchMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322509"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="d3648-103">D3DXLoadPatchMeshFromXof (funzione)</span><span class="sxs-lookup"><span data-stu-id="d3648-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="d3648-104">Carica una mesh patch da un oggetto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="d3648-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3648-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3648-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d3648-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3648-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3648-107">*pxofMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3648-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="d3648-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="d3648-109">Puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) che rappresenta l'oggetto dati del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="d3648-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="d3648-110">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d3648-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3648-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3648-112">Combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) , che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="d3648-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d3648-113">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3648-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d3648-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d3648-115">Puntatore al dispositivo da cui viene creata la mesh.</span><span class="sxs-lookup"><span data-stu-id="d3648-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="d3648-116">*ppMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3648-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3648-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d3648-118">Matrice di materiali contenuti nella rete.</span><span class="sxs-lookup"><span data-stu-id="d3648-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="d3648-119">Ogni materiale è indicizzato da un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d3648-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d3648-120">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3648-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3648-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d3648-122">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="d3648-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="d3648-123">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="d3648-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="d3648-124">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="d3648-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="d3648-125">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="d3648-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3648-126">*pNumMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3648-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-127">Tipo: **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="d3648-127">Type: **PDWORD**</span></span>

<span data-ttu-id="d3648-128">Puntatore che contiene il numero di materiali nella mesh.</span><span class="sxs-lookup"><span data-stu-id="d3648-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d3648-129">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3648-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3648-130">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3648-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="d3648-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXPatchMesh**](id3dxpatchmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="d3648-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3648-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3648-132">Return value</span></span>

<span data-ttu-id="d3648-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3648-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3648-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3648-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d3648-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="d3648-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3648-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3648-136">Remarks</span></span>

<span data-ttu-id="d3648-137">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="d3648-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="d3648-138">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="d3648-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="d3648-139">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="d3648-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="d3648-140">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="d3648-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="d3648-141">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="d3648-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3648-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3648-142">Requirements</span></span>



| <span data-ttu-id="d3648-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3648-143">Requirement</span></span> | <span data-ttu-id="d3648-144">Valore</span><span class="sxs-lookup"><span data-stu-id="d3648-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3648-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3648-145">Header</span></span><br/>  | <dl> <span data-ttu-id="d3648-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3648-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d3648-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3648-147">Library</span></span><br/> | <dl> <span data-ttu-id="d3648-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3648-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3648-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3648-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3648-150">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="d3648-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d3648-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d3648-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="d3648-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="d3648-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
