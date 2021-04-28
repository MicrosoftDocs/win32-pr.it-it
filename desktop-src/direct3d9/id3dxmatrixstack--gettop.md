---
description: "Metodo ID3DXMATRIXStack::GetTop (D3dx9math.h): recupera la matrice corrente all'inizio dello stack."
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: Metodo ID3DXMATRIXStack::GetTop (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093579"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="36d7f-103">Metodo ID3DXMATRIXStack::GetTop (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="36d7f-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="36d7f-104">Recupera la matrice corrente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="36d7f-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d7f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36d7f-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="36d7f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="36d7f-106">Parameters</span></span>

<span data-ttu-id="36d7f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="36d7f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36d7f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36d7f-108">Return value</span></span>

<span data-ttu-id="36d7f-109">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="36d7f-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="36d7f-110">Questo metodo restituisce un puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="36d7f-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d7f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="36d7f-111">Remarks</span></span>

<span data-ttu-id="36d7f-112">Non è garantito che il puntatore [**D3DXMATRIX**](d3dxmatrix.md) restituito da questo metodo sia valido dopo le successive operazioni dello stack.</span><span class="sxs-lookup"><span data-stu-id="36d7f-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="36d7f-113">Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. restituisce invece solo la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="36d7f-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d7f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36d7f-114">Requirements</span></span>



| <span data-ttu-id="36d7f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36d7f-115">Requirement</span></span> | <span data-ttu-id="36d7f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="36d7f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d7f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36d7f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="36d7f-118"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="36d7f-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="36d7f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="36d7f-119">Library</span></span><br/> | <dl> <span data-ttu-id="36d7f-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d7f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36d7f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36d7f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d7f-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="36d7f-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="36d7f-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="36d7f-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="36d7f-124">**ID3DXMATRIXStack::P ush**</span><span class="sxs-lookup"><span data-stu-id="36d7f-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




