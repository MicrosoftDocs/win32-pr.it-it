---
description: La macro del nome genera una stringa di solo debug.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOME (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328074"
---
# <a name="name"></a><span data-ttu-id="5b078-103">NAME</span><span class="sxs-lookup"><span data-stu-id="5b078-103">NAME</span></span>

<span data-ttu-id="5b078-104">La macro del **nome** genera una stringa di solo debug.</span><span class="sxs-lookup"><span data-stu-id="5b078-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="5b078-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b078-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b078-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="5b078-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="5b078-107">Stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="5b078-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b078-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b078-108">Remarks</span></span>

<span data-ttu-id="5b078-109">Nelle build di debug questa macro è equivalente alla macro di **testo** .</span><span class="sxs-lookup"><span data-stu-id="5b078-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="5b078-110">Nelle compilazioni finali, viene risolto in (TCHAR \* ) **null**.</span><span class="sxs-lookup"><span data-stu-id="5b078-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="5b078-111">Questa macro è utile quando si dichiara il nome di un oggetto che deriva dalla classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="5b078-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="5b078-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b078-112">Requirements</span></span>



| <span data-ttu-id="5b078-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b078-113">Requirement</span></span> | <span data-ttu-id="5b078-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5b078-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b078-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b078-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5b078-116"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b078-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b078-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b078-117">Library</span></span><br/> | <dl> <span data-ttu-id="5b078-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5b078-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b078-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b078-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b078-120">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="5b078-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




