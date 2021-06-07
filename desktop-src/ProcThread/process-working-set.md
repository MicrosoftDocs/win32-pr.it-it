---
description: Il working set di un programma è una raccolta di tali pagine nello spazio indirizzi virtuale a cui è stato fatto riferimento di recente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Elabora working set
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549903"
---
# <a name="process-working-set"></a>Elabora working set

Il *working set* di un programma è una raccolta di tali pagine nello spazio indirizzi virtuale a cui è stato fatto riferimento di recente. Include dati condivisi e privati. I dati condivisi includono pagine che contengono tutte le istruzioni eseguite dall'applicazione, incluse quelle nelle DLL e nelle DLL di sistema. Con l'working set aumentano le dimensioni, aumenta la richiesta di memoria.

A un processo sono associate dimensioni minime working set e dimensioni working set massime. Ogni volta che si chiama [**CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)riserva le dimensioni minime working set per il processo. Il gestore della memoria virtuale tenta di mantenere una quantità di memoria sufficiente per il working set minimo quando il processo è attivo, ma non oltre le dimensioni massime.

Per ottenere le dimensioni minime e massime richieste del working set per l'applicazione, chiamare la [**funzione GetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)

Il sistema imposta le dimensioni working set predefinite. È anche possibile modificare le dimensioni working set usando la [**funzione SetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) L'impostazione di questi valori non garantisce che la memoria sia riservata o residente. Prestare attenzione a richiedere dimensioni minime o massime troppo grandi working set, perché questa operazione può compromettere le prestazioni del sistema.

Per ottenere la dimensione corrente o massima del working set per il processo, usare la [**funzione GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle prestazioni della memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Working Set](../memory/working-set.md)
</dt> </dl>

 

 
