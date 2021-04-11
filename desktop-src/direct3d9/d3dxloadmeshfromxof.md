---
description: Carica una mesh da un oggetto ID3DXFileData.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: Funzione D3DXLoadMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354799"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="65a97-103">D3DXLoadMeshFromXof (funzione)</span><span class="sxs-lookup"><span data-stu-id="65a97-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="65a97-104">Carica una mesh da un oggetto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="65a97-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65a97-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="65a97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65a97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a97-107">*pxofMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65a97-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="65a97-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="65a97-109">Puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) che rappresenta l'oggetto dati del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="65a97-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="65a97-110">*Opzioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="65a97-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a97-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65a97-112">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="65a97-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="65a97-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65a97-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="65a97-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="65a97-115">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="65a97-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="65a97-116">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65a97-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65a97-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65a97-118">Puntatore a un buffer che contiene dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="65a97-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="65a97-119">I dati adiacenza contengono una matrice di tre DWORD per ogni volto che specificano i tre elementi adiacenti per ogni viso nella rete.</span><span class="sxs-lookup"><span data-stu-id="65a97-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="65a97-120">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="65a97-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a97-121">*ppMaterials* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="65a97-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65a97-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65a97-123">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="65a97-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="65a97-124">Quando il metodo restituisce un risultato, questo parametro viene compilato con una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="65a97-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="65a97-125">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65a97-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65a97-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65a97-127">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="65a97-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="65a97-128">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="65a97-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="65a97-129">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="65a97-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="65a97-130">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="65a97-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a97-131">*pNumMaterials* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="65a97-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="65a97-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="65a97-133">Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="65a97-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="65a97-134">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65a97-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a97-135">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="65a97-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="65a97-136">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="65a97-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a97-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65a97-137">Return value</span></span>

<span data-ttu-id="65a97-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65a97-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65a97-139">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65a97-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65a97-140">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="65a97-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a97-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="65a97-141">Remarks</span></span>

<span data-ttu-id="65a97-142">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="65a97-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="65a97-143">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="65a97-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="65a97-144">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="65a97-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="65a97-145">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="65a97-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="65a97-146">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="65a97-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a97-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65a97-147">Requirements</span></span>



| <span data-ttu-id="65a97-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a97-148">Requirement</span></span> | <span data-ttu-id="65a97-149">Valore</span><span class="sxs-lookup"><span data-stu-id="65a97-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65a97-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65a97-150">Header</span></span><br/>  | <dl> <span data-ttu-id="65a97-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="65a97-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="65a97-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="65a97-152">Library</span></span><br/> | <dl> <span data-ttu-id="65a97-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65a97-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65a97-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65a97-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a97-155">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="65a97-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="65a97-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="65a97-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="65a97-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="65a97-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
