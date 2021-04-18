---
description: I set di CPU forniscono le API per dichiarare l'affinità dell'applicazione in un modo "flessibile" compatibile con il risparmio energia del sistema operativo.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Set di CPU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801474591751f04a5bffe570d6b8caff4974203f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311993"
---
# <a name="cpu-sets"></a>Set di CPU

I set di CPU forniscono le API per dichiarare l'affinità dell'applicazione in un modo "flessibile" compatibile con il risparmio energia del sistema operativo. Inoltre, l'API offre alle applicazioni la possibilità di reaffinitize tutti i thread in background del processo a un subset di processori usando il meccanismo **predefinito di elaborazione** per evitare interferenze dai thread del sistema operativo all'interno del processo. Alcune versioni di Windows supportano i criteri di prenotazione di base, in cui un subset dei set di CPU del sistema può essere dedicato all'uso esclusivo di singole applicazioni e carichi di lavoro.

L'API set CPU funziona con ID set CPU, associati alle affinità del processore virtuale. Nella maggior parte dei sistemi e, nella maggior parte dei casi, ogni ID del set di CPU viene mappato direttamente a un singolo processore logico **Home** . Un thread creata un'affinità a un set di CPU specificato viene in genere eseguito su uno dei processori nell'elenco degli ID dei set di CPU selezionati.

I set di CPU riservati possono essere determinati controllando il flag **allocato** nelle informazioni sul \_ set di CPU del sistema \_ \_ . Il sistema controlla l'accesso ai set di CPU riservati ed è possibile eseguire query sull'assegnazione utilizzando il flag **AllocatedToTargetProcess** della \_ struttura delle informazioni del set di CPU di sistema \_ \_ . Se un processo tenta di utilizzare un'assegnazione di set di CPU allocata esclusivamente ad altri processi, la richiesta viene ignorata e i thread assegnati a set di CPU non consentiti vengono pianificati altrove. I set di CPU possono essere assegnati a due livelli. I set di CPU predefiniti del processo vengono assegnati a tutti i thread in un processo che non dispongono di un'assegnazione a livello di thread selezionato. Se per un thread o un processo è impostata una maschera di affinità restrittiva, la maschera di affinità viene rispettata sopra qualsiasi assegnazione del set di CPU in conflitto. Nei sistemi a più gruppi, le assegnazioni di CPU vengono ignorate se si trovano in gruppi che non corrispondono al gruppo nella maschera di affinità del thread. Se un thread viene assegnato a più set di CPU validi, verrà eseguito su uno dei processori corrispondenti in base alle relative priorità e alle priorità dei thread in conflitto su tali processori.

**Funzioni set CPU/enumerazioni/strutture**

-   [**GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md) (funzione)
-   [**GetSystemCpuSetInformation**](getsystemcpusetinformation.md) (funzione)
-   [**GetThreadSelectedCpuSets**](getthreadselectedcpusets.md) (funzione)
-   [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md) (funzione)
-   [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) (funzione)
-   [**CPU \_ IMPOSTA \_ enumerazione \_ tipo informazioni**](cpu-set-information-type.md)
-   [**Sistema \_ di Struttura \_ \_ delle informazioni sul set di CPU**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



