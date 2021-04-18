---
description: Salva una mesh in un file con estensione x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Funzione D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322603"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="5946f-103">D3DXSaveMeshToX (funzione)</span><span class="sxs-lookup"><span data-stu-id="5946f-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="5946f-104">Salva una mesh in un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5946f-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5946f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5946f-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="5946f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5946f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5946f-107">*pFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5946f-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5946f-109">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="5946f-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="5946f-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5946f-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5946f-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5946f-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5946f-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5946f-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5946f-113">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5946f-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5946f-115">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh da salvare in un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5946f-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="5946f-116">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5946f-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5946f-118">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="5946f-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="5946f-119">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5946f-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5946f-120">*pMaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-121">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="5946f-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="5946f-122">Puntatore a una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni sul materiale da salvare nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5946f-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="5946f-123">*pEffectInstances* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-124">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="5946f-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="5946f-125">Puntatore a una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh.</span><span class="sxs-lookup"><span data-stu-id="5946f-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="5946f-126">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5946f-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="5946f-127">Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="5946f-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="5946f-128">Per ulteriori informazioni, vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="5946f-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="5946f-129">*NumMaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5946f-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5946f-131">Numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *pMaterials* .</span><span class="sxs-lookup"><span data-stu-id="5946f-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="5946f-132">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5946f-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5946f-133">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5946f-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5946f-134">Combinazione del formato di file e delle opzioni di salvataggio quando si salva un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5946f-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="5946f-135">Vedere [D3DX X file costanti](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5946f-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5946f-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5946f-136">Return value</span></span>

<span data-ttu-id="5946f-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5946f-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5946f-138">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5946f-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5946f-139">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5946f-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5946f-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="5946f-140">Remarks</span></span>

<span data-ttu-id="5946f-141">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="5946f-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5946f-142">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveMeshToXW.</span><span class="sxs-lookup"><span data-stu-id="5946f-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="5946f-143">In caso contrario, la chiamata di funzione viene risolta in D3DXSaveMeshToXA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="5946f-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="5946f-144">Il formato di file predefinito è binario; Tuttavia, se un file viene specificato sia come file binario sia come file di testo, verrà salvato come file di testo.</span><span class="sxs-lookup"><span data-stu-id="5946f-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="5946f-145">Indipendentemente dal formato del file, è anche possibile usare il formato compresso per ridurre le dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="5946f-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="5946f-146">Di seguito è riportato un esempio di codice tipico di come usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="5946f-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="5946f-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5946f-147">Requirements</span></span>



| <span data-ttu-id="5946f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5946f-148">Requirement</span></span> | <span data-ttu-id="5946f-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5946f-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5946f-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5946f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="5946f-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5946f-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5946f-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="5946f-152">Library</span></span><br/> | <dl> <span data-ttu-id="5946f-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5946f-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5946f-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5946f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5946f-155">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="5946f-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="5946f-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5946f-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="5946f-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="5946f-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
