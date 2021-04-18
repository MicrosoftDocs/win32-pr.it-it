---
title: Controls. currentPositionTimecode
description: La proprietà currentPositionTimecode specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Media Player di Windows Controls. currentPositionTimecode
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324831"
---
# <a name="controlscurrentpositiontimecode"></a>Controls. currentPositionTimecode

La proprietà **currentPositionTimecode** specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Il codice di ora SMPTE fornisce un modo standard per identificare un singolo frame video, utile per sincronizzare la riproduzione. Se un file multimediale digitale supporta il codice ora SMPTE, Windows Media Player possibile recuperare le informazioni sulla posizione del codice ora corrente o cercare un frame video identificato da una **stringa** di codice temporale particolare.

Il codice di ora SMPTE identifica un frame specifico per il numero di ore, minuti, secondi e frame che lo separa da un particolare frame di riferimento il frame designato come ora zero. In genere, il fotogramma ora zero è l'inizio del file e un determinato valore del codice ora SMPTE rappresenta il tempo trascorso dall'inizio del file.

La **stringa** del codice temporale è nell'intervallo di formato \[  \] *HH*:*mm*:*SS*.*FF* con \[ *intervallo* \] che rappresenta l'intervallo, *HH* rappresenta le ore, *mm* rappresenta minuti, *SS* rappresenta i secondi e *FF* rappresenta i frame. Quando si specifica un valore usando **currentPositionTimecode**, è necessario includere tutte e otto le cifre usando zeri come segnaposto.

L' \[ identificatore di *intervallo* \] corrisponde al membro **Wrange** della struttura di dati dell' **\_ estensione del \_ timecode \_ WMT** del formato Windows Media. Per ulteriori informazioni sugli intervalli di codice temporali, vedere Windows Media Format SDK.

La specifica e il recupero di **currentPositionTimecode** sono supportati solo per i file che contengono informazioni sul codice ora SMPTE.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene specificato **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi. L'oggetto **Player** è stato creato con ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





