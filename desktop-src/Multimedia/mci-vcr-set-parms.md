---
title: MCI_VCR_SET_PARMS struttura (Vcr.h)
description: La struttura MCI VCR SET PARMS contiene i parametri per \_ \_ il comando \_ MCI SET per i \_ registratori di videocassette.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS struttura Windows Multimediali
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
ms.openlocfilehash: 9fe32f93500ae4c294bad372868e9f7818c672824611bcbc29c3315eb75a9742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802986"
---
# <a name="mci_vcr_set_parms-structure"></a>Struttura MCI \_ VCR \_ SET \_ PARMS

La **struttura MCI \_ VCR SET \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ SET**](mci-set.md) per i registratori di videocassette.

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

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

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

Costante che specifica l'origine di temporizzazione usata dal dispositivo. L'origine di temporizzazione è un codice di tempo registrato nella videotape o i contatori nel dispositivo che inserivano lo spostamento della videotape.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Frequenza di registrazione.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Formato di un nuovo valore di ora del contatore.

</dd> <dt>

**dwIndex**
</dt> <dd>

Contenuto della visualizzazione su schermo.

</dd> <dt>

**dwTracking**
</dt> <dd>

Regolazione della velocità usata per tenere traccia della velocità di riproduzione del videoregistratore.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocità di riproduzione usata dal dispositivo come numero intero. La velocità di riproduzione normale è 1000, la doppia velocità è 2000 e la metà velocità è 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Lunghezza della videotape quando la lunghezza non è rilevabile dal dispositivo.

</dd> <dt>

**dwCounter**
</dt> <dd>

Nuovo valore del contatore.

</dd> <dt>

**dwClock**
</dt> <dd>

Nuova ora dell'orologio.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Nuovo valore di timeout per il comando pause.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Lunghezza della videotape necessaria per stabilizzare l'output del videoregistratore.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Lunghezza della videotape necessaria per bloccare il trasporto del videoregistratore quando viene eseguito un comando [**MCI \_ STOP**](mci-stop.md) o [**MCI \_ PAUSE.**](mci-pause.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ PAUSE**](mci-pause.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**ARRESTO \_ MCI**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

