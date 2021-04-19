---
description: La macro nota Invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Nota (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332632"
---
# <a name="note"></a><span data-ttu-id="a92d8-104">NOTA</span><span class="sxs-lookup"><span data-stu-id="a92d8-104">NOTE</span></span>

<span data-ttu-id="a92d8-105">La `NOTE` macro invia una stringa al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="a92d8-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="a92d8-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="a92d8-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="a92d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a92d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92d8-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span><span class="sxs-lookup"><span data-stu-id="a92d8-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="a92d8-109">Stringa di formato in stile printf.</span><span class="sxs-lookup"><span data-stu-id="a92d8-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="a92d8-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*-*arg5*</span><span class="sxs-lookup"><span data-stu-id="a92d8-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="a92d8-111">Argomenti aggiuntivi per la stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="a92d8-111">Additional arguments for the format string.</span></span> <span data-ttu-id="a92d8-112">Il numero di argomenti deve corrispondere al nome della macro.</span><span class="sxs-lookup"><span data-stu-id="a92d8-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="a92d8-113">Ad esempio, **Note1** accetta un argomento e **NOTE5** accetta cinque argomenti.</span><span class="sxs-lookup"><span data-stu-id="a92d8-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a92d8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a92d8-114">Remarks</span></span>

<span data-ttu-id="a92d8-115">Queste macro sono varianti della macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="a92d8-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="a92d8-116">Generano messaggi di traccia del LOG di livello 5 \_ .</span><span class="sxs-lookup"><span data-stu-id="a92d8-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="a92d8-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a92d8-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="a92d8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a92d8-118">Requirements</span></span>



| <span data-ttu-id="a92d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92d8-119">Requirement</span></span> | <span data-ttu-id="a92d8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a92d8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a92d8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a92d8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a92d8-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a92d8-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a92d8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a92d8-123">Library</span></span><br/> | <dl> <span data-ttu-id="a92d8-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a92d8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a92d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a92d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92d8-126">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="a92d8-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




