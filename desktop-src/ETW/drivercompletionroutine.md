---
description: Questa classe è la classe del tipo di evento per gli eventi di routine di driver completi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Classe DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878730"
---
# <a name="drivercompletionroutine-class"></a>Classe DriverCompletionRoutine

Questa classe è la classe del tipo di evento per gli eventi di routine di driver completi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La classe **DriverCompletionRoutine** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **DriverCompletionRoutine** dispone di queste proprietà.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Pacchetto di richiesta IO.

</dd> <dt>

**Routine**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo della funzione di driver chiamata.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Identificatore che identifica in modo univoco la richiesta. Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




