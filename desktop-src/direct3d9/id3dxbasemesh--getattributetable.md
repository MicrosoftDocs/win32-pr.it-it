---
description: Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'Metodo ID3DXBaseMesh:: GetAttributeTable (D3DX9Mesh. h)'
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
ms.openlocfilehash: 70c93c8f477655200418793f53706731b42a47ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322983"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="baeb5-103">Metodo ID3DXBaseMesh:: GetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="baeb5-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="baeb5-104">Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.</span><span class="sxs-lookup"><span data-stu-id="baeb5-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="baeb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baeb5-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="baeb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="baeb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baeb5-107">*pAttribTable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="baeb5-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="baeb5-108">Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="baeb5-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="baeb5-109">Puntatore a una matrice di strutture [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , che rappresenta le voci nella tabella degli attributi della mesh.</span><span class="sxs-lookup"><span data-stu-id="baeb5-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="baeb5-110">Specificare **null** per recuperare il valore per pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="baeb5-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="baeb5-111">*pAttribTableSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="baeb5-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="baeb5-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="baeb5-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="baeb5-113">Puntatore al numero di voci archiviate in pAttribTable o a un valore da compilare con il numero di voci archiviate nella tabella degli attributi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="baeb5-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baeb5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="baeb5-114">Return value</span></span>

<span data-ttu-id="baeb5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="baeb5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="baeb5-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="baeb5-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="baeb5-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="baeb5-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="baeb5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="baeb5-118">Remarks</span></span>

<span data-ttu-id="baeb5-119">Una tabella attribute viene creata da [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) e passando D3DXMESHOPT \_ ATTRSORT per il parametro flags.</span><span class="sxs-lookup"><span data-stu-id="baeb5-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="baeb5-120">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="baeb5-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="baeb5-121">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="baeb5-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="baeb5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baeb5-122">Requirements</span></span>



| <span data-ttu-id="baeb5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="baeb5-123">Requirement</span></span> | <span data-ttu-id="baeb5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="baeb5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baeb5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baeb5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="baeb5-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="baeb5-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="baeb5-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="baeb5-127">Library</span></span><br/> | <dl> <span data-ttu-id="baeb5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="baeb5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="baeb5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baeb5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baeb5-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="baeb5-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
