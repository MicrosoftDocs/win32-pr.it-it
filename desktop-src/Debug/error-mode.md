---
description: La modalità di errore indica al sistema in che modo l'applicazione sta per rispondere a errori gravi.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modalità di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125715"
---
# <a name="error-mode"></a><span data-ttu-id="3e503-103">Modalità di errore</span><span class="sxs-lookup"><span data-stu-id="3e503-103">Error Mode</span></span>

<span data-ttu-id="3e503-104">La modalità di errore indica al sistema in che modo l'applicazione sta per rispondere a errori gravi.</span><span class="sxs-lookup"><span data-stu-id="3e503-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="3e503-105">Gli errori gravi includono errore del disco, errori dell'unità non pronta, allineamento dei dati e eccezioni non gestite.</span><span class="sxs-lookup"><span data-stu-id="3e503-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="3e503-106">Questa modalità di errore può essere gestita per singolo thread o per processo.</span><span class="sxs-lookup"><span data-stu-id="3e503-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="3e503-107">Un'applicazione può consentire al sistema di visualizzare una finestra di messaggio che informa l'utente che si è verificato un errore o che è in grado di gestire gli errori.</span><span class="sxs-lookup"><span data-stu-id="3e503-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="3e503-108">Per gestire questi errori senza l'intervento dell'utente, usare [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o il [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)specifico del thread.</span><span class="sxs-lookup"><span data-stu-id="3e503-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="3e503-109">Quando si chiama una di queste funzioni e si specificano i flag appropriati, nel sistema non vengono visualizzate le caselle di messaggio di errore corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="3e503-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="3e503-110">Un processo può recuperare la modalità di errore utilizzando [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) o [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span><span class="sxs-lookup"><span data-stu-id="3e503-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="3e503-111">È consigliabile che tutte le applicazioni chiamino la funzione [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) a livello di processo con un parametro di **sem \_ FAILCRITICALERRORS** all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3e503-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="3e503-112">Ciò consente di evitare che le finestre di dialogo in modalità di errore appendino l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e503-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="3e503-113">A parte questo, i chiamanti devono prediligere le versioni specifiche dei thread di queste funzioni perché sono meno problematiche rispetto al normale comportamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="3e503-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
