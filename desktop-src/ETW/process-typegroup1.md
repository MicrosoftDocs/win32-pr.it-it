---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Classe Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ad2ebcd9a3e1563f6e2f4c82d90dd4d2c80112f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879701"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="f33c5-104">\_Classe Process TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="f33c5-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="f33c5-105">Questa classe è la classe del tipo di evento per gli eventi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f33c5-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="f33c5-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f33c5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f33c5-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="f33c5-108">Members</span><span class="sxs-lookup"><span data-stu-id="f33c5-108">Members</span></span>

<span data-ttu-id="f33c5-109">La classe **Process \_ TypeGroup1** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f33c5-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f33c5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f33c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f33c5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f33c5-111">Properties</span></span>

<span data-ttu-id="f33c5-112">La classe **Process \_ TypeGroup1** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f33c5-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f33c5-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="f33c5-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f33c5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-116">Qualificatori: WmiDataId (9), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="f33c5-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-117">Riga di comando completa del processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="f33c5-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-121">Qualificatori: WmiDataId (6), puntatore</span><span class="sxs-lookup"><span data-stu-id="f33c5-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-122">Indirizzo fisico della tabella della pagina del processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="f33c5-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-126">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="f33c5-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-127">Stato di uscita del processo interrotto.</span><span class="sxs-lookup"><span data-stu-id="f33c5-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="f33c5-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f33c5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-131">Qualificatori: WmiDataId (8), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="f33c5-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-132">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="f33c5-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-136">Qualificatori: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f33c5-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-137">Identificatore univoco del processo che crea questo processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="f33c5-138">I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="f33c5-139">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f33c5-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="f33c5-140">È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="f33c5-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-144">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f33c5-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-145">Identificatore di processo globale che è possibile utilizzare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="f33c5-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="f33c5-146">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="f33c5-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="f33c5-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-150">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="f33c5-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-151">Identificatore univoco generato da un sistema operativo quando crea una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="f33c5-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="f33c5-152">Una sessione si estende a un periodo di tempo dall'accesso fino a quando non si disconnette da un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="f33c5-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="f33c5-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33c5-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-156">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="f33c5-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-157">Indirizzo dell'oggetto processo nel kernel.</span><span class="sxs-lookup"><span data-stu-id="f33c5-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="f33c5-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="f33c5-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33c5-159">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="f33c5-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f33c5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33c5-161">Qualificatori: WmiDataId (7), estensione ("SID")</span><span class="sxs-lookup"><span data-stu-id="f33c5-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="f33c5-162">ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="f33c5-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f33c5-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="f33c5-163">Remarks</span></span>

<span data-ttu-id="f33c5-164">I tipi di evento DCStart e DCEnd enumerano il processo attualmente in esecuzione, inclusi i processi inattivi e di sistema, nel momento in cui la sessione kernel inizia e termina, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="f33c5-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33c5-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f33c5-165">Requirements</span></span>



| <span data-ttu-id="f33c5-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33c5-166">Requirement</span></span> | <span data-ttu-id="f33c5-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f33c5-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f33c5-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f33c5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f33c5-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f33c5-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f33c5-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f33c5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f33c5-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f33c5-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f33c5-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f33c5-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33c5-173">**Processo**</span><span class="sxs-lookup"><span data-stu-id="f33c5-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




