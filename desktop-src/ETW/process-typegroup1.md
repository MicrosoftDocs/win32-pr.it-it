---
description: 'Process_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b1a172b7c3c09ca5735e9e58da2003fcb3790f584cda5809e393ae721393e6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070031"
---
# <a name="process_typegroup1-class"></a>Classe \_ TypeGroup1 del processo

Questa classe è la classe del tipo di evento per gli eventi del processo.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Members

La **classe \_ Process TypeGroup1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup1** del processo ha queste proprietà.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(9), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Riga di comando completa del processo.

</dd> <dt>

DirectoryTableBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6), Puntatore
</dt> </dl>

Indirizzo fisico della tabella di pagine del processo.

</dd> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5)
</dt> </dl>

Stato di uscita del processo arrestato.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8), StringTermination("NullTerminated")
</dt> </dl>

Percorso del file eseguibile del processo.

</dd> <dt>

Parentid
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Format("x")
</dt> </dl>

Identificatore univoco del processo che crea questo processo. I numeri di identificatore del processo vengono riutilizzati, quindi identificano un processo solo per la durata del processo. È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che ParentProcessId faccia erroneamente riferimento a un processo che riutilizza un identificatore di processo.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Format("x")
</dt> </dl>

Identificatore di processo globale che è possibile usare per identificare un processo. Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

Identificatore univoco generato da un sistema operativo quando crea una nuova sessione. Una sessione si estende per un periodo di tempo dall'accesso fino alla disconnessione da un sistema specifico.

</dd> <dt>

UniqueProcessKey
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Indirizzo dell'oggetto processo nel kernel.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7), Extension("Sid")
</dt> </dl>

Identificatore di sicurezza (SID) per il contesto utente in cui si verifica l'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

I tipi di evento DCStart e DCEnd enumerano il processo attualmente in esecuzione, inclusi i processi inattivi e di sistema, rispettivamente al momento dell'avvio e della fine della sessione del kernel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo**](process.md)
</dt> </dl>

 

 




