---
title: Blocchi di dati audio
description: Blocchi di dati audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimediale, blocchi di dati
- audio, blocchi di dati
- audio Waveform, blocchi di dati
- blocchi di dati audio, informazioni
- Struttura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956383"
---
# <a name="audio-data-blocks"></a>Blocchi di dati audio

Per le funzioni [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) e [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) è necessario che le applicazioni allochino i blocchi di dati da passare ai driver di dispositivo a scopo di registrazione o riproduzione. Entrambe queste funzioni usano la struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per descrivere il relativo blocco di dati.

Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il blocco di dati e la struttura di intestazione che descrive il blocco di dati. È possibile preparare e non preparare le intestazioni usando le funzioni seguenti.



| Funzione                                                 | Descrizione                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prepara un blocco di dati di input audio e di forma d'onda.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Pulisce la preparazione in un blocco di dati di input audio e di forma d'onda.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prepara un blocco di dati di output dell'audio e della forma d'onda.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Pulisce la preparazione in un blocco di dati di output dell'audio e della forma d'onda. |



 

Prima di passare un blocco di dati audio a un driver di dispositivo, è necessario preparare il blocco di dati passandolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader). Quando il driver di dispositivo è terminato con il blocco di dati e lo restituisce, è necessario pulire la preparazione passando il blocco di dati a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) prima di poter liberare la memoria allocata.

A meno che i dati di input e di output della forma d'onda non siano sufficientemente piccoli da essere contenuti in un singolo blocco di dati, le applicazioni devono fornire continuamente al driver di dispositivo i blocchi di dati fino al completamento della riproduzione o della registrazione.

Anche se viene utilizzato un singolo blocco di dati, un'applicazione deve essere in grado di determinare quando un driver di dispositivo è terminato con il blocco di dati, in modo che l'applicazione possa liberare la memoria associata al blocco di dati e alla struttura dell'intestazione. Esistono diversi modi per determinare quando un driver di dispositivo è terminato con un blocco di dati:

-   Specificando una funzione di callback per ricevere un messaggio inviato dal driver al termine di un blocco di dati
-   Utilizzando un callback di evento
-   Specificando una finestra o un thread per ricevere un messaggio inviato dal driver al termine di un blocco di dati
-   Eseguendo il polling del \_ bit WHDR eseguito nel membro **dwFlags** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) inviata con ogni blocco di dati

Se un'applicazione non ottiene un blocco di dati al driver di dispositivo quando necessario, potrebbe verificarsi una lacuna udibile nella riproduzione o una perdita di informazioni registrate in entrata. Questa operazione richiede almeno uno schema a doppio buffer, rimanendo almeno un blocco di dati prima del driver di dispositivo.

Negli argomenti seguenti vengono descritti i modi per determinare quando un driver di dispositivo è terminato con un blocco di dati:

Utilizzo di una funzione di callback per elaborare i messaggi del driver

-   [Utilizzo di una funzione di callback per elaborare i messaggi del driver](using-a-callback-function-to-process-driver-messages.md)
-   [Utilizzo di un callback di evento per elaborare i messaggi del driver](using-an-callback-to-process-driver-messages.md)
-   [Uso di una finestra o di un thread per elaborare i messaggi dei driver](using-a-window-or-thread-to-process-driver-messages.md)
-   [Gestione dei blocchi di dati tramite polling](managing-data-blocks-by-polling.md)

 

 