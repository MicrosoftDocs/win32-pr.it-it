---
title: Proprietà currentPositionTimecode IWMPControls3
description: La proprietà currentPositionTimecode ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un time code predefinito. Questa proprietà supporta attualmente le time code SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Proprietà currentPositionTimecode Windows Media Player
- proprietà currentPositionTimecode Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player proprietà currentPositionTimecode
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
ms.openlocfilehash: b91c00c166050f4f3a3bc05861fa92d4fb66efcfa139e726c7cc799e21623fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760921"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Proprietà IWMPControls3::currentPositionTimecode

La **proprietà currentPositionTimecode** ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un time code predefinito. Questa proprietà supporta attualmente le time code SMPTE.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta l'oggetto SMPTE time code.

## <a name="remarks"></a>Commenti

SMPTE time code un modo standard per identificare un singolo fotogramma video, utile per sincronizzare la riproduzione. Se un file multimediale digitale supporta SMPTE time code, Windows Media Player può recuperare le informazioni correnti sulla posizione time code o cercare un fotogramma video identificato da un determinato time code.

SMPTE time code un frame specifico in base al numero di ore, minuti, secondi e fotogrammi che lo separano da un frame di riferimento specifico designato come tempo zero. In genere l'intervallo di tempo zero è l'inizio del file e un particolare valore di time code SMPTE rappresenta il tempo trascorso dall'inizio del file.

Il time code è nel formato \[  \] *hh*:*mm*:*ss*.*ff* dove \[ *range* \] rappresenta l'intervallo, hh rappresenta le ore, *mm* rappresenta i minuti, *ss* rappresenta i secondi e *ff* rappresenta i fotogrammi. Quando si imposta un valore per **currentPositionTimecode,** è necessario includere tutte le otto cifre, usando zeri come segnaposto.

\[*intervallo* \] corrisponde al membro **wRange** della struttura WINDOWS MEDIA FORMAT **WMT \_ TIMECODE \_ EXTENSION \_ DATA.** Per altre informazioni sugli intervalli time code, vedere l'SDK Windows Media Format.

L'impostazione e il **recupero di currentPositionTimecode** sono supportati solo per i file che contengono time code SMPTE.

## <a name="examples"></a>Esempio

L'esempio di codice seguente specifica **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





