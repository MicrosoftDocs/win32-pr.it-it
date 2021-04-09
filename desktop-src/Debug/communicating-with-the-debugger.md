---
description: La funzione OutputDebugString invia una stringa dal processo sottoposto a debug al debugger generando un evento di debug degli eventi di stringa di debug di OUTPUT \_ \_ \_ . Un processo può rilevare se è in fase di debug chiamando la funzione IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicazione con il debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877177"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="2c62c-104">Comunicazione con il debugger</span><span class="sxs-lookup"><span data-stu-id="2c62c-104">Communicating with the Debugger</span></span>

<span data-ttu-id="2c62c-105">La funzione [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) invia una stringa dal processo sottoposto a debug al debugger generando un evento di debug degli eventi di stringa di debug di output \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c62c-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="2c62c-106">Un processo può rilevare se è in fase di debug chiamando la funzione [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="2c62c-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="2c62c-107">La funzione [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) causa un'eccezione del punto di interruzione nel processo corrente.</span><span class="sxs-lookup"><span data-stu-id="2c62c-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="2c62c-108">Un punto di interruzione è un percorso in un programma in cui l'esecuzione viene arrestata per consentire allo sviluppatore di esaminare il codice, le variabili e i valori di registrazione del programma e, in base alle esigenze, di apportare modifiche, continuare l'esecuzione o terminare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2c62c-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="2c62c-109">La funzione [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) termina il processo corrente e fornisce il controllo di esecuzione al debugger, ma a differenza di [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), non genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="2c62c-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="2c62c-110">Questa funzione deve essere usata solo come ultima risorsa, perché non sempre libera la memoria del processo o chiude i relativi file.</span><span class="sxs-lookup"><span data-stu-id="2c62c-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 
