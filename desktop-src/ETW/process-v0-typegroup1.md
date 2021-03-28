---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Classe Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977703"
---
# <a name="process_v0_typegroup1-class"></a>\_ \_ Classe TypeGroup1 del processo V0

Questa classe è la classe del tipo di evento per gli eventi di elaborazione.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Members

La classe **Process \_ V0 \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Process \_ V0 \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), StringTermination ("NullTerminated")
</dt> </dl>

Percorso del file eseguibile del processo.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Identificatore univoco del processo di creazione di un processo. I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo. È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Identificatore di processo globale che è possibile utilizzare per identificare un processo. Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Extension ("SID")
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

[**Processo \_ V0**](process-v0.md)
</dt> </dl>

 

 




