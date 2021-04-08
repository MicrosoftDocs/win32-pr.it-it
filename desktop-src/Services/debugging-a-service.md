---
description: Per eseguire il debug del servizio, è possibile utilizzare uno dei metodi seguenti.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Debug di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750799"
---
# <a name="debugging-a-service"></a>Debug di un servizio

Per eseguire il debug del servizio, è possibile utilizzare uno dei metodi seguenti.

-   Usare il debugger per eseguire il debug del servizio mentre è in esecuzione. Ottenere innanzitutto l'identificatore di processo (PID) del processo del servizio. Una volta ottenuto il PID, connettersi al processo in esecuzione. Per informazioni sulla sintassi, vedere la documentazione inclusa nel debugger.
-   Chiamare la funzione [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) per richiamare il debugger per il debug JIT.
-   Specificare un debugger da usare all'avvio di un programma. A tale scopo, creare una chiave denominata **Image File Execution Options** nel seguente percorso del registro di sistema:

    **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**

    Creare una sottochiave con lo stesso nome del servizio, ad esempio MYSERV.EXE. Per questa sottochiave aggiungere un valore di tipo **reg \_ SZ**, denominato **debugger**. Utilizzare il percorso completo del debugger come valore stringa. Nell'applet del pannello di controllo dei servizi selezionare il servizio, fare clic su **avvio** e selezionare **Consenti al servizio di interagire con il desktop**. Il servizio deve essere un servizio interattivo. in caso contrario, il debugger non può essere eseguito sul desktop predefinito. Si noti che questa tecnica non è più supportata a partire da Windows Vista perché tutti i servizi vengono eseguiti nella sessione riservata esclusivamente ai servizi e non supporta la visualizzazione di un'interfaccia utente.

-   Usare la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) per registrare le informazioni.

Per eseguire il debug del codice di inizializzazione di un servizio di avvio automatico, sarà necessario installare ed eseguire temporaneamente il servizio come servizio di avvio a richiesta.

In alcuni casi potrebbe essere necessario eseguire un servizio come applicazione console a scopo di debug. In questo scenario, la funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) restituirà un **errore di \_ \_ \_ \_ connessione del controller di servizio non riuscito**. Pertanto, assicurarsi di strutturare il codice in modo tale che il codice specifico del servizio non venga chiamato quando viene restituito l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di un'applicazione di servizio](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Strumenti di debug per Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
