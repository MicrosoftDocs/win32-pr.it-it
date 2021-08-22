---
description: Contiene informazioni sull'inattività del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143304"
---
# <a name="system_power_information-structure"></a>Struttura SYSTEM \_ POWER \_ INFORMATION

Contiene informazioni sull'inattività del sistema.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**MaxIdlenessAllowed**
</dt> <dd>

Inattività in cui il sistema viene considerato inattivo e inizia il conteggio del timeout di inattività, espresso come percentuale. Se si scende sotto questo numero, il timer viene annullato.

</dd> <dt>

**Inattività**
</dt> <dd>

Livello di inattività corrente, espresso come percentuale.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Tempo rimanente del timer di inattività, espresso in secondi.

</dd> <dt>

**CoolingMode**
</dt> <dd>

Modalità di raffreddamento del sistema corrente. Questo membro deve avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Ordine di acquisto \_ TZ \_ ACTIVE**</dt> <dt>0</dt> </dl>                    | Il sistema è attualmente in modalità di raffreddamento attivo.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Ordine di acquisto \_ MODALITÀ TZ \_ NON \_ VALIDA**</dt> <dt>2</dt> </dl> | Il sistema non supporta la limitazione della CPU o non esiste alcuna zona termica definita nel sistema.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Ordine di acquisto \_ TZ \_ PASSIVE**</dt> <dt>1</dt> </dl>                 | Il sistema è attualmente in modalità di raffreddamento passivo.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che questa definizione di struttura è stata accidentalmente omessa da WinNT.h. Questo errore verrà corretto in futuro. Nel frattempo, per compilare l'applicazione, includere la definizione della struttura contenuta in questo argomento nel codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




