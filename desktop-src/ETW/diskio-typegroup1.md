---
description: Questa classe è la classe del tipo di evento per gli eventi di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: Classe DiskIo_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526868"
---
# <a name="diskio_typegroup1-class"></a>\_Classe DiskIo TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di I/O su disco.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Members

La **classe \_ TypeGroup1 di DiskIo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup1 di DiskIo** dispone di queste proprietà.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Offset dei byte dall'inizio del disco fisico.

</dd> <dt>

**Numerodisco**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Numero che identifica il disco fisico.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento del [**\_ nome di FileIO**](fileio-name.md) per determinare il file richiesto nell'operazione di i/O.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Tempo che intercorre tra l'avvio e il completamento di I/O misurato da Gestione partizioni (nelle unità di misura [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003:** Questa proprietà ha un valore [**WmiDataId**](event-tracing-mof-qualifiers.md) pari a 7.

**Windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacchetto della richiesta di I/O, che identifica l'attività di I/O.

**Windows server 2003, windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Può contenere uno o più dei seguenti flag di pacchetti di richieste di I/O (definiti in ntddk. h, ovvero un file di intestazione DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **NoCache IRP \_**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **\_io paging \_ IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **\_completamento montaggio \_ IRP**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **\_API sincrona IRP \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP associato a IRP \_**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **\_io memorizzato nel buffer IRP \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**\_buffer di DEallocazione IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_operazione di input IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **\_io paging sincrono IRP \_ \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_operazione di creazione IRP \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_operazione di lettura IRP \_**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_operazione di scrittura IRP \_**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **\_operazione di chiusura IRP \_**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **completamento i/o \_ posticipato IRP \_ \_**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Identificatore del thread emittente.

**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Riservato.

**Windows server 2008 R2, Windows server 2008 e Windows 7:** Il nome della proprietà è **QueueDepth**, che contiene il numero di cicli della CPU dall'inizio dell'operazione fino alla fine dell'operazione. Si noti che questo valore può essere overflow.

**Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server e windows 2000 Professional:** Il nome della proprietà è **ResponseTime**, che contiene il numero di cicli della CPU dall'inizio dell'operazione fino alla fine dell'operazione. Si noti che questo valore può essere overflow.

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Dimensioni in byte dei dati letti o scritti dal disco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Windows Server 2003 utilizza la definizione seguente per la classe del tipo di evento **DiskIo \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

La proprietà **ResponseTime** contiene il numero di cicli della CPU dall'inizio dell'operazione alla fine dell'operazione. Si noti che questo valore può essere overflow.

La proprietà **HighResResponseTime** non è supportata.

Windows Server 2003 con SP1 e Windows Vista usa la definizione seguente per la classe del tipo di evento **DiskIo \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

La proprietà **IRP** è il pacchetto di richiesta di i/O. Questa proprietà identifica l'attività di I/O. È possibile usare questa proprietà con gli [**eventi \_ TypeGroup2 di DiskIo**](diskio-typegroup2.md) per correlare il tempo di risposta.

La proprietà **HighResResponseTime** è supportata. La proprietà contiene l'intervallo di tempo tra l'inizio e il completamento I/O misurato da PartitionManager (nelle unità KeQueryPerformanceCounter). Utilizzare questa proprietà anziché la proprietà **ResponseTime** per determinare il tempo di risposta di i/O su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 
