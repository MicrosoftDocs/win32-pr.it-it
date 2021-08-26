---
description: Questa classe è la classe del tipo di evento che contrassegna l'inizio degli eventi di lettura, scrittura e scaricamento di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2 classe
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
ms.openlocfilehash: 60c1f2be2e90ddb8b3d7a396bfa925f0b7e83181effe7fb8c947bd911133f441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963141"
---
# <a name="diskio_typegroup2-class"></a>Classe \_ TypeGroup2 DiskIo

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

La **classe \_ DiskIo TypeGroup2** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup2 DiskIo** ha queste proprietà.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacchetto di richiesta di I/O. Questa proprietà identifica l'attività di I/O.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Identificatore del thread emittente.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 e Windows Vista:** Questa proprietà non è supportata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




