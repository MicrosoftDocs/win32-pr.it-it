---
description: Carica una mesh da un file DirectX. x.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: Funzione D3DXLoadMeshFromX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354804"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="85d4b-103">D3DXLoadMeshFromX (funzione)</span><span class="sxs-lookup"><span data-stu-id="85d4b-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="85d4b-104">Carica una mesh da un file DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="85d4b-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85d4b-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="85d4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d4b-107">*pFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85d4b-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85d4b-109">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="85d4b-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="85d4b-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="85d4b-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="85d4b-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="85d4b-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="85d4b-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="85d4b-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-113">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85d4b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85d4b-115">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="85d4b-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-116">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="85d4b-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="85d4b-118">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="85d4b-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-119">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d4b-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="85d4b-121">Puntatore a un buffer che contiene dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="85d4b-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="85d4b-122">I dati adiacenza contengono una matrice di tre DWORD per ogni volto che specificano i tre elementi adiacenti per ogni viso nella rete.</span><span class="sxs-lookup"><span data-stu-id="85d4b-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="85d4b-123">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="85d4b-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-124">*ppMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d4b-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="85d4b-126">Puntatore a un buffer contenente dati di materiali.</span><span class="sxs-lookup"><span data-stu-id="85d4b-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="85d4b-127">Il buffer contiene una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni del file DirectX.</span><span class="sxs-lookup"><span data-stu-id="85d4b-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="85d4b-128">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="85d4b-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-129">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d4b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="85d4b-131">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="85d4b-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="85d4b-132">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="85d4b-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="85d4b-133">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="85d4b-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="85d4b-134">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="85d4b-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-135">*pNumMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d4b-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85d4b-137">Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="85d4b-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="85d4b-138">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85d4b-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d4b-139">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d4b-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="85d4b-140">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="85d4b-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d4b-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85d4b-141">Return value</span></span>

<span data-ttu-id="85d4b-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85d4b-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85d4b-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85d4b-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85d4b-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="85d4b-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d4b-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="85d4b-145">Remarks</span></span>

<span data-ttu-id="85d4b-146">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="85d4b-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="85d4b-147">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadMeshFromXW.</span><span class="sxs-lookup"><span data-stu-id="85d4b-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="85d4b-148">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadMeshFromXA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="85d4b-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="85d4b-149">Tutte le mesh nel file verranno compresse in una mesh di output.</span><span class="sxs-lookup"><span data-stu-id="85d4b-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="85d4b-150">Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.</span><span class="sxs-lookup"><span data-stu-id="85d4b-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="85d4b-151">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="85d4b-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="85d4b-152">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="85d4b-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="85d4b-153">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="85d4b-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="85d4b-154">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="85d4b-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="85d4b-155">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="85d4b-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d4b-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85d4b-156">Requirements</span></span>



| <span data-ttu-id="85d4b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="85d4b-157">Requirement</span></span> | <span data-ttu-id="85d4b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="85d4b-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d4b-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85d4b-159">Header</span></span><br/>  | <dl> <span data-ttu-id="85d4b-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d4b-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85d4b-161">Libreria</span><span class="sxs-lookup"><span data-stu-id="85d4b-161">Library</span></span><br/> | <dl> <span data-ttu-id="85d4b-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85d4b-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85d4b-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85d4b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d4b-164">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="85d4b-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="85d4b-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="85d4b-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="85d4b-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="85d4b-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
