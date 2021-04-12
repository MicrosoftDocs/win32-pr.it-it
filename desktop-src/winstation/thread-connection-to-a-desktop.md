---
title: Connessione thread a un desktop
description: Quando un processo si connette a una stazione di finestra, il sistema assegna un desktop al thread che effettua la connessione.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223921"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="ea666-103">Connessione thread a un desktop</span><span class="sxs-lookup"><span data-stu-id="ea666-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="ea666-104">Quando un processo si connette a una stazione di finestra, il sistema assegna un desktop al thread che effettua la connessione.</span><span class="sxs-lookup"><span data-stu-id="ea666-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="ea666-105">Il sistema determina il desktop da assegnare al thread in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea666-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="ea666-106">Se il thread ha chiamato la funzione [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , si connette al desktop specificato.</span><span class="sxs-lookup"><span data-stu-id="ea666-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="ea666-107">Se il thread non ha chiamato [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), si connette al desktop ereditato dal processo padre.</span><span class="sxs-lookup"><span data-stu-id="ea666-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="ea666-108">Se il thread non ha chiamato [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) e non ha ereditato un desktop, il sistema tenta di aprire per l' \_ accesso massimo consentito e si connette a un desktop come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ea666-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="ea666-109">Se è stato specificato un nome desktop nel membro **lpDesktop** della struttura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) utilizzata al momento della creazione del processo, il thread si connette al desktop specificato.</span><span class="sxs-lookup"><span data-stu-id="ea666-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="ea666-110">In caso contrario, il thread si connette al desktop predefinito della stazione della finestra a cui è connesso il processo.</span><span class="sxs-lookup"><span data-stu-id="ea666-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="ea666-111">Il desktop assegnato durante questo processo di connessione non può essere chiuso chiamando la funzione [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .</span><span class="sxs-lookup"><span data-stu-id="ea666-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="ea666-112">Quando un processo si connette a un desktop, il sistema esegue una ricerca nella tabella di handle del processo per gli handle ereditati.</span><span class="sxs-lookup"><span data-stu-id="ea666-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="ea666-113">Il sistema utilizza il primo handle desktop rilevato.</span><span class="sxs-lookup"><span data-stu-id="ea666-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="ea666-114">Se si desidera che un processo figlio si connetta a un particolare desktop ereditato, è necessario assicurarsi che l'unico handle desiderato sia contrassegnato come ereditabile.</span><span class="sxs-lookup"><span data-stu-id="ea666-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="ea666-115">Se un processo figlio eredita più handle desktop, i risultati della connessione desktop non saranno definiti.</span><span class="sxs-lookup"><span data-stu-id="ea666-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="ea666-116">Gli handle a un desktop aperto dal sistema durante la connessione di un processo a un desktop non sono ereditabili.</span><span class="sxs-lookup"><span data-stu-id="ea666-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea666-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea666-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea666-118">Elaborare la connessione a una stazione di finestra</span><span class="sxs-lookup"><span data-stu-id="ea666-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 