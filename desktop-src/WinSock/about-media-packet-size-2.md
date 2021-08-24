---
description: Le dimensioni dei pacchetti multimediali influiscono sulla capacità dei protocolli IPX di trasferire i dati tra reti e possono risultare difficili da gestire in modo indipendente dal trasporto.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Informazioni sulle dimensioni del pacchetto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03be30402dc94b22315292b281565572f04cbc89803eeed79f67d55a77ceeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412191"
---
# <a name="about-media-packet-size"></a>Informazioni sulle dimensioni del pacchetto multimediale

Le dimensioni dei pacchetti multimediali influiscono sulla capacità dei protocolli IPX di trasferire i dati tra reti e possono risultare difficili da gestire in modo indipendente dal trasporto. IPX non segmenta i pacchetti né segnala quando i pacchetti vengono eliminati a causa di violazioni delle dimensioni. Ciò significa che alcune entità nella stazione finale devono mantenere la conoscenza delle dimensioni massime del pacchetto da usare in un determinato percorso di internetwork. Tradizionalmente, i datagrammi IPX e i servizi orientati alla connessione SPX hanno lasciato questo carico di lavoro all'applicazione, mentre SPXII ha usato una negoziazione di pacchetti Internet di grandi dimensioni per gestirlo in modo trasparente.

Winsock tenta di impostare limiti razionali per le dimensioni dei pacchetti per i vari protocolli IPX, come descritto nella sezione successiva. Questi limiti possono essere visualizzati e modificati dalle applicazioni tramite le opzioni get/set socket. Quando si determinano le dimensioni massime dei pacchetti, le tre aree di interesse sono:

-   \# Dimensioni del pacchetto multimediale
-   \# Dimensioni del pacchetto instradabile
-   \# Dimensioni del pacchetto della stazione finale

*Le dimensioni del pacchetto* multimediale riflettono le dimensioni massime consentite per tutti i supporti attraversati dal pacchetto fino alla destinazione. Le dimensioni del pacchetto variano tra supporti diversi, ad esempio Ethernet e token ring. La quantità di spazio dati all'interno di un pacchetto può variare anche all'interno di un determinato supporto, a seconda della disposizione dell'intestazione del pacchetto. Ad esempio, la dimensione effettiva dei dati di un pacchetto Ethernet varia a seconda che sia di tipo Ethernet II, Ethernet 802.2 o Ethernet SNAP.

*La dimensione del pacchetto instradabile* riflette le dimensioni massime del pacchetto che un router intermedio è disposto a inoltrare. La maggior parte dei router IPX è compilata per indirizzare qualsiasi datagramma di dimensioni purché rimanga all'interno delle dimensioni dei supporti della rete mittente e ricevente. Tuttavia, i router meno recenti possono limitare le dimensioni massime del pacchetto a 576 byte, incluse le intestazioni del protocollo.

*Le dimensioni dei pacchetti delle stazioni finali* riflettono le dimensioni dei buffer di attesa che le stazioni finali hanno inviato per ricevere i pacchetti in ingresso. Anche quando i limiti dei supporti e del router consentono un pacchetto, è possibile che venga eliminato dalla stazione finale se l'applicazione ricevente ha pubblicato un buffer più piccolo. Molte applicazioni IPX/SPX tradizionali limitano la ricezione delle dimensioni del buffer in modo che la parte dei dati non deve essere superiore a 512 o 1024 byte.

 

 



