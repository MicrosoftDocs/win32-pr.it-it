---
description: Un'eccezione è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Gestione strutturata delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877318"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="153bb-103">Gestione strutturata delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="153bb-103">Structured Exception Handling</span></span>

<span data-ttu-id="153bb-104">Un' *eccezione* è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo.</span><span class="sxs-lookup"><span data-stu-id="153bb-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="153bb-105">Esistono due tipi di eccezioni: eccezioni hardware ed eccezioni software.</span><span class="sxs-lookup"><span data-stu-id="153bb-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="153bb-106">Le *eccezioni hardware* vengono avviate dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="153bb-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="153bb-107">Possono derivare dall'esecuzione di determinate sequenze di istruzioni, ad esempio la divisione per zero o un tentativo di accedere a un indirizzo di memoria non valido.</span><span class="sxs-lookup"><span data-stu-id="153bb-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="153bb-108">Le *eccezioni software* vengono avviate in modo esplicito dalle applicazioni o dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="153bb-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="153bb-109">Ad esempio, il sistema è in grado di rilevare quando viene specificato un valore di parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="153bb-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="153bb-110">La *gestione strutturata delle eccezioni* è un meccanismo per gestire le eccezioni hardware e software.</span><span class="sxs-lookup"><span data-stu-id="153bb-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="153bb-111">Il codice gestirà pertanto le eccezioni hardware e software in modo identico.</span><span class="sxs-lookup"><span data-stu-id="153bb-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="153bb-112">La gestione strutturata delle eccezioni consente di avere il controllo completo sulla gestione delle eccezioni, fornisce il supporto per i debugger ed è utilizzabile in tutti i linguaggi di programmazione e nei computer.</span><span class="sxs-lookup"><span data-stu-id="153bb-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="153bb-113">La *gestione delle eccezioni con vettori* è un'estensione della gestione strutturata delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="153bb-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="153bb-114">Il sistema supporta anche la *gestione della terminazione*, che consente di garantire che ogni volta che viene eseguito un corpo sorvegliato del codice venga eseguito anche un blocco di codice di terminazione specificato.</span><span class="sxs-lookup"><span data-stu-id="153bb-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="153bb-115">Il codice di terminazione viene eseguito indipendentemente dal modo in cui il flusso di controllo lascia il corpo sorvegliato.</span><span class="sxs-lookup"><span data-stu-id="153bb-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="153bb-116">Un gestore di terminazione può ad esempio garantire che le attività di pulizia vengano eseguite anche se si verifica un'eccezione o un altro errore durante l'esecuzione del corpo sorvegliato del codice.</span><span class="sxs-lookup"><span data-stu-id="153bb-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="153bb-117">Informazioni sulla gestione delle eccezioni strutturata</span><span class="sxs-lookup"><span data-stu-id="153bb-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="153bb-118">Uso della gestione strutturata delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="153bb-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="153bb-119">Guida di riferimento alla gestione delle eccezioni strutturata</span><span class="sxs-lookup"><span data-stu-id="153bb-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



