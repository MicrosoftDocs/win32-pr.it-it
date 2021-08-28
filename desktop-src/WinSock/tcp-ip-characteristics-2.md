---
description: TCP/IP ha caratteristiche che consentono il funzionamento del protocollo in base ai requisiti di implementazione standardizzati.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Caratteristiche TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f720dac1157149fe34da1b6bcbc08928654f268c7ac3e32b2e22599ae43cb701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733421"
---
# <a name="tcpip-characteristics"></a>Caratteristiche TCP/IP

TCP/IP ha caratteristiche che consentono il funzionamento del protocollo in base ai requisiti di implementazione standardizzati. Queste caratteristiche possono essere combinate con scelte di sviluppo che comportano prestazioni scarse. L'impatto di queste caratteristiche TCP/IP su un'applicazione dipende dal fatto che l'applicazione sia transazionale o in streaming.

Le applicazioni transazionali sono interessate dal sovraccarico necessario per la creazione e la terminazione della connessione. Ad esempio, ogni volta che viene stabilita una connessione in una rete Ethernet, è necessario inviare tre pacchetti di circa 60 byte ciascuno ed è necessario circa un RTT per lo scambio. Quando si verifica la terminazione di una connessione, vengono s scambiati quattro pacchetti. Questo è per ogni connessione. Un'applicazione che apre e chiude le connessioni spesso comporta questo sovraccarico a ogni occorrenza.

Un altro aspetto di TCP/IP è *l'avvio lento,* che avviene ogni volta che viene stabilita una connessione. L'avvio lento è un limite artificiale al numero di segmenti di dati che possono essere inviati prima della ricezione del riconoscimento di tali segmenti. L'avvio lento è progettato per limitare la congestione della rete. Quando viene stabilita una connessione tramite Ethernet, indipendentemente dalle dimensioni della finestra del ricevitore, una trasmissione da 4 KB può richiedere fino a 3-4 RTT a causa di un avvio lento.

Un'ottimizzazione TCP/IP denominata Algoritmo Nagle può anche limitare la velocità di trasferimento dei dati in una connessione. L'algoritmo Nagle è progettato per ridurre il sovraccarico del protocollo per le applicazioni che inviano piccole quantità di dati, ad esempio Telnet, che inviano un singolo carattere alla volta. Anziché inviare immediatamente un pacchetto con molte intestazioni e pochi dati, lo stack attende più dati dall'applicazione, o un riconoscimento, prima di procedere.

I riconoscimenti ritardati, comunemente definiti *ACK* ritardati, sono progettati anche in TCP/IP per consentire un più efficiente piggyback dei riconoscimenti quando i dati restituiti vengono restituiti dall'applicazione lato ricevente. Sfortunatamente, se questi dati non sono imminenti e il lato di invio è in attesa di un riconoscimento, possono verificarsi ritardi di circa 200 millisecondi per ogni invio.

Quando una connessione TCP viene chiusa, le risorse di connessione nel nodo che ha avviato la chiusura vengono messe in uno stato di attesa, denominato TIME-WAIT, per proteggersi dal danneggiamento dei dati se i pacchetti duplicati si trastendono nella rete. In questo modo, entrambe le estremità vengono completate con la connessione. Ciò può causare un esaurimento delle risorse necessarie per ogni connessione, ad esempio RAM e porte, quando le applicazioni aprono e chiudono spesso le connessioni.

Oltre a essere interessate da ACK ritardato e da altri schemi di evitare la congestione, le applicazioni di streaming possono anche essere interessate da dimensioni troppo ridotte della finestra di ricezione predefinita sul lato ricevente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comportamento dell'applicazione](application-behavior-2.md)
</dt> <dt>

[Applicazioni socket Windows ad alte prestazioni](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



