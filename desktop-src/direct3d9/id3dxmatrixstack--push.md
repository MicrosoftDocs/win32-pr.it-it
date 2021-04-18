---
description: Aggiunge una matrice allo stack.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: Metodo ID3DXMATRIXStack::P USH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1678ad9481a7c76fdb0e92a0c3b2de66d638de71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322333"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="db356-103">Metodo ID3DXMATRIXStack::P USH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="db356-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="db356-104">Aggiunge una matrice allo stack.</span><span class="sxs-lookup"><span data-stu-id="db356-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="db356-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db356-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="db356-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db356-106">Parameters</span></span>

<span data-ttu-id="db356-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="db356-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db356-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db356-108">Return value</span></span>

<span data-ttu-id="db356-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db356-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db356-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db356-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db356-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db356-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db356-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="db356-112">Remarks</span></span>

<span data-ttu-id="db356-113">Questo metodo incrementa il numero di elementi nello stack di 1, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="db356-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="db356-114">Lo stack aumenterà in modo dinamico man mano che vengono aggiunti altri elementi.</span><span class="sxs-lookup"><span data-stu-id="db356-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="db356-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db356-115">Requirements</span></span>



| <span data-ttu-id="db356-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db356-116">Requirement</span></span> | <span data-ttu-id="db356-117">Valore</span><span class="sxs-lookup"><span data-stu-id="db356-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db356-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db356-118">Header</span></span><br/>  | <dl> <span data-ttu-id="db356-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="db356-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="db356-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="db356-120">Library</span></span><br/> | <dl> <span data-ttu-id="db356-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db356-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db356-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db356-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db356-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="db356-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="db356-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="db356-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="db356-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="db356-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




