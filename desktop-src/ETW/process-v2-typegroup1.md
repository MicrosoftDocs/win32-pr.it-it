---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Classe Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980407"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="668dd-104">\_ \_ Classe TypeGroup1 del processo V2</span><span class="sxs-lookup"><span data-stu-id="668dd-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="668dd-105">Questa classe è la classe del tipo di evento per gli eventi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="668dd-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="668dd-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="668dd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="668dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="668dd-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="668dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="668dd-108">Members</span></span>

<span data-ttu-id="668dd-109">La **classe \_ \_ TypeGroup1 del processo v2** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="668dd-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="668dd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="668dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="668dd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="668dd-111">Properties</span></span>

<span data-ttu-id="668dd-112">La classe **Process \_ v2 \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="668dd-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="668dd-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="668dd-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="668dd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-116">Qualificatori: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="668dd-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="668dd-117">Riga di comando completa del processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="668dd-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-119">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="668dd-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-121">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="668dd-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="668dd-122">Stato di uscita del processo interrotto.</span><span class="sxs-lookup"><span data-stu-id="668dd-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-123">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="668dd-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="668dd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-126">Qualificatori: WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="668dd-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="668dd-127">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="668dd-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="668dd-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-131">Qualificatori: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="668dd-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="668dd-132">Identificatore univoco del processo che crea questo processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="668dd-133">I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="668dd-134">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="668dd-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="668dd-135">È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="668dd-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="668dd-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-139">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="668dd-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="668dd-140">Identificatore di processo globale che è possibile utilizzare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="668dd-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="668dd-141">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="668dd-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="668dd-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="668dd-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-145">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="668dd-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="668dd-146">Identificatore univoco generato da un sistema operativo quando crea una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="668dd-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="668dd-147">Una sessione si estende a un periodo di tempo dall'accesso fino a quando non si disconnette da un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="668dd-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-148">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="668dd-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="668dd-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-151">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="668dd-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="668dd-152">Indirizzo dell'oggetto processo nel kernel.</span><span class="sxs-lookup"><span data-stu-id="668dd-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="668dd-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="668dd-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668dd-154">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="668dd-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="668dd-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="668dd-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668dd-156">Qualificatori: WmiDataId (6), Extension ("SID")</span><span class="sxs-lookup"><span data-stu-id="668dd-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="668dd-157">ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="668dd-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="668dd-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="668dd-158">Remarks</span></span>

<span data-ttu-id="668dd-159">I tipi di evento DCStart e DCEnd enumerano il processo attualmente in esecuzione, inclusi i processi inattivi e di sistema, nel momento in cui la sessione kernel inizia e termina, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="668dd-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="668dd-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="668dd-160">Requirements</span></span>



| <span data-ttu-id="668dd-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="668dd-161">Requirement</span></span> | <span data-ttu-id="668dd-162">Valore</span><span class="sxs-lookup"><span data-stu-id="668dd-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="668dd-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="668dd-163">Minimum supported client</span></span><br/> | <span data-ttu-id="668dd-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="668dd-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="668dd-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="668dd-165">Minimum supported server</span></span><br/> | <span data-ttu-id="668dd-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="668dd-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="668dd-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="668dd-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668dd-168">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="668dd-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




