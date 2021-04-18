---
description: Sebbene questo meccanismo sia sufficiente per le applicazioni semplici, non può supportare i requisiti complessi per l'invio di messaggi di applicazioni più avanzate, ad esempio quelle che utilizzano il modello MDI (Multiple Document Interface).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Hook di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307042"
---
# <a name="blocking-hook"></a>Hook di blocco

Sebbene questo meccanismo sia sufficiente per le applicazioni semplici, non può supportare i requisiti complessi per l'invio di messaggi di applicazioni più avanzate, ad esempio quelle che utilizzano il modello MDI (Multiple Document Interface). Per tali applicazioni, l'applicazione può installare un hook di blocco specifico del thread. Questa operazione verrà chiamata dal provider di servizi anziché dall'hook di blocco predefinito descritto nell'oggetto precedente. Un provider di servizi deve recuperare un puntatore all'hook di blocco per thread dal32.dll WS2 chiamando \_ [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback). Se l'applicazione non ha installato il proprio hook di blocco, verrà restituito un puntatore alla funzione di hook di blocco predefinita.

Un provider di servizi Windows Sockets non può presupporre che un hook di blocco fornito dall'applicazione consenta la continuazione dell'elaborazione dei messaggi in quanto l'hook di blocco predefinito. Alcune applicazioni non possono tollerare la possibilità di messaggi rientranti mentre un'operazione di blocco è in attesa. Questa funzione hook di blocco di un'applicazione restituisce semplicemente **false**. Se un provider di servizi dipende dai messaggi per l'operazione interna, può eseguire **PeekMessage**(hMyWnd...) prima di eseguire l'hook di blocco dell'applicazione in modo che possa ottenere i propri messaggi senza influire sul resto del sistema.

Non è installato alcun hook di blocco predefinito nelle versioni di Windows preemptive con multithreading. Ciò è dovuto al fatto che altri processi non verranno bloccati se una singola applicazione è in attesa del completamento di un'operazione (e, di conseguenza, non chiama **PeekMessage** o **GetMessage** , che fa sì che l'applicazione restituisca il processore in finestre non preemptive). Quando il provider di servizi chiama [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) , viene restituito un puntatore null che indica che il provider deve usare funzioni native di blocco del sistema operativo. Tuttavia, per mantenere la compatibilità con le versioni precedenti, è comunque possibile installare un hook di blocco fornito dall'applicazione per thread in Windows.

Il provider di servizi Winsock chiama l'hook di blocco solo se si verificano tutte le condizioni seguenti: la routine è una che è definita come in grado di bloccarsi, il socket specificato è un socket di blocco e la richiesta non può essere completata immediatamente. Se vengono usati solo socket non di blocco e [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) anziché [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) , l'hook di blocco non verrà mai chiamato.

> [!Note]  
> Se, durante il periodo in cui viene usato pseudoblocking per bloccare un thread, viene ricevuto un messaggio di Windows per il thread, esiste il rischio che il thread tenti di emettere un'altra chiamata Winsock. A causa della difficoltà di gestire questa condizione in modo sicuro, la specifica di Windows Sockets 1,1 non consente questo comportamento. Non è consentito per un determinato thread effettuare più chiamate di funzione Winsock nidificate. È consentita una sola chiamata di funzione in attesa per un thread specifico. Qualsiasi chiamata di funzione Winsock nidificata ha esito negativo con l'errore WSAEINPROGRESS. È opportuno sottolineare che questa restrizione si applica alle operazioni di blocco e non blocco, ma solo negli ambienti Windows Sockets 1,1. Esistono alcune eccezioni a questa regola, incluse due funzioni che consentono a un'applicazione di determinare se un'operazione pseudoblocking è effettivamente in corso e di annullare tale operazione, se necessario. Questi elementi sono descritti di seguito.

 

 

 
