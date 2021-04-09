---
description: Le dimensioni del pacchetto multimediale influiscono sulla capacità dei protocolli IPX di trasferire i dati tra le reti e possono risultare difficili da gestire in modo indipendente dal trasporto.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Informazioni sulle dimensioni del pacchetto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f97e36a81b90b72d4d1148e9461f58ae2147ba
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968963"
---
# <a name="about-media-packet-size"></a>Informazioni sulle dimensioni del pacchetto multimediale

Le dimensioni del pacchetto multimediale influiscono sulla capacità dei protocolli IPX di trasferire i dati tra le reti e possono risultare difficili da gestire in modo indipendente dal trasporto. IPX non segmenta i pacchetti né segnala quando i pacchetti vengono eliminati a causa di violazioni delle dimensioni. Ciò significa che alcune entità della stazione finale devono mantenere la conoscenza delle dimensioni massime dei pacchetti da usare in qualsiasi percorso di Internet. Tradizionalmente, i servizi IPX datagrams e SPX Connection-oriented hanno lasciato questo onere per l'applicazione, mentre SPXII ha utilizzato la negoziazione di pacchetti Internet di grandi dimensioni per gestirla in modo trasparente.

Winsock tenta di impostare limiti di dimensioni del pacchetto razionali per i vari protocolli IPX, come descritto nella sezione successiva. Questi limiti possono essere visualizzati e modificati dalle applicazioni tramite le opzioni get/set socket. Quando si determinano le dimensioni massime del pacchetto, le tre aree problematiche sono:

-   \# Dimensioni del pacchetto multimediale
-   \# Dimensioni pacchetto instradabile
-   \# Dimensioni del pacchetto della stazione di fine

*Dimensioni del pacchetto multimediale* riflette le dimensioni massime del pacchetto accettabili su qualsiasi supporto che il pacchetto attraversa alla propria destinazione. Le dimensioni del pacchetto variano tra supporti diversi, ad esempio Ethernet e token ring. La quantità di spazio dati all'interno di un pacchetto può variare anche all'interno di un determinato supporto, a seconda della disposizione dell'intestazione del pacchetto. Ad esempio, le dimensioni effettive dei dati di un pacchetto Ethernet variano a seconda che si tratti di un tipo Ethernet II, Ethernet 802,2 o Ethernet.

Le *dimensioni del pacchetto instradabile* riflettono le dimensioni massime del pacchetto che un router intermedio è disposto a inviare. La maggior parte dei router IPX è stata creata per indirizzare qualsiasi datagramma di dimensioni purché rimanga entro la dimensione media della rete di invio e ricezione. Tuttavia, i router meno recenti possono limitare le dimensioni massime del pacchetto a 576 byte, incluse le intestazioni del protocollo.

Le *dimensioni del pacchetto della stazione di fine* riflettono le dimensioni dei buffer di ascolto che le stazioni finali hanno inviato per ricevere i pacchetti in ingresso. Anche quando i limiti per i supporti e i router consentono un pacchetto, è possibile che venga rimosso dalla stazione di fine se l'applicazione ricevente ha inviato un buffer più piccolo. Molte applicazioni IPX/SPX tradizionali limitano le dimensioni del buffer di ricezione in modo tale che la parte di dati non deve essere maggiore di 512 o 1024 byte.

 

 



