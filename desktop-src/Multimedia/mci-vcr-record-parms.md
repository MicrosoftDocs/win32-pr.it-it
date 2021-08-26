---
title: MCI_VCR_RECORD_PARMS struttura (Vcr.h)
description: La struttura MCI VCR RECORD PARMS contiene i parametri per \_ \_ il comando \_ MCI RECORD per i \_ registratori di videocassette.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b613c2b64bae1395b3fc402816145c0ef690801b9fd6402201198f7ff28a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038231"
---
# <a name="mci_vcr_record_parms-structure"></a>Struttura MCI \_ VCR \_ RECORD \_ PARMS

La **struttura MCI \_ VCR RECORD \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ RECORD**](mci-record.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

Valore temporale che influisce [**sul comando MCI \_ RECORD**](mci-record.md) [**o MCI \_ CUE.**](mci-cue.md) Per **MCI \_ RECORD,** si tratta dell'ora di inizio della registrazione. Per **MCI \_ CUE,** questo è il momento in cui il dispositivo cued raggiunge la posizione specificata in **dwFrom**.

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

[**MCI \_ RECORD**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

