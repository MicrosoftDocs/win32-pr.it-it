---
description: Questa classe è la classe del tipo di evento per gli eventi di errore di pagina hardware. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Classe PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967826"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="48b54-104">\_Classe pagefault HardFault</span><span class="sxs-lookup"><span data-stu-id="48b54-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="48b54-105">Questa classe è la classe del tipo di evento per gli eventi di errore di pagina hardware.</span><span class="sxs-lookup"><span data-stu-id="48b54-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="48b54-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="48b54-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b54-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48b54-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="48b54-108">Members</span><span class="sxs-lookup"><span data-stu-id="48b54-108">Members</span></span>

<span data-ttu-id="48b54-109">La **classe \_ HardFault di pagefault** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48b54-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="48b54-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48b54-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48b54-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48b54-111">Properties</span></span>

<span data-ttu-id="48b54-112">La **classe \_ HardFault di pagefault** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48b54-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48b54-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="48b54-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48b54-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-116">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="48b54-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="48b54-117">Quantità di dati letti da ReadOffset per soddisfare l'errore.</span><span class="sxs-lookup"><span data-stu-id="48b54-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="48b54-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="48b54-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48b54-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-121">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="48b54-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="48b54-122">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento del [**\_ nome**](fileio-name.md) di FileIO per determinare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="48b54-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="48b54-123">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="48b54-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="48b54-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-126">Qualificatori: WmiDataId (1), Extension ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="48b54-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="48b54-127">Timestamp di inizio in cui si è verificato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="48b54-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="48b54-128">**ReadOffset**</span><span class="sxs-lookup"><span data-stu-id="48b54-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48b54-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-131">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="48b54-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="48b54-132">Offset del file da cui sono stati letti i dati per soddisfare l'errore.</span><span class="sxs-lookup"><span data-stu-id="48b54-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="48b54-133">**TThreadId**</span><span class="sxs-lookup"><span data-stu-id="48b54-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48b54-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-136">Qualificatori: WmiDataId (5), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="48b54-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="48b54-137">Identificatore del thread che ha rilevato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="48b54-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="48b54-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="48b54-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48b54-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48b54-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48b54-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48b54-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48b54-141">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="48b54-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="48b54-142">Indirizzo di errore.</span><span class="sxs-lookup"><span data-stu-id="48b54-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48b54-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48b54-143">Requirements</span></span>



| <span data-ttu-id="48b54-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b54-144">Requirement</span></span> | <span data-ttu-id="48b54-145">Valore</span><span class="sxs-lookup"><span data-stu-id="48b54-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48b54-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48b54-146">Minimum supported client</span></span><br/> | <span data-ttu-id="48b54-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48b54-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48b54-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48b54-148">Minimum supported server</span></span><br/> | <span data-ttu-id="48b54-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48b54-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48b54-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48b54-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b54-151">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="48b54-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




