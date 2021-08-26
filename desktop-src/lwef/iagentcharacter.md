---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7144c6d3379a2237d3f14c955d8052ff4d20d1ff98d9c2f2637796f8b931b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962091"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgentCharacter** definisce un'interfaccia che consente alle applicazioni di eseguire query sulle proprietà dei caratteri e riprodurre animazioni. Queste funzioni sono disponibili anche da [**IAgentCharacterEx.**](iagentcharacterex.md) È possibile usare alcuni ID richiesta di restituzione del metodo per tenere traccia del relativo stato nella coda del carattere e sincronizzare il codice con lo stato di animazione corrente del carattere.

**Metodi nell'ordine Vtable**



| Metodi di IAgentCharacter                                           | Descrizione                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Restituisce un valore che indica se il carattere (frame) è attualmente visibile.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Imposta la posizione del frame di caratteri.                                         |
| [**Getposition**](iagentcharacter--getposition.md)               | Restituisce la posizione del frame di caratteri.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Imposta le dimensioni del frame di caratteri.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Restituisce le dimensioni del frame di caratteri.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Restituisce il nome del carattere.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Restituisce la descrizione del carattere.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Restituisce l'impostazione corrente della velocità di output TTS per il carattere.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Restituisce l'impostazione corrente del passo TTS per il carattere.                          |
| [**Attiva**](iagentcharacter--activate.md)                     | Imposta se un client è attivo o se un carattere è in primo piano.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Imposta l'elaborazione inattiva del server.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Restituisce l'impostazione dell'elaborazione inattiva del server.                              |
| [**Preparare**](iagentcharacter--prepare.md)                       | Recupera i dati di animazione per il carattere.                                       |
| [**Esegui**](iagentcharacter--play.md)                             | Riproduce un'animazione specificata.                                                      |
| [**Fermare**](iagentcharacter--stop.md)                             | Arresta un'animazione per un carattere.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Arresta tutte le animazioni per un carattere.                                             |
| [**Attesa**](iagentcharacter--wait.md)                             | Contiene la coda di animazione del carattere.                                            |
| [**Interrompere**](iagentcharacter--interrupt.md)                   | Interrompe l'animazione di un carattere.                                               |
| [**Mostra**](iagentcharacter--show.md)                             | Visualizza il carattere e riproduce l'animazione dello stato **Di** visualizzazione del carattere.     |
| [**Nascondi**](iagentcharacter--hide.md)                             | Riproduce l'animazione **dello stato Nascondi** del carattere e nasconde il fotogramma del carattere. |
| [**Speak**](iagentcharacter--speak.md)                           | Riproduce l'output parlato per il carattere.                                            |
| [**Moveto**](iagentcharacter--moveto.md)                         | Sposta la cornice del carattere nella posizione specificata.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Riproduce un'animazione di inserimento in base alla posizione specificata.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera la causa dell'ultimo spostamento del carattere.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera la causa dell'ultima modifica allo stato di visibilità del carattere.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera se il carattere dispone di altri client correnti.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina se gli effetti sonori di un'animazione carattere vengono riprodotti.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera se l'impostazione degli effetti sonori di un carattere è abilitata.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Imposta il nome del carattere.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Imposta la descrizione del carattere.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera dati aggiuntivi archiviati con il carattere .                              |



 

 

 




