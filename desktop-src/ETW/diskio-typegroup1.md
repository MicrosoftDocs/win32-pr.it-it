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
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="8f526-104">\_Classe DiskIo TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="8f526-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="8f526-105">Questa classe è la classe del tipo di evento per gli eventi di I/O su disco.</span><span class="sxs-lookup"><span data-stu-id="8f526-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="8f526-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="8f526-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f526-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f526-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="8f526-108">Members</span><span class="sxs-lookup"><span data-stu-id="8f526-108">Members</span></span>

<span data-ttu-id="8f526-109">La **classe \_ TypeGroup1 di DiskIo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8f526-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="8f526-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f526-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f526-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f526-111">Properties</span></span>

<span data-ttu-id="8f526-112">La **classe \_ TypeGroup1 di DiskIo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f526-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f526-113">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="8f526-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-114">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="8f526-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-116">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="8f526-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-117">Offset dei byte dall'inizio del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="8f526-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-118">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="8f526-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-121">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="8f526-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-122">Numero che identifica il disco fisico.</span><span class="sxs-lookup"><span data-stu-id="8f526-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="8f526-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-126">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**puntatore**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8f526-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-127">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento del [**\_ nome di FileIO**](fileio-name.md) per determinare il file richiesto nell'operazione di i/O.</span><span class="sxs-lookup"><span data-stu-id="8f526-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-128">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="8f526-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f526-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-131">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="8f526-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-132">Tempo che intercorre tra l'avvio e il completamento di I/O misurato da Gestione partizioni (nelle unità di misura [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="8f526-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="8f526-133">**Windows Server 2003:** Questa proprietà ha un valore [**WmiDataId**](event-tracing-mof-qualifiers.md) pari a 7.</span><span class="sxs-lookup"><span data-stu-id="8f526-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="8f526-134">**Windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f526-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-135">**IRP**</span><span class="sxs-lookup"><span data-stu-id="8f526-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-136">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-138">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**puntatore**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8f526-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-139">Pacchetto della richiesta di I/O, che identifica l'attività di I/O.</span><span class="sxs-lookup"><span data-stu-id="8f526-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="8f526-140">**Windows server 2003, windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f526-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-141">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="8f526-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-144">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="8f526-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="8f526-145">Può contenere uno o più dei seguenti flag di pacchetti di richieste di I/O (definiti in ntddk. h, ovvero un file di intestazione DDK):</span><span class="sxs-lookup"><span data-stu-id="8f526-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="8f526-146">**NoCache IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="8f526-147">**\_io paging \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="8f526-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="8f526-148">**\_completamento montaggio \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="8f526-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="8f526-149">**\_API sincrona IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="8f526-150">**\_IRP associato a IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="8f526-151">**\_io memorizzato nel buffer IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="8f526-152">**\_buffer di DEallocazione IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="8f526-153">**\_operazione di input IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="8f526-154">**\_io paging sincrono IRP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="8f526-155">**\_operazione di creazione IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="8f526-156">**\_operazione di lettura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="8f526-157">**\_operazione di scrittura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="8f526-158">**\_operazione di chiusura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="8f526-159">**completamento i/o \_ posticipato IRP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f526-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f526-160">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="8f526-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-163">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="8f526-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-164">Identificatore del thread emittente.</span><span class="sxs-lookup"><span data-stu-id="8f526-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="8f526-165">**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server e windows 2000 Professional:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f526-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8f526-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-169">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="8f526-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-170">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8f526-170">Reserved.</span></span>

<span data-ttu-id="8f526-171">**Windows server 2008 R2, Windows server 2008 e Windows 7:** Il nome della proprietà è **QueueDepth**, che contiene il numero di cicli della CPU dall'inizio dell'operazione fino alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8f526-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="8f526-172">Si noti che questo valore può essere overflow.</span><span class="sxs-lookup"><span data-stu-id="8f526-172">Note that this value can overflow.</span></span>

<span data-ttu-id="8f526-173">**Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server e windows 2000 Professional:** Il nome della proprietà è **ResponseTime**, che contiene il numero di cicli della CPU dall'inizio dell'operazione fino alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8f526-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="8f526-174">Si noti che questo valore può essere overflow.</span><span class="sxs-lookup"><span data-stu-id="8f526-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="8f526-175">**TransferSize**</span><span class="sxs-lookup"><span data-stu-id="8f526-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f526-176">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f526-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f526-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f526-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f526-178">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="8f526-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="8f526-179">Dimensioni in byte dei dati letti o scritti dal disco.</span><span class="sxs-lookup"><span data-stu-id="8f526-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f526-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f526-180">Remarks</span></span>

<span data-ttu-id="8f526-181">Windows Server 2003 utilizza la definizione seguente per la classe del tipo di evento **DiskIo \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="8f526-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="8f526-182">La proprietà **ResponseTime** contiene il numero di cicli della CPU dall'inizio dell'operazione alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8f526-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="8f526-183">Si noti che questo valore può essere overflow.</span><span class="sxs-lookup"><span data-stu-id="8f526-183">Note that this value can overflow.</span></span>

<span data-ttu-id="8f526-184">La proprietà **HighResResponseTime** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f526-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="8f526-185">Windows Server 2003 con SP1 e Windows Vista usa la definizione seguente per la classe del tipo di evento **DiskIo \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="8f526-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="8f526-186">La proprietà **IRP** è il pacchetto di richiesta di i/O.</span><span class="sxs-lookup"><span data-stu-id="8f526-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="8f526-187">Questa proprietà identifica l'attività di I/O.</span><span class="sxs-lookup"><span data-stu-id="8f526-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="8f526-188">È possibile usare questa proprietà con gli [**eventi \_ TypeGroup2 di DiskIo**](diskio-typegroup2.md) per correlare il tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="8f526-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="8f526-189">La proprietà **HighResResponseTime** è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f526-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="8f526-190">La proprietà contiene l'intervallo di tempo tra l'inizio e il completamento I/O misurato da PartitionManager (nelle unità KeQueryPerformanceCounter).</span><span class="sxs-lookup"><span data-stu-id="8f526-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="8f526-191">Utilizzare questa proprietà anziché la proprietà **ResponseTime** per determinare il tempo di risposta di i/O su disco.</span><span class="sxs-lookup"><span data-stu-id="8f526-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f526-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f526-192">Requirements</span></span>



| <span data-ttu-id="8f526-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f526-193">Requirement</span></span> | <span data-ttu-id="8f526-194">Valore</span><span class="sxs-lookup"><span data-stu-id="8f526-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8f526-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f526-195">Minimum supported client</span></span><br/> | <span data-ttu-id="8f526-196">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f526-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8f526-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f526-197">Minimum supported server</span></span><br/> | <span data-ttu-id="8f526-198">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f526-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8f526-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f526-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f526-200">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="8f526-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
