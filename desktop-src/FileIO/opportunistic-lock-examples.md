---
description: Diagrammi delle visualizzazioni di traffico di rete per un blocco opportunistico di livello 1, un blocco opportunistico batch e un blocco opportunistico di filtro.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Esempi di blocco opportunistico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529263"
---
# <a name="opportunistic-lock-examples"></a>Esempi di blocco opportunistico

Negli esempi seguenti vengono illustrati i dati e i movimenti dei messaggi SMB come blocchi opportunistici e interrotti. Si noti che i client possono memorizzare nella cache i dati degli attributi del file e i dati del file.

Si noti inoltre che questi esempi sono basati su situazioni in cui le applicazioni client richiedono blocchi opportunistici da server remoti. Questi processi vengono avviati automaticamente dal redirector di rete e dal server remoto: non esiste alcun coinvolgimento diretto da parte dell'applicazione client o delle applicazioni. I processi descritti in questi esempi possono essere generalizzati in situazioni in cui le applicazioni client locali richiedono direttamente i blocchi opportunistici dal file system locale, con l'eccezione che non è previsto alcun scambio di dati sulla rete.

## <a name="level-1-opportunistic-lock"></a>Blocco opportunistico di livello 1

Il diagramma seguente mostra una visualizzazione del traffico di rete di un blocco opportunistico di livello 1 su un file. Le frecce indicano la direzione dello spostamento dei dati, se disponibile.



| Evento | Client X                                          | Server                                   | Y client                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Apre il file, le richieste di livello 1 blocco = =>          |                                          |                                                   |
| 2     |                                                   | <= = il blocco opportunistico di livello 1 viene concesso |                                                   |
| 3     | Esegue operazioni di lettura, scrittura e altro = => |                                          |                                                   |
| 4     |                                                   |                                          | <= = richieste di apertura file                      |
| 5     |                                                   | <= = interrompe il blocco opportunistico         |                                                   |
| 6     | Elimina i dati read-ahead                          |                                          |                                                   |
| 7     | Scrive i dati = =>                                |                                          |                                                   |
| 8     | Invia il messaggio "close" o "Done" = =>            |                                          |                                                   |
| 9     |                                                   | Operazione di apertura OK = =>              |                                                   |
| 10    | Esegue operazioni di lettura, scrittura e altro = => |                                          | <= = esegue operazioni di lettura, scrittura e altre operazioni |



 

Nell'evento 1, il client X apre un file e come parte dell'operazione di apertura richiede un blocco opportunistico di livello 1 sul file. Nell'evento 2, il server concede il blocco di livello 1 perché nessun altro client ha aperto il file. Il client continua ad accedere al file nel modo consueto nell'evento 3.

Nell'evento 4, il client Y tenta di aprire il file e richiede un blocco opportunistico. Il server rileva che il client X ha aperto il file. Il server ignora la richiesta Y mentre client X Scarica tutti i dati di scrittura e abbandona la cache di lettura per il file.

Il server impone la pulizia di X inviando a X un messaggio SMB che interrompe il blocco opportunistico, evento 5. Il client X "invisibile all'utente" Elimina tutti i dati read-ahead; in altre parole, questo processo non genera alcun traffico di rete. Nell'evento 7, client X scrive tutti i dati di scrittura memorizzati nella cache nel server. Quando il client X ha completato la scrittura dei dati memorizzati nella cache nel server, il client X invia un messaggio "Chiudi" o "completato" al server, evento 8.

Dopo che il server è stato informato che il client X ha completato lo scaricamento della cache di scrittura nel server o ha chiuso il file, il server può aprire il file per il client Y, nell'evento 9. Poiché il server dispone ora di due client con lo stesso file aperto, concede un blocco opportunistico a nessuno dei due. Entrambi i client procedono alla lettura dal file e una o nessuna delle scritture nel file.

## <a name="batch-opportunistic-lock"></a>Blocco opportunistico batch

Il diagramma seguente mostra una visualizzazione del traffico di rete di un blocco opportunistico batch. Le frecce indicano la direzione dello spostamento dei dati, se disponibile.



| Evento | Client X                               | Server                                 | Y client                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Apre il file, richiede il blocco batch = => |                                        |                                                   |
| 2     |                                        | <= = concede un blocco opportunistico batch |                                                   |
| 3     | Letture file = =>                      |                                        |                                                   |
| 4     |                                        | <= = invia dati                      |                                                   |
| 5     | Chiude il file                            |                                        |                                                   |
| 6     | Apre il file                             |                                        |                                                   |
| 7     | Cerca dati                      |                                        |                                                   |
| 8     | Legge i dati = =>                      |                                        |                                                   |
| 9     |                                        | <= = invia dati                      |                                                   |
| 10    | Chiude il file                            |                                        |                                                   |
| 11    |                                        |                                        | <= = apre il file                                 |
| 12    |                                        | <= = interrompe il blocco opportunistico       |                                                   |
| 13    | Chiude il file = =>                     |                                        |                                                   |
| 14    |                                        | Operazione di apertura OK = =>            |                                                   |
| 15    |                                        |                                        | <= = esegue operazioni di lettura, scrittura e altre operazioni |



 

Nel blocco opportunistico batch, client X apre un file, evento 1, e il server concede al client X un blocco batch nell'evento 2. Il client X tenta di leggere i dati, evento 3, a cui il server risponde con i dati, evento 4.

L'evento 5 Mostra il blocco opportunistico batch al lavoro. L'applicazione sul client X chiude il file. Tuttavia, il redirector di rete filtra l'operazione di chiusura e non trasmette un messaggio di chiusura, eseguendo così una chiusura invisibile. Il redirector di rete può eseguire questa operazione perché il client X ha solo la proprietà del file. Successivamente, nell'evento 6, l'applicazione riapre il file. Anche in questo caso, nessun flusso di dati attraverso la rete. Per quanto riguarda il server, il client ha aperto il file dall'evento 2.

Gli eventi 7, 8 e 9 mostrano il normale corso di traffico di rete. Nell'evento 10 si verifica un'altra chiusura invisibile all'utente.

Nell'evento 11, il client Y tenta di aprire il file. La visualizzazione del file del server è che il client X è aperto, anche se l'applicazione è stata chiusa dal client X. Pertanto, il server invia un messaggio che suddivide il blocco opportunistico sul client X. il client X ora invia il messaggio di chiusura attraverso la rete, evento 13. L'evento 14 segue quando il server apre il file per il client Y. L'applicazione sul client X ha chiuso il file, pertanto non viene più trasferito da o verso il server per tale file. Il client Y avvia i trasferimenti di dati come di consueto nell'evento 15.

Tra il momento in cui il client X viene concesso il blocco sul file nell'evento 2 e la chiusura finale dell'evento 13, i dati dei file che il client ha memorizzato nella cache sono validi, nonostante le operazioni di apertura e chiusura dell'applicazione coinvolte. Tuttavia, dopo che il blocco opportunistico è stato danneggiato, i dati memorizzati nella cache non possono essere considerati validi.

## <a name="filter-opportunistic-lock"></a>Filtra blocco opportunistico

Il diagramma seguente mostra una visualizzazione del traffico di rete di un blocco opportunistico di filtro. Le frecce indicano la direzione dello spostamento dei dati, se disponibile.



| Evento | Client X                                | Server                   | Y client                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Apre il file senza diritti di accesso = => |                          |                             |
| 2     |                                         | <= = apre il file    |                             |
| 3     | Richieste di blocco filtro = =>              |                          |                             |
| 4     |                                         | <= = il blocco viene concesso       |                             |
| 5     | Apre il file per la lettura = =>           |                          |                             |
| 6     |                                         | <= = riapre il file  |                             |
| 7     | Legge i dati usando l'handle di lettura = => |                          |                             |
| 8     |                                         | <= = invia dati        |                             |
| 9     |                                         | <= = invia dati        |                             |
| 10    |                                         | <= = invia dati        |                             |
| 11    |                                         |                          | <= = apre il file       |
| 12    |                                         | Apre il file = =>    |                             |
| 13    |                                         |                          | <= = blocco filtro richieste |
| 14    |                                         | Nega il blocco del filtro = => |                             |
| 15    |                                         |                          | <= = legge i dati           |
| 16    |                                         | Invia dati = =>        |                             |
| 17    | Lettura dati (memorizzati nella cache)                     |                          |                             |
| 18    | Chiude il file = =>                      |                          |                             |
| 19    |                                         |                          | <= = chiude il file          |



 

Nel filtro di blocco opportunistico, client X apre un file, evento 1, e il server risponde nell'evento 2. Il client richiede quindi un blocco opportunistico di filtro nell'evento 3, seguito dal server che concede il blocco opportunistico nell'evento 4. Il client X riapre quindi il file per la lettura nell'evento 5, a cui il server risponde nell'evento 6. Il client tenta quindi di leggere i dati, a cui il server risponde con i dati, evento 8.

L'evento 9 Mostra il filtro di blocco opportunistico al lavoro. Il server legge il client e invia i dati attraverso la rete anche se il client non lo ha richiesto. Il client memorizza nella cache i dati. Nell'evento 10, il server prevede anche una richiesta futura di dati e invia un'altra parte del file per la cache del client.

Negli eventi 11 e 12, un altro client, Y, apre il file. Il client Y richiede anche un blocco opportunistico di filtro. Nell'evento 14 il server lo nega. Nell'evento 15, il client Y richiede i dati, inviati dal server nell'evento 16. Nessuno di questi influisca sul client X. In qualsiasi momento, un altro client può aprire questo file per l'accesso in lettura. Nessun altro client influisca sul blocco del filtro del client X.

L'evento 17 Mostra la lettura dei dati da client X. Tuttavia, poiché il server ha già inviato i dati e il client lo ha memorizzato nella cache, nessun traffico attraversa la rete.

In questo esempio, client X non tenta mai di leggere tutti i dati nel file, quindi il read-ahead indicato dagli eventi 9 e 10 è "Wasted"; ovvero i dati non vengono mai usati effettivamente. Si tratta di una perdita accettabile perché il read-ahead ha accelerato l'applicazione.

Nell'evento 18, client X chiude il file. Il redirector di rete del client abbandona i dati memorizzati nella cache. Il server chiude il file.

 

 



