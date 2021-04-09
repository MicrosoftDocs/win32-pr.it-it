---
description: Quando si descrive il debug, vengono utilizzati i termini seguenti.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologia di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965889"
---
# <a name="debugging-terminology"></a><span data-ttu-id="782d3-103">Terminologia di debug</span><span class="sxs-lookup"><span data-stu-id="782d3-103">Debugging Terminology</span></span>

<span data-ttu-id="782d3-104">Quando si descrive il debug, vengono utilizzati i termini seguenti.</span><span class="sxs-lookup"><span data-stu-id="782d3-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="782d3-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Schermata blu</span><span class="sxs-lookup"><span data-stu-id="782d3-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="782d3-106">Quando il sistema rileva un problema hardware, un'incoerenza dei dati o un errore simile, può visualizzare una schermata blu contenente informazioni che possono essere utilizzate per determinare la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="782d3-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="782d3-107">Queste informazioni includono il codice di arresto e se è stato creato un file di dump di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="782d3-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="782d3-108">Può inoltre includere un elenco di driver caricati e una traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="782d3-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>File di dump di arresto anomalo</span><span class="sxs-lookup"><span data-stu-id="782d3-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="782d3-110">È possibile configurare il sistema per la scrittura di informazioni in un file di dump di arresto anomalo sul disco rigido ogni volta che viene generato un codice di arresto.</span><span class="sxs-lookup"><span data-stu-id="782d3-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="782d3-111">Il file contiene informazioni che il debugger può utilizzare per analizzare l'errore.</span><span class="sxs-lookup"><span data-stu-id="782d3-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="782d3-112">Questo file può essere molto grande della memoria fisica contenuta nel computer.</span><span class="sxs-lookup"><span data-stu-id="782d3-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span><span class="sxs-lookup"><span data-stu-id="782d3-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="782d3-114">Programma progettato per consentire di rilevare, individuare e correggere gli errori in un altro programma.</span><span class="sxs-lookup"><span data-stu-id="782d3-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="782d3-115">Consente allo sviluppatore di scorrere l'esecuzione del processo e dei relativi thread, monitorando la memoria, le variabili e altri elementi del contesto del processo e del thread.</span><span class="sxs-lookup"><span data-stu-id="782d3-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modalità kernel</span><span class="sxs-lookup"><span data-stu-id="782d3-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="782d3-117">Modalità del processore in cui vengono eseguiti i servizi di sistema e i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="782d3-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="782d3-118">Tutte le interfacce e le istruzioni della CPU sono disponibili e tutta la memoria è accessibile.</span><span class="sxs-lookup"><span data-stu-id="782d3-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>File minidump</span><span class="sxs-lookup"><span data-stu-id="782d3-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="782d3-120">Le applicazioni possono produrre file minidump in modalità utente che contengono un subset utile delle informazioni contenute in un file di dump di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="782d3-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="782d3-121">Per altre informazioni, vedere [file di minidump](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="782d3-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="782d3-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>INTERROMPi codice</span><span class="sxs-lookup"><span data-stu-id="782d3-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="782d3-123">Codice di errore che identifica l'errore che ha impedito al kernel di sistema di continuare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="782d3-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>File di simboli</span><span class="sxs-lookup"><span data-stu-id="782d3-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="782d3-125">Tutte le applicazioni di sistema, i driver e le dll sono compilati in modo tale che le informazioni di debug si trovino in file distinti noti come file di simboli.</span><span class="sxs-lookup"><span data-stu-id="782d3-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="782d3-126">Pertanto, il sistema è più piccolo e più veloce, ma è comunque possibile eseguirne il debug se i file di simboli sono installati.</span><span class="sxs-lookup"><span data-stu-id="782d3-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="782d3-127">Per ulteriori informazioni, vedere [file di simboli](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="782d3-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="782d3-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modalità utente</span><span class="sxs-lookup"><span data-stu-id="782d3-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="782d3-129">Modalità del processore in cui vengono eseguite le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="782d3-129">The processor mode in which applications run.</span></span> <span data-ttu-id="782d3-130">In questa modalità è disponibile un set limitato di interfacce e l'accesso ai dati di sistema è limitato.</span><span class="sxs-lookup"><span data-stu-id="782d3-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="782d3-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="782d3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="782d3-132">Configurazione del debug automatico</span><span class="sxs-lookup"><span data-stu-id="782d3-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



