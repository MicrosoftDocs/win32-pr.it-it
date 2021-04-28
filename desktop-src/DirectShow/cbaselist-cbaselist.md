---
description: Costruttore CBaseList.CBaseList(TCHAR \* , INT) - Metodo costruttore.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Costruttore CBaseList.CBaseList(TCHAR*, INT) (Wxlist.h)
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099639"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="d0b58-103">Costruttore CBaseList.CBaseList(TCHAR \* , INT)</span><span class="sxs-lookup"><span data-stu-id="d0b58-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="d0b58-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d0b58-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b58-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0b58-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="d0b58-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0b58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b58-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="d0b58-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b58-108">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d0b58-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="d0b58-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="d0b58-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b58-110">Dimensioni della cache del nodo.</span><span class="sxs-lookup"><span data-stu-id="d0b58-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0b58-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0b58-111">Remarks</span></span>

<span data-ttu-id="d0b58-112">Per migliorare l'efficienza, `CBaseList` la classe gestisce una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="d0b58-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="d0b58-113">Se si conosce approssimativamente il numero di elementi che saranno presenti nell'elenco, usare questa versione del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d0b58-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b58-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0b58-114">Requirements</span></span>



| <span data-ttu-id="d0b58-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b58-115">Requirement</span></span> | <span data-ttu-id="d0b58-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d0b58-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b58-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0b58-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d0b58-118"><dt>Wxlist.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b58-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d0b58-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0b58-119">Library</span></span><br/> | <dl> <span data-ttu-id="d0b58-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b58-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b58-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0b58-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b58-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="d0b58-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




