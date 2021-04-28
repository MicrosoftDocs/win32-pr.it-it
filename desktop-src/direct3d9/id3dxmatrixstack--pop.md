---
description: "Metodo ID3DXMATRIXStack::P op (D3dx9math.h): rimuove la matrice corrente dall'inizio dello stack."
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: Metodo ID3DXMATRIXStack::P op (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093504"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="69112-103">Metodo ID3DXMATRIXStack::P op (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="69112-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="69112-104">Rimuove la matrice corrente dall'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="69112-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="69112-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69112-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="69112-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69112-106">Parameters</span></span>

<span data-ttu-id="69112-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="69112-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69112-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69112-108">Return value</span></span>

<span data-ttu-id="69112-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69112-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69112-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69112-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69112-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="69112-111">Remarks</span></span>

<span data-ttu-id="69112-112">Si noti che questo metodo decrementa il numero di elementi nello stack di 1, rimuovendo in modo efficace la matrice corrente dall'inizio dello stack e innalzando di livello una matrice all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="69112-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="69112-113">Se il numero corrente di elementi nello stack è 0, questo metodo restituisce senza eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="69112-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="69112-114">Se il numero corrente di elementi nello stack è 1, questo metodo svuota lo stack.</span><span class="sxs-lookup"><span data-stu-id="69112-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="69112-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69112-115">Requirements</span></span>



| <span data-ttu-id="69112-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69112-116">Requirement</span></span> | <span data-ttu-id="69112-117">Valore</span><span class="sxs-lookup"><span data-stu-id="69112-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69112-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69112-118">Header</span></span><br/>  | <dl> <span data-ttu-id="69112-119"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="69112-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="69112-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="69112-120">Library</span></span><br/> | <dl> <span data-ttu-id="69112-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="69112-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69112-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69112-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69112-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="69112-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="69112-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="69112-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="69112-125">**ID3DXMATRIXStack::P ush**</span><span class="sxs-lookup"><span data-stu-id="69112-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




