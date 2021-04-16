---
description: Blocca il buffer dell'indice.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'Metodo ID3DXPatchMesh:: LockIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531081"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="0af79-103">Metodo ID3DXPatchMesh:: LockIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="0af79-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="0af79-104">Blocca il buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="0af79-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0af79-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="0af79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0af79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af79-107">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0af79-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af79-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0af79-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0af79-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="0af79-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="0af79-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="0af79-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="0af79-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="0af79-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="0af79-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="0af79-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="0af79-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="0af79-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="0af79-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0af79-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="0af79-115">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="0af79-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="0af79-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0af79-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0af79-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0af79-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0af79-118">\*Puntatore void a un buffer di memoria contenente i dati dell'indice restituiti.</span><span class="sxs-lookup"><span data-stu-id="0af79-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af79-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0af79-119">Return value</span></span>

<span data-ttu-id="0af79-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0af79-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0af79-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0af79-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0af79-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="0af79-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af79-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0af79-123">Remarks</span></span>

<span data-ttu-id="0af79-124">Il buffer dell'indice viene in genere bloccato, scritto e quindi sbloccato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="0af79-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="0af79-125">I buffer dell'indice mesh della patch sono buffer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0af79-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af79-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0af79-126">Requirements</span></span>



| <span data-ttu-id="0af79-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0af79-127">Requirement</span></span> | <span data-ttu-id="0af79-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0af79-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0af79-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0af79-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0af79-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0af79-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0af79-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0af79-131">Library</span></span><br/> | <dl> <span data-ttu-id="0af79-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0af79-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0af79-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0af79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af79-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="0af79-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="0af79-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="0af79-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
