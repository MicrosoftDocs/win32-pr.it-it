---
description: Causa un'eccezione del punto di interruzione e registra la stringa specificata utilizzando la macro DbgLog. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324789"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="f8ede-104">KDbgBreak (macro)</span><span class="sxs-lookup"><span data-stu-id="f8ede-104">KDbgBreak macro</span></span>

<span data-ttu-id="f8ede-105">Causa un'eccezione del punto di interruzione e registra la stringa specificata utilizzando la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ede-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="f8ede-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="f8ede-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ede-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8ede-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="f8ede-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8ede-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ede-109">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="f8ede-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ede-110">Stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="f8ede-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ede-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8ede-111">Return value</span></span>

<span data-ttu-id="f8ede-112">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f8ede-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ede-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8ede-113">Remarks</span></span>

<span data-ttu-id="f8ede-114">A differenza della macro [**DbgBreak**](dbgbreak.md) , questa macro non visualizza una finestra di messaggio che richiede all'utente.</span><span class="sxs-lookup"><span data-stu-id="f8ede-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="f8ede-115">Nelle compilazioni di debug, causa automaticamente un'eccezione del punto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="f8ede-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ede-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8ede-116">Requirements</span></span>



| <span data-ttu-id="f8ede-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ede-117">Requirement</span></span> | <span data-ttu-id="f8ede-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f8ede-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ede-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8ede-119">Header</span></span><br/> | <dl> <span data-ttu-id="f8ede-120"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ede-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ede-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8ede-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ede-122">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="f8ede-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




