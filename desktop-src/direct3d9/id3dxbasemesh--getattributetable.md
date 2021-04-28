---
description: 'Metodo ID3DXBaseMesh::GetAttributeTable: recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: Metodo ID3DXBaseMesh::GetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115449"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="1ed02-103">Metodo ID3DXBaseMesh::GetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="1ed02-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="1ed02-104">Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.</span><span class="sxs-lookup"><span data-stu-id="1ed02-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ed02-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="1ed02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ed02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed02-107">*pAttribTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-108">Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ed02-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="1ed02-109">Puntatore a una matrice [**di strutture D3DXATTRIBUTERANGE,**](d3dxattributerange.md) che rappresenta le voci nella tabella degli attributi della mesh.</span><span class="sxs-lookup"><span data-stu-id="1ed02-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="1ed02-110">Specificare **NULL** per recuperare il valore per pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="1ed02-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="1ed02-111">*pAttribTableSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ed02-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1ed02-113">Puntatore al numero di voci archiviate in pAttribTable o a un valore da riempire con il numero di voci archiviate nella tabella degli attributi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="1ed02-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed02-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ed02-114">Return value</span></span>

<span data-ttu-id="1ed02-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ed02-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ed02-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ed02-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ed02-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1ed02-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed02-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ed02-118">Remarks</span></span>

<span data-ttu-id="1ed02-119">Una tabella degli attributi viene creata da [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) e passa D3DXMESHOPT \_ ATTRSORT per il parametro Flags.</span><span class="sxs-lookup"><span data-stu-id="1ed02-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="1ed02-120">Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi.</span><span class="sxs-lookup"><span data-stu-id="1ed02-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="1ed02-121">Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un identificatore di attributo specificato durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="1ed02-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed02-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ed02-122">Requirements</span></span>



| <span data-ttu-id="1ed02-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed02-123">Requirement</span></span> | <span data-ttu-id="1ed02-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1ed02-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed02-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ed02-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1ed02-126"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1ed02-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ed02-127">Library</span></span><br/> | <dl> <span data-ttu-id="1ed02-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ed02-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ed02-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed02-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="1ed02-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
