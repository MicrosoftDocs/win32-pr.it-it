---
title: Controls.currentPositionTimecode
description: La proprietà currentPositionTimecode specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un time code predefinito. Questa proprietà supporta attualmente le time code SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls.currentPositionTimecode Windows Media Player
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
ms.openlocfilehash: 2dd0dcdf4c5337cf8dc447452ce9667c261a9c7ea4b11f98753a294bca20c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736541"
---
# <a name="controlscurrentpositiontimecode"></a>Controls.currentPositionTimecode

La **proprietà currentPositionTimecode** specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un time code predefinito. Questa proprietà supporta attualmente le time code SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

SMPTE time code un modo standard per identificare un singolo fotogramma video, utile per sincronizzare la riproduzione. Se un file multimediale digitale supporta SMPTE time code, Windows Media Player può recuperare le informazioni correnti sulla posizione del time code o cercare un fotogramma video identificato da un particolare time code **String**.

SMPTE time code un frame specifico in base al numero di ore, minuti, secondi e fotogrammi che lo separano da un frame di riferimento specifico designato come tempo zero. In genere l'intervallo di tempo zero è l'inizio del file e un particolare valore di time code SMPTE rappresenta il tempo trascorso dall'inizio del file.

Il time code **String** è nel formato \[  \] *hh*:*mm*:*ss*.*ff* dove \[ *range* \] rappresenta l'intervallo, *hh* rappresenta le ore, *mm* rappresenta i minuti, *ss* rappresenta i secondi e *ff* rappresenta i fotogrammi. Quando si specifica un valore usando **currentPositionTimecode,** è necessario includere tutte le otto cifre usando zeri come segnaposto.

\[ *L'identificatore* di intervallo corrisponde al \] membro **wRange** della struttura WINDOWS MEDIA FORMAT **WMT \_ TIMECODE \_ EXTENSION \_ DATA.** Per altre informazioni sugli intervalli time code, vedere l'SDK Windows Media Format.

La specifica e il recupero di **currentPositionTimecode** sono supportati solo per i file che contengono time code SMPTE.

## <a name="examples"></a>Esempio

L'esempio di codice seguente specifica **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi. **L'oggetto** Player è stato creato con ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





