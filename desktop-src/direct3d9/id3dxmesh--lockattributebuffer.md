---
description: Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Metodo ID3DXMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322324"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="09258-103">Metodo ID3DXMesh:: LockAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="09258-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="09258-104">Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="09258-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="09258-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09258-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="09258-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09258-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09258-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09258-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09258-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09258-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="09258-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="09258-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="09258-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="09258-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="09258-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="09258-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="09258-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="09258-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="09258-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="09258-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="09258-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="09258-115">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="09258-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="09258-116">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09258-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09258-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09258-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="09258-118">Indirizzo di un puntatore a un buffer contenente un valore DWORD per ogni viso della mesh.</span><span class="sxs-lookup"><span data-stu-id="09258-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09258-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09258-119">Return value</span></span>

<span data-ttu-id="09258-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09258-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09258-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09258-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="09258-122">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="09258-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="09258-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="09258-123">Remarks</span></span>

<span data-ttu-id="09258-124">Se è stato chiamato [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) , per la mesh sarà disponibile anche una tabella di attributi a cui è possibile accedere tramite il metodo [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .</span><span class="sxs-lookup"><span data-stu-id="09258-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="09258-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09258-125">Requirements</span></span>



| <span data-ttu-id="09258-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="09258-126">Requirement</span></span> | <span data-ttu-id="09258-127">Valore</span><span class="sxs-lookup"><span data-stu-id="09258-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09258-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09258-128">Header</span></span><br/>  | <dl> <span data-ttu-id="09258-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="09258-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="09258-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="09258-130">Library</span></span><br/> | <dl> <span data-ttu-id="09258-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09258-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09258-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09258-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09258-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="09258-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="09258-134">**ID3DXMesh:: UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="09258-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="09258-135">**ID3DXBaseMesh:: GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="09258-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="09258-136">**ID3DXMesh:: SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="09258-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
