---
description: Blocca un buffer di indice e ottiene un puntatore alla memoria del buffer dell'indice.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'Metodo ID3DXBaseMesh:: LockIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058584"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="2a997-103">Metodo ID3DXBaseMesh:: LockIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="2a997-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="2a997-104">Blocca un buffer di indice e ottiene un puntatore alla memoria del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2a997-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a997-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a997-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="2a997-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a997-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a997-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a997-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a997-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a997-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a997-109">Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2a997-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="2a997-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="2a997-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="2a997-111">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="2a997-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="2a997-112">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="2a997-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="2a997-113">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="2a997-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="2a997-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2a997-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="2a997-115">Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="2a997-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a997-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2a997-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2a997-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a997-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2a997-118">\*Puntatore void a un buffer contenente i dati dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2a997-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="2a997-119">Il numero di indici in questo buffer sarà uguale a [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="2a997-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a997-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a997-120">Return value</span></span>

<span data-ttu-id="2a997-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a997-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a997-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a997-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a997-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2a997-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a997-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a997-124">Remarks</span></span>

<span data-ttu-id="2a997-125">Quando si utilizzano buffer di indice, è possibile effettuare più chiamate di blocco.</span><span class="sxs-lookup"><span data-stu-id="2a997-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="2a997-126">Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.</span><span class="sxs-lookup"><span data-stu-id="2a997-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="2a997-127">Le chiamate DrawPrimitive non riusciranno con il conteggio dei blocchi in attesa su un buffer di indice attualmente impostato.</span><span class="sxs-lookup"><span data-stu-id="2a997-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a997-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a997-128">Requirements</span></span>



| <span data-ttu-id="2a997-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a997-129">Requirement</span></span> | <span data-ttu-id="2a997-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2a997-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a997-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a997-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2a997-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a997-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2a997-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a997-133">Library</span></span><br/> | <dl> <span data-ttu-id="2a997-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a997-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a997-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a997-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a997-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="2a997-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
