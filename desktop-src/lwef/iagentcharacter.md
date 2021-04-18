---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a56272ba095f244e48e335049ec5b88b64855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298643"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgentCharacter** definisce un'interfaccia che consente alle applicazioni di eseguire query sulle proprietà del carattere e riprodurre le animazioni. Queste funzioni sono disponibili anche da [**IAgentCharacterEx**](iagentcharacterex.md). È possibile usare alcuni ID richiesta restituiti dal metodo per tenere traccia del proprio stato nella coda del carattere e sincronizzare il codice con lo stato di animazione corrente del carattere.

**Metodi nell'ordine Vtable**



| Metodi IAgentCharacter                                           | Descrizione                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Restituisce un valore che indica se il carattere (frame) è attualmente visibile.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Imposta la posizione del fotogramma del carattere.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Restituisce la posizione del frame di caratteri.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Imposta la dimensione del frame di caratteri.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Restituisce la dimensione del frame di caratteri.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Restituisce il nome del carattere.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Restituisce la descrizione per il carattere.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Restituisce l'impostazione della velocità di output TTS corrente per il carattere.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Restituisce l'impostazione del pitch TTS corrente per il carattere.                          |
| [**Activate**](iagentcharacter--activate.md)                     | Imposta un valore che indica se un client è attivo o un carattere è in primo piano.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Imposta l'elaborazione inattiva del server.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Restituisce l'impostazione dell'elaborazione inattiva del server.                              |
| [**Preparazione**](iagentcharacter--prepare.md)                       | Recupera i dati di animazione per il carattere.                                       |
| [**Esegui**](iagentcharacter--play.md)                             | Riproduce un'animazione specificata.                                                      |
| [**Interrompere**](iagentcharacter--stop.md)                             | Arresta un'animazione per un carattere.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Arresta tutte le animazioni per un carattere.                                             |
| [**Attesa**](iagentcharacter--wait.md)                             | Include la coda di animazione del carattere.                                            |
| [**Interrompere**](iagentcharacter--interrupt.md)                   | Interrompe l'animazione di un carattere.                                               |
| [**Visualizza**](iagentcharacter--show.md)                             | Visualizza il carattere e riproduce l'animazione dello stato di **visualizzazione** del carattere.     |
| [**Nascondi**](iagentcharacter--hide.md)                             | Riproduce l'animazione dello stato di **occultamento** del carattere e nasconde il frame del carattere. |
| [**Speak**](iagentcharacter--speak.md)                           | Riproduce l'output parlato per il carattere.                                            |
| [**MoveTo**](iagentcharacter--moveto.md)                         | Sposta il frame di caratteri nella posizione specificata.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Riproduce un'animazione gestuale in base alla posizione specificata.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera la motivo dell'ultima spostamento del carattere.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera la motivo dell'Ultima modifica allo stato di visibilità del carattere.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera un valore che indica se il carattere dispone di altri client correnti.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina se riprodurre gli effetti audio di un'animazione di caratteri.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera un valore che indica se l'impostazione degli effetti audio di un carattere è abilitata.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Imposta il nome del carattere.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Imposta la descrizione del carattere.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera dati aggiuntivi archiviati con il carattere.                              |



 

 

 




