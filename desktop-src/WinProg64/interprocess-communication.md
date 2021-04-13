---
title: Comunicazione interprocesso
description: Le tecniche seguenti possono essere utilizzate per la comunicazione tra applicazioni a 32 bit e a 64 bit.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- comunicazione interprocesso-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399411"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="f0714-104">Comunicazione interprocesso tra applicazioni a 32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="f0714-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="f0714-105">Per la comunicazione tra applicazioni a 32 bit e a 64 bit, è possibile usare le tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0714-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="f0714-106">le versioni a 64 bit di Windows usano handle a 32 bit per l'interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="f0714-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="f0714-107">Quando si condivide un handle tra applicazioni a 32 bit e a 64 bit, solo i 32 bit inferiori sono significativi, quindi è possibile troncare il punto di controllo (quando lo si passa da 64 bit a 32 bit) o estendere la firma dell'handle (quando viene passato da 32 a 64 bit).</span><span class="sxs-lookup"><span data-stu-id="f0714-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="f0714-108">Gli handle che possono essere condivisi includono handle per oggetti utente quali Windows (**HWND**), handle per oggetti GDI quali penne e pennelli (**HBRUSH** e **HPEN**) e handle a oggetti denominati, quali mutex, semafori e handle di file.</span><span class="sxs-lookup"><span data-stu-id="f0714-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="f0714-109">È possibile utilizzare le chiamate di procedura remota (RPC).</span><span class="sxs-lookup"><span data-stu-id="f0714-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="f0714-110">LocalServers COM può essere usato se le DLL di proxy/stub a 32 bit e 64 sono registrate per tutte le interfacce usate.</span><span class="sxs-lookup"><span data-stu-id="f0714-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="f0714-111">È possibile usare la memoria condivisa se i tipi dipendenti dal puntatore vengono convertiti correttamente (o evitati).</span><span class="sxs-lookup"><span data-stu-id="f0714-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="f0714-112">Le funzioni [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) possono avviare processi a 32 bit e a 64 bit da processi a 32 bit o a 64 bit con determinate limitazioni.</span><span class="sxs-lookup"><span data-stu-id="f0714-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="f0714-113">Impossibile avviare un file eseguibile a 64 bit in% windir% \\ system32 da un processo a 32 bit, perché il redirector file System reindirizza il percorso.</span><span class="sxs-lookup"><span data-stu-id="f0714-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="f0714-114">Non disabilitare il reindirizzamento per eseguire questa operazione. utilizzare% windir% \\ SysNative in alternativa.</span><span class="sxs-lookup"><span data-stu-id="f0714-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="f0714-115">Per ulteriori informazioni, vedere [redirector del file System](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="f0714-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 