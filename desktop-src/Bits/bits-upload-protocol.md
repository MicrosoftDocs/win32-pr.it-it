---
title: Protocollo di caricamento BITS
description: Questa sezione descrive il protocollo di rete per i tipi di processo di caricamento BITS e di caricamento-risposta.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708143"
---
# <a name="bits-upload-protocol"></a>Protocollo di caricamento BITS

Questa sezione descrive il protocollo di rete per i tipi di processo di caricamento BITS e di caricamento-risposta. Il protocollo di caricamento BITS è sovrapposto alla parte superiore di HTTP 1,1 e usa molte delle intestazioni HTTP esistenti e definisce nuove intestazioni. Il protocollo di caricamento BITS supporta un singolo file di caricamento per sessione.

BITS usa i pacchetti per descrivere le richieste client e le risposte del server. L'intestazione BITS-Packet-Type specifica il tipo di pacchetto da inviare. Ogni pacchetto contiene intestazioni specifiche. BITS usa il \_ verbo Post bits per identificare i pacchetti di caricamento BITS. I pacchetti di risposta usano sempre il tipo di pacchetto ACK che sta per confermare. Il pacchetto ACK viene inviato nel contesto della richiesta precedente; può essere presente una sola richiesta in attesa alla volta.

Per i processi di caricamento-risposta, BITS usa questo protocollo per caricare il file, ma non usa questo protocollo per inviare la risposta al client. Al contrario, il server BITS invia il percorso del file di risposta al client e il client crea un processo di download BITS per scaricare il file di risposta.

Usare il protocollo di caricamento per sostituire il client BITS o il software server con la propria implementazione. Per un elenco di pacchetti di richiesta inviati dal client BITS, vedere [pacchetti di richiesta bits](bits-request-packets.md). Per un elenco di pacchetti di risposta inviati dal server BITS, vedere [pacchetti di risposta bits](bits-response-packets.md).

Il client determina il modo in cui risponde a errori o pacchetti imprevisti dal server BITS. Se il server riceve un pacchetto che non si aspetta, il server deve inviare un pacchetto ACK con un codice restituito 400 (richiesta non valida).

 

 




