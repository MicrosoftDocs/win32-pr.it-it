---
description: Questa classe è la classe del tipo di evento per gli eventi di scaricamento di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: DiskIo_TypeGroup3 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e421a8bd596869ac06af61f05ed1af8c633fb23b95e576398de6418620249c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050661"
---
# <a name="diskio_typegroup3-class"></a>Classe DiskIo \_ TypeGroup3

Questa classe è la classe del tipo di evento per gli eventi di scaricamento di I/O su disco.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Members

La **classe DiskIo \_ TypeGroup3** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DiskIo \_ TypeGroup3** ha queste proprietà.

<dl> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Numero che identifica il disco fisico.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Conteggio tick CPU dall'inizio dell'operazione alla fine dell'operazione.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacchetto di richiesta di I/O. Questa proprietà identifica l'attività di I/O.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Può contenere uno o più dei flag di pacchetto della richiesta di I/O seguenti (definiti in Ntddk.h, ovvero un file di intestazione DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOCACHE**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **IRP \_ PAGING \_ IO**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **COMPLETAMENTO \_ DEL MONTAGGIO IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **API \_ SINCRONA IRP \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **IRP \_ ASSOCIATO \_ A IRP**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **IRP \_ MEMORIZZATO NEL \_ BUFFER**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**BUFFER \_ DEALLOCATO IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **OPERAZIONE DI \_ INPUT \_ IRP**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **I/O \_ DI PAGING SINCRONO IRP \_ \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **OPERAZIONE DI \_ CREAZIONE \_ IRP**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**OPERAZIONE DI \_ LETTURA \_ IRP**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **OPERAZIONE DI \_ SCRITTURA \_ IRP**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **OPERAZIONE DI \_ CHIUSURA \_ IRP**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ DEFER \_ \_ I/O COMPLETAMENTO I/O**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Identificatore del thread emittente.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 e Windows Vista:** Questa proprietà non è supportata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




