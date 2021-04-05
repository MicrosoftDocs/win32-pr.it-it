---
description: TCP/IP dispone di caratteristiche che consentono al protocollo di funzionare come requisito di implementazione standardizzato.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Caratteristiche TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882605"
---
# <a name="tcpip-characteristics"></a>Caratteristiche TCP/IP

TCP/IP dispone di caratteristiche che consentono al protocollo di funzionare come requisito di implementazione standardizzato. Queste caratteristiche possono essere combinate con scelte di sviluppo che comportano una riduzione delle prestazioni. L'effetto di queste caratteristiche TCP/IP su un'applicazione dipende dal fatto che l'applicazione sia transazionale o in streaming.

Le applicazioni transazionali sono interessate dal sovraccarico necessario per l'attivazione e la terminazione della connessione. Ad esempio, ogni volta che viene stabilita una connessione su una rete Ethernet, devono essere inviati tre pacchetti di circa 60 byte e circa un RTT è necessario per lo scambio. Quando si verifica la chiusura di una connessione, vengono scambiati quattro pacchetti. Per ogni connessione. un'applicazione che apre e chiude le connessioni spesso comporta questo sovraccarico a ogni occorrenza.

Un altro aspetto di TCP/IP è l' *avvio lento*, che viene eseguito ogni volta che viene stabilita una connessione. Slow-Start è un limite artificiale per il numero di segmenti di dati che è possibile inviare prima che venga ricevuto il riconoscimento di tali segmenti. Slow-Start è progettato per limitare la congestione della rete. Quando viene stabilita una connessione su Ethernet, a prescindere dalle dimensioni della finestra del ricevitore, una trasmissione di 4 KB può richiedere fino a 3-4 RTT a causa dell'avvio lento.

Un'ottimizzazione TCP/IP denominata algoritmo Nagle può anche limitare la velocità di trasferimento dei dati su una connessione. L'algoritmo Nagle è progettato per ridurre il sovraccarico del protocollo per le applicazioni che inviano piccole quantità di dati, ad esempio Telnet, che invia un singolo carattere alla volta. Anziché inviare immediatamente un pacchetto con un numero elevato di dati di intestazione e dati, lo stack attende più dati dall'applicazione o un riconoscimento prima di procedere.

I riconoscimenti ritardati, comunemente noti come *ACK ritardati*, sono inoltre progettati in TCP/IP per consentire un piggybacking più efficiente dei riconoscimenti quando i dati restituiti sono imminenti dall'applicazione sul lato ricevente. Sfortunatamente, se questi dati non sono imminenti e il lato di invio è in attesa di un riconoscimento, possono verificarsi ritardi di circa 200 millisecondi per invio.

Quando una connessione TCP viene chiusa, le risorse di connessione nel nodo che ha avviato la chiusura vengono inserite in uno stato di attesa, denominato tempo di attesa, per evitare il danneggiamento dei dati se i pacchetti duplicati vengono sospesi nella rete. In questo modo si garantisce che entrambe le estremità siano finite con la connessione. Questo può causare l'esaurimento delle risorse richieste per connessione, ad esempio la RAM e le porte, quando le applicazioni aprono e chiudono spesso le connessioni.

Oltre a essere interessati dall'ACK ritardato e da altri schemi di prevenzione della congestione, le applicazioni di streaming possono anche essere influenzate da una dimensione della finestra di ricezione predefinita troppo piccola nell'estremità ricevente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comportamento dell'applicazione](application-behavior-2.md)
</dt> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



