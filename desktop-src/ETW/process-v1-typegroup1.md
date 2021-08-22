---
description: 'Process_V1_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1 classe
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
ms.openlocfilehash: cd2b4ab072b04246351ede86027536d777bce3c7e2321260be4d0622f55663d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070001"
---
# <a name="process_v1_typegroup1-class"></a>Elaborare \_ la classe \_ TypeGroup1 V1

Questa classe è la classe del tipo di evento per gli eventi del processo.

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

La **classe \_ \_ TypeGroup1 Process V1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ TypeGroup1 Process V1** ha queste proprietà.

<dl> <dt>

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

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7), StringTermination("NullTerminated")
</dt> </dl>

Percorso del file eseguibile del processo.

</dd> <dt>

PageDirectoryBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Riservato.

</dd> <dt>

Parentid
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Identificatore univoco del processo che crea il processo. I numeri di identificatore di processo vengono riutilizzati, quindi identificano solo un processo per la durata di tale processo. È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che ParentProcessId faccia erroneamente riferimento a un processo che riutilizza un identificatore di processo.

**Windows Server 2003:** Include il qualificatore Format("x").

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Identificatore di processo globale che è possibile usare per identificare un processo. Il valore è valido dal momento in cui viene creato un processo fino a quando non viene terminato.

**Windows Server 2003:** Include il qualificatore Format("x").

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

UserSID
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6), Extension("Sid")
</dt> </dl>

ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ V1**](process.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> </dl>

 

 




