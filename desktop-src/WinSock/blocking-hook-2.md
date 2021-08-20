---
description: Sebbene questo meccanismo sia sufficiente per applicazioni semplici, non può supportare i complessi requisiti di invio dei messaggi di applicazioni più avanzate, ad esempio quelle che usano il modello MDI (Multiple Document Interface).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Hook di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df8138db7d40f6333ff53a635927e10307fef222d8dbfd1126a2f9ba6e7cd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112619"
---
# <a name="blocking-hook"></a>Hook di blocco

Sebbene questo meccanismo sia sufficiente per applicazioni semplici, non può supportare i complessi requisiti di invio dei messaggi di applicazioni più avanzate, ad esempio quelle che usano il modello MDI (Multiple Document Interface). Per tali applicazioni, un hook di blocco specifico del thread può essere installato dall'applicazione. Verrà chiamato dal provider di servizi anziché dall'hook di blocco predefinito descritto in precedenza. Un provider di servizi deve recuperare un puntatore all'hook di blocco per thread dal32.dll WS2 \_ chiamando [**WPUQueryBlockingCallback.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) Se l'applicazione non ha installato il proprio hook di blocco, verrà restituito un puntatore alla funzione hook di blocco predefinita.

Un provider Windows Sockets non può presupporre che un hook di blocco fornito dall'applicazione consenta di continuare l'elaborazione dei messaggi come l'hook di blocco predefinito. Alcune applicazioni non possono tollerare la possibilità di reentranti messaggi mentre un'operazione di blocco è in sospeso. La funzione hook di blocco di un'applicazione di questo tipo restituirebbe **semplicemente FALSE.** Se un provider di servizi dipende dai messaggi per l'operazione interna, può eseguire **PeekMessage**(hMyWnd...) prima di eseguire l'hook di blocco dell'applicazione in modo che possa ottenere i propri messaggi senza influire sul resto del sistema.

Non esiste alcun hook di blocco predefinito installato nelle versioni multithreading preemptive di Windows. Ciò è dovuto al fatto che gli altri processi non verranno bloccati se una singola applicazione è in attesa del completamento di un'operazione e quindi non chiama **PeekMessage** o **GetMessage,** il che fa sì che l'applicazione ceda il processore in Windows. Quando il provider di servizi chiama [**WPUQueryBlockingCallback,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) viene restituito un puntatore Null che indica che il provider deve usare funzioni di blocco native del sistema operativo. Tuttavia, per mantenere la compatibilità con le versioni precedenti, un hook di blocco fornito dall'applicazione può comunque essere installato per ogni thread in Windows.

Il provider di servizi Winsock chiama l'hook di blocco solo se tutti gli elementi seguenti sono true: la routine è una routine definita come in grado di bloccare, il socket specificato è un socket di blocco e la richiesta non può essere completata immediatamente. Se vengono usati solo socket non di blocco e [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) anziché [**WSPSelect,**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) l'hook di blocco non verrà mai chiamato.

> [!Note]  
> Se durante il periodo in cui viene usato lo pseudoblocking per bloccare un thread, viene ricevuto un messaggio Windows per il thread, esiste il rischio che il thread tenti di eseguire un'altra chiamata Winsock. A causa della difficoltà di gestire questa condizione in modo sicuro, la specifica Windows Sockets 1.1 non consente questo comportamento. Non è consentito per un determinato thread effettuare più chiamate di funzione Winsock annidate. Per un thread specifico è consentita una sola chiamata di funzione in sospeso. Qualsiasi chiamata di funzione Winsock annidata ha esito negativo con l'errore WSAEINPROGRESS. È opportuno sottolineare che questa restrizione si applica sia alle operazioni di blocco che di non blocco, ma solo in Windows Sockets 1.1. Esistono alcune eccezioni a questa regola, incluse due funzioni che consentono a un'applicazione di determinare se è in corso un'operazione di pseudo-blocco e di annullare tale operazione, se necessario. Queste informazioni sono descritte di seguito.

 

 

 
