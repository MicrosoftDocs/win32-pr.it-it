---
title: Proprietà currentPositionTimecode di IWMPControls3
description: La proprietà currentPositionTimecode Ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Finestra delle proprietà di currentPositionTimecode Media Player
- Proprietà di currentPositionTimecode Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332456"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Proprietà IWMPControls3:: currentPositionTimecode

La proprietà **currentPositionTimecode** Ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta il codice ora SMPTE.

## <a name="remarks"></a>Commenti

Il codice di ora SMPTE fornisce un modo standard per identificare un singolo frame video, utile per sincronizzare la riproduzione. Se un file multimediale digitale supporta il codice ora SMPTE, Windows Media Player possibile recuperare le informazioni sulla posizione del codice ora corrente o cercare un frame video identificato da un particolare codice temporale.

Il codice di ora SMPTE identifica un frame specifico per il numero di ore, minuti, secondi e frame che lo separa da un particolare frame di riferimento il frame designato come ora zero. In genere, il fotogramma ora zero è l'inizio del file e un determinato valore del codice ora SMPTE rappresenta il tempo trascorso dall'inizio del file.

Il codice temporale è nell'intervallo di formato \[  \] *HH*:*mm*:*SS*.*FF* con \[ *intervallo* \] che rappresenta l'intervallo, hh rappresenta le ore, *mm* rappresenta minuti, *SS* rappresenta i secondi e *FF* rappresenta i frame. Quando si imposta un valore per **currentPositionTimecode**, è necessario includere tutte e otto le cifre, usando zeri come segnaposto.

\[*intervallo* \] corrisponde al membro **Wrange** della struttura di **dati dell'estensione del \_ timecode \_ \_ WMT** del formato Windows Media. Per ulteriori informazioni sugli intervalli di codice temporali, vedere Windows Media Format SDK.

L'impostazione e il recupero di **currentPositionTimecode** sono supportati solo per i file che contengono informazioni sul codice ora SMPTE.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene specificato **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





