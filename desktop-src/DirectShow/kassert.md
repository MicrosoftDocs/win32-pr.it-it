---
description: Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è FALSE. Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati utilizzando la macro DbgLog. Ignorato nelle compilazioni al dettaglio.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333429"
---
# <a name="kassert-macro"></a><span data-ttu-id="0aa99-105">KASSERT (macro)</span><span class="sxs-lookup"><span data-stu-id="0aa99-105">KASSERT macro</span></span>

<span data-ttu-id="0aa99-106">Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è **false**.</span><span class="sxs-lookup"><span data-stu-id="0aa99-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="0aa99-107">Il testo dell'espressione, il nome del file di origine e il numero di riga vengono registrati utilizzando la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa99-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="0aa99-108">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="0aa99-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa99-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0aa99-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="0aa99-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0aa99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa99-111">*cond*</span><span class="sxs-lookup"><span data-stu-id="0aa99-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa99-112">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="0aa99-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0aa99-113">Return value</span></span>

<span data-ttu-id="0aa99-114">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0aa99-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa99-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0aa99-115">Remarks</span></span>

<span data-ttu-id="0aa99-116">Diversamente dalle macro [**Assert**](assert.md) ed [**Execute \_ Assert**](execute-assert.md) , questa macro non visualizza una finestra di messaggio che richiede all'utente.</span><span class="sxs-lookup"><span data-stu-id="0aa99-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="0aa99-117">Nelle compilazioni di debug, se l'espressione è **false**, la macro causa automaticamente un'eccezione del punto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="0aa99-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa99-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aa99-118">Requirements</span></span>



| <span data-ttu-id="0aa99-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa99-119">Requirement</span></span> | <span data-ttu-id="0aa99-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0aa99-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa99-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aa99-121">Header</span></span><br/> | <dl> <span data-ttu-id="0aa99-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa99-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa99-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aa99-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa99-124">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="0aa99-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




