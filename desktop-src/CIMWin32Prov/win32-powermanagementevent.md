---
description: Win32 \_ PowerManagementEvent &\# 32; Classe WMI che rappresenta gli eventi di risparmio energia derivanti da modifiche allo stato di alimentazione.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Classe Win32_PowerManagementEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126840"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="ca66f-103">Win32 \_ PowerManagementEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="ca66f-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="ca66f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent Win32** rappresenta eventi di risparmio energia derivanti da modifiche allo stato di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="ca66f-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="ca66f-105">Queste modifiche di stato sono associate a Advanced Power Management (APM) o ai protocolli di gestione del sistema ACPI (Advanced Configuration and Power Interface).</span><span class="sxs-lookup"><span data-stu-id="ca66f-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="ca66f-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ca66f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ca66f-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ca66f-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca66f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca66f-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="ca66f-109">Members</span><span class="sxs-lookup"><span data-stu-id="ca66f-109">Members</span></span>

<span data-ttu-id="ca66f-110">La classe **Win32 \_ PowerManagementEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca66f-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ca66f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca66f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca66f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca66f-112">Properties</span></span>

<span data-ttu-id="ca66f-113">La classe **Win32 \_ PowerManagementEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca66f-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca66f-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="ca66f-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca66f-115">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca66f-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca66f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-117">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventi di risparmio \| energia Win32API")</span><span class="sxs-lookup"><span data-stu-id="ca66f-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="ca66f-118">Tipo di modifica nello stato di alimentazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="ca66f-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="ca66f-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Immissione della sospensione** (4)</span><span class="sxs-lookup"><span data-stu-id="ca66f-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ca66f-120">Durante la sospensione, il computer sembra spento; Tuttavia, può essere riattivato in risposta a vari eventi, incluso l'input dell'utente, ad esempio lo spostamento del mouse o la pressione di un tasto sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="ca66f-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="ca66f-121">Quando il computer viene sospeso, il consumo di energia viene ridotto a uno dei diversi livelli, a seconda della modalità di utilizzo del sistema.</span><span class="sxs-lookup"><span data-stu-id="ca66f-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="ca66f-122">Minore è il livello di consumo energetico, maggiore è il tempo necessario al sistema per tornare allo stato di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ca66f-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="ca66f-123">Quando il computer entra nello stato Suspend, il desktop è bloccato ed è necessario premere CTRL + ALT + CANC e specificare un nome utente e una password validi per riprendere le operazioni</span><span class="sxs-lookup"><span data-stu-id="ca66f-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="ca66f-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Riprendi da Sospendi** (7)</span><span class="sxs-lookup"><span data-stu-id="ca66f-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ca66f-125">Indica che è stato inviato un messaggio di ripresa da Suspend, che consente al computer di tornare allo stato di alimentazione normale.</span><span class="sxs-lookup"><span data-stu-id="ca66f-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="ca66f-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Modifica dello stato di alimentazione** (10)</span><span class="sxs-lookup"><span data-stu-id="ca66f-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="ca66f-127">Indica una modifica dello stato di alimentazione del computer, ad esempio un passaggio dall'alimentazione a batteria ad AC o da AC a un alimentatore di continuità.</span><span class="sxs-lookup"><span data-stu-id="ca66f-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="ca66f-128">Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.</span><span class="sxs-lookup"><span data-stu-id="ca66f-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="ca66f-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)</span><span class="sxs-lookup"><span data-stu-id="ca66f-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="ca66f-130">Indica che un BIOS di Advanced Power Management (APM) ha inviato un evento OEM.</span><span class="sxs-lookup"><span data-stu-id="ca66f-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="ca66f-131">Il valore dell'evento verrà acquisito nella proprietà **OEMEventCode** .</span><span class="sxs-lookup"><span data-stu-id="ca66f-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="ca66f-132">Poiché alcune implementazioni del BIOS APM non forniscono notifiche degli eventi OEM, questo evento potrebbe non essere mai trasmesso in alcuni computer.</span><span class="sxs-lookup"><span data-stu-id="ca66f-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="ca66f-133">APM è uno schema di risparmio energia legacy.</span><span class="sxs-lookup"><span data-stu-id="ca66f-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="ca66f-134">Anche se ancora supportata, APM è stato ampiamente sostituito da ACPI (Advanced Configuration and Power Interface).</span><span class="sxs-lookup"><span data-stu-id="ca66f-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="ca66f-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Riprendi automaticamente** (18)</span><span class="sxs-lookup"><span data-stu-id="ca66f-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ca66f-136">Indica che il computer è stato riattivato in risposta a un evento.</span><span class="sxs-lookup"><span data-stu-id="ca66f-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="ca66f-137">Se il sistema rileva l'attività dell'utente (ad esempio un clic del mouse), il messaggio ResumeSuspend verrà trasmesso, consentendo alle applicazioni di tenere presente che è possibile riprendere l'interattività completa con l'utente.</span><span class="sxs-lookup"><span data-stu-id="ca66f-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca66f-138">**OEMEventCode**</span><span class="sxs-lookup"><span data-stu-id="ca66f-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca66f-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca66f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca66f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-141">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventi di risparmio \| energia Win32API")</span><span class="sxs-lookup"><span data-stu-id="ca66f-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="ca66f-142">Stato di alimentazione del sistema definito dall'OEM (Original Equipment Manufacturer) quando la proprietà **eventType** di questa classe è impostata su 11 (evento OEM); in caso contrario, questa proprietà è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="ca66f-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="ca66f-143">Gli eventi OEM vengono generati quando un BIOS APM segnala un evento APM OEM.</span><span class="sxs-lookup"><span data-stu-id="ca66f-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="ca66f-144">I codici evento OEM sono compresi nell'intervallo 0x0200h-0x02FFh.</span><span class="sxs-lookup"><span data-stu-id="ca66f-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="ca66f-145">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="ca66f-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca66f-146">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ca66f-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca66f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca66f-148">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="ca66f-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ca66f-149">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="ca66f-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="ca66f-150">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ca66f-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca66f-151">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="ca66f-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca66f-152">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca66f-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca66f-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca66f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca66f-154">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ca66f-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ca66f-155">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="ca66f-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ca66f-156">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ca66f-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="ca66f-157">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="ca66f-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="ca66f-158">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ca66f-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca66f-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca66f-159">Remarks</span></span>

<span data-ttu-id="ca66f-160">La classe **Win32 \_ PowerManagementEvent** deriva da [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="ca66f-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="ca66f-161">Le modifiche allo stato di alimentazione spesso indicano che si è verificato un problema con un computer o con un altro dispositivo gestito.</span><span class="sxs-lookup"><span data-stu-id="ca66f-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="ca66f-162">Se un server passa improvvisamente dall'alimentazione AC a un alimentatore di continuità, questa modifica può indicare che si è verificato un problema elettrico, sia con il computer che con il sistema elettrico nella stanza in cui viene mantenuto il computer.</span><span class="sxs-lookup"><span data-stu-id="ca66f-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="ca66f-163">Gli amministratori devono monitorare queste modifiche nello stato di alimentazione e ricevere immediatamente notifiche relative a tali modifiche.</span><span class="sxs-lookup"><span data-stu-id="ca66f-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="ca66f-164">In questo modo è possibile intervenire prima che il dispositivo perda completamente l'energia.</span><span class="sxs-lookup"><span data-stu-id="ca66f-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="ca66f-165">(È possibile, ad esempio, che i sistemi di continuità elettrica continuino a essere eseguiti solo 15 minuti prima di essere arrestati).</span><span class="sxs-lookup"><span data-stu-id="ca66f-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="ca66f-166">La classe **Win32 \_ PowerManagementEvent** può essere usata per monitorare le modifiche dello stato di alimentazione in un computer.</span><span class="sxs-lookup"><span data-stu-id="ca66f-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="ca66f-167">Queste modifiche possono includere un passaggio da una fonte di alimentazione a un'altra e una modifica dello stato di alimentazione del computer (ad esempio, immissione o uscita dalla modalità di sospensione).</span><span class="sxs-lookup"><span data-stu-id="ca66f-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="ca66f-168">La classe **Win32 \_ PowerManagementEvent** dispone solo di due proprietà: EventType, usata per indicare il tipo di evento di modifica di risparmio energia che si è verificato e OEMEventType, usato da alcuni produttori di apparecchiature originali per definire eventi di modifica del risparmio di energia aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ca66f-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="ca66f-169">Per ulteriori informazioni sulla risposta agli eventi di alimentazione di Windows, vedere l'articolo [monitorare e rispondere agli eventi di Power Windows con PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) in</span><span class="sxs-lookup"><span data-stu-id="ca66f-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="ca66f-170">Scripting Guy!</span><span class="sxs-lookup"><span data-stu-id="ca66f-170">Scripting Guy!</span></span> <span data-ttu-id="ca66f-171">.</span><span class="sxs-lookup"><span data-stu-id="ca66f-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="ca66f-172">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca66f-172">Examples</span></span>

<span data-ttu-id="ca66f-173">Il codice VBScript seguente monitora le modifiche allo stato di alimentazione in un computer.</span><span class="sxs-lookup"><span data-stu-id="ca66f-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="ca66f-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca66f-174">Requirements</span></span>



| <span data-ttu-id="ca66f-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca66f-175">Requirement</span></span> | <span data-ttu-id="ca66f-176">Valore</span><span class="sxs-lookup"><span data-stu-id="ca66f-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca66f-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca66f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ca66f-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca66f-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca66f-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca66f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ca66f-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca66f-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca66f-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca66f-181">Namespace</span></span><br/>                | <span data-ttu-id="ca66f-182">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ca66f-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca66f-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ca66f-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca66f-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca66f-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca66f-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ca66f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca66f-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca66f-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca66f-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca66f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca66f-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="ca66f-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="ca66f-189">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ca66f-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="ca66f-190">[Monitoraggio delle modifiche allo stato di alimentazione del computer](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="ca66f-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
