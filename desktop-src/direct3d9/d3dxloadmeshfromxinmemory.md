---
description: Carica una mesh dalla memoria.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Funzione D3DXLoadMeshFromXInMemory (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322639"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="a99cb-103">D3DXLoadMeshFromXInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="a99cb-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="a99cb-104">Carica una mesh dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="a99cb-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a99cb-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a99cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a99cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a99cb-107">*Memoria* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a99cb-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a99cb-109">Puntatore al buffer di memoria che contiene i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="a99cb-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-110">*SizeOfMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a99cb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a99cb-112">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="a99cb-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-113">*Opzioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a99cb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a99cb-115">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="a99cb-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-116">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a99cb-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a99cb-118">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="a99cb-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-119">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a99cb-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a99cb-121">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a99cb-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a99cb-122">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="a99cb-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-123">*ppMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a99cb-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a99cb-125">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a99cb-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a99cb-126">Quando questo metodo viene restituito, questo parametro viene compilato con una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni salvate nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="a99cb-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-127">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a99cb-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a99cb-129">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="a99cb-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="a99cb-130">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="a99cb-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="a99cb-131">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="a99cb-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="a99cb-132">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a99cb-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-133">*pNumMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a99cb-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a99cb-135">Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="a99cb-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="a99cb-136">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a99cb-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99cb-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a99cb-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a99cb-138">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="a99cb-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a99cb-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a99cb-139">Return value</span></span>

<span data-ttu-id="a99cb-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a99cb-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a99cb-141">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a99cb-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a99cb-142">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a99cb-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a99cb-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="a99cb-143">Remarks</span></span>

<span data-ttu-id="a99cb-144">Tutte le mesh nel file verranno compresse in una mesh di output.</span><span class="sxs-lookup"><span data-stu-id="a99cb-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="a99cb-145">Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.</span><span class="sxs-lookup"><span data-stu-id="a99cb-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="a99cb-146">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="a99cb-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="a99cb-147">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="a99cb-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="a99cb-148">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="a99cb-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="a99cb-149">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="a99cb-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="a99cb-150">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="a99cb-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99cb-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a99cb-151">Requirements</span></span>



| <span data-ttu-id="a99cb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99cb-152">Requirement</span></span> | <span data-ttu-id="a99cb-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a99cb-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a99cb-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a99cb-154">Header</span></span><br/>  | <dl> <span data-ttu-id="a99cb-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a99cb-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a99cb-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="a99cb-156">Library</span></span><br/> | <dl> <span data-ttu-id="a99cb-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a99cb-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a99cb-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a99cb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99cb-159">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="a99cb-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="a99cb-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a99cb-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="a99cb-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="a99cb-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
