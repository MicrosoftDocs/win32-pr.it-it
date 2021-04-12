---
description: Segnala un evento di creazione di istanza, ovvero un tipo di evento intrinseco che viene generato quando una nuova istanza di viene aggiunta allo spazio dei nomi.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233479"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="49f48-103">\_\_Classe InstanceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="49f48-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="49f48-104">La classe di sistema **\_ \_ InstanceCreationEvent** segnala un evento di creazione di istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) che viene generato quando una nuova istanza viene aggiunta allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="49f48-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="49f48-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="49f48-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="49f48-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="49f48-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49f48-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="49f48-108">Members</span><span class="sxs-lookup"><span data-stu-id="49f48-108">Members</span></span>

<span data-ttu-id="49f48-109">La classe **\_ \_ InstanceCreationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="49f48-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="49f48-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49f48-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49f48-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49f48-111">Properties</span></span>

<span data-ttu-id="49f48-112">La classe **\_ \_ InstanceCreationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="49f48-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49f48-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="49f48-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f48-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="49f48-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="49f48-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="49f48-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f48-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="49f48-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="49f48-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="49f48-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f48-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="49f48-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f48-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="49f48-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="49f48-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="49f48-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f48-121">Copia dell'istanza di creata.</span><span class="sxs-lookup"><span data-stu-id="49f48-121">Copy of the instance that was created.</span></span> <span data-ttu-id="49f48-122">Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="49f48-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f48-123">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="49f48-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f48-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f48-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f48-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="49f48-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f48-126">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="49f48-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="49f48-127">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="49f48-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="49f48-128">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="49f48-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="49f48-129">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="49f48-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="49f48-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f48-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49f48-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="49f48-131">Remarks</span></span>

<span data-ttu-id="49f48-132">La classe **\_ \_ InstanceCreationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="49f48-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="49f48-133">**Creazione di una risorsa: \_ \_ InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="49f48-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="49f48-134">Si supponga di essere interessati a ricevere una notifica se il blocco note viene eseguito in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="49f48-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="49f48-135">Quando viene eseguito il blocco note, viene creato un processo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="49f48-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="49f48-136">I processi possono essere gestiti tramite WMI e sono rappresentati dalla \_ classe di processo Win32.</span><span class="sxs-lookup"><span data-stu-id="49f48-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="49f48-137">Quando viene avviata l'esecuzione del blocco note, un'istanza corrispondente della \_ classe di processo Win32 diventa disponibile tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="49f48-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="49f48-138">Se l'interesse è stato registrato in questo evento (eseguendo la query di notifica degli eventi appropriata), la disponibilità di questa istanza comporta la creazione di un'istanza della classe **\_ \_ InstanceCreationEvent** .</span><span class="sxs-lookup"><span data-stu-id="49f48-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="49f48-139">Per le query di notifica che richiedono la notifica della creazione di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="49f48-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="49f48-140">Per una descrizione più approfondita dell'uso di **\_ \_ InstanceCreationEvent** come metodo per il monitoraggio dei file System, vedere [WMI e monitoraggio del file System](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) in CodeProject.</span><span class="sxs-lookup"><span data-stu-id="49f48-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="49f48-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="49f48-141">Examples</span></span>

<span data-ttu-id="49f48-142">Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ InstanceCreationEvent** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="49f48-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="49f48-143">L'esempio PowerShell per [gli eventi permanenti WMI di PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) nella raccolta TechNet USA **\_ \_ InstanceCreationEvent** come parte di uno script di dimostrazione per la configurazione di una registrazione di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="49f48-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="49f48-144">L'esempio di [monitoraggio del processo di creazione dell'evento](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript in TechNet utilizza **\_ \_ InstanceCreationEvent** per monitorare il primo evento di creazione dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="49f48-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="49f48-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49f48-145">Requirements</span></span>



| <span data-ttu-id="49f48-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f48-146">Requirement</span></span> | <span data-ttu-id="49f48-147">Valore</span><span class="sxs-lookup"><span data-stu-id="49f48-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="49f48-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49f48-148">Minimum supported client</span></span><br/> | <span data-ttu-id="49f48-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49f48-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="49f48-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49f48-150">Minimum supported server</span></span><br/> | <span data-ttu-id="49f48-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49f48-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="49f48-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49f48-152">Namespace</span></span><br/>                | <span data-ttu-id="49f48-153">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="49f48-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="49f48-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49f48-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f48-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="49f48-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="49f48-156">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="49f48-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

