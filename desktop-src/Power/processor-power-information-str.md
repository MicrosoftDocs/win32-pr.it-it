---
description: Contiene informazioni su un processore.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3bdb6a3bb8ae5b768c42609817c76934c203989ba6dea665fc6cc0a6896659de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143334"
---
# <a name="processor_power_information-structure"></a>Struttura DELLE \_ INFORMAZIONI \_ SULL'ALIMENTAZIONE DEL PROCESSORE

Contiene informazioni su un processore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**Number**
</dt> <dd>

Numero del processore di sistema.

</dd> <dt>

**MaxMhz**
</dt> <dd>

Frequenza di clock massima specificata del processore di sistema, in megahertz.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Frequenza del clock del processore, in megahertz. Questo numero è la frequenza di clock massima specificata del processore moltiplicata per la limitazione del processore corrente.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Limite di frequenza del clock del processore, in megahertz. Questo numero è la frequenza di clock massima specificata del processore moltiplicata per il limite di velocità termica del processore corrente.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

Stato di inattività massimo del processore.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

Stato di inattività corrente del processore.

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

 

 




