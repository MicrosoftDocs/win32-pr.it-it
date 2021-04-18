---
title: Struttura MPEXPIRATION_DATA (MpClient. h)
description: Notifica sullo stato di scadenza del prodotto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- Struttura MPEXPIRATION_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPEXPIRATION_DATA
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301036"
---
# <a name="mpexpiration_data-structure"></a>\_Struttura dei dati MPEXPIRATION

Notifica sullo stato di scadenza del prodotto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Motivo**
</dt> <dd>

Tipo: **\_ \_ motivo scadenza MP**

</dd> <dd>

Motivo della scadenza. Si tratta di uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                                | Significato                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_ SCADUTO \_ sconosciuto**</dt> <dt>0</dt> </dl> | Sconosciuto.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_ Valutazione \_ scaduta**</dt> <dt>1</dt> </dl>          | Valutazione.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_ \_Wat**</dt> <dt>2</dt> scaduti </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Tipo: **\_ \_ \_ report stato di scadenza MP**

</dd> <dd>

Stato di scadenza. Si tratta di uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                                                                      | Significato                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_ \_Rapporto stato scadenza \_ \_ sconosciuto**</dt> <dt>0</dt> </dl> | Stato sconosciuto.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_ \_Rapporto stato scadenza \_ \_ valido**</dt> <dt>1</dt> </dl>       | Nessuna scadenza.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_ \_ \_ \_ Avviso rapporto di stato scadenza**</dt> <dt>2</dt> </dl> | Quasi scaduto.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_ Il \_ report sullo stato di scadenza è \_ \_ scaduto**</dt> <dt>3</dt> </dl> | Scaduto.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





