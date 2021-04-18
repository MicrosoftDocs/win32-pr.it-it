---
description: Criteri di isolamento degli errori e FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Criteri di isolamento degli errori e FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523433"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="9a347-103">Criteri di isolamento degli errori e FailFast</span><span class="sxs-lookup"><span data-stu-id="9a347-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="9a347-104">COM+ esegue verifiche di coerenza e integrità interne estese.</span><span class="sxs-lookup"><span data-stu-id="9a347-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="9a347-105">Se COM+ rileva una condizione di errore interno imprevista, termina immediatamente il processo.</span><span class="sxs-lookup"><span data-stu-id="9a347-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="9a347-106">Questi criteri, denominati *FailFast*, facilitano il contenimento degli errori e i risultati in sistemi più affidabili e affidabili.</span><span class="sxs-lookup"><span data-stu-id="9a347-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="9a347-107">Si consideri un caso in cui COM+ rileva che una delle relative strutture di dati è in uno stato danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9a347-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="9a347-108">A questo punto, sia la provocazione che la grandezza del danneggiamento sono sconosciute e, sfortunatamente, COM+ non è in grado di indicare la distanza del danno.</span><span class="sxs-lookup"><span data-stu-id="9a347-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="9a347-109">Tuttavia, anche se COM+ è in uno stato indeterminato, non viene eseguito in isolamento.</span><span class="sxs-lookup"><span data-stu-id="9a347-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="9a347-110">Analogamente ad altre dll, è ospitato in un ambiente di processo e condivide un singolo spazio di indirizzi con l'eseguibile del programma principale e molte altre dll.</span><span class="sxs-lookup"><span data-stu-id="9a347-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="9a347-111">Pertanto, COM+ presuppone che l'intero processo sia stato danneggiato e che il processo venga terminato immediatamente per impedire che la distribuzione di informazioni potenzialmente danneggiate ad altri processi o, peggio ancora, non consenta il commit e la durevolezza dei dati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="9a347-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="9a347-112">COM+ non consente la propagazione delle eccezioni all'esterno di un contesto.</span><span class="sxs-lookup"><span data-stu-id="9a347-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="9a347-113">Se si verifica un'eccezione durante l'esecuzione all'interno di un contesto COM+ e l'applicazione non rileva l'eccezione prima di restituire il contesto, COM+ intercetta l'eccezione e termina il processo.</span><span class="sxs-lookup"><span data-stu-id="9a347-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="9a347-114">L'uso del criterio FailFast in questo caso si basa sul presupposto che l'eccezione abbia indeterminato lo stato del processo. non è sicuro continuare l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9a347-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="9a347-115">Per gli sviluppatori o gli amministratori, è necessario esaminare il registro applicazioni Visualizzatore eventi per informazioni dettagliate su qualsiasi azione FailFast o errori gravi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a347-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a347-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a347-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a347-117">Individuazione dell'origine di un errore</span><span class="sxs-lookup"><span data-stu-id="9a347-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="9a347-118">Modalità di modifica dei valori restituiti da COM+</span><span class="sxs-lookup"><span data-stu-id="9a347-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="9a347-119">Interpretazione dei codici di errore</span><span class="sxs-lookup"><span data-stu-id="9a347-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="9a347-120">Strategie per la gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="9a347-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="9a347-121">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="9a347-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



