---
description: Questa funzione interrompe in modo forzato il programma chiamante se viene richiamato all'interno di un callout del caricatore. In caso contrario, non ha alcun effetto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324697"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="fd9d2-104">LdrFastFailInLoaderCallout (funzione)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="fd9d2-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd9d2-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="fd9d2-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd9d2-107">Questa funzione interrompe in modo forzato il programma chiamante se viene richiamato all'interno di un callout del caricatore.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="fd9d2-108">In caso contrario, non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9d2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd9d2-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="fd9d2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd9d2-110">Parameters</span></span>

<span data-ttu-id="fd9d2-111">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd9d2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd9d2-112">Return value</span></span>

<span data-ttu-id="fd9d2-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9d2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd9d2-114">Remarks</span></span>

<span data-ttu-id="fd9d2-115">Questa routine non rileva tutti i potenziali casi di deadlock; è possibile che un thread all'interno di un callout del caricatore acquisisca un blocco mentre un thread esterno a un callout del caricatore contiene lo stesso blocco ed effettua una chiamata al caricatore.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="fd9d2-116">In altre parole, può essere presente un'inversione dell'ordine di blocco tra il blocco del caricatore e un blocco client.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9d2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd9d2-117">Requirements</span></span>



| <span data-ttu-id="fd9d2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9d2-118">Requirement</span></span> | <span data-ttu-id="fd9d2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fd9d2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9d2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd9d2-120">Library</span></span><br/> | <dl> <span data-ttu-id="fd9d2-121"><dt>NTDll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd9d2-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd9d2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9d2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd9d2-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd9d2-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




