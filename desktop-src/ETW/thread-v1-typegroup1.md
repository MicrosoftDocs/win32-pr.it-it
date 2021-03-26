---
description: Questa classe è la classe del tipo di evento per gli eventi di avvio del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Classe Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967741"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="4db48-104">\_Classe thread V1 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="4db48-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="4db48-105">Questa classe è la classe del tipo di evento per gli eventi di avvio del thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="4db48-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4db48-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4db48-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="4db48-108">Members</span><span class="sxs-lookup"><span data-stu-id="4db48-108">Members</span></span>

<span data-ttu-id="4db48-109">I tipi di membri della classe **thread \_ V1 \_ TypeGroup1** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4db48-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4db48-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4db48-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4db48-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4db48-111">Properties</span></span>

<span data-ttu-id="4db48-112">La classe **thread \_ V1 \_ TypeGroup1** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4db48-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4db48-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="4db48-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-116">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4db48-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4db48-117">Identificatore del processo del thread che interessano l'evento.</span><span class="sxs-lookup"><span data-stu-id="4db48-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="4db48-118">**Windows Server 2003:** Contiene il qualificatore di formato ("x").</span><span class="sxs-lookup"><span data-stu-id="4db48-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="4db48-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-122">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-123">Indirizzo di base dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="4db48-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-127">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-128">Limite dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-129">StartAddr</span><span class="sxs-lookup"><span data-stu-id="4db48-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-132">Qualificatori: WmiDataId (7), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-133">Indirizzo di memoria in cui viene avviata la traccia.</span><span class="sxs-lookup"><span data-stu-id="4db48-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-134">TThreadId</span><span class="sxs-lookup"><span data-stu-id="4db48-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-137">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4db48-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4db48-138">Identificatore del thread associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="4db48-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="4db48-139">**Windows Server 2003:** Contiene il qualificatore di formato ("x").</span><span class="sxs-lookup"><span data-stu-id="4db48-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-140">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="4db48-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-143">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-144">Indirizzo di base dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-145">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="4db48-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-148">Qualificatori: WmiDataId (6), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-149">Limite dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-150">WaitMode</span><span class="sxs-lookup"><span data-stu-id="4db48-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-151">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="4db48-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-153">Qualificatori: WmiDataId (9), Format ("c")</span><span class="sxs-lookup"><span data-stu-id="4db48-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="4db48-154">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4db48-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="4db48-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db48-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db48-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db48-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4db48-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db48-158">Qualificatori: WmiDataId (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="4db48-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db48-159">Indirizzo iniziale della funzione che deve essere eseguita da questo thread.</span><span class="sxs-lookup"><span data-stu-id="4db48-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4db48-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4db48-160">Requirements</span></span>



| <span data-ttu-id="4db48-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db48-161">Requirement</span></span> | <span data-ttu-id="4db48-162">Valore</span><span class="sxs-lookup"><span data-stu-id="4db48-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4db48-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4db48-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4db48-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4db48-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4db48-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4db48-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4db48-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4db48-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4db48-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4db48-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db48-168">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4db48-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




