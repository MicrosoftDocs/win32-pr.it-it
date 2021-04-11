---
description: La parte più problematica della scrittura di componenti è la gestione di possibili errori.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Gestione degli errori in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127794"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="844ce-103">Gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="844ce-103">Handling Errors in COM+</span></span>

<span data-ttu-id="844ce-104">La parte più problematica della scrittura di componenti è la gestione di possibili errori.</span><span class="sxs-lookup"><span data-stu-id="844ce-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="844ce-105">Il tentativo di determinare cosa può andare male e le operazioni da eseguire su di esso può essere difficile in caso di condizioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="844ce-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="844ce-106">Errori comuni che il componente potrebbe controllare e gestire sono le connessioni di rete non riuscite, errori di sicurezza ed errori associati a oggetti non raggiungibili.</span><span class="sxs-lookup"><span data-stu-id="844ce-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="844ce-107">Inoltre, è possibile sviluppare codici di errore personalizzati per segnalare errori specifici dell'interfaccia, ad esempio quando una regola business è stata violata.</span><span class="sxs-lookup"><span data-stu-id="844ce-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="844ce-108">In conformità con il modello di programmazione COM+, un oggetto può (e spesso) chiamare metodi di interfaccia su altri oggetti per eseguire il lavoro.</span><span class="sxs-lookup"><span data-stu-id="844ce-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="844ce-109">Poiché i programmatori possono scrivere componenti in linguaggi di programmazione diversi, COM+ richiede che tutti i meccanismi di gestione degli errori siano indipendenti dalla lingua, ad esempio: HRESULTs e raccolte [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="844ce-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="844ce-110">In questa sezione sono inclusi argomenti, descritti nella tabella seguente, in cui vengono illustrate le tecniche per la gestione degli errori nelle applicazioni COM+, le funzionalità di COM+ che influiscono sul comportamento degli errori e suggerimenti per la diagnosi degli errori COM+.</span><span class="sxs-lookup"><span data-stu-id="844ce-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="844ce-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="844ce-111">Topic</span></span>                                                                                           | <span data-ttu-id="844ce-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="844ce-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="844ce-113">Strategie per la gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="844ce-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="844ce-114">Elenca e descrive le linee guida di base per la gestione degli errori in COM+, incluso il momento in cui usare HRESULTs e le raccolte [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="844ce-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="844ce-115">Modalità di modifica dei valori restituiti da COM+</span><span class="sxs-lookup"><span data-stu-id="844ce-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="844ce-116">Identifica la singola condizione in cui COM+ converte un valore HRESULT standard in un codice di errore COM+ prima di passarlo di nuovo al chiamante.</span><span class="sxs-lookup"><span data-stu-id="844ce-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="844ce-117">Criteri di isolamento degli errori e FailFast</span><span class="sxs-lookup"><span data-stu-id="844ce-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="844ce-118">Mostra in che modo l'isolamento degli errori e i criteri di FailFast influiscono sul comportamento COM+.</span><span class="sxs-lookup"><span data-stu-id="844ce-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="844ce-119">Individuazione dell'origine di un errore</span><span class="sxs-lookup"><span data-stu-id="844ce-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="844ce-120">Viene descritto come è possibile diagnosticare l'origine e ottenere una descrizione degli errori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="844ce-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="844ce-121">Interpretazione dei codici di errore</span><span class="sxs-lookup"><span data-stu-id="844ce-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="844ce-122">Identifica il meccanismo di gestione degli errori predominante per Microsoft Visual C++, il linguaggio Java e Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="844ce-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="844ce-123">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="844ce-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="844ce-124">Fornisce assistenza aggiuntiva per la diagnosi degli errori.</span><span class="sxs-lookup"><span data-stu-id="844ce-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="844ce-125">Contattare il supporto tecnico</span><span class="sxs-lookup"><span data-stu-id="844ce-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="844ce-126">Identifica importanti informazioni di risoluzione dei problemi da fornire quando si contatta il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="844ce-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="844ce-127">Per informazioni dettagliate sulla gestione degli errori associati a vari servizi COM+, vedere le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="844ce-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="844ce-128">Velocizzare le transazioni inviando una notifica all'oggetto radice</span><span class="sxs-lookup"><span data-stu-id="844ce-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="844ce-129">[Gestione degli errori](handling-errors-in-queued-components.md) (per i componenti in coda)</span><span class="sxs-lookup"><span data-stu-id="844ce-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="844ce-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="844ce-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="844ce-131">Debug di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="844ce-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




