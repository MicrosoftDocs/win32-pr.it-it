---
description: 'Process_V0_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi di processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 524d3c7da9f8ff76608da120834c5365eb1deb41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106359"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="6c2b6-104">Elaborare \_ la classe \_ TypeGroup1 V0</span><span class="sxs-lookup"><span data-stu-id="6c2b6-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="6c2b6-105">Questa classe è la classe del tipo di evento per gli eventi del processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="6c2b6-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c2b6-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="6c2b6-108">Members</span><span class="sxs-lookup"><span data-stu-id="6c2b6-108">Members</span></span>

<span data-ttu-id="6c2b6-109">La **classe \_ \_ TypeGroup1 Process V0** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6c2b6-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6c2b6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c2b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c2b6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c2b6-111">Properties</span></span>

<span data-ttu-id="6c2b6-112">La **classe \_ \_ TypeGroup1 Process V0** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c2b6-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="6c2b6-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2b6-114">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="6c2b6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2b6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-116">Qualificatori: WmiDataId(4), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="6c2b6-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="6c2b6-117">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="6c2b6-118">Parentid</span><span class="sxs-lookup"><span data-stu-id="6c2b6-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2b6-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c2b6-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2b6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-121">Qualificatori: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="6c2b6-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6c2b6-122">Identificatore univoco del processo che crea un processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="6c2b6-123">I numeri di identificatore di processo vengono riutilizzati, quindi identificano solo un processo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="6c2b6-124">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="6c2b6-125">È anche possibile che ParentProcessId faccia erroneamente riferimento a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6c2b6-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6c2b6-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2b6-127">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c2b6-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2b6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-129">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="6c2b6-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6c2b6-130">Identificatore di processo globale che è possibile usare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="6c2b6-131">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="6c2b6-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="6c2b6-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2b6-133">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="6c2b6-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2b6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2b6-135">Qualificatori: WmiDataId(3), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="6c2b6-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="6c2b6-136">Identificatore di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c2b6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c2b6-137">Requirements</span></span>



| <span data-ttu-id="6c2b6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c2b6-138">Requirement</span></span> | <span data-ttu-id="6c2b6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="6c2b6-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c2b6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c2b6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2b6-141">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6c2b6-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6c2b6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c2b6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2b6-143">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c2b6-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c2b6-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c2b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2b6-145">**Processo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="6c2b6-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




