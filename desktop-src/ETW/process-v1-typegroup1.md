---
description: 'Process_V1_TypeGroup1 classe : questa classe è la classe del tipo di evento per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106329"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="f9bf9-104">Elaborare \_ la classe \_ TypeGroup1 V1</span><span class="sxs-lookup"><span data-stu-id="f9bf9-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="f9bf9-105">Questa classe è la classe del tipo di evento per gli eventi del processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="f9bf9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9bf9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9bf9-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="f9bf9-108">Members</span><span class="sxs-lookup"><span data-stu-id="f9bf9-108">Members</span></span>

<span data-ttu-id="f9bf9-109">La **classe \_ \_ TypeGroup1 Process V1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f9bf9-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f9bf9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9bf9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9bf9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9bf9-111">Properties</span></span>

<span data-ttu-id="f9bf9-112">La **classe \_ \_ TypeGroup1 Process V1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9bf9-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="f9bf9-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-114">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-116">Qualificatori: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="f9bf9-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-117">Stato di uscita del processo arrestato.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="f9bf9-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-119">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-121">Qualificatori: WmiDataId(7), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="f9bf9-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-122">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="f9bf9-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-126">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="f9bf9-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-128">Parentid</span><span class="sxs-lookup"><span data-stu-id="f9bf9-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-129">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-131">Qualificatori: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="f9bf9-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-132">Identificatore univoco del processo che crea questo processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="f9bf9-133">I numeri di identificatore del processo vengono riutilizzati, quindi identificano un processo solo per la durata del processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="f9bf9-134">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="f9bf9-135">È anche possibile che ParentProcessId faccia erroneamente riferimento a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="f9bf9-136">**Windows Server 2003:** Include il qualificatore Format("x").</span><span class="sxs-lookup"><span data-stu-id="f9bf9-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="f9bf9-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-138">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-140">Qualificatori: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="f9bf9-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-141">Identificatore di processo globale che è possibile usare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="f9bf9-142">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="f9bf9-143">**Windows Server 2003:** Include il qualificatore Format("x").</span><span class="sxs-lookup"><span data-stu-id="f9bf9-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="f9bf9-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-145">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-147">Qualificatori: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="f9bf9-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-148">Identificatore univoco generato da un sistema operativo quando crea una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="f9bf9-149">Una sessione si estende per un periodo di tempo dall'accesso fino alla disconnessione da un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="f9bf9-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="f9bf9-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bf9-151">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9bf9-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bf9-153">Qualificatori: WmiDataId(6), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="f9bf9-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="f9bf9-154">Identificatore di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="f9bf9-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9bf9-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9bf9-155">Requirements</span></span>



| <span data-ttu-id="f9bf9-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9bf9-156">Requirement</span></span> | <span data-ttu-id="f9bf9-157">Valore</span><span class="sxs-lookup"><span data-stu-id="f9bf9-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9bf9-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bf9-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bf9-159">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f9bf9-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f9bf9-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bf9-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bf9-161">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9bf9-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9bf9-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9bf9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bf9-163">**Processo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="f9bf9-164">**Processo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f9bf9-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




