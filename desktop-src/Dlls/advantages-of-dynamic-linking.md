---
description: Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vantaggi del collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313386"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="8a755-103">Vantaggi del collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="8a755-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="8a755-104">Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico:</span><span class="sxs-lookup"><span data-stu-id="8a755-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="8a755-105">Più processi che caricano la stessa DLL nello stesso indirizzo di base condividono una singola copia della DLL nella memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="8a755-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="8a755-106">Questa operazione consente di risparmiare memoria di sistema e di ridurre lo scambio.</span><span class="sxs-lookup"><span data-stu-id="8a755-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="8a755-107">Quando le funzioni in una DLL cambiano, non è necessario ricompilare o ricollegare le applicazioni che le utilizzano finché gli argomenti della funzione, le convenzioni di chiamata e i valori restituiti non cambiano.</span><span class="sxs-lookup"><span data-stu-id="8a755-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="8a755-108">Al contrario, il codice oggetto collegato staticamente richiede che l'applicazione venga ricollegata quando le funzioni cambiano.</span><span class="sxs-lookup"><span data-stu-id="8a755-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="8a755-109">Una DLL può fornire supporto After-Market.</span><span class="sxs-lookup"><span data-stu-id="8a755-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="8a755-110">Ad esempio, è possibile modificare una DLL del driver di visualizzazione per supportare una visualizzazione che non era disponibile quando l'applicazione è stata inizialmente spedita.</span><span class="sxs-lookup"><span data-stu-id="8a755-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="8a755-111">I programmi scritti in linguaggi di programmazione diversi possono chiamare la stessa funzione DLL purché i programmi seguano la stessa convenzione di chiamata utilizzata dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="8a755-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="8a755-112">La convenzione di chiamata, ad esempio C, Pascal o chiamata standard, controlla l'ordine in cui la funzione chiamante deve effettuare il push degli argomenti nello stack, se la funzione o la funzione chiamante è responsabile della pulizia dello stack e se gli argomenti vengono passati nei registri.</span><span class="sxs-lookup"><span data-stu-id="8a755-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="8a755-113">Per ulteriori informazioni, vedere la documentazione inclusa con il compilatore.</span><span class="sxs-lookup"><span data-stu-id="8a755-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="8a755-114">Un potenziale svantaggio nell'uso delle dll è che l'applicazione non è indipendente. dipende dall'esistenza di un modulo DLL separato.</span><span class="sxs-lookup"><span data-stu-id="8a755-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="8a755-115">Il sistema termina i processi utilizzando il collegamento dinamico in fase di caricamento se richiedono una DLL non trovata all'avvio del processo e genera un messaggio di errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="8a755-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="8a755-116">Il sistema non termina un processo utilizzando il collegamento dinamico in fase di esecuzione in questa situazione, ma le funzioni esportate dalla DLL mancante non sono disponibili per il programma.</span><span class="sxs-lookup"><span data-stu-id="8a755-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



