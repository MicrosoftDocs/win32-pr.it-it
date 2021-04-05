---
description: Informazioni sul metodo del costruttore per CGenericList. CGenericList (Wxlist. h). Questo metodo usa il parametro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Costruttore CGenericList. CGenericList (Wxlist. h)-parametro pName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103886336"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="d7f13-104">Costruttore CGenericList. CGenericList (Wxlist. h)-parametro pName</span><span class="sxs-lookup"><span data-stu-id="d7f13-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="d7f13-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d7f13-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f13-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7f13-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="d7f13-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7f13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f13-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="d7f13-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f13-109">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d7f13-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7f13-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7f13-110">Remarks</span></span>

<span data-ttu-id="d7f13-111">Per migliorare l'efficienza, la `CGenericList` classe mantiene una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="d7f13-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="d7f13-112">Questa versione del costruttore usa una dimensione della cache predefinita.</span><span class="sxs-lookup"><span data-stu-id="d7f13-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f13-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7f13-113">Requirements</span></span>

| <span data-ttu-id="d7f13-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f13-114">Requirement</span></span> | <span data-ttu-id="d7f13-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d7f13-115">Value</span></span> |
|-|-|
| <span data-ttu-id="d7f13-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7f13-116">Header</span></span> | <span data-ttu-id="d7f13-117">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="d7f13-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="d7f13-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7f13-118">Library</span></span>| <span data-ttu-id="d7f13-119">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="d7f13-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7f13-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7f13-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f13-121">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="d7f13-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




