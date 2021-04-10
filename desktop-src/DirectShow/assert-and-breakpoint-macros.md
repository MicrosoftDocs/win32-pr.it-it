---
description: Macro di asserzione e punti di interruzione
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macro di asserzione e punti di interruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125349"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="855d6-103">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="855d6-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="855d6-104">Le [classi base di DirectShow](directshow-base-classes.md) forniscono diverse macro che eseguono asserzioni o generano punti di interruzione.</span><span class="sxs-lookup"><span data-stu-id="855d6-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="855d6-105">Macro</span><span class="sxs-lookup"><span data-stu-id="855d6-105">Macro</span></span>                                        | <span data-ttu-id="855d6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="855d6-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="855d6-107">**ASSERT**</span><span class="sxs-lookup"><span data-stu-id="855d6-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="855d6-108">Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è **false**.</span><span class="sxs-lookup"><span data-stu-id="855d6-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="855d6-109">**DbgAssertAligned**</span><span class="sxs-lookup"><span data-stu-id="855d6-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="855d6-110">Verifica se un puntatore è allineato a un limite specificato.</span><span class="sxs-lookup"><span data-stu-id="855d6-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="855d6-111">**DbgBreak**</span><span class="sxs-lookup"><span data-stu-id="855d6-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="855d6-112">Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="855d6-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="855d6-113">**Esegui \_ asserzione**</span><span class="sxs-lookup"><span data-stu-id="855d6-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="855d6-114">Valuta un'espressione nelle compilazioni di debug e di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="855d6-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="855d6-115">Nelle build di debug, Visualizza un messaggio di diagnostica se l'espressione è **false**.</span><span class="sxs-lookup"><span data-stu-id="855d6-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="855d6-116">**KASSERT**</span><span class="sxs-lookup"><span data-stu-id="855d6-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="855d6-117">Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è **false**.</span><span class="sxs-lookup"><span data-stu-id="855d6-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="855d6-118">**KDbgBreak**</span><span class="sxs-lookup"><span data-stu-id="855d6-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="855d6-119">Causa un'eccezione del punto di interruzione e registra la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="855d6-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="855d6-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="855d6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855d6-121">Utilità di debug</span><span class="sxs-lookup"><span data-stu-id="855d6-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



