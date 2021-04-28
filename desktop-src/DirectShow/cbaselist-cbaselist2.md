---
description: 'Costruttore CBaseList.CBaseList : metodo costruttore.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Costruttore CBaseList.CBaseList (Wxlist.h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096328"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="cec8b-103">Costruttore CBaseList.CBaseList</span><span class="sxs-lookup"><span data-stu-id="cec8b-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="cec8b-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="cec8b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cec8b-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="cec8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cec8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec8b-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="cec8b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cec8b-108">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="cec8b-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cec8b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="cec8b-109">Remarks</span></span>

<span data-ttu-id="cec8b-110">Per migliorare l'efficienza, `CBaseList` la classe gestisce una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="cec8b-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="cec8b-111">Questa versione del costruttore usa una dimensione della cache predefinita.</span><span class="sxs-lookup"><span data-stu-id="cec8b-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec8b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cec8b-112">Requirements</span></span>



| <span data-ttu-id="cec8b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec8b-113">Requirement</span></span> | <span data-ttu-id="cec8b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cec8b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec8b-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cec8b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cec8b-116"><dt>Wxlist.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cec8b-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cec8b-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="cec8b-117">Library</span></span><br/> | <dl> <span data-ttu-id="cec8b-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cec8b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec8b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cec8b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec8b-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="cec8b-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




