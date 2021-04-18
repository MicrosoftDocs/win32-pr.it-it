---
description: Concatena un gruppo di mesh in un'unica mesh comune. Questo metodo può applicare facoltativamente una trasformazione matrice a ogni mesh di input e alle relative coordinate di trama.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Funzione D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323009"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="19e53-104">D3DXConcatenateMeshes (funzione)</span><span class="sxs-lookup"><span data-stu-id="19e53-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="19e53-105">Concatena un gruppo di mesh in un'unica mesh comune.</span><span class="sxs-lookup"><span data-stu-id="19e53-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="19e53-106">Questo metodo può applicare facoltativamente una trasformazione matrice a ogni mesh di input e alle relative coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="19e53-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e53-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19e53-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="19e53-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19e53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e53-109">*ppMeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="19e53-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="19e53-111">Matrice di puntatori mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="19e53-112">Il numero di elementi nella matrice è NumMeshes.</span><span class="sxs-lookup"><span data-stu-id="19e53-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-113">*NumMeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19e53-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19e53-115">Numero di mesh di input da concatenare.</span><span class="sxs-lookup"><span data-stu-id="19e53-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-116">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19e53-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19e53-118">Opzioni di creazione mesh; si tratta di una combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="19e53-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="19e53-119">Le opzioni di creazione di mesh sono equivalenti al parametro options richiesto da [**D3DXCreateMesh**](d3dxcreatemesh.md).</span><span class="sxs-lookup"><span data-stu-id="19e53-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="19e53-120">*pGeomXForms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-121">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="19e53-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19e53-122">Matrice facoltativa di trasformazioni geometriche.</span><span class="sxs-lookup"><span data-stu-id="19e53-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="19e53-123">Il numero di elementi nella matrice è NumMeshes; ogni elemento è una matrice di trasformazione (vedere [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="19e53-124">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="19e53-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-125">*pTextureXForms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="19e53-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19e53-127">Matrice facoltativa di trasformazioni di trama.</span><span class="sxs-lookup"><span data-stu-id="19e53-127">Optional array of texture transforms.</span></span> <span data-ttu-id="19e53-128">Il numero di elementi nella matrice è NumMeshes; ogni elemento è una matrice di trasformazione (vedere [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="19e53-129">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="19e53-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-130">*pDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-131">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="19e53-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="19e53-132">Puntatore facoltativo a una dichiarazione di vertice (vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="19e53-133">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="19e53-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-134">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e53-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-135">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="19e53-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="19e53-136">Puntatore a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per creare la nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="19e53-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="19e53-137">*ppMeshOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19e53-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19e53-138">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="19e53-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="19e53-139">Indirizzo di un puntatore alla mesh creata (vedere [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e53-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19e53-140">Return value</span></span>

<span data-ttu-id="19e53-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19e53-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19e53-142">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19e53-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="19e53-143">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="19e53-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e53-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="19e53-144">Remarks</span></span>

<span data-ttu-id="19e53-145">Se non viene fornita alcuna [dichiarazione del vertice](vertex-declaration.md) come parte del parametro di creazione mesh delle opzioni, il metodo genererà un'Unione di tutte le dichiarazioni dei vertici dei sottomesh, innalzando di canale e i tipi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="19e53-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="19e53-146">Il metodo creerà una tabella degli attributi dalle tabelle degli attributi dei mesh di input.</span><span class="sxs-lookup"><span data-stu-id="19e53-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="19e53-147">Per garantire la creazione di una tabella di attributi, chiamare [**optimize**](id3dxmesh--optimize.md) with flags impostato su D3DXMESHOPT \_ Compact e D3DXMESHOPT \_ ATTRSORT (vedere [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="19e53-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="19e53-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19e53-148">Requirements</span></span>



| <span data-ttu-id="19e53-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e53-149">Requirement</span></span> | <span data-ttu-id="19e53-150">Valore</span><span class="sxs-lookup"><span data-stu-id="19e53-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e53-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19e53-151">Header</span></span><br/>  | <dl> <span data-ttu-id="19e53-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="19e53-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19e53-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="19e53-153">Library</span></span><br/> | <dl> <span data-ttu-id="19e53-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19e53-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19e53-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19e53-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e53-156">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="19e53-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
