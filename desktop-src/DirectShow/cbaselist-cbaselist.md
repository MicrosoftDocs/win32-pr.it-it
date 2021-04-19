---
description: Metodo del costruttore.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Costruttore CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328671"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="00528-103">Costruttore CBaseList. CBaseList (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="00528-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="00528-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="00528-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00528-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00528-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="00528-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00528-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="00528-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="00528-108">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="00528-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="00528-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="00528-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="00528-110">Dimensioni della cache del nodo.</span><span class="sxs-lookup"><span data-stu-id="00528-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00528-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="00528-111">Remarks</span></span>

<span data-ttu-id="00528-112">Per migliorare l'efficienza, la `CBaseList` classe mantiene una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="00528-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="00528-113">Se si conosce approssimativamente il numero di elementi che l'elenco conterrà, usare questa versione del costruttore.</span><span class="sxs-lookup"><span data-stu-id="00528-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="00528-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00528-114">Requirements</span></span>



| <span data-ttu-id="00528-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00528-115">Requirement</span></span> | <span data-ttu-id="00528-116">Valore</span><span class="sxs-lookup"><span data-stu-id="00528-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00528-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00528-117">Header</span></span><br/>  | <dl> <span data-ttu-id="00528-118"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00528-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="00528-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="00528-119">Library</span></span><br/> | <dl> <span data-ttu-id="00528-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00528-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00528-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00528-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00528-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="00528-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




