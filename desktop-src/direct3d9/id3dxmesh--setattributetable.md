---
description: Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Metodo ID3DXMesh:: SetAttributeTable (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322323"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="78562-103">Metodo ID3DXMesh:: SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="78562-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="78562-104">Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.</span><span class="sxs-lookup"><span data-stu-id="78562-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="78562-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78562-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="78562-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78562-107">*pAttribTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78562-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78562-108">Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="78562-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="78562-109">Puntatore a una matrice di strutture [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , che rappresenta le voci nella tabella dell'attributo mesh.</span><span class="sxs-lookup"><span data-stu-id="78562-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="78562-110">*cAttribTableSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78562-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78562-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78562-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78562-112">Numero di attributi nella tabella dell'attributo mesh.</span><span class="sxs-lookup"><span data-stu-id="78562-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78562-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78562-113">Return value</span></span>

<span data-ttu-id="78562-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78562-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78562-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78562-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78562-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="78562-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78562-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="78562-117">Remarks</span></span>

<span data-ttu-id="78562-118">Se un'applicazione tiene traccia delle informazioni in una tabella degli attributi e riorganizza la tabella in seguito a modifiche apportate agli attributi o ai visi, questo metodo consente all'applicazione di aggiornare le tabelle degli attributi anziché chiamare di nuovo [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="78562-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="78562-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78562-119">Requirements</span></span>



| <span data-ttu-id="78562-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78562-120">Requirement</span></span> | <span data-ttu-id="78562-121">Valore</span><span class="sxs-lookup"><span data-stu-id="78562-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78562-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78562-122">Header</span></span><br/>  | <dl> <span data-ttu-id="78562-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78562-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78562-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="78562-124">Library</span></span><br/> | <dl> <span data-ttu-id="78562-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78562-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78562-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78562-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78562-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="78562-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="78562-128">**ID3DXMesh:: LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="78562-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="78562-129">**ID3DXMesh:: LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="78562-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
