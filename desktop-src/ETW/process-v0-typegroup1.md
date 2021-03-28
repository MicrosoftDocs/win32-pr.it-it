---
description: Questa classe è la classe del tipo di evento per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Classe Process_V0_TypeGroup1
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
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977703"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="9a5ef-104">\_ \_ Classe TypeGroup1 del processo V0</span><span class="sxs-lookup"><span data-stu-id="9a5ef-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="9a5ef-105">Questa classe è la classe del tipo di evento per gli eventi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="9a5ef-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5ef-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a5ef-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="9a5ef-108">Members</span><span class="sxs-lookup"><span data-stu-id="9a5ef-108">Members</span></span>

<span data-ttu-id="9a5ef-109">La classe **Process \_ V0 \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9a5ef-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="9a5ef-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9a5ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a5ef-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9a5ef-111">Properties</span></span>

<span data-ttu-id="9a5ef-112">La classe **Process \_ V0 \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a5ef-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="9a5ef-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a5ef-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9a5ef-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a5ef-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-116">Qualificatori: WmiDataId (4), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="9a5ef-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="9a5ef-117">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ef-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="9a5ef-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a5ef-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a5ef-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a5ef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-121">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="9a5ef-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9a5ef-122">Identificatore univoco del processo di creazione di un processo.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="9a5ef-123">I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="9a5ef-124">È possibile che il processo identificato da ParentProcessId venga terminato, quindi ParentProcessId potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="9a5ef-125">È anche possibile che ParentProcessId si riferisca erroneamente a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ef-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9a5ef-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a5ef-127">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a5ef-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a5ef-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-129">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="9a5ef-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9a5ef-130">Identificatore di processo globale che è possibile utilizzare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="9a5ef-131">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ef-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="9a5ef-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a5ef-133">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="9a5ef-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a5ef-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a5ef-135">Qualificatori: WmiDataId (3), Extension ("SID")</span><span class="sxs-lookup"><span data-stu-id="9a5ef-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="9a5ef-136">ID di sicurezza (SID) per il contesto utente in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="9a5ef-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a5ef-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a5ef-137">Requirements</span></span>



| <span data-ttu-id="9a5ef-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a5ef-138">Requirement</span></span> | <span data-ttu-id="9a5ef-139">Valore</span><span class="sxs-lookup"><span data-stu-id="9a5ef-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a5ef-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a5ef-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5ef-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9a5ef-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9a5ef-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a5ef-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5ef-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a5ef-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a5ef-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a5ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5ef-145">**Processo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="9a5ef-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




