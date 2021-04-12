---
title: Struttura MCI_VCR_SET_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ set contiene i \_ parametri per il \_ comando set MCI per i registratori di nastri video.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Struttura MCI_VCR_SET_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400864"
---
# <a name="mci_vcr_set_parms-structure"></a>\_ \_ Struttura parametri set VCR MCI \_

La struttura **parametri di MCI \_ VCR \_ set \_** contiene i parametri per il comando [**\_ set MCI**](mci-set.md) per i registratori di nastri video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato dell'ora corrente.

</dd> <dt>

**dwAudio**
</dt> <dd>

Non usato.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Costante che specifica l'origine dell'intervallo utilizzata dal dispositivo. L'origine dell'intervallo è un timecode registrato in un nastro o i contatori nel dispositivo che rilevano lo spostamento del nastro.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Velocità di registrazione.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Formato di un nuovo valore di ora del contatore.

</dd> <dt>

**dwIndex**
</dt> <dd>

Contenuto della visualizzazione sullo schermo.

</dd> <dt>

**dwTracking**
</dt> <dd>

Regolazione della velocità utilizzata per tenere traccia della frequenza di riproduzione dei VCR.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocità di riproduzione usata dal dispositivo come numero intero. La velocità di riproduzione normale è 1000, la velocità doppia è 2000 e la metà della velocità è 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Lunghezza del nastro quando la lunghezza non è rilevabile dal dispositivo.

</dd> <dt>

**dwCounter**
</dt> <dd>

Nuovo valore del contatore.

</dd> <dt>

**dwClock**
</dt> <dd>

Nuova ora di clock.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Nuovo valore di timeout per il comando Sospendi.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Lunghezza del nastro necessaria per stabilizzare l'output del VCR.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Lunghezza del nastro necessaria per bloccare il trasporto VCR quando viene emesso un comando [**MCI \_ Stop**](mci-stop.md) o [**MCI \_ pause**](mci-pause.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_pausa MCI**](mci-pause.md)
</dt> <dt>

[**SET di MCI \_**](mci-set.md)
</dt> <dt>

[**\_arresto MCI**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

