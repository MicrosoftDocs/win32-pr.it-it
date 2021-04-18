---
description: Le funzioni seguenti vengono utilizzate nella gestione strutturata delle eccezioni.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funzioni di gestione delle eccezioni strutturate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304662"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="786d7-103">Funzioni di gestione delle eccezioni strutturate</span><span class="sxs-lookup"><span data-stu-id="786d7-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="786d7-104">Le funzioni seguenti vengono utilizzate nella gestione strutturata delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="786d7-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="786d7-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="786d7-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="786d7-106">Indica se il blocco **\_ \_ try** di un gestore di terminazione è terminato normalmente.</span><span class="sxs-lookup"><span data-stu-id="786d7-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="786d7-107">**AddVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="786d7-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="786d7-108">Registra un gestore di continuazione vettoriale.</span><span class="sxs-lookup"><span data-stu-id="786d7-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="786d7-109">**AddVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="786d7-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="786d7-110">Registra un gestore di eccezioni vettoriale.</span><span class="sxs-lookup"><span data-stu-id="786d7-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="786d7-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="786d7-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="786d7-112">Recupera un codice che identifica il tipo di eccezione che si è verificata.</span><span class="sxs-lookup"><span data-stu-id="786d7-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="786d7-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="786d7-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="786d7-114">Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si è verificata l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="786d7-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="786d7-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="786d7-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="786d7-116">Genera un'eccezione nel thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="786d7-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="786d7-117">**RemoveVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="786d7-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="786d7-118">Annulla la registrazione di un gestore di continuazione vettoriale.</span><span class="sxs-lookup"><span data-stu-id="786d7-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="786d7-119">**RemoveVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="786d7-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="786d7-120">Annulla la registrazione di un gestore di eccezioni vettoriale.</span><span class="sxs-lookup"><span data-stu-id="786d7-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="786d7-121">**RtlAddGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="786d7-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="786d7-122">Informa il sistema di una tabella di funzioni dinamiche che rappresenta un'area di memoria contenente il codice.</span><span class="sxs-lookup"><span data-stu-id="786d7-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="786d7-123">**RtlDeleteGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="786d7-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="786d7-124">Informa il sistema che una tabella di funzioni dinamiche segnalata in precedenza non è più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="786d7-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="786d7-125">**RtlGrowFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="786d7-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="786d7-126">Segnala che una tabella di funzioni dinamiche è aumentata di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="786d7-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="786d7-127">**SetUnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="786d7-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="786d7-128">Consente a un'applicazione di sostituire il gestore di eccezioni di primo livello di ogni thread e processo.</span><span class="sxs-lookup"><span data-stu-id="786d7-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="786d7-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="786d7-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="786d7-130">Passa le eccezioni non gestite al debugger, se è in corso il debug del processo.</span><span class="sxs-lookup"><span data-stu-id="786d7-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="786d7-131">**VectoredHandler**</span><span class="sxs-lookup"><span data-stu-id="786d7-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="786d7-132">Funzione definita dall'applicazione che funge da gestore di eccezioni vettoriale.</span><span class="sxs-lookup"><span data-stu-id="786d7-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="786d7-133">Le funzioni seguenti vengono utilizzate solo in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="786d7-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="786d7-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="786d7-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="786d7-135">Aggiunge una tabella di funzioni dinamiche all'elenco di tabelle di funzioni dinamiche.</span><span class="sxs-lookup"><span data-stu-id="786d7-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="786d7-136">**RtlCaptureContext**</span><span class="sxs-lookup"><span data-stu-id="786d7-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="786d7-137">Recupera un record di contesto nel contesto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="786d7-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="786d7-138">**RtlDeleteFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="786d7-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="786d7-139">Rimuove una tabella di funzioni dinamiche dall'elenco tabella di funzioni dinamiche.</span><span class="sxs-lookup"><span data-stu-id="786d7-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="786d7-140">**RtlInstallFunctionTableCallback**</span><span class="sxs-lookup"><span data-stu-id="786d7-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="786d7-141">Aggiunge una tabella di funzioni dinamiche all'elenco di tabelle di funzioni dinamiche.</span><span class="sxs-lookup"><span data-stu-id="786d7-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="786d7-142">**RtlRestoreContext**</span><span class="sxs-lookup"><span data-stu-id="786d7-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="786d7-143">Ripristina il contesto del chiamante nel record di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="786d7-143">Restores the context of the caller to the specified context record.</span></span>

 

 
