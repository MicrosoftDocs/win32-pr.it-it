---
title: Informazioni su Bluetooth
description: Bluetooth è un protocollo standard del settore che consente la connettività wireless per molti dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi palmari.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, descritto
- Bluetooth Bluetooth, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046355"
---
# <a name="about-bluetooth"></a>Informazioni su Bluetooth

Bluetooth è un protocollo standard del settore che consente la connettività wireless per molti dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi palmari.

Le principali funzionalità Bluetooth includono:

-   Un protocollo wireless a basso costo e a basso consumo di energia con supporto standard del settore e accettazione in tutto il mondo.
-   Interfaccia di programmazione definita e familiare che gli sviluppatori possono utilizzare per sviluppare o trasferire rapidamente le applicazioni.
-   Un sito web ufficiale e un'organizzazione cooperativa a livello di settore che spiega, promuove e standardizza la tecnologia Bluetooth. Per ulteriori informazioni, vedere [www.Bluetooth.com](https://www.bluetooth.com/).

Bluetooth in Windows fornisce servizi di base simili a quelli esposti da Transmission Control Protocol (la parte TCP di TCP/IP). Analogamente a molti protocolli e servizi di rete, la connettività Bluetooth e il trasferimento dei dati vengono programmati tramite le chiamate di funzione Windows Sockets, utilizzando le tecniche comuni di programmazione di Windows Socket e specifiche estensioni Bluetooth. Tuttavia, poiché esistono differenze significative tra una rete cablata e fissa e una rete ad hoc senza fili, Bluetooth fornisce estensioni quali l'individuazione di servizi/dispositivi e la notifica che consentono alle applicazioni di funzionare correttamente nell'ambiente wireless. Queste estensioni aprono anche la modalità di trasferimento semplice a tecnologie simili, ad esempio IrDA, o trasporti wireless futuri.

Microsoft fornisce supporto per Bluetooth in Windows XP con Service Pack 1 (SP1) e versioni successive, in Windows XP Embedded con Service Pack 2 e in Windows CE. Le applicazioni Bluetooth eseguite in Windows XP devono essere in grado di essere eseguite in un'immagine di run-time basata su Windows XP Embedded che include le dipendenze richieste. Per ulteriori informazioni su Windows XP Embedded, vedere la documentazione della Guida di Windows XP Embedded su MSDN. Per ulteriori informazioni sulla programmazione Windows CE, consultare l'SDK di Windows CE.

Microsoft offre due approcci per la programmazione di Bluetooth in Windows:

-   Utilizzo dell'interfaccia Windows Sockets
-   Gestione diretta dei dispositivi mediante interfacce Bluetooth non socket

In questa sezione vengono fornite informazioni generali su entrambi questi approcci negli argomenti seguenti. Per ulteriori informazioni sull'utilizzo di elementi API Windows Sockets per programmare il Bluetooth, vedere la pagina relativa alla [programmazione Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md).



| Sezione                                                                                | Content                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md)     | Descrive la relazione tra Bluetooth e Windows Sockets. |
| [Gestione dei dispositivi e dei servizi Bluetooth](managing-bluetooth-devices-and-services.md) | Viene descritto come gestire i dispositivi e i servizi Bluetooth.           |



 

 

 




