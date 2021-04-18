---
description: Blocca il buffer dell'attributo.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'Metodo ID3DXPatchMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323718"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="8071a-103">Metodo ID3DXPatchMesh:: LockAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="8071a-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="8071a-104">Blocca il buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="8071a-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8071a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8071a-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="8071a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8071a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8071a-107">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8071a-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8071a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8071a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8071a-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8071a-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="8071a-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="8071a-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="8071a-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="8071a-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="8071a-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="8071a-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="8071a-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="8071a-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="8071a-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8071a-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="8071a-115">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="8071a-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="8071a-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8071a-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8071a-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8071a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="8071a-118">Indirizzo di un puntatore a un buffer contenente un valore DWORD per ogni viso della mesh.</span><span class="sxs-lookup"><span data-stu-id="8071a-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8071a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8071a-119">Return value</span></span>

<span data-ttu-id="8071a-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8071a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8071a-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8071a-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8071a-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8071a-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8071a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8071a-123">Remarks</span></span>

<span data-ttu-id="8071a-124">Il buffer dell'attributo viene in genere bloccato, scritto e quindi sbloccato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="8071a-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="8071a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8071a-125">Requirements</span></span>



| <span data-ttu-id="8071a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8071a-126">Requirement</span></span> | <span data-ttu-id="8071a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8071a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8071a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8071a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8071a-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8071a-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8071a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="8071a-130">Library</span></span><br/> | <dl> <span data-ttu-id="8071a-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8071a-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8071a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8071a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8071a-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8071a-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
