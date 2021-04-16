---
description: Sono disponibili diverse funzioni per ottenere informazioni sui processi.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Recupero di informazioni aggiuntive sul processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529089"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="dc883-103">Recupero di informazioni aggiuntive sul processo</span><span class="sxs-lookup"><span data-stu-id="dc883-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="dc883-104">Sono disponibili diverse funzioni per ottenere informazioni sui processi.</span><span class="sxs-lookup"><span data-stu-id="dc883-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="dc883-105">Alcune di queste funzioni possono essere usate solo per il processo chiamante, perché non accettano un handle di processo come parametro.</span><span class="sxs-lookup"><span data-stu-id="dc883-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="dc883-106">È possibile utilizzare funzioni che accettano un handle di processo per ottenere informazioni su altri processi.</span><span class="sxs-lookup"><span data-stu-id="dc883-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="dc883-107">Per ottenere la stringa della riga di comando per il processo corrente, usare la funzione [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="dc883-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="dc883-108">Per recuperare la struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) specificata al momento della creazione del processo corrente, utilizzare la funzione [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .</span><span class="sxs-lookup"><span data-stu-id="dc883-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="dc883-109">Per ottenere le informazioni sulla versione dall'intestazione eseguibile, usare la funzione [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .</span><span class="sxs-lookup"><span data-stu-id="dc883-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="dc883-110">Per ottenere il percorso completo e il nome file per il file eseguibile che contiene il codice del processo, usare la funzione [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="dc883-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="dc883-111">Per ottenere il numero di handle per gli oggetti dell'interfaccia utente grafica (GUI) in uso, usare la funzione [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .</span><span class="sxs-lookup"><span data-stu-id="dc883-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="dc883-112">Per determinare se è in corso il debug di un processo, usare la funzione [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="dc883-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="dc883-113">Per recuperare le informazioni di contabilità per tutte le operazioni di I/O eseguite dal processo, usare la funzione [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="dc883-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
