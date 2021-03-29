---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Classe Process_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347841"
---
# <a name="process_v1_typegroup1-class"></a>Process \_ V1 \_ classe TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di elaborazione.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Members

La classe **Process \_ V1 \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Process \_ V1 \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Stato di uscita del processo interrotto.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), StringTermination ("NullTerminated")
</dt> </dl>

Percorso del file eseguibile del processo.

</dd> <dt>

PageDirectoryBase
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Riservato.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Identificatore univoco del processo che crea questo processo. I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo. È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.

**Windows Server 2003:** Include il qualificatore Format ("x").

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Identificatore di processo globale che è possibile utilizzare per identificare un processo. Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.

**Windows Server 2003:** Include il qualificatore Format ("x").

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Identificatore univoco generato da un sistema operativo quando crea una nuova sessione. Una sessione si estende a un periodo di tempo dall'accesso fino a quando non si disconnette da un sistema specifico.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6), Extension ("SID")
</dt> </dl>

ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ V1**](process.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> </dl>

 

 




