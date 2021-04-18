---
title: Individuazione di dispositivi e servizi Bluetooth
description: Per semplificare l'individuazione di dispositivi e servizi Bluetooth, Windows mappa il protocollo SDP (Bluetooth Service Discovery Protocol) sulle interfacce dello spazio dei nomi Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, attività, individuazione di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/07/2020
ms.locfileid: "106299493"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Individuazione di dispositivi e servizi Bluetooth

Per semplificare l'individuazione di dispositivi e servizi Bluetooth, Windows mappa il protocollo SDP (Bluetooth Service Discovery Protocol) sulle interfacce dello spazio dei nomi Windows Sockets. Le funzioni primarie usate per questo mapping sono le funzioni [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . La struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) viene inoltre utilizzata insieme a queste funzioni.

Poiché alcuni concetti e parametri del sistema SDP Bluetooth non eseguono necessariamente il mapping direttamente alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , è necessario prestare attenzione alla modalità di creazione e di utilizzo dei membri. Per molte operazioni Bluetooth complesse, ad esempio la creazione di record SDP, viene usato il membro **lpBlob** di **WSAQUERYSET** . Quando è necessario prestare particolare attenzione, viene descritta in modo specifico, ad esempio nelle pagine di riferimento come [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e altre.

È importante comprendere che la registrazione SDP è separata dal controllo socket. Quando un'applicazione server è preparata ad accettare la connessione client, deve chiamare la funzione [**WSASetService**](bluetooth-and-wsasetservice.md) per registrare un record SDP Bluetooth corrispondente a tale servizio. L'applicazione Bluetooth deve chiamare nuovamente la funzione **WSASetService** prima di chiudere, per annullare la registrazione del record SDP Bluetooth.

Quando si usano le funzioni di mapping descritte in questa pagina, \_ viene assegnato lo spazio dei nomi NS BTH.

Per ulteriori informazioni sull'individuazione di dispositivi e servizi, consultare le pagine di riferimento seguenti:

-   [**Bluetooth e WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth e WSALookupServiceBegin per l'individuazione del servizio**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth e WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth e BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth e WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

Per un esempio completo, è anche possibile scaricare l' [esempio di connessione Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Esempio di connessione Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




