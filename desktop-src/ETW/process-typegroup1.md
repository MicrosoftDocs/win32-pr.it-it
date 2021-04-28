---
description: 'Process_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi di processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1 classe
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
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106379"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="2eb8b-104">Classe \_ TypeGroup1 del processo</span><span class="sxs-lookup"><span data-stu-id="2eb8b-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="2eb8b-105">Questa classe è la classe del tipo di evento per gli eventi del processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="2eb8b-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2eb8b-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2eb8b-108">Members</span><span class="sxs-lookup"><span data-stu-id="2eb8b-108">Members</span></span>

<span data-ttu-id="2eb8b-109">La **classe \_ Process TypeGroup1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2eb8b-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="2eb8b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2eb8b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2eb8b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2eb8b-111">Properties</span></span>

<span data-ttu-id="2eb8b-112">La **classe \_ Process TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2eb8b-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="2eb8b-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-114">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-116">Qualificatori: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="2eb8b-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-117">Riga di comando completa del processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="2eb8b-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-121">Qualificatori: WmiDataId(6), Pointer</span><span class="sxs-lookup"><span data-stu-id="2eb8b-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-122">Indirizzo fisico della tabella di pagine del processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="2eb8b-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-126">Qualificatori: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="2eb8b-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-127">Stato di uscita del processo arrestato.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="2eb8b-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-129">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-131">Qualificatori: WmiDataId(8), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="2eb8b-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-132">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-133">Parentid</span><span class="sxs-lookup"><span data-stu-id="2eb8b-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-136">Qualificatori: WmiDataId(3), Format("x")</span><span class="sxs-lookup"><span data-stu-id="2eb8b-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-137">Identificatore univoco del processo che crea questo processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="2eb8b-138">I numeri di identificatore del processo vengono riutilizzati, quindi identificano un processo solo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="2eb8b-139">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="2eb8b-140">È anche possibile che ParentProcessId faccia erroneamente riferimento a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="2eb8b-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-142">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-144">Qualificatori: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="2eb8b-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-145">Identificatore di processo globale che è possibile usare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="2eb8b-146">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="2eb8b-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-148">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-150">Qualificatori: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="2eb8b-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-151">Identificatore univoco generato da un sistema operativo quando crea una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="2eb8b-152">Una sessione si estende per un periodo di tempo dall'accesso fino alla disconnessione da un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="2eb8b-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-154">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-156">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="2eb8b-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-157">Indirizzo dell'oggetto processo nel kernel.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="2eb8b-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="2eb8b-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb8b-159">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eb8b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb8b-161">Qualificatori: WmiDataId(7), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="2eb8b-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="2eb8b-162">ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eb8b-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="2eb8b-163">Remarks</span></span>

<span data-ttu-id="2eb8b-164">I tipi di evento DCStart e DCEnd enumerano il processo attualmente in esecuzione, inclusi i processi inattivi e di sistema, rispettivamente al momento dell'avvio e della fine della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="2eb8b-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb8b-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2eb8b-165">Requirements</span></span>



| <span data-ttu-id="2eb8b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb8b-166">Requirement</span></span> | <span data-ttu-id="2eb8b-167">Valore</span><span class="sxs-lookup"><span data-stu-id="2eb8b-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2eb8b-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eb8b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb8b-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2eb8b-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2eb8b-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eb8b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb8b-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2eb8b-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2eb8b-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2eb8b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb8b-173">**Processo**</span><span class="sxs-lookup"><span data-stu-id="2eb8b-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




