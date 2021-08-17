---
title: Blocchi di dati audio
description: Blocchi di dati audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimediale, blocchi di dati
- audio, blocchi di dati
- audio waveform, blocchi di dati
- blocchi di dati audio, informazioni
- Struttura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a4a0c7236c52854911b51677cf792fa504371fb18900ac947e8fdf1391bd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941755"
---
# <a name="audio-data-blocks"></a>Blocchi di dati audio

Le [**funzioni waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) e [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) richiedono alle applicazioni di allocare blocchi di dati da passare ai driver di dispositivo a scopo di registrazione o riproduzione. Entrambe queste funzioni usano la [**struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per descrivere il blocco di dati.

Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il blocco di dati e la struttura di intestazione che descrive il blocco di dati. Le intestazioni possono essere preparate e non preparate usando le funzioni seguenti.



| Funzione                                                 | Descrizione                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prepara un blocco di dati di input audio-waveform.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Pulisce la preparazione in un blocco di dati di input audio-forma d'onda.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prepara un blocco di dati di output audio-waveform.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Pulisce la preparazione in un blocco di dati di output audio-waveform. |



 

Prima di passare un blocco di dati audio a un driver di dispositivo, è necessario preparare il blocco di dati passandolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) Quando il driver di dispositivo termina con il blocco di dati e lo restituisce, è necessario pulire questa preparazione passando il blocco di dati a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) prima che sia possibile liberare memoria allocata.

A meno che i dati di input e output audio waveform non siano sufficientemente piccoli da essere contenuti in un singolo blocco di dati, le applicazioni devono fornire continuamente al driver di dispositivo blocchi di dati fino al completamento della riproduzione o della registrazione.

Anche se viene usato un singolo blocco di dati, un'applicazione deve essere in grado di determinare quando un driver di dispositivo termina con il blocco di dati in modo che l'applicazione possa liberare la memoria associata al blocco di dati e alla struttura dell'intestazione. Esistono diversi modi per determinare quando un driver di dispositivo termina con un blocco di dati:

-   Specificando una funzione di callback per ricevere un messaggio inviato dal driver al termine di un blocco di dati
-   Usando un callback dell'evento
-   Specificando una finestra o un thread per ricevere un messaggio inviato dal driver al termine di un blocco di dati
-   Tramite il polling del bit WHDR DONE nel \_ **membro dwFlags** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) inviato con ogni blocco di dati

Se un'applicazione non ottiene un blocco di dati per il driver di dispositivo quando necessario, può verificarsi un gap udibile nella riproduzione o una perdita di informazioni registrate in ingresso. Questa operazione richiede almeno uno schema di doppio buffering, che rimane almeno un blocco di dati prima del driver di dispositivo.

Negli argomenti seguenti vengono descritti i modi per determinare quando un driver di dispositivo termina con un blocco di dati:

Uso di una funzione di callback per elaborare i messaggi dei driver

-   [Uso di una funzione di callback per elaborare i messaggi dei driver](using-a-callback-function-to-process-driver-messages.md)
-   [Uso di un callback di eventi per elaborare i messaggi dei driver](using-an-callback-to-process-driver-messages.md)
-   [Uso di una finestra o di un thread per elaborare i messaggi del driver](using-a-window-or-thread-to-process-driver-messages.md)
-   [Gestione dei blocchi di dati tramite polling](managing-data-blocks-by-polling.md)

 

 