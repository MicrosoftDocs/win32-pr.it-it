---
title: Pam Version-Independent i nomi e la destinazione di versioni specifiche di Windows
description: In molti casi, l'API Windows Filtering Platform (WFP) fornisce più di una versione di una funzione o di una struttura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297789"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="faa22-103">Pam Version-Independent i nomi e la destinazione di versioni specifiche di Windows</span><span class="sxs-lookup"><span data-stu-id="faa22-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="faa22-104">In molti casi, l'API Windows Filtering Platform (WFP) fornisce più di una versione di una funzione o di una struttura.</span><span class="sxs-lookup"><span data-stu-id="faa22-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="faa22-105">La maggior parte dei nomi di dati e funzioni nell'API PAM termina con un numero di versione, ad esempio "0" o "1", anche se è presente una sola versione.</span><span class="sxs-lookup"><span data-stu-id="faa22-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="faa22-106">Mapping della versione in fwpvi. h</span><span class="sxs-lookup"><span data-stu-id="faa22-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="faa22-107">Il file di intestazione fwpvi. h è incluso a partire da Windows 7 SDK e WDK.</span><span class="sxs-lookup"><span data-stu-id="faa22-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="faa22-108">Questo file di intestazione esegue il mapping del nome API senza versione alla versione appropriata per l'uso con un sistema operativo specifico.</span><span class="sxs-lookup"><span data-stu-id="faa22-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="faa22-109">Ecco, ad esempio, un breve estratto dalla versione di fwpvi. h inclusa in Windows 8 SDK.</span><span class="sxs-lookup"><span data-stu-id="faa22-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="faa22-110">Come illustrato in precedenza, esiste una sola versione di **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) , pertanto qualsiasi chiamata a **FwpmNetEventCreateEnumHandle** chiamerà sempre **FwpmNetEventCreateEnumHandle0**, indipendentemente dal sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="faa22-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="faa22-111">Tuttavia, sono disponibili tre versioni di **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)e [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span><span class="sxs-lookup"><span data-stu-id="faa22-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="faa22-112">Il file di intestazione fwpvi. h garantisce che una chiamata a **FwpmNetEventEnum** chiamerà la versione più appropriata per il sistema operativo di destinazione:</span><span class="sxs-lookup"><span data-stu-id="faa22-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="faa22-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) per Windows 8 (o versioni successive)</span><span class="sxs-lookup"><span data-stu-id="faa22-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="faa22-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) per Windows 7 è destinato</span><span class="sxs-lookup"><span data-stu-id="faa22-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="faa22-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) per sistemi operativi precedenti, ad esempio Windows Vista o Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="faa22-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="faa22-116">Chiamata di funzioni e strutture Version-Independent</span><span class="sxs-lookup"><span data-stu-id="faa22-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="faa22-117">Gli sviluppatori WFP destinati a un particolare sistema operativo o a una versione WDK sono invitati a programmare sempre in base alle macro indipendenti dalla versione.</span><span class="sxs-lookup"><span data-stu-id="faa22-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="faa22-118">Verrà selezionata automaticamente la versione più recente supportata nel sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="faa22-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="faa22-119">È consigliabile usare i file di intestazione più recenti, anche quando la destinazione è un sistema operativo precedente.</span><span class="sxs-lookup"><span data-stu-id="faa22-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="faa22-120">In questo modo si garantisce che venga usata la versione supportata più recente e che sia possibile semplificare la manutenzione e l'aggiornamento del codice.</span><span class="sxs-lookup"><span data-stu-id="faa22-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="faa22-121">La [documentazione di riferimento dell'API WFP](fwp-reference.md) descrive ogni versione di un'API numerata.</span><span class="sxs-lookup"><span data-stu-id="faa22-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="faa22-122">Se esiste più di una versione, viene indicato il sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="faa22-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="faa22-123">Tuttavia, gli sviluppatori in genere vogliono chiamare le API indipendenti dalla versione (numerate) e indicare il sistema operativo di destinazione (ad esempio **NTDDI \_ WIN6** per Windows Vista o **NTDDI \_ Win8** per Windows 8).</span><span class="sxs-lookup"><span data-stu-id="faa22-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="faa22-124">Per garantire la corretta gestione delle funzioni che accettano parametri diversi in versioni diverse, è possibile includere blocchi condizionali, ad esempio `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="faa22-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




