---
description: La funzione DbgInitialise Inizializza la libreria di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Funzione DbgInitialise (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327526"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="b2f38-104">DbgInitialise (funzione)</span><span class="sxs-lookup"><span data-stu-id="b2f38-104">DbgInitialise function</span></span>

<span data-ttu-id="b2f38-105">La funzione **DbgInitialise** Inizializza la libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="b2f38-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="b2f38-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b2f38-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f38-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="b2f38-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2f38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f38-109">*hInst*</span><span class="sxs-lookup"><span data-stu-id="b2f38-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f38-110">Handle per l'istanza del modulo.</span><span class="sxs-lookup"><span data-stu-id="b2f38-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f38-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2f38-111">Return value</span></span>

<span data-ttu-id="b2f38-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b2f38-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f38-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2f38-113">Remarks</span></span>

<span data-ttu-id="b2f38-114">In un eseguibile chiamare questo metodo prima di usare le funzionalità di debug DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b2f38-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="b2f38-115">Prima che l'eseguibile venga chiuso, chiamare la funzione [**DbgTerminate**](dbgterminate.md) per pulire la libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="b2f38-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="b2f38-116">In una DLL che si collega alla libreria di classi di base (Strmbase. lib), non è necessario chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b2f38-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="b2f38-117">La funzione viene chiamata automaticamente quando viene caricata la DLL.</span><span class="sxs-lookup"><span data-stu-id="b2f38-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f38-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2f38-118">Requirements</span></span>



| <span data-ttu-id="b2f38-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f38-119">Requirement</span></span> | <span data-ttu-id="b2f38-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b2f38-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f38-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2f38-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b2f38-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f38-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2f38-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2f38-123">Library</span></span><br/> | <dl> <span data-ttu-id="b2f38-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f38-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f38-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f38-126">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="b2f38-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




