---
description: Le applicazioni TAPI si trovano nello spazio di processo.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Panoramica del provider di servizi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564454"
---
# <a name="tapi-service-provider-overview"></a>Panoramica del provider di servizi TAPI

Le applicazioni TAPI si trovano nello spazio di processo. Le applicazioni TAPI caricano il Tapi32.dll o Tapi3.dll nel loro processo e TAPI comunica con TAPISRV tramite un'interfaccia RPC privata. Un TSP viene eseguito nel contesto di TAPISRV. Un determinato TSP può trovarsi in un computer diverso dal computer dell'utente ed è possibile accedervi usando un TSP remoto. TAPISRV viene implementato come processo del servizio all'interno di SVCHOST. Un MSP risiede nello spazio di processo dell'applicazione ed è sempre locale.

Una coppia TSP/MSP può essere considerata come avente un percorso di comunicazione privato virtuale. È possibile inviare informazioni tra i due usando buffer opachi che non vengono interpretati da TAPISRV o dalla DLL TAPI.

Alcuni provider di servizi implementano operazioni specifiche per l'hardware necessario. TAPI 2. x consente di accedere a tali operazioni tramite la funzione [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) o [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . TAPI 3. x espone [interfacce specifiche del provider](./provider-specific-interfaces.md).

Il diagramma seguente illustra il flusso di controlli e informazioni, mostrando un TSP autonomo (Unimodem) e una coppia TSP/MSP (H. 323).

![un TSP autonomo e un flusso di controllo e di informazioni di un TSP/msp associato](images/tsp-msp1.png)

Il diagramma seguente illustra lo stato di avanzamento di una chiamata in ingresso che prevede sia un TSP che un MSP.

![chiamata in ingresso con un TSP e un MSP](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Impostazione delle chiamate in ingresso

-   Il TSP Invia un messaggio di [**riga \_ NEWCALL**](line-newcall.md) a tapisrv. Lo [**stato della chiamata**](./linecallstate--constants.md) è LINECALLSTATE \_ offering.
-   TAPISRV notifica ai client la chiamata.
-   TAPI3 crea l'oggetto chiamata TAPI, quindi chiama [**ITMSPAddress:: CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), che viene implementato da msp.
-   MSP crea un oggetto chiamata MSP e flussi predefiniti in base ai [**tipi di supporto**](./tapimediatype--constants.md) richiesti per la chiamata. Restituisce un puntatore IUnknown all'oggetto chiamata MSP.
-   TAPI3 aggrega l'oggetto chiamata MSP nell'oggetto chiamata TAPI, rendendo disponibili le interfacce come [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) per l'applicazione. Viene quindi inviata una notifica all'applicazione della nuova chiamata.

L'applicazione può quindi usare metodi come [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) per completare i preparativi per il completamento della chiamata.

## <a name="incoming-call-completion"></a>Completamento delle chiamate in ingresso

-   L'applicazione chiama [**ITBasicCallControl:: Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 chiama [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV chiama [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   Il TSP avvia lo streaming delle chiamate. In genere, il TSP Invia un messaggio al MSP corrispondente e il MSP avvia i flussi. In alcune implementazioni di TSP/MSP, il TSP avvia i flussi.

## <a name="tspmsp-communication-during-call-progress"></a>Comunicazione TSP/MSP durante lo stato della chiamata

Dopo che è in corso la chiamata, il TSP e il MSP comunicano passando buffer opachi attraverso TAPISRV e TAPI3.

-   Il TSP Invia le informazioni al MSP inviando il messaggio di [**riga \_ SENDMSPDATA**](line-sendmspdata.md) a tapisrv.
-   Il MSP riceve informazioni da TSP tramite il metodo [**ITMSPAddress:: ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) . Se i dati sono correlati a un oggetto chiamata MSP, un puntatore di interfaccia all'oggetto chiamata MSP viene fornito come parametro di tale metodo.
-   Il MSP invia informazioni al TSP inviando \_ a TAPI 3 un evento di dati del tsp di msp \_ .
-   Il TSP riceve informazioni da MSP tramite la funzione [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) .

Il processo esatto e il contenuto della comunicazione tra i provider di servizi sono specifici di un determinato set di TSP/MSP.

> [!Note]  
> Per le chiamate in uscita, il MSP è in genere in grado di riconoscere la chiamata prima del TSP. Se il MSP tenta di comunicare con il TSP prima che il TSP venga informato su una chiamata, la comunicazione avrà esito negativo. Quando il MSP e il TSP devono scambiare informazioni relative a una chiamata specifica, il TSP deve avviare la comunicazione.

 

 

 
