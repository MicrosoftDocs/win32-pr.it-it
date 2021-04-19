---
description: La macro di avviso genera un promemoria in fase di compilazione. Questa macro genera una stringa che include la stringa del parametro, il nome del file di origine e il numero di riga.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: RICORDA (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328452"
---
# <a name="remind"></a><span data-ttu-id="9bd7e-104">RICORDARE</span><span class="sxs-lookup"><span data-stu-id="9bd7e-104">REMIND</span></span>

<span data-ttu-id="9bd7e-105">La `REMIND` macro genera un promemoria in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="9bd7e-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="9bd7e-106">Questa macro genera una stringa che include la stringa del parametro, il nome del file di origine e il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="9bd7e-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="9bd7e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bd7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd7e-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="9bd7e-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="9bd7e-109">Stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="9bd7e-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bd7e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bd7e-110">Remarks</span></span>

<span data-ttu-id="9bd7e-111">Questa macro è utile per la generazione di avvisi in fase di compilazione:</span><span class="sxs-lookup"><span data-stu-id="9bd7e-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="9bd7e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bd7e-112">Requirements</span></span>



| <span data-ttu-id="9bd7e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd7e-113">Requirement</span></span> | <span data-ttu-id="9bd7e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9bd7e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd7e-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bd7e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9bd7e-116"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7e-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9bd7e-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="9bd7e-117">Library</span></span><br/> | <dl> <span data-ttu-id="9bd7e-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd7e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bd7e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd7e-120">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="9bd7e-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




