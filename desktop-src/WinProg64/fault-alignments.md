---
title: Errori di allineamento
description: Errori di allineamento
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- 'errori di allineamento: programmazione Windows a 64 bit'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300290"
---
# <a name="alignment-faults"></a><span data-ttu-id="d79e0-104">Errori di allineamento</span><span class="sxs-lookup"><span data-stu-id="d79e0-104">Alignment Faults</span></span>

<span data-ttu-id="d79e0-105">Il gestore degli errori di allineamento del sistema è disattivato per impostazione predefinita nei sistemi basati su Itanium.</span><span class="sxs-lookup"><span data-stu-id="d79e0-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="d79e0-106">Pertanto, qualsiasi accesso ai dati non allineato genera un'eccezione che non verrà corretta automaticamente dal sistema, a meno che l'applicazione non riprenda l'eccezione in un [gestore di eccezioni basato su frame](/windows/desktop/Debug/frame-based-exception-handling).</span><span class="sxs-lookup"><span data-stu-id="d79e0-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="d79e0-107">Per abilitare il gestore degli errori di allineamento del sistema, chiamare la funzione [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) con **sem \_ NOALIGNMENTFAULTEXCEPT**.</span><span class="sxs-lookup"><span data-stu-id="d79e0-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="d79e0-108">Si noti tuttavia che i processi possono comportare un peggioramento delle prestazioni se il gestore degli errori di allineamento del sistema è abilitato e il processo genera errori di allineamento.</span><span class="sxs-lookup"><span data-stu-id="d79e0-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="d79e0-109">Se il debugger WinDbg è stato installato come debugger di sistema, WinDbg verrà avviato automaticamente se un processo del sistema genera un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="d79e0-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="d79e0-110">Se non si dispone di un debugger installato come debugger del sistema, viene visualizzata una finestra di dialogo che informa che l'applicazione ha rilevato un errore e che è stata rilevata la possibilità di segnalare il problema a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d79e0-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="d79e0-111">Nei sistemi x64 e ARM64 tutti gli errori di allineamento vengono gestiti da una combinazione di hardware e software.</span><span class="sxs-lookup"><span data-stu-id="d79e0-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="d79e0-112">Per ottenere prestazioni ottimali, tutti gli accessi alla memoria devono essere allineati correttamente.</span><span class="sxs-lookup"><span data-stu-id="d79e0-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="d79e0-113">Inoltre, [l'accesso a variabili Interlocked](/windows/desktop/Sync/interlocked-variable-access) non allineate deve essere evitato su ARM64, poiché queste operazioni non sono atomiche.</span><span class="sxs-lookup"><span data-stu-id="d79e0-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 