---
description: Blocca un buffer dei vertici e ottiene un puntatore alla memoria del buffer del vertice.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'Metodo ID3DXBaseMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322849"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="7b87c-103">Metodo ID3DXBaseMesh:: LockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="7b87c-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="7b87c-104">Blocca un buffer dei vertici e ottiene un puntatore alla memoria del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="7b87c-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b87c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b87c-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="7b87c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b87c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b87c-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b87c-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b87c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b87c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b87c-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="7b87c-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="7b87c-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="7b87c-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="7b87c-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="7b87c-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="7b87c-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="7b87c-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="7b87c-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="7b87c-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="7b87c-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7b87c-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="7b87c-115">Nosovrascrive D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="7b87c-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="7b87c-116">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="7b87c-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b87c-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7b87c-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7b87c-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b87c-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7b87c-119">\*Puntatore void a un buffer contenente i dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="7b87c-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b87c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b87c-120">Return value</span></span>

<span data-ttu-id="7b87c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b87c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b87c-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b87c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7b87c-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7b87c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b87c-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b87c-124">Remarks</span></span>

<span data-ttu-id="7b87c-125">Quando si utilizzano i buffer dei vertici, è possibile effettuare più chiamate di blocco; Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.</span><span class="sxs-lookup"><span data-stu-id="7b87c-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="7b87c-126">Le chiamate DrawPrimitive non riusciranno con il conteggio dei blocchi in attesa su qualsiasi buffer vertex attualmente impostato.</span><span class="sxs-lookup"><span data-stu-id="7b87c-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b87c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b87c-127">Requirements</span></span>



| <span data-ttu-id="7b87c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b87c-128">Requirement</span></span> | <span data-ttu-id="7b87c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7b87c-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b87c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b87c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7b87c-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b87c-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7b87c-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b87c-132">Library</span></span><br/> | <dl> <span data-ttu-id="7b87c-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b87c-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b87c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b87c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b87c-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="7b87c-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
