---
description: 'Metodo ID3DXMATRIXStack::P ush (D3dx9math.h): aggiunge una matrice nello stack.'
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: Metodo ID3DXMATRIXStack::P ush (D3dx9math.h)
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
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093505"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="48533-103">Metodo ID3DXMATRIXStack::P ush (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="48533-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="48533-104">Aggiunge una matrice nello stack.</span><span class="sxs-lookup"><span data-stu-id="48533-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="48533-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48533-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="48533-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="48533-106">Parameters</span></span>

<span data-ttu-id="48533-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="48533-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48533-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48533-108">Return value</span></span>

<span data-ttu-id="48533-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48533-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48533-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48533-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48533-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="48533-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="48533-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="48533-112">Remarks</span></span>

<span data-ttu-id="48533-113">Questo metodo incrementa il numero di elementi nello stack di 1, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="48533-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="48533-114">Lo stack aumenta in modo dinamico man appena vengono aggiunti altri elementi.</span><span class="sxs-lookup"><span data-stu-id="48533-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="48533-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48533-115">Requirements</span></span>



| <span data-ttu-id="48533-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="48533-116">Requirement</span></span> | <span data-ttu-id="48533-117">Valore</span><span class="sxs-lookup"><span data-stu-id="48533-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48533-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48533-118">Header</span></span><br/>  | <dl> <span data-ttu-id="48533-119"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="48533-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="48533-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="48533-120">Library</span></span><br/> | <dl> <span data-ttu-id="48533-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="48533-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48533-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48533-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48533-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="48533-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="48533-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="48533-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="48533-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="48533-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




