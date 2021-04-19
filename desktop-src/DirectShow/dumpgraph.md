---
description: La funzione DumpGraph invia informazioni su un grafico di filtro al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Funzione DumpGraph (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329359"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="70223-104">DumpGraph (funzione)</span><span class="sxs-lookup"><span data-stu-id="70223-104">DumpGraph function</span></span>

<span data-ttu-id="70223-105">La `DumpGraph` funzione Invia informazioni su un grafico di filtro al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="70223-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="70223-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="70223-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="70223-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70223-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="70223-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70223-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70223-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="70223-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="70223-110">Puntatore all'interfaccia [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="70223-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="70223-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="70223-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="70223-112">Livello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="70223-112">Logging level.</span></span> <span data-ttu-id="70223-113">La funzione genera un \_ messaggio di traccia del log con il livello di registrazione specificato.</span><span class="sxs-lookup"><span data-stu-id="70223-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70223-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70223-114">Return value</span></span>

<span data-ttu-id="70223-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="70223-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70223-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70223-116">Requirements</span></span>



| <span data-ttu-id="70223-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70223-117">Requirement</span></span> | <span data-ttu-id="70223-118">Valore</span><span class="sxs-lookup"><span data-stu-id="70223-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70223-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70223-119">Header</span></span><br/>  | <dl> <span data-ttu-id="70223-120"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70223-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70223-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="70223-121">Library</span></span><br/> | <dl> <span data-ttu-id="70223-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="70223-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70223-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70223-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70223-124">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="70223-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




