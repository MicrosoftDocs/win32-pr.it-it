---
description: Carica una mesh di interfaccia personalizzata da un oggetto dati di file DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Funzione D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761950"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="41d1e-103">D3DXLoadSkinMeshFromXof (funzione)</span><span class="sxs-lookup"><span data-stu-id="41d1e-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="41d1e-104">Carica una mesh di interfaccia personalizzata da un oggetto dati di file DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="41d1e-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41d1e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="41d1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41d1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d1e-107">*pxofMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="41d1e-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="41d1e-109">Puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) che rappresenta l'oggetto dati del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="41d1e-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-110">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41d1e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41d1e-112">Combinazione di uno o più flag dall'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="41d1e-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-113">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="41d1e-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="41d1e-115">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="41d1e-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-116">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="41d1e-118">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="41d1e-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="41d1e-119">Quando questo metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="41d1e-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-120">*ppMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="41d1e-122">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="41d1e-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="41d1e-123">Quando il metodo restituisce un risultato, questo parametro viene compilato con una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="41d1e-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-124">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="41d1e-126">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="41d1e-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="41d1e-127">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="41d1e-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="41d1e-128">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="41d1e-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="41d1e-129">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="41d1e-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-130">*pMatOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="41d1e-132">Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="41d1e-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-133">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-134">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="41d1e-135">Indirizzo di un puntatore a un'interfaccia [**ID3DXSkinInfo**](id3dxskininfo.md) , che rappresenta le informazioni di skinning.</span><span class="sxs-lookup"><span data-stu-id="41d1e-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-136">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="41d1e-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="41d1e-138">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="41d1e-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d1e-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41d1e-139">Return value</span></span>

<span data-ttu-id="41d1e-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41d1e-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41d1e-141">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41d1e-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="41d1e-142">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="41d1e-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="41d1e-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="41d1e-143">Remarks</span></span>

<span data-ttu-id="41d1e-144">Questo metodo accetta un puntatore a un oggetto interno nel file con estensione x, consentendo di caricare la gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="41d1e-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="41d1e-145">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="41d1e-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="41d1e-146">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="41d1e-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="41d1e-147">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="41d1e-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="41d1e-148">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="41d1e-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="41d1e-149">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="41d1e-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d1e-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41d1e-150">Requirements</span></span>



| <span data-ttu-id="41d1e-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d1e-151">Requirement</span></span> | <span data-ttu-id="41d1e-152">Valore</span><span class="sxs-lookup"><span data-stu-id="41d1e-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d1e-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41d1e-153">Header</span></span><br/>  | <dl> <span data-ttu-id="41d1e-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d1e-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="41d1e-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="41d1e-155">Library</span></span><br/> | <dl> <span data-ttu-id="41d1e-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41d1e-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41d1e-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41d1e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d1e-158">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="41d1e-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="41d1e-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="41d1e-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="41d1e-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="41d1e-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
