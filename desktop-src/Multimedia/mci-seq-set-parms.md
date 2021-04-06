---
title: Struttura MCI_SEQ_SET_PARMS (Mciapi. h)
description: La \_ struttura MCI seq \_ set \_ parametri contiene informazioni per il \_ comando set di MCI per i dispositivi MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Struttura MCI_SEQ_SET_PARMS di Windows Multimedia
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
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963876"
---
# <a name="mci_seq_set_parms-structure"></a>\_ \_ Struttura parametri della serie MCI seq \_

La struttura **MCI \_ seq \_ set \_ parametri** contiene informazioni per il comando [**\_ set di MCI**](mci-set.md) per i dispositivi MIDI Sequencer.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

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

**dwSlave**
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

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**SET di MCI \_**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

