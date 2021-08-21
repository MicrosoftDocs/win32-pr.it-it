---
title: Prevenzione di più caricamenti
description: Quando si carica un file, BITS crea un ID sessione che identifica la sessione di caricamento sia nel client BITS che nel server BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c08555acf8bcdc99576675b0ec5852f322f7b37fea9821f3f0156352a29b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701701"
---
# <a name="preventing-multiple-uploads"></a>Prevenzione di più caricamenti

Quando si carica un file, BITS crea un ID sessione che identifica la sessione di caricamento sia nel client BITS che nel server BITS. Se la connessione tra il client BITS e il server viene interrotta durante il caricamento di un file da parte di BITS, il client userà l'ID sessione per provare a riprendere il caricamento.

Se il client BITS si connette allo stesso server di prima, il server riconoscerà l'ID sessione e il caricamento riprenderà dal punto di interruzione. Tuttavia, se il client si connette a un server diverso, il client deve avviare il caricamento dall'inizio perché il nuovo server non ha il contesto di sessione o i dati caricati in precedenza. BITS può connettersi a un server diverso quando il server BITS è ospitato in una Web farm e la proprietà di estensione BITS IIS BITS, [BITSHostId,](bits-iis-extension-properties.md)non è impostata. La proprietà BITSHostId impedisce il riavvio forzando la connessione del client BITS all'indirizzo univoco del server precedente anziché all'indirizzo del server condiviso.

Il server BITS tenterà di inviare il file di caricamento una sola volta all'applicazione server, ma è possibile che il file venga inviato più volte. Ciò può verificarsi, ad esempio, se il server BITS invia il file all'applicazione server e quindi termina durante l'attesa della risposta dall'applicazione server. Il client BITS riceverà un codice di errore dal livello HTTP e ritenterà il caricamento dopo un ritardo. Se il server rimane offline per più tempo del timeout [BITSHostIdFallbackTimeout,](bits-iis-extension-properties.md) il client invierà di nuovo la richiesta all'indirizzo del server condiviso. un server BITS diverso riceverà il file e lo inviare nuovamente all'applicazione server.

Un caso simile può verificarsi anche con un singolo server front-end. Ad esempio, quando il client ha caricato l'intero file nel server, il blocco finale fa sì che il server inoltra il file all'applicazione server. Se il server BITS o l'applicazione server termina dopo l'elaborazione del file, ma prima dell'invio del riconoscimento al client, il client riceverà un codice di errore e riprovarà in un secondo momento. Quando il client esegue un nuovo tentativo, il server BITS vede che il blocco finale è stato caricato e inoltra nuovamente il file all'applicazione server. Se la ricezione del file di caricamento più volte rappresenta un problema per l'applicazione server, è consigliabile includere un identificatore di transazione nei dati.

 

 




