---
description: Questa classe è la classe del tipo di evento per gli eventi di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: DiskIo_TypeGroup1 classe
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
ms.openlocfilehash: 3a69643602a59fa7be8cd844f3f2908c92e2e08545f7444d1002ec1542b36730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814977"
---
# <a name="diskio_typegroup1-class"></a>Classe DiskIo \_ TypeGroup1

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

La **classe DiskIo \_ TypeGroup1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DiskIo \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Offset di byte dall'inizio del disco fisico.

</dd> <dt>

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

**Oggetto FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Trovare la corrispondenza tra il valore di questo puntatore e il valore del puntatore **FileObject** in un [**evento FileIo \_ Name**](fileio-name.md) per determinare il file interessato dall'operazione di I/O.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Tempo tra l'avvio e il completamento dell'I/O misurato dal gestore partizioni (nelle unità tick [**KeQueryPerformanceCounter).**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter)

**Windows Server 2003:** Questa proprietà ha un [**valore WmiDataId**](event-tracing-mof-qualifiers.md) pari a 7.

**Windows 2000 Server e Windows 2000 Professional:** Questa proprietà non è supportata.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Puntatore**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacchetto di richiesta di I/O, che identifica l'attività di I/O.

**Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:** Questa proprietà non è supportata.

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

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Identificatore del thread emittente.

**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 con SP1, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:** Questa proprietà non è supportata.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Riservato.

**Windows Server 2008 R2, Windows Server 2008 e Windows 7:** Il nome della proprietà è **QueueDepth**, che contiene il conteggio dei tick della CPU dall'inizio dell'operazione alla fine dell'operazione. Si noti che questo valore può verificarsi un overflow.

**Windows Vista, Windows Server 2003 con SP1, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:** Il nome della proprietà è **ResponseTime**, che contiene il conteggio dei tick della CPU dall'inizio dell'operazione alla fine dell'operazione. Si noti che questo valore può verificarsi un overflow.

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Dimensioni in byte dei dati letti o scritti dal disco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Windows Server 2003 usa la definizione seguente per la classe di tipo di evento **\_ DiskIo TypeGroup1.**

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

La **proprietà ResponseTime** contiene il numero di tick della CPU dall'inizio dell'operazione alla fine dell'operazione. Si noti che questo valore può verificarsi un overflow.

La **proprietà HighResResponseTime** non è supportata.

Windows Server 2003 con SP1 e Windows Vista usa la definizione seguente per la classe di tipo di evento **\_ DiskIo TypeGroup1.**

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

La **proprietà Irp** è il pacchetto di richiesta di I/O. Questa proprietà identifica l'attività di I/O. È possibile usare questa proprietà con gli [**eventi DiskIo \_ TypeGroup2**](diskio-typegroup2.md) per correlare il tempo di risposta.

La **proprietà HighResResponseTime** è supportata. La proprietà contiene il tempo tra l'avvio e il completamento di I/O misurato da PartitionManager (nelle unità KeQueryPerformanceCounter). Usare questa proprietà anziché la **proprietà ResponseTime** per determinare il tempo di risposta di I/O su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 
