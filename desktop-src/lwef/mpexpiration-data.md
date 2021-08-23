---
title: MPEXPIRATION_DATA (MpClient.h)
description: Notifica dello stato di scadenza del prodotto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA funzionalità dell'ambiente Windows legacy
- PMPEXPIRATION_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976031"
---
# <a name="mpexpiration_data-structure"></a>Struttura MPEXPIRATION \_ DATA

Notifica dello stato di scadenza del prodotto.

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

Tipo: **MP \_ EXPIRE \_ REASON**

</dd> <dd>

Motivo della scadenza. Si tratta di uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                                | Significato                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**Mp \_ EXPIRED \_ UNKNOWN**</dt> <dt>0</dt> </dl> | Sconosciuto.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**Mp \_ EXPIRED \_ EVAL**</dt> <dt>1</dt> </dl>          | Valutazione.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**Mp \_ \_WAT**</dt> <dt>2 SCADUTO</dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Tipo: **MP \_ EXPIRE \_ STATE \_ REPORT**

</dd> <dd>

Stato di scadenza. Si tratta di uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                                                                      | Significato                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**Mp \_ EXPIRE \_ STATE \_ REPORT \_ UNKNOWN**</dt> <dt>0</dt> </dl> | Stato sconosciuto.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**Mp \_ EXPIRE \_ STATE \_ REPORT \_ VALID**</dt> <dt>1</dt> </dl>       | Nessuna scadenza.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**Mp \_ EXPIRE \_ STATE \_ REPORT \_ WARNING**</dt> <dt>2</dt> </dl> | Quasi scaduto.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**Mp \_ EXPIRE \_ STATE \_ REPORT \_ EXPIRED**</dt> <dt>3</dt> </dl> | Scaduto.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





