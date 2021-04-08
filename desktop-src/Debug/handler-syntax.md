---
description: In questa sezione vengono descritte la sintassi e l'utilizzo della gestione strutturata delle eccezioni come implementato nel compilatore di ottimizzazione Microsoft C/C++. Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo di gestione delle eccezioni strutturato.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintassi del gestore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877325"
---
# <a name="handler-syntax"></a><span data-ttu-id="5504f-104">Sintassi del gestore</span><span class="sxs-lookup"><span data-stu-id="5504f-104">Handler Syntax</span></span>

<span data-ttu-id="5504f-105">In questa sezione vengono descritte la sintassi e l'utilizzo della gestione strutturata delle eccezioni come implementato nel compilatore di ottimizzazione Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="5504f-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="5504f-106">Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo di gestione delle eccezioni strutturato.</span><span class="sxs-lookup"><span data-stu-id="5504f-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="5504f-107">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="5504f-107">Keyword</span></span>         | <span data-ttu-id="5504f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5504f-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5504f-109">**\_\_provare**</span><span class="sxs-lookup"><span data-stu-id="5504f-109">**\_\_try**</span></span>     | <span data-ttu-id="5504f-110">Inizia un corpo sorvegliato del codice.</span><span class="sxs-lookup"><span data-stu-id="5504f-110">Begins a guarded body of code.</span></span> <span data-ttu-id="5504f-111">Usato con la parola chiave **\_ \_ except** per costruire un [gestore di eccezioni](exception-handler-syntax.md)o con la parola chiave **\_ \_ finally** per costruire un gestore di [terminazione](termination-handler-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5504f-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="5504f-112">**\_\_ad eccezione**</span><span class="sxs-lookup"><span data-stu-id="5504f-112">**\_\_except**</span></span>  | <span data-ttu-id="5504f-113">Inizia un blocco di codice che viene eseguito solo quando si verifica un'eccezione all'interno del blocco **\_ \_ try** associato.</span><span class="sxs-lookup"><span data-stu-id="5504f-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="5504f-114">**\_\_Infine**</span><span class="sxs-lookup"><span data-stu-id="5504f-114">**\_\_finally**</span></span> | <span data-ttu-id="5504f-115">Inizia un blocco di codice che viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try** associato.</span><span class="sxs-lookup"><span data-stu-id="5504f-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="5504f-116">**\_\_lasciare**</span><span class="sxs-lookup"><span data-stu-id="5504f-116">**\_\_leave**</span></span>   | <span data-ttu-id="5504f-117">Consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5504f-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="5504f-118">Il compilatore interpreta inoltre le funzioni [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)e [**AbnormalTermination**](abnormaltermination.md) come parole chiave e il loro utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="5504f-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="5504f-119">Di seguito sono riportate brevi descrizioni di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="5504f-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="5504f-120">Funzione</span><span class="sxs-lookup"><span data-stu-id="5504f-120">Function</span></span>                                                   | <span data-ttu-id="5504f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5504f-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5504f-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="5504f-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="5504f-123">Restituisce un codice che identifica il tipo di eccezione.</span><span class="sxs-lookup"><span data-stu-id="5504f-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="5504f-124">Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro o dal blocco del gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="5504f-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="5504f-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="5504f-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="5504f-126">Restituisce un puntatore a una struttura di [**\_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene i puntatori al record di contesto e al record di eccezione.</span><span class="sxs-lookup"><span data-stu-id="5504f-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="5504f-127">Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="5504f-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="5504f-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="5504f-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="5504f-129">Indica se il flusso di controllo ha lasciato il blocco **\_ \_ try** associato in sequenza dopo l'esecuzione dell'ultima istruzione nel blocco.</span><span class="sxs-lookup"><span data-stu-id="5504f-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="5504f-130">Questa funzione può essere chiamata solo dall'interno del blocco **\_ \_ finally** di un gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="5504f-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



