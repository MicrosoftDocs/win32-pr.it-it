---
description: Metodo del costruttore.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Costruttore CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328669"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="06210-103">Costruttore CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="06210-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="06210-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="06210-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06210-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06210-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="06210-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06210-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="06210-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="06210-108">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="06210-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06210-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="06210-109">Remarks</span></span>

<span data-ttu-id="06210-110">Per migliorare l'efficienza, la `CBaseList` classe mantiene una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="06210-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="06210-111">Questa versione del costruttore usa una dimensione della cache predefinita.</span><span class="sxs-lookup"><span data-stu-id="06210-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="06210-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06210-112">Requirements</span></span>



| <span data-ttu-id="06210-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="06210-113">Requirement</span></span> | <span data-ttu-id="06210-114">Valore</span><span class="sxs-lookup"><span data-stu-id="06210-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06210-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06210-115">Header</span></span><br/>  | <dl> <span data-ttu-id="06210-116"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06210-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="06210-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="06210-117">Library</span></span><br/> | <dl> <span data-ttu-id="06210-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06210-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06210-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06210-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06210-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="06210-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




