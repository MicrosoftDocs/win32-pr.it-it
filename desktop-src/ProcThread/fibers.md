---
description: Un fiber è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: Fiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756560"
---
# <a name="fibers"></a>Fiber

Un *Fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione. I fiber vengono eseguiti nel contesto dei thread che li pianificano. Ogni thread può pianificare più Fiber. In generale, i fiber non offrono vantaggi in un'applicazione multithreading progettata correttamente. Tuttavia, l'uso di fiber può semplificare la portabilità delle applicazioni progettate per pianificare i propri thread.

Dal punto di vista del sistema, una fibra presuppone l'identità del thread che lo esegue. Ad esempio, se un fiber accede all' [archiviazione locale di thread](thread-local-storage.md) (TLS), accede alla risorsa di archiviazione locale del thread che lo esegue. Inoltre, se un fiber chiama la funzione [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) , il thread che lo esegue viene chiuso. Tuttavia, a una fibra non sono associate tutte le stesse informazioni sullo stato associate a un thread. Le uniche informazioni sullo stato gestite per un fiber sono lo stack, un subset dei relativi registri e i dati Fiber forniti durante la creazione della Fiber. I registri salvati sono il set di registri generalmente mantenuti in una chiamata di funzione.

I fiber non vengono pianificati preventivamente. È possibile pianificare una fibra passando da un'altra Fiber. Il sistema pianifica ancora i thread per l'esecuzione. Quando un thread che esegue Fiber viene interrotto, la relativa fibra attualmente in esecuzione viene superata ma rimane selezionata. Il fiber selezionato viene eseguito quando viene eseguito il thread.

Prima di pianificare la prima fibra, chiamare la funzione [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) per creare un'area in cui salvare le informazioni sullo stato della Fiber. Il thread chiamante è ora il fiber attualmente in esecuzione. Le informazioni sullo stato archiviato per questa fiber includono i dati Fiber passati come argomento a **ConvertThreadToFiber**.

La funzione [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) viene usata per creare un nuovo fiber da una fibra esistente. la chiamata richiede le dimensioni dello stack, l'indirizzo iniziale e i dati Fiber. L'indirizzo iniziale è in genere una funzione fornita dall'utente, denominata funzione Fiber, che accetta un parametro (i dati Fiber) e non restituisce alcun valore. Se la funzione Fiber restituisce, il thread che esegue il fiber viene chiuso. Per eseguire qualsiasi Fiber creata con **CreateFiber**, chiamare la funzione [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) . È possibile chiamare **SwitchToFiber** con l'indirizzo di una fibra creata da un thread diverso. A tale scopo, è necessario che l'indirizzo venga restituito all'altro thread quando si chiama **CreateFiber** ed è necessario usare la sincronizzazione corretta.

Un fiber può recuperare i dati Fiber chiamando la macro [**GetFiberData**](/windows/win32/api/winnt/nf-winnt-getfiberdata) . Un fiber può recuperare l'indirizzo Fiber in qualsiasi momento chiamando la macro [**GetCurrentFiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) .

## <a name="fiber-local-storage"></a>Archiviazione locale Fiber

Un fiber può usare l' *archiviazione locale di Fiber* (FLS) per creare una copia univoca di una variabile per ogni Fiber. Se non si verifica alcun cambio di fibra, FLS funziona esattamente come l' [archiviazione thread-local](thread-local-storage.md). Le funzioni FLS ([**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc), [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree), [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)e [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) modificano il FLS associato al thread corrente. Se il thread sta eseguendo una fibra e la fibra è cambiata, viene anche scambiata la FLS.

Per pulire i dati associati a un fiber, chiamare la funzione [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) . Questi dati includono lo stack, un subset dei registri e i dati Fiber. Se il fiber attualmente in esecuzione chiama **DeleteFiber**, il thread chiama [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) e termina. Tuttavia, se il fiber selezionato di un thread viene eliminato da una fibra in esecuzione in un altro thread, è probabile che il thread con la fibra eliminata venga interrotto in modo anomalo perché lo stack Fiber è stato liberato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Fiber](using-fibers.md)
</dt> </dl>

 

 
