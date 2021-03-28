---
description: Questa classe è la classe del tipo di evento che contrassegna l'inizio degli eventi di lettura, scrittura e scaricamento di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Classe DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525261"
---
# <a name="diskio_typegroup2-class"></a>\_Classe DiskIo TypeGroup2

Questa classe è la classe del tipo di evento che contrassegna l'inizio degli eventi di lettura, scrittura e scaricamento di I/O su disco.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Members

La **classe \_ TypeGroup2 di DiskIo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup2 di DiskIo** dispone di queste proprietà.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacchetto della richiesta di I/O. Questa proprietà identifica l'attività IO.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Identificatore del thread emittente.

**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Questa proprietà non è supportata.

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

 

 




