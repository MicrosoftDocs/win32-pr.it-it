---
description: I servizi vengono in genere scritti come applicazioni console.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Punto di ingresso del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966616"
---
# <a name="service-entry-point"></a>Punto di ingresso del servizio

I servizi vengono in genere scritti come applicazioni console. Il punto di ingresso di un'applicazione console è la funzione **principale** . La funzione **Main** riceve gli argomenti dal valore **ImagePath** dalla chiave del registro di sistema per il servizio. Per ulteriori informazioni, vedere la sezione Osservazioni della funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .

Quando SCM avvia un programma di servizio, attende che chiami la funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) . Usare le linee guida seguenti.

-   Un servizio di tipo servizio \_ Win32 \_ proprietario \_ processo deve chiamare [**immediatamente Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) dal thread principale. È possibile eseguire qualsiasi inizializzazione dopo l'avvio del servizio, come descritto in [servizio ServiceMain funzione](service-servicemain-function.md).
-   Se il tipo di servizio è il \_ processo di condivisione Win32 del servizio \_ \_ ed è presente un'inizializzazione comune per tutti i servizi nel programma, è possibile eseguire l'inizializzazione nel thread principale prima di chiamare [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), purché sia necessario meno di 30 secondi. In caso contrario, è necessario creare un altro thread per eseguire l'inizializzazione comune, mentre il thread principale chiama **Impossibile eseguire StartServiceCtrlDispatcher**. È comunque necessario eseguire qualsiasi inizializzazione specifica del servizio dopo l'avvio del servizio.

La funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) accetta una struttura di [**\_ \_ voci della tabella del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) per ogni servizio contenuto nel processo. Ogni struttura specifica il nome del servizio e il punto di ingresso per il servizio. Per un esempio, vedere [scrittura della funzione principale di un programma di servizio](writing-a-service-program-s-main-function.md).

Se [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) ha esito positivo, il thread chiamante non viene restituito finché tutti i servizi in esecuzione nel processo non sono \_ passati allo stato interrotto del servizio. SCM Invia le richieste di controllo al thread tramite un named pipe. Il thread funge da dispatcher di controllo, eseguendo le attività seguenti:

-   Consente di creare un nuovo thread per chiamare il punto di ingresso appropriato quando viene avviato un nuovo servizio.
-   Chiamare la [funzione del gestore](service-control-handler-function.md) appropriata per gestire le richieste di controllo del servizio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura della funzione principale di un programma del servizio](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



