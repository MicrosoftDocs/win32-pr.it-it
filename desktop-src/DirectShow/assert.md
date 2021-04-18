---
description: Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è FALSE. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328275"
---
# <a name="assert-macro"></a><span data-ttu-id="355d9-104">ASSERT (macro)</span><span class="sxs-lookup"><span data-stu-id="355d9-104">ASSERT macro</span></span>

<span data-ttu-id="355d9-105">Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è **false**.</span><span class="sxs-lookup"><span data-stu-id="355d9-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="355d9-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="355d9-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="355d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="355d9-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="355d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="355d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355d9-109">*cond*</span><span class="sxs-lookup"><span data-stu-id="355d9-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="355d9-110">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="355d9-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355d9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="355d9-111">Return value</span></span>

<span data-ttu-id="355d9-112">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="355d9-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="355d9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="355d9-113">Remarks</span></span>

<span data-ttu-id="355d9-114">Nelle compilazioni di debug, se l'espressione è **false**, questa macro Visualizza una finestra di messaggio con il testo dell'espressione, il nome del file di origine e il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="355d9-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="355d9-115">L'utente può ignorare l'asserzione, immettere il debugger o chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="355d9-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="355d9-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="355d9-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="355d9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="355d9-117">Requirements</span></span>



| <span data-ttu-id="355d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="355d9-118">Requirement</span></span> | <span data-ttu-id="355d9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="355d9-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="355d9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="355d9-120">Header</span></span><br/> | <dl> <span data-ttu-id="355d9-121"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="355d9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="355d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355d9-123">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="355d9-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




