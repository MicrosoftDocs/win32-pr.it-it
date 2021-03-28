---
description: Questa classe è la classe del tipo di evento per gli eventi di scaricamento I/O del disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: Classe DiskIo_TypeGroup3
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
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977146"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="24313-104">\_Classe DiskIo TypeGroup3</span><span class="sxs-lookup"><span data-stu-id="24313-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="24313-105">Questa classe è la classe del tipo di evento per gli eventi di scaricamento I/O del disco.</span><span class="sxs-lookup"><span data-stu-id="24313-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="24313-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="24313-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="24313-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24313-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="24313-108">Members</span><span class="sxs-lookup"><span data-stu-id="24313-108">Members</span></span>

<span data-ttu-id="24313-109">La **classe \_ TypeGroup3 di DiskIo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="24313-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="24313-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="24313-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24313-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="24313-111">Properties</span></span>

<span data-ttu-id="24313-112">La **classe \_ TypeGroup3 di DiskIo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="24313-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24313-113">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="24313-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24313-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24313-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24313-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="24313-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24313-116">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="24313-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="24313-117">Numero che identifica il disco fisico.</span><span class="sxs-lookup"><span data-stu-id="24313-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="24313-118">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="24313-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24313-119">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="24313-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24313-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="24313-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24313-121">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="24313-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="24313-122">Numero di cicli della CPU dall'inizio dell'operazione alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="24313-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="24313-123">**IRP**</span><span class="sxs-lookup"><span data-stu-id="24313-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24313-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24313-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24313-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="24313-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24313-126">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**puntatore**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="24313-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="24313-127">Pacchetto della richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="24313-127">I/O request packet.</span></span> <span data-ttu-id="24313-128">Questa proprietà identifica l'attività di I/O.</span><span class="sxs-lookup"><span data-stu-id="24313-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="24313-129">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="24313-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24313-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24313-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24313-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="24313-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24313-132">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="24313-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="24313-133">Può contenere uno o più dei seguenti flag di pacchetti di richieste di I/O (definiti in ntddk. h, ovvero un file di intestazione DDK):</span><span class="sxs-lookup"><span data-stu-id="24313-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="24313-134">**NoCache IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="24313-135">**\_io paging \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="24313-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="24313-136">**\_completamento montaggio \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="24313-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="24313-137">**\_API sincrona IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="24313-138">**\_IRP associato a IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="24313-139">**\_io memorizzato nel buffer IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="24313-140">**\_buffer di DEallocazione IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="24313-141">**\_operazione di input IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="24313-142">**\_io paging sincrono IRP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="24313-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="24313-143">**\_operazione di creazione IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="24313-144">**\_operazione di lettura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="24313-145">**\_operazione di scrittura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="24313-146">**\_operazione di chiusura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="24313-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="24313-147">**completamento i/o \_ posticipato IRP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="24313-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="24313-148">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="24313-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24313-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24313-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24313-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="24313-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24313-151">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="24313-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="24313-152">Identificatore del thread emittente.</span><span class="sxs-lookup"><span data-stu-id="24313-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="24313-153">**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="24313-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24313-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24313-154">Requirements</span></span>



| <span data-ttu-id="24313-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="24313-155">Requirement</span></span> | <span data-ttu-id="24313-156">Valore</span><span class="sxs-lookup"><span data-stu-id="24313-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24313-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24313-157">Minimum supported client</span></span><br/> | <span data-ttu-id="24313-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24313-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24313-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24313-159">Minimum supported server</span></span><br/> | <span data-ttu-id="24313-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24313-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24313-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24313-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24313-162">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="24313-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




