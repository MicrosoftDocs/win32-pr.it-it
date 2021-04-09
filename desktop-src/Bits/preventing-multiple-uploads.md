---
title: Prevenzione di più caricamenti
description: Quando si carica un file, BITS crea un ID di sessione che identifica la sessione di caricamento sia nel client BITS che nel server BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044163"
---
# <a name="preventing-multiple-uploads"></a>Prevenzione di più caricamenti

Quando si carica un file, BITS crea un ID di sessione che identifica la sessione di caricamento sia nel client BITS che nel server BITS. Se la connessione tra il client BITS e il server viene interruppe mentre è in corso il caricamento di un file in bit, il client userà l'ID sessione per tentare di riprendere il caricamento.

Se il client BITS si connette allo stesso server di prima, il server riconoscerà l'ID sessione e il caricamento riprenderà dal punto di interruzione. Tuttavia, se il client si connette a un server diverso, il client deve avviare il caricamento dall'inizio perché il nuovo server non dispone del contesto della sessione o dei dati caricati in precedenza. BITS può connettersi a un server diverso quando il server BITS è ospitato in una Web farm e la proprietà di estensione IIS BITS, [BITSHostId](bits-iis-extension-properties.md), non è impostata. La proprietà BITSHostId impedisce i riavvii forzando il client BITS a connettersi all'indirizzo univoco del server precedente anziché all'indirizzo del server condiviso.

Il server BITS tenterà di inviare il file di caricamento solo una volta all'applicazione server, ma è possibile che il file venga inviato più di una volta. Questa situazione può verificarsi, ad esempio, se il server BITS invia il file all'applicazione server e quindi viene terminato durante l'attesa della risposta dall'applicazione server. Il client BITS riceverà un codice di errore dal livello HTTP e ritenterà il caricamento dopo un ritardo. Se il server rimane offline per un periodo di tempo maggiore del timeout di [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) , il client invierà di nuovo la richiesta all'indirizzo del server condiviso. un altro server BITS riceverà il file e lo recapiterà nuovamente all'applicazione server.

Un caso simile può verificarsi anche con un unico server front-end. Ad esempio, quando il client ha caricato l'intero file nel server, il blocco finale fa in modo che il server inoltri il file all'applicazione server. Se il server BITS o l'applicazione server termina dopo l'elaborazione del file ma prima che il riconoscimento venga inviato al client, il client riceverà un codice di errore e riproverà in seguito. Quando il client ritenta, il server BITS vedrà che il blocco finale è stato caricato e il file verrà nuovamente inviato all'applicazione server. Se la ricezione più volte del file di caricamento è un problema per l'applicazione server, è necessario considerare l'inclusione di un identificatore di transazione nei dati.

 

 




