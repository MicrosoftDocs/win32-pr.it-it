---
description: Contiene informazioni sull'inattività del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Struttura SYSTEM_POWER_INFORMATION
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
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967486"
---
# <a name="system_power_information-structure"></a>\_ \_ Struttura delle informazioni sull'alimentazione del sistema

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

L'inattività in cui il sistema viene considerato inattivo e il timeout di inattività inizia il conteggio, espresso come percentuale. Se si scende sotto questo numero, il timer verrà annullato.

</dd> <dt>

**Inattività**
</dt> <dd>

Il livello di inattività corrente, espresso come percentuale.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Tempo rimanente del timer di inattività, in secondi.

</dd> <dt>

**CoolingMode**
</dt> <dd>

Modalità di raffreddamento del sistema corrente. Questo membro deve avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Ordine di acquisto \_ TZ \_ attivo**</dt> <dt>0</dt> </dl>                    | Il sistema è attualmente in modalità di raffreddamento attiva.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Ordine di acquisto \_ TZ \_ \_ modalità non valida**</dt> <dt>2</dt> </dl> | Il sistema non supporta la limitazione della CPU oppure non è stata definita alcuna zona termica nel sistema.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Ordine di acquisto \_ TZ \_ passive**</dt> <dt>1</dt> </dl>                 | Il sistema è attualmente in modalità di raffreddamento passiva.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che questa definizione di struttura è stata accidentalmente omessa da WinNT. h. Questo errore verrà corretto in futuro. Nel frattempo, per compilare l'applicazione, includere la definizione della struttura contenuta in questo argomento nel codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




