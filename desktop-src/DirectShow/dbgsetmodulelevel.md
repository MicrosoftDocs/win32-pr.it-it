---
description: La funzione DbgSetModuleLevel imposta il livello di registrazione per uno o più tipi di messaggio. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Funzione DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327520"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="4a4d9-104">DbgSetModuleLevel (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a4d9-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="4a4d9-105">La funzione **DbgSetModuleLevel** imposta il livello di registrazione per uno o più tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4a4d9-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="4a4d9-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="4a4d9-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a4d9-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="4a4d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a4d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4d9-109">*Tipi*</span><span class="sxs-lookup"><span data-stu-id="4a4d9-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4d9-110">Combinazione bit per bit di uno o più tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4a4d9-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="4a4d9-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="4a4d9-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4d9-112">Livello di registrazione per i tipi di messaggio specificati.</span><span class="sxs-lookup"><span data-stu-id="4a4d9-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4d9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a4d9-113">Return value</span></span>

<span data-ttu-id="4a4d9-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4a4d9-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4d9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a4d9-115">Requirements</span></span>



| <span data-ttu-id="4a4d9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a4d9-116">Requirement</span></span> | <span data-ttu-id="4a4d9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4a4d9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4d9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a4d9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a4d9-119"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a4d9-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a4d9-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a4d9-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a4d9-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4a4d9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a4d9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a4d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4d9-123">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="4a4d9-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




