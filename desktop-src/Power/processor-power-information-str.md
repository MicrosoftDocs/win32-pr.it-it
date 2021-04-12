---
description: Contiene informazioni su un processore.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Struttura PROCESSOR_POWER_INFORMATION
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
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345486"
---
# <a name="processor_power_information-structure"></a>\_ \_ Struttura delle informazioni sul risparmio di energia del processore

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

Numero di processori del sistema.

</dd> <dt>

**MaxMhz**
</dt> <dd>

Frequenza di clock massima specificata del processore di sistema, in megahertz.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Frequenza di clock del processore, in megahertz. Questo numero è la frequenza di clock del processore massima specificata moltiplicata per la limitazione del processore corrente.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Limite sulla frequenza di clock del processore, in megahertz. Questo numero è la frequenza di clock del processore massima specificata moltiplicata per il limite di limitazione termica del processore corrente.

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

 

 




