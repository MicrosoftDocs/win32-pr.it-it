---
description: Blocca il buffer dei vertici.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'Metodo ID3DXPatchMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886303"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="fbecd-103">Metodo ID3DXPatchMesh:: LockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="fbecd-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="fbecd-104">Blocca il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="fbecd-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbecd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbecd-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="fbecd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbecd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbecd-107">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbecd-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbecd-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbecd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbecd-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="fbecd-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="fbecd-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="fbecd-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="fbecd-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="fbecd-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="fbecd-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="fbecd-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="fbecd-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="fbecd-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="fbecd-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fbecd-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="fbecd-115">Nosovrascrive D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="fbecd-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="fbecd-116">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="fbecd-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbecd-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fbecd-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fbecd-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbecd-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fbecd-119">\*Puntatore void a un buffer di memoria contenente i dati dei vertici restituiti.</span><span class="sxs-lookup"><span data-stu-id="fbecd-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbecd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbecd-120">Return value</span></span>

<span data-ttu-id="fbecd-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbecd-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbecd-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fbecd-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fbecd-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="fbecd-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbecd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbecd-124">Remarks</span></span>

<span data-ttu-id="fbecd-125">Il buffer vertex viene in genere bloccato, scritto e quindi sbloccato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="fbecd-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="fbecd-126">Le mesh di patch utilizzano buffer di indice a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fbecd-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbecd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbecd-127">Requirements</span></span>



| <span data-ttu-id="fbecd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbecd-128">Requirement</span></span> | <span data-ttu-id="fbecd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fbecd-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbecd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbecd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fbecd-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbecd-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fbecd-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="fbecd-132">Library</span></span><br/> | <dl> <span data-ttu-id="fbecd-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbecd-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fbecd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbecd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbecd-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="fbecd-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
