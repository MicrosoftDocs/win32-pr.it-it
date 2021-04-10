---
description: Il working set di un programma è una raccolta di tali pagine nello spazio degli indirizzi virtuali a cui è stato fatto riferimento di recente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Working set di processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231515"
---
# <a name="process-working-set"></a>Working set di processo

Il *working set* di un programma è una raccolta di tali pagine nello spazio degli indirizzi virtuali a cui è stato fatto riferimento di recente. Include sia i dati condivisi che quelli privati. I dati condivisi includono pagine che contengono tutte le istruzioni eseguite dall'applicazione, incluse quelle nelle DLL e nelle DLL di sistema. Man mano che aumentano le dimensioni del working set, aumenta la richiesta di memoria.

A un processo sono associate dimensioni minime working set e dimensioni massime working set. Ogni volta che si chiama [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), vengono riservate le dimensioni minime working set per il processo. Il gestore della memoria virtuale tenta di conservare memoria sufficiente per il working set residente minimo quando il processo è attivo, ma non supera la dimensione massima.

Per ottenere le dimensioni minime e massime richieste del working set per l'applicazione, chiamare la funzione [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .

Il sistema imposta le dimensioni working set predefinite. È anche possibile modificare le dimensioni working set usando la funzione [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) . L'impostazione di questi valori non garantisce che la memoria sarà riservata o residente. Prestare attenzione alla richiesta di dimensioni minime o massime di working set, perché questa operazione può influire negativamente sulle prestazioni del sistema.

Per ottenere le dimensioni correnti o massime del working set per il processo, usare la funzione [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle prestazioni della memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Working Set](../memory/working-set.md)
</dt> </dl>

 

 
