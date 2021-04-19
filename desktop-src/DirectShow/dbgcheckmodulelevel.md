---
description: La funzione DbgCheckModuleLevel controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati. Ignorato nelle compilazioni al dettaglio.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Funzione DbgCheckModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332693"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="d26ae-104">DbgCheckModuleLevel (funzione)</span><span class="sxs-lookup"><span data-stu-id="d26ae-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="d26ae-105">La `DbgCheckModuleLevel` funzione controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati.</span><span class="sxs-lookup"><span data-stu-id="d26ae-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="d26ae-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="d26ae-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d26ae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d26ae-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="d26ae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d26ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d26ae-109">*Tipi*</span><span class="sxs-lookup"><span data-stu-id="d26ae-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="d26ae-110">Combinazione bit per bit di uno o più tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="d26ae-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="d26ae-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="d26ae-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="d26ae-112">Livello di registrazione</span><span class="sxs-lookup"><span data-stu-id="d26ae-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d26ae-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d26ae-113">Return value</span></span>

<span data-ttu-id="d26ae-114">Restituisce **true** se la registrazione per uno dei tipi di messaggio specificati è impostata sul livello specificato o su un valore superiore.</span><span class="sxs-lookup"><span data-stu-id="d26ae-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="d26ae-115">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="d26ae-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d26ae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d26ae-116">Requirements</span></span>



| <span data-ttu-id="d26ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d26ae-117">Requirement</span></span> | <span data-ttu-id="d26ae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d26ae-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d26ae-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d26ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d26ae-120"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d26ae-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d26ae-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d26ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="d26ae-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d26ae-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d26ae-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d26ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d26ae-124">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="d26ae-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




