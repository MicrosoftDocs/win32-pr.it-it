---
title: Informazioni Bluetooth
description: Bluetooth è un protocollo standard del settore che consente la connettività wireless per una vasta gamma di dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi portatili.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth , descritto
- Bluetooth Bluetooth , informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ed0f50b6fbe800960c7451bde4d7b43b744d1d2f2d8e398a7656a9f3261479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173182"
---
# <a name="about-bluetooth"></a>Informazioni Bluetooth

Bluetooth è un protocollo standard del settore che consente la connettività wireless per una vasta gamma di dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi portatili.

Le Bluetooth principali includono:

-   Protocollo wireless a basso costo e a basso consumo energetico con supporto standard del settore e accettazione a livello mondiale.
-   Interfaccia di programmazione definita e familiare che gli sviluppatori possono usare per sviluppare o convertire rapidamente applicazioni.
-   Un sito Web ufficiale e un'organizzazione cooperativa a livello di settore che spiega, promuove e standardizza Bluetooth tecnologia. Per altre informazioni, vedere [www.bluetooth.com](https://www.bluetooth.com/).

Bluetooth in Windows fornisce servizi di base simili a quelli esposti da Transmission Control Protocol (la parte TCP di TCP/IP). Come molti servizi e protocolli di rete, la connettività Bluetooth e il trasferimento dei dati vengono programmati tramite chiamate di funzione Windows Sockets, usando tecniche di programmazione Windows Sockets comuni ed estensioni Bluetooth specifiche. Tuttavia, poiché esistono differenze significative tra una rete cablata e fissa e una rete ad hoc wireless, Bluetooth fornisce estensioni come l'individuazione di servizi/dispositivi e la notifica che consentono alle applicazioni di funzionare correttamente nell'ambiente wireless. Queste estensioni aprono anche la strada per la portabilità semplice a tecnologie simili, ad esempio IrDA, o futuri trasporti wireless.

Microsoft offre supporto per Bluetooth in Windows XP con Service Pack 1 (SP1) e versioni successive, in Windows XP Embedded con Service Pack 2 e in Windows CE. Bluetooth le applicazioni eseguite in Windows XP devono essere in grado di essere eseguite in un'immagine di run-time basata su Windows XP Embedded che include le dipendenze necessarie. Per altre informazioni su Windows XP Embedded, vedere la documentazione della Guida Windows XP Embedded su MSDN. Per altre informazioni sulla programmazione Windows CE, vedere Windows CE SDK.

Microsoft offre due approcci per la programmazione Bluetooth in Windows:

-   Uso dell'Windows Sockets
-   Gestione diretta dei dispositivi tramite interfacce Bluetooth non Bluetooth nonket

In questa sezione vengono fornite informazioni generali su entrambi questi approcci negli argomenti seguenti. Per altre informazioni sull'Windows degli elementi dell'API Sockets per programmare Bluetooth, vedere Programmazione Bluetooth [con Windows Socket.](bluetooth-programming-with-windows-sockets.md)



| Sezione                                                                                | Content                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md)     | Viene descritta la relazione tra Bluetooth e Windows socket. |
| [Gestione Bluetooth dispositivi e servizi](managing-bluetooth-devices-and-services.md) | Viene descritto come gestire i Bluetooth e i servizi.           |



 

 

 




