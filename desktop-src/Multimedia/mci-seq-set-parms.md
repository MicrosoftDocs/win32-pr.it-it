---
title: MCI_SEQ_SET_PARMS struttura (Mciapi.h)
description: La struttura MCI SEQ SET PARMS contiene informazioni per \_ \_ il comando \_ MCI SET per i dispositivi \_ sequencer MIDI.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffb96cfd2f652bf989673bad68c95c6765034d2105fa554efee057faf099a9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374969"
---
# <a name="mci_seq_set_parms-structure"></a>Struttura MCI \_ SEQ \_ SET \_ PARMS

La **struttura MCI \_ SEQ SET \_ \_ PARMS** contiene informazioni per il [**comando MCI \_ SET**](mci-set.md) per i dispositivi sequencer MIDI.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato dell'ora di Sequencer.

</dd> <dt>

**dwAudio**
</dt> <dd>

Canale di output audio.

</dd> <dt>

**dwTempo**
</dt> <dd>

Tempo.

</dd> <dt>

**dwPort**
</dt> <dd>

Porta.

</dd> <dt>

**dwAvare**
</dt> <dd>

Tipo di sincronizzazione utilizzato dal sequencer per l'operazione subordinata.

</dd> <dt>

**dwMaster**
</dt> <dd>

Tipo di sincronizzazione utilizzato dal sequencer per l'operazione master.

</dd> <dt>

**dwOffset**
</dt> <dd>

Offset dei dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

