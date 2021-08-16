---
description: I servizi vengono in genere scritti come applicazioni console.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Punto di ingresso del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8f44322048351161bb8f3b8afdd619129d18b5effb5dc850d8909afbb3673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888973"
---
# <a name="service-entry-point"></a>Punto di ingresso del servizio

I servizi vengono in genere scritti come applicazioni console. Il punto di ingresso di un'applicazione console è la **funzione** principale. La **funzione main** riceve gli argomenti dal valore **ImagePath** dalla chiave del Registro di sistema per il servizio. Per altre informazioni, vedere la sezione Osservazioni della [**funzione CreateService.**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)

Quando gestione controllo servizi avvia un programma del servizio, attende che chiami la [**funzione StartServiceCtrlDispatcher.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) Usare le linee guida seguenti.

-   Un servizio di tipo SERVICE \_ WIN32 OWN PROCESS deve chiamare \_ immediatamente \_ [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) dal thread principale. È possibile eseguire qualsiasi inizializzazione dopo l'avvio del servizio, come descritto in [Service ServiceMain Function](service-servicemain-function.md).
-   Se il tipo di servizio è SERVICE WIN32 SHARE PROCESS ed è presente un'inizializzazione comune per tutti i servizi nel programma, è possibile eseguire l'inizializzazione nel thread principale prima di chiamare \_ \_ \_ [**StartServiceCtrlDispatcher,**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)purché siano necessari meno di 30 secondi. In caso contrario, è necessario creare un altro thread per eseguire l'inizializzazione comune, mentre il thread principale chiama **StartServiceCtrlDispatcher**. È comunque necessario eseguire qualsiasi inizializzazione specifica del servizio dopo l'avvio del servizio.

La [**funzione StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) accetta una [**struttura SERVICE TABLE \_ \_ ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) per ogni servizio contenuto nel processo. Ogni struttura specifica il nome del servizio e il punto di ingresso per il servizio. Per un esempio, vedere [Writing a Service Program's main Function](writing-a-service-program-s-main-function.md).

Se [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) ha esito positivo, il thread chiamante non restituisce il controllo finché tutti i servizi in esecuzione nel processo non sono nello stato SERVICE \_ STOPPED. Gestione controllo servizi invia richieste di controllo a questo thread tramite un named pipe. Il thread funge da dispatcher di controlli, eseguendo le attività seguenti:

-   Creare un nuovo thread per chiamare il punto di ingresso appropriato all'avvio di un nuovo servizio.
-   Chiamare la funzione del [gestore appropriata per](service-control-handler-function.md) gestire le richieste di controllo del servizio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura della funzione principale di un programma di servizio](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



