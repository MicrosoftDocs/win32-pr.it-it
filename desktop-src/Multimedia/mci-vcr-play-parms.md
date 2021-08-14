---
title: MCI_VCR_PLAY_PARMS struttura (Vcr.h)
description: La struttura MCI VCR PLAY PARMS contiene i parametri per \_ \_ il comando \_ MCI PLAY per i \_ registratori di videocassette.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2e725ca3dc04fa13dd89aff0a5fbd60ede66f83154740803c98679eb77aec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374361"
---
# <a name="mci_vcr_play_parms-structure"></a>Struttura PARMS DI MCI \_ VCR \_ \_ PLAY

La **struttura MCI \_ VCR PLAY \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ PLAY**](mci-play.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui eseguire la riproduzione.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eseguire la riproduzione.

</dd> <dt>

**dwAt**
</dt> <dd>

Valore temporale che influisce [**sul comando MCI \_ PLAY**](mci-play.md) [**o MCI \_ CUE.**](mci-cue.md) Per [**MCI \_ PLAY,**](mci-play-parms.md)questo è il momento in cui inizia la riproduzione. Per **MCI \_ CUE,** questo è il momento in cui il dispositivo cued raggiunge la posizione specificata in **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le posizioni vengono specificate nel formato di ora corrente.

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

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

