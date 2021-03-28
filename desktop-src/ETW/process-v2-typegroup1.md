---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Classe Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980407"
---
# <a name="process_v2_typegroup1-class"></a>\_ \_ Classe TypeGroup1 del processo V2

Questa classe è la classe del tipo di evento per gli eventi di elaborazione.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Members

La **classe \_ \_ TypeGroup1 del processo v2** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Process \_ v2 \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Riga di comando completa del processo.

</dd> <dt>

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

ParentId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Format ("x")
</dt> </dl>

Identificatore univoco del processo che crea questo processo. I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo. È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Identificatore di processo globale che è possibile utilizzare per identificare un processo. Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.

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

UniqueProcessKey
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo dell'oggetto processo nel kernel.

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

## <a name="remarks"></a>Commenti

I tipi di evento DCStart e DCEnd enumerano il processo attualmente in esecuzione, inclusi i processi inattivi e di sistema, nel momento in cui la sessione kernel inizia e termina, rispettivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ v2**](process-v2.md)
</dt> </dl>

 

 




