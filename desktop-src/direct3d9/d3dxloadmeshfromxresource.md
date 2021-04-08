---
description: Carica una mesh da una risorsa.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Funzione D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762029"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="a19eb-103">D3DXLoadMeshFromXResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="a19eb-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="a19eb-104">Carica una mesh da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a19eb-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a19eb-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a19eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a19eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a19eb-107">*Modulo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a19eb-109">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="a19eb-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="a19eb-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a19eb-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-111">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a19eb-113">Puntatore a una stringa che specifica la risorsa da cui creare la mesh.</span><span class="sxs-lookup"><span data-stu-id="a19eb-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="a19eb-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a19eb-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-115">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a19eb-117">Puntatore a una stringa che specifica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a19eb-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="a19eb-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a19eb-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-119">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a19eb-121">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="a19eb-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-122">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a19eb-124">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="a19eb-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-125">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a19eb-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a19eb-127">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a19eb-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a19eb-128">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="a19eb-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-129">*ppMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a19eb-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a19eb-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a19eb-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a19eb-132">Quando questo metodo viene restituito, questo parametro viene compilato con una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni salvate nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="a19eb-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-133">*ppEffectInstances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a19eb-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a19eb-135">Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="a19eb-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="a19eb-136">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="a19eb-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="a19eb-137">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="a19eb-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="a19eb-138">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a19eb-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-139">*pNumMaterials* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a19eb-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a19eb-141">Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="a19eb-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="a19eb-142">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a19eb-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19eb-143">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a19eb-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a19eb-144">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.</span><span class="sxs-lookup"><span data-stu-id="a19eb-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a19eb-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a19eb-145">Return value</span></span>

<span data-ttu-id="a19eb-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a19eb-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a19eb-147">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a19eb-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a19eb-148">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a19eb-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a19eb-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="a19eb-149">Remarks</span></span>

<span data-ttu-id="a19eb-150">Vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) per altre informazioni sui parametri Module, Name e Type.</span><span class="sxs-lookup"><span data-stu-id="a19eb-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="a19eb-151">Tutte le mesh nel file verranno compresse in una mesh di output.</span><span class="sxs-lookup"><span data-stu-id="a19eb-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="a19eb-152">Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.</span><span class="sxs-lookup"><span data-stu-id="a19eb-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="a19eb-153">Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="a19eb-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="a19eb-154">Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="a19eb-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="a19eb-155">Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="a19eb-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="a19eb-156">Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name".</span><span class="sxs-lookup"><span data-stu-id="a19eb-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="a19eb-157">Questo conterrà il nome del file di stringa per la trama.</span><span class="sxs-lookup"><span data-stu-id="a19eb-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a19eb-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a19eb-158">Requirements</span></span>



| <span data-ttu-id="a19eb-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19eb-159">Requirement</span></span> | <span data-ttu-id="a19eb-160">Valore</span><span class="sxs-lookup"><span data-stu-id="a19eb-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a19eb-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a19eb-161">Header</span></span><br/>  | <dl> <span data-ttu-id="a19eb-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a19eb-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a19eb-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="a19eb-163">Library</span></span><br/> | <dl> <span data-ttu-id="a19eb-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a19eb-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a19eb-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a19eb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19eb-166">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="a19eb-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="a19eb-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a19eb-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="a19eb-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="a19eb-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
