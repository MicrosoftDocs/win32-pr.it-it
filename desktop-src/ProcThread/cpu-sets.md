---
description: I set di CPU forniscono LE API per dichiarare l'affinità dell'applicazione in modo "soft" compatibile con il risparmio energia del sistema operativo.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Set di CPU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 092559fbf5646a0938696c953f4136f1fe1a9567e56e02a04c6c36510d03d729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143124"
---
# <a name="cpu-sets"></a>Set di CPU

I set di CPU forniscono LE API per dichiarare l'affinità dell'applicazione in modo "soft" compatibile con il risparmio energia del sistema operativo. Inoltre, l'API offre alle applicazioni la possibilità di riaffiziare tutti i thread  in background nel processo a un subset di processori usando il meccanismo predefinito del processo per evitare interferenze dai thread del sistema operativo all'interno del processo. Alcune versioni di Windows supportano i criteri di prenotazione core, in cui un subset dei set di CPU del sistema può essere dedicato all'uso esclusivo di singole applicazioni e carichi di lavoro.

L'API del set di CPU funziona con gli ID dei set di CPU, associati alle affinità del processore virtuale. Nella maggior parte dei sistemi e nella maggior parte delle condizioni, ogni ID del set di CPU verrà mappato direttamente a un singolo **processore logico home.** Un thread con affinità a un determinato set di CPU viene in genere eseguito in uno dei processori nell'elenco degli ID dei set di CPU selezionati.

I set di CPU riservati possono essere determinati esaminando il flag **Allocato** in SYSTEM \_ CPU SET \_ \_ INFORMATION. Il sistema controlla l'accesso ai set di CPU riservati e l'assegnazione può essere eseguita tramite il flag **AllocatedToTargetProcess** della struttura SYSTEM \_ CPU SET \_ \_ INFORMATION. Se un processo tenta di usare un'assegnazione del set di CPU allocata esclusivamente ad altri processi, la richiesta viene ignorata e i thread assegnati ai set di CPU non consentiti vengono pianificati altrove. I set di CPU possono essere assegnati a due livelli. I set di CPU predefiniti del processo vengono assegnati a tutti i thread di un processo che non dispongono di un'assegnazione al livello Thread selezionato. Se per un thread o un processo è impostata una maschera di affinità restrittiva, la maschera di affinità viene rispettata al di sopra di qualsiasi assegnazione di set di CPU in conflitto. Nei sistemi a più gruppi, le assegnazioni di CPU vengono ignorate se si trova in gruppi che non corrispondono al gruppo nella maschera di affinità del thread. Se un thread viene assegnato a più set di CPU validi, verrà eseguito in uno dei processori corrispondenti in base alle priorità e alle priorità dei thread concorrenti su tali processori.

**Funzioni/enumerazioni/strutture dei set di CPU**

-   [**Funzione GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md)
-   [**Funzione GetSystemCpuSetInformation**](getsystemcpusetinformation.md)
-   [**Funzione GetThreadSelectedCpuSets**](getthreadselectedcpusets.md)
-   [**Funzione SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)
-   [**Funzione SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)
-   [**CPU \_ Enumerazione SET \_ INFORMATION \_ TYPE**](cpu-set-information-type.md)
-   [**SYSTEM \_ Struttura \_ DELLE INFORMAZIONI SUI SET \_ DI CPU**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



