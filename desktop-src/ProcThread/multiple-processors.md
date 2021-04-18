---
description: 'I computer con più processori sono in genere progettati per una delle due architetture seguenti: NUMA (non-Uniform Memory Access) o SMP (symmetric multiprocessing).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Processori multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311984"
---
# <a name="multiple-processors"></a>Processori multipli

I computer con più processori sono in genere progettati per una delle due architetture seguenti: NUMA (non-Uniform Memory Access) o SMP (symmetric multiprocessing).

In un computer NUMA, ogni processore è più vicino ad alcune parti della memoria rispetto ad altri, rendendo più veloce l'accesso alla memoria per alcune parti della memoria rispetto ad altre parti. Nel modello NUMA, il sistema tenta di pianificare i thread sui processori vicini alla memoria utilizzata. Per ulteriori informazioni su NUMA, vedere [supporto NUMA](numa-support.md).

In un computer SMP, due o più processori o Core identici si connettono a una singola memoria principale condivisa. Nel modello SMP è possibile assegnare qualsiasi thread a qualsiasi processore. Pertanto, la pianificazione dei thread in un computer SMP è simile alla pianificazione dei thread in un computer con un singolo processore. Tuttavia, l'utilità di pianificazione dispone di un pool di processori, in modo che sia in grado di pianificare l'esecuzione simultanea dei thread. La pianificazione è ancora determinata dalla priorità dei thread, ma può essere influenzata dall'impostazione dell'affinità dei thread e del processore ideale del thread, come descritto in questo argomento.

## <a name="thread-affinity"></a>Affinità di thread

L' *affinità dei thread* impone l'esecuzione di un thread su un subset specifico di processori. È in genere consigliabile evitare di impostare l'affinità di thread, perché può interferire con la capacità dell'utilità di pianificazione di pianificare i thread in modo efficiente tra i processori. Questo può ridurre il miglioramento delle prestazioni prodotto dall'elaborazione parallela. Un uso appropriato dell'affinità di thread sta testando ogni processore.

Il sistema rappresenta l'affinità con una maschera di stato chiamata maschera di affinità del processore. La maschera di affinità è la dimensione del numero massimo di processori nel sistema, con bit impostati per identificare un subset di processori. Inizialmente, il sistema determina il subset di processori nella maschera.

È possibile ottenere l'affinità di thread corrente per tutti i thread del processo chiamando la funzione [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Utilizzare la funzione [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) per specificare l'affinità di thread per tutti i thread del processo. Per impostare l'affinità di thread per un singolo thread, usare la funzione [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) . L'affinità di thread deve essere un subset dell'affinità del processo.

Nei sistemi con più di 64 processori, affinity mask rappresenta inizialmente i processori in un singolo gruppo di processori. Tuttavia, l'affinità di thread può essere impostata su un processore in un gruppo diverso, che modifica la maschera di affinità per il processo. Per ulteriori informazioni, vedere [gruppi di processori](processor-groups.md).

## <a name="thread-ideal-processor"></a>Processore ideale per thread

Quando si specifica un *processore ideale* per i thread, l'utilità di pianificazione esegue il thread sul processore specificato, quando possibile. Utilizzare la funzione [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) per specificare un processore preferito per un thread. Ciò non garantisce che venga scelto il processore ideale, ma fornisce un suggerimento utile all'utilità di pianificazione. Nei sistemi con più di 64 processori, è possibile usare la funzione [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) per specificare un processore preferito in un gruppo di processori specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto NUMA](numa-support.md)
</dt> <dt>

[Gruppi di processori](processor-groups.md)
</dt> </dl>

 

 
