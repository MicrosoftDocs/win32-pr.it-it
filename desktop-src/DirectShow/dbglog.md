---
description: La macro DbgLog invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. Questa macro viene ignorata nelle compilazioni al dettaglio.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327523"
---
# <a name="dbglog-macro"></a><span data-ttu-id="56401-104">DbgLog (macro)</span><span class="sxs-lookup"><span data-stu-id="56401-104">DbgLog macro</span></span>

<span data-ttu-id="56401-105">La macro **DbgLog** invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati.</span><span class="sxs-lookup"><span data-stu-id="56401-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="56401-106">Questa macro viene ignorata nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="56401-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="56401-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56401-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="56401-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56401-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56401-109">*Tipi*</span><span class="sxs-lookup"><span data-stu-id="56401-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="56401-110">Combinazione bit per bit di uno o più tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="56401-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="56401-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="56401-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="56401-112">Livello di registrazione per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="56401-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="56401-113">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="56401-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="56401-114">Stringa di formato in stile **printf** .</span><span class="sxs-lookup"><span data-stu-id="56401-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="56401-115">*...*</span><span class="sxs-lookup"><span data-stu-id="56401-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="56401-116">Argomenti aggiuntivi per la stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="56401-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56401-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56401-117">Return value</span></span>

<span data-ttu-id="56401-118">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="56401-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56401-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="56401-119">Remarks</span></span>

<span data-ttu-id="56401-120">Se la registrazione del debug per uno dei tipi di messaggio è impostata sul livello specificato o su un valore superiore, questa macro invia la stringa formattata al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="56401-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="56401-121">La macro aggiunge automaticamente un carattere di nuova riga alla stringa di output.</span><span class="sxs-lookup"><span data-stu-id="56401-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="56401-122">Un set aggiuntivo di parentesi deve racchiudere i parametri della macro:</span><span class="sxs-lookup"><span data-stu-id="56401-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="56401-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56401-123">Requirements</span></span>



| <span data-ttu-id="56401-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="56401-124">Requirement</span></span> | <span data-ttu-id="56401-125">Valore</span><span class="sxs-lookup"><span data-stu-id="56401-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56401-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56401-126">Header</span></span><br/> | <dl> <span data-ttu-id="56401-127"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56401-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56401-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56401-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56401-129">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="56401-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




