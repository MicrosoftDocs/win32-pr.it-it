---
title: Oggetto Controls
description: L'oggetto Controls consente di modificare la riproduzione dei supporti usando le proprietà e i metodi seguenti.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Controlla le finestre degli oggetti Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103718949"
---
# <a name="controls-object"></a>Oggetto Controls

L'oggetto **Controls** consente di modificare la riproduzione dei supporti usando le proprietà e i metodi seguenti.

L'oggetto **Controls** supporta le proprietà seguenti.



| Proprietà                                                            | Descrizione                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | Recupera il numero di lingue audio supportate.                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | Specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | Specifica o recupera l'indice in base uno che corrisponde alla lingua audio per la riproduzione.                                                   |
| [currentItem](controls-currentitem.md)                             | Specifica o recupera l'elemento multimediale corrente.                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | Specifica o Recupera il numero di marcatore corrente.                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | Specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | Recupera la posizione corrente nell'elemento multimediale sotto forma di **stringa**.                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE. |
| [isAvailable](controls-isavailable.md)                             | Recupera un valore che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire una determinata azione.                                                |



 

L'oggetto **Controls** supporta i metodi seguenti:



| Metodo                                                                  | Descrizione                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [fastForward](controls-fastforward.md)                                 | Avvia la riproduzione veloce dell'elemento multimediale nella direzione in avanti.                                     |
| [fastReverse](controls-fastreverse.md)                                 | Avvia la riproduzione veloce dell'elemento multimediale nella direzione inversa.                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | Recupera la descrizione della lingua audio corrispondente all'indice in base 1 specificato. |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | Recupera l'LCID per un indice di lingua audio specificato.                                         |
| [getLanguageName](controls-getlanguagename.md)                         | Recupera il nome della lingua audio con l'LCID specificato.                                |
| [avanti](controls-next.md)                                               | Imposta l'elemento corrente sull'elemento successivo nella playlist.                                          |
| [pause](controls-pause.md)                                             | Sospende la riproduzione dell'elemento multimediale.                                                            |
| [Play](controls-play.md)                                               | Determina l'avvio della riproduzione dell'elemento multimediale.                                                          |
| [playItem](controls-playitem.md)                                       | Determina la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.                |
| [previous](controls-previous.md)                                       | Imposta l'elemento corrente sull'elemento precedente nella playlist.                                      |
| [passo](controls-step.md)                                               | Fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo.                        |
| [stop](controls-stop.md)                                               | Interrompe la riproduzione dell'elemento multimediale.                                                             |



 

L'accesso all'oggetto **Controls** viene effettuato tramite la proprietà seguente.



| Oggetto                      | Proprietà                        |
|-----------------------------|---------------------------------|
| [Player](player-object.md) | [controlli](player-controls.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




