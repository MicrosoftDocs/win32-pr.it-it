---
description: Le applicazioni TAPI risiedono nel proprio spazio di elaborazione.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Panoramica del provider di servizi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29871b21124eab7ea4e7e84a9e7e8ca49853cb7a236c6f7a482dbf842a568304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760304"
---
# <a name="tapi-service-provider-overview"></a>Panoramica del provider di servizi TAPI

Le applicazioni TAPI risiedono nel proprio spazio di elaborazione. Le applicazioni TAPI caricano Tapi32.dll o Tapi3.dll processo e TAPI comunica con TAPISRV tramite un'interfaccia RPC privata. Un provider di servizi di configurazione viene eseguito nel contesto di TAPISRV. Un TSP specifico può risiedere in un computer diverso dal computer dell'utente e viene eseguito l'accesso tramite un provider di servizi di configurazione remoto. TAPISRV viene implementato come processo di servizio all'interno di SVCHOST. Un msp si trova all'interno dello spazio di elaborazione dell'applicazione ed è sempre locale.

Una coppia TSP/MSP può essere considerata come un percorso di comunicazione privata virtuale. Le informazioni possono essere inviate tra i due utilizzando buffer opachi che non vengono interpretati da TAPISRV o dalla DLL TAPI.

Alcuni provider di servizi implementano operazioni specifiche per l'hardware interessato. TAPI 2.x fornisce l'accesso a tali operazioni tramite la [**funzione lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) o [**phoneDevSpecific.**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) TAPI 3.x espone interfacce [specifiche del provider](./provider-specific-interfaces.md).

Il diagramma seguente illustra il flusso di controlli e informazioni, che mostrano un provider di servizi di configurazione autonomo (Unimodem) e una coppia TSP/MSP (H.323).

![flusso di controllo e informazioni tsp autonomo e tsp/msp associato](images/tsp-msp1.png)

Il diagramma seguente illustra lo stato di una chiamata in ingresso che coinvolge sia un provider di servizi di configurazione che un provider di servizi di configurazione.

![chiamata in ingresso con tsp e msp](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Configurazione delle chiamate in ingresso

-   Il TSP invia un [**messaggio LINE \_ NEWCALL**](line-newcall.md) a TAPISRV. Lo [**stato della chiamata**](./linecallstate--constants.md) è LINECALLSTATE \_ OFFERING.
-   TAPISRV notifica ai client la chiamata.
-   TAPI3 crea l'oggetto TapI Call, quindi chiama [**ITMSPAddress::CreateMSPCall,**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall)implementato dal provider di servizi di amministrazione.
-   Il msp crea un oggetto Chiamata MSP e i flussi predefiniti in base ai [**tipi di supporti**](./tapimediatype--constants.md) necessari per la chiamata. Restituisce un puntatore IUnknown all'oggetto chiamata MSP.
-   TAPI3 aggrega l'oggetto Msp Call nell'oggetto TapI Call, rendendo disponibili all'applicazione interfacce come [**ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) Invia quindi una notifica all'applicazione della nuova chiamata.

L'applicazione può quindi usare metodi come [**ITStream::SelectTerminal per**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) completare i preparativi per il completamento delle chiamate.

## <a name="incoming-call-completion"></a>Completamento delle chiamate in ingresso

-   L'applicazione chiama [**ITBasicCallControl::Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 chiama [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV chiama [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   Il provider di servizi di trasmissione delle chiamate avvia il flusso di chiamate. In genere, il provider di servizi di recapito invia un messaggio al provider di servizi di amministrazione corrispondente e il provider di servizi di amministrazione avvia i flussi. In alcune implementazioni TSP/MSP, il provider di servizi di streaming avvia i flussi.

## <a name="tspmsp-communication-during-call-progress"></a>Comunicazione TSP/MSP durante lo stato di avanzamento delle chiamate

Dopo che la chiamata è in corso, il provider di servizi di gestione delle comunicazioni e il provider di servizi condivisi comunicano passando buffer opachi tramite TAPISRV e TAPI3.

-   Il provider di servizi di configurazione invia informazioni al provider di servizi di configurazione inviando il messaggio [**LINE \_ SENDMSPDATA**](line-sendmspdata.md) a TAPISRV.
-   Il provider di servizi di configurazione riceve informazioni dal provider di servizi di configurazione tramite [**il metodo ITMSPAddress::ReceiveTSPData.**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) Se i dati sono correlati a un oggetto chiamata MSP, come parametro di tale metodo viene fornito un puntatore a interfaccia all'oggetto chiamata MSP.
-   Il provider di servizi di configurazione invia informazioni al provider di servizi di configurazione inviando un evento \_ MSP TSP \_ DATA a TAPI 3.
-   Il provider di servizi di configurazione riceve informazioni dal provider di servizi di configurazione tramite la [**funzione \_ lineReceiveMSPData TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)

Il processo esatto e il contenuto della comunicazione tra provider di servizi sono specifici di un determinato set TSP/MSP.

> [!Note]  
> Per le chiamate in uscita, il provider di servizi di configurazione è in genere a conoscenza della chiamata prima del provider di servizi di configurazione. Se il provider di servizi di configurazione tenta di comunicare con il provider di servizi di rete prima che venga informato di una chiamata, la comunicazione avrà esito negativo. Quando il provider di servizi di configurazione e il provider di servizi di configurazione devono scambiare informazioni relative a una chiamata specifica, il provider di servizi di distribuzione deve avviare la comunicazione.

 

 

 
