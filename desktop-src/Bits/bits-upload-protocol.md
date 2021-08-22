---
title: Protocollo Upload BITS
description: In questa sezione viene descritto il protocollo di rete per i tipi di processo di caricamento e di risposta BITS.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01fea1ff4703dba9a0429c0b37e9c34ebe0d0099016af788c972dd8ee9fddef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021238"
---
# <a name="bits-upload-protocol"></a>Protocollo Upload BITS

In questa sezione viene descritto il protocollo di rete per i tipi di processo di caricamento e di risposta BITS. Il protocollo di caricamento BITS è a livelli su HTTP 1.1 e usa molte delle intestazioni HTTP esistenti e definisce nuove intestazioni. Il protocollo di caricamento BITS supporta un singolo file di caricamento per sessione.

BITS usa i pacchetti per descrivere le richieste client e le risposte del server. L'intestazione BITS-Packet-Type specifica il tipo di pacchetto inviato. Ogni pacchetto contiene intestazioni specifiche. BITS usa il verbo POST BITS \_ per identificare i pacchetti di caricamento BITS. I pacchetti di risposta usano sempre il tipo di pacchetto Ack che è l'acronimo di acknowledge. Il pacchetto Ack viene inviato nel contesto della richiesta precedente. può essere presente una sola richiesta in sospeso alla volta.

Per i processi upload-reply, BITS usa questo protocollo per caricare il file, ma non usa questo protocollo per inviare la risposta al client. Il server BITS invia invece il percorso del file di risposta al client e il client crea un processo di download BITS per scaricare il file di risposta.

Usare il protocollo di caricamento per sostituire il software client o server BITS con la propria implementazione. Per un elenco dei pacchetti di richiesta inviati dal client BITS, vedere [Pacchetti di richiesta BITS](bits-request-packets.md). Per un elenco dei pacchetti di risposta inviati dal server BITS, vedere [Pacchetti di risposta BITS](bits-response-packets.md).

Il client determina la modalità di risposta agli errori o ai pacchetti imprevisti dal server BITS. Se il server riceve un pacchetto non previsto, il server deve inviare un pacchetto Ack con un codice restituito 400 (richiesta non valida).

 

 




