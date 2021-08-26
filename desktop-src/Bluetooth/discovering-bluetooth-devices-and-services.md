---
title: Individuazione di dispositivi e servizi Bluetooth
description: Per facilitare l'individuazione di dispositivi e servizi Bluetooth, Windows esegue il mapping di Bluetooth Service Discovery Protocol (SDP) alle interfacce dello spazio dei nomi Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, attività, individuazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004041"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Individuazione di dispositivi e servizi Bluetooth

Per facilitare l'individuazione di dispositivi e servizi Bluetooth, Windows esegue il mapping di Bluetooth Service Discovery Protocol (SDP) alle interfacce dello spazio dei nomi Windows Sockets. Le funzioni principali usate per questo mapping sono [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd.**](bluetooth-and-wsalookupserviceend.md) La [**struttura WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) viene utilizzata anche in combinazione con queste funzioni.

Poiché alcuni concetti e parametri di Bluetooth SDP non sono necessariamente mappati direttamente alla struttura [**WSAQUERYSET,**](bluetooth-and-wsaqueryset-for-set-service.md) è necessario prestare attenzione alla modalità di creazione e utilizzo dei relativi membri. Per molte operazioni Bluetooth, ad esempio la creazione di record SDP, viene usato il membro **lpBlob** di **WSAQUERYSET.** Quando tale considerazione speciale è necessaria, viene descritta in modo specifico, ad esempio nelle pagine di riferimento come Bluetooth e [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e altre.

È importante comprendere che la registrazione SDP è separata dal controllo socket. Quando un'applicazione server è pronta ad accettare la connessione client, deve chiamare la funzione [**WSASetService**](bluetooth-and-wsasetservice.md) per registrare un record SDP Bluetooth corrispondente a tale servizio. Tale Bluetooth'applicazione deve chiamare di nuovo la funzione **WSASetService** prima della chiusura, per annullare la registrazione Bluetooth record SDP.

Quando si usano le funzioni di mapping descritte in questa pagina, viene assegnato lo spazio dei nomi \_ NS BTH.

Per altre informazioni sull'individuazione di dispositivi e servizi, vedere le pagine di riferimento seguenti:

-   [**Bluetooth e WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth e WSALookupServiceBegin per l'individuazione del servizio**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth e WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth e BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth e WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

È anche possibile scaricare [l'Bluetooth di connessione per](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) un esempio completo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth Programmazione con Windows Socket](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Bluetooth di connessione](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




