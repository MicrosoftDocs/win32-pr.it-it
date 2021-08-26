---
description: "I computer con più processori sono in genere progettati per una delle due architetture: l'accesso alla memoria non uniforme (NUMA) o SMP (Symmetric MultiProcessing)."
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Processori multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28b381faaceb5a171ddcf33c0705fee144f98952c4d473c0db8c7d99050deb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032411"
---
# <a name="multiple-processors"></a>Processori multipli

I computer con più processori sono in genere progettati per una delle due architetture: l'accesso alla memoria non uniforme (NUMA) o SMP (Symmetric MultiProcessing).

In un computer NUMA, ogni processore è più vicino ad alcune parti della memoria rispetto ad altre, rendendo più veloce l'accesso alla memoria per alcune parti della memoria rispetto ad altre parti. Nel modello NUMA il sistema tenta di pianificare thread su processori vicini alla memoria usata. Per altre informazioni su NUMA, vedere [Supporto NUMA.](numa-support.md)

In un computer SMP due o più processori o core identici si connettono a una singola memoria principale condivisa. Nel modello SMP qualsiasi thread può essere assegnato a qualsiasi processore. Pertanto, la pianificazione dei thread in un computer SMP è simile alla pianificazione dei thread in un computer con un singolo processore. Tuttavia, l'utilità di pianificazione dispone di un pool di processori, in modo che possa pianificare l'esecuzione simultanea dei thread. La pianificazione è ancora determinata dalla priorità dei thread, ma può essere influenzata dall'impostazione dell'affinità dei thread e del processore ideale per i thread, come descritto in questo argomento.

## <a name="thread-affinity"></a>Affinità di thread

*L'affinità di* thread forza l'esecuzione di un thread in un subset specifico di processori. L'impostazione dell'affinità dei thread in genere deve essere evitata, perché può interferire con la capacità dell'utilità di pianificazione di pianificare i thread in modo efficace tra i processori. Ciò può ridurre i miglioramenti delle prestazioni generati dall'elaborazione parallela. Un uso appropriato dell'affinità di thread è il test di ogni processore.

Il sistema rappresenta l'affinità con una maschera di bit denominata maschera di affinità del processore. La maschera di affinità è la dimensione del numero massimo di processori nel sistema, con i bit impostati per identificare un subset di processori. Inizialmente, il sistema determina il subset di processori nella maschera.

È possibile ottenere l'affinità thread corrente per tutti i thread del processo chiamando la [**funzione GetProcessAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) Usare la [**funzione SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) per specificare l'affinità di thread per tutti i thread del processo. Per impostare l'affinità di thread per un singolo thread, usare la [**funzione SetThreadAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) L'affinità di thread deve essere un subset dell'affinità di processo.

Nei sistemi con più di 64 processori, la maschera di affinità rappresenta inizialmente i processori in un singolo gruppo di processori. Tuttavia, l'affinità di thread può essere impostata su un processore in un gruppo diverso, che modifica la maschera di affinità per il processo. Per altre informazioni, vedere [Gruppi di processori](processor-groups.md).

## <a name="thread-ideal-processor"></a>Processore ideale per thread

Quando si specifica un *processore ideale per i thread,* l'utilità di pianificazione esegue il thread nel processore specificato, quando possibile. Usare la [**funzione SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) per specificare un processore preferito per un thread. Ciò non garantisce che verrà scelto il processore ideale, ma fornisce un suggerimento utile all'utilità di pianificazione. Nei sistemi con più di 64 processori è possibile usare la [**funzione SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) per specificare un processore preferito in un gruppo di processori specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto NUMA](numa-support.md)
</dt> <dt>

[Gruppi di processori](processor-groups.md)
</dt> </dl>

 

 
