---
description: La funzione DbgDumpObjectRegister Visualizza informazioni sugli oggetti attivi. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Funzione DbgDumpObjectRegister (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327528"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="15b6c-104">DbgDumpObjectRegister (funzione)</span><span class="sxs-lookup"><span data-stu-id="15b6c-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="15b6c-105">La `DbgDumpObjectRegister` funzione Visualizza informazioni sugli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="15b6c-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="15b6c-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="15b6c-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b6c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15b6c-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="15b6c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15b6c-108">Parameters</span></span>

<span data-ttu-id="15b6c-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="15b6c-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15b6c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15b6c-110">Return value</span></span>

<span data-ttu-id="15b6c-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="15b6c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15b6c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="15b6c-112">Remarks</span></span>

<span data-ttu-id="15b6c-113">Nelle build di debug la libreria di debug gestisce un elenco di oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="15b6c-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="15b6c-114">L'elenco include tutti gli oggetti che derivano da [**CBaseObject**](cbaseobject.md), che sono stati creati dal modulo corrente e che non sono stati eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="15b6c-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="15b6c-115">I metodi del costruttore e del distruttore **CBaseObject** aggiornano l'elenco.</span><span class="sxs-lookup"><span data-stu-id="15b6c-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="15b6c-116">Questa funzione genera diversi messaggi di memoria del LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="15b6c-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="15b6c-117">Al livello di registrazione 1, la funzione Visualizza solo il numero totale di oggetti.</span><span class="sxs-lookup"><span data-stu-id="15b6c-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="15b6c-118">Al livello di registrazione 2 o superiore, viene visualizzato un elenco degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="15b6c-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b6c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15b6c-119">Requirements</span></span>



| <span data-ttu-id="15b6c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b6c-120">Requirement</span></span> | <span data-ttu-id="15b6c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="15b6c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b6c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15b6c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="15b6c-123"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15b6c-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15b6c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="15b6c-124">Library</span></span><br/> | <dl> <span data-ttu-id="15b6c-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15b6c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b6c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15b6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b6c-127">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="15b6c-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




