---
description: Segnala un evento di eliminazione di un'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene eliminata dallo spazio dei nomi.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Classe __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315259"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="0b9f8-103">\_\_Classe InstanceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="0b9f8-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="0b9f8-104">La classe di sistema **\_ \_ InstanceDeletionEvent** segnala un evento di eliminazione di un'istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando un'istanza viene eliminata dallo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="0b9f8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b9f8-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b9f8-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="0b9f8-108">Members</span><span class="sxs-lookup"><span data-stu-id="0b9f8-108">Members</span></span>

<span data-ttu-id="0b9f8-109">La classe **\_ \_ InstanceDeletionEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b9f8-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="0b9f8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b9f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b9f8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b9f8-111">Properties</span></span>

<span data-ttu-id="0b9f8-112">La classe **\_ \_ InstanceDeletionEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b9f8-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9f8-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0b9f8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b9f8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b9f8-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="0b9f8-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b9f8-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9f8-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0b9f8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b9f8-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b9f8-121">Copia dell'istanza di eliminata.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="0b9f8-122">Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b9f8-123">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9f8-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b9f8-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b9f8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b9f8-126">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="0b9f8-127">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="0b9f8-128">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="0b9f8-129">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="0b9f8-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b9f8-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b9f8-131">Remarks</span></span>

<span data-ttu-id="0b9f8-132">La classe **\_ \_ InstanceDeletionEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="0b9f8-133">**Eliminazione di una risorsa: \_ \_ InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="0b9f8-134">Se si desidera garantire che un programma antivirus specifico continui a essere eseguito in un computer, è possibile scrivere uno script che monitora i processi nel computer per determinare se uno di essi viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="0b9f8-135">Per le query di notifica che richiedono la notifica dell'eliminazione di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="0b9f8-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="0b9f8-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b9f8-136">Examples</span></span>

<span data-ttu-id="0b9f8-137">Il codice di esempio di [monitoraggio dell'evento di eliminazione del processo](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript nella raccolta TechNet utilizza **\_ \_ InstanceDeletionEvent** per monitorare la prima occorrenza di un evento di eliminazione di un'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="0b9f8-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b9f8-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b9f8-138">Requirements</span></span>



| <span data-ttu-id="0b9f8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9f8-139">Requirement</span></span> | <span data-ttu-id="0b9f8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="0b9f8-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0b9f8-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b9f8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9f8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b9f8-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0b9f8-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b9f8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9f8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b9f8-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0b9f8-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b9f8-145">Namespace</span></span><br/>                | <span data-ttu-id="0b9f8-146">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="0b9f8-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0b9f8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b9f8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9f8-148">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="0b9f8-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="0b9f8-149">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="0b9f8-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

