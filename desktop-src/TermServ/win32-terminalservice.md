---
title: Classe Win32_TerminalService
description: Sottoclasse della classe del \_ servizio Win32. Win32 \_ TerminalService rappresenta la proprietà dell'elemento dell' \_ associazione TerminalServiceToSetting Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalService Servizi Desktop remoto
- Classe Win32_TerminalService Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478844"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="26e64-106">Win32 \_ TerminalService (classe)</span><span class="sxs-lookup"><span data-stu-id="26e64-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="26e64-107">La classe WMI **\_ TerminalService Win32** è una sottoclasse della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="26e64-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="26e64-108">**Win32 \_ TerminalService** rappresenta la proprietà dell' **elemento** dell' [**associazione \_ TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="26e64-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="26e64-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="26e64-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e64-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26e64-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="26e64-111">Members</span><span class="sxs-lookup"><span data-stu-id="26e64-111">Members</span></span>

<span data-ttu-id="26e64-112">La classe **Win32 \_ TerminalService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26e64-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="26e64-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="26e64-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="26e64-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26e64-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="26e64-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="26e64-115">Methods</span></span>

<span data-ttu-id="26e64-116">La classe **Win32 \_ TerminalService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="26e64-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="26e64-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="26e64-117">Method</span></span>                                                                       | <span data-ttu-id="26e64-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26e64-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26e64-119">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="26e64-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="26e64-120">Modifica un servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="26e64-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="26e64-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="26e64-122">Modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="26e64-123">**Creare**</span><span class="sxs-lookup"><span data-stu-id="26e64-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="26e64-124">Crea un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="26e64-125">**Delete**</span><span class="sxs-lookup"><span data-stu-id="26e64-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="26e64-126">Elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="26e64-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="26e64-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="26e64-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="26e64-128">Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="26e64-129">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="26e64-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="26e64-130">Richiede che un servizio aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="26e64-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="26e64-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="26e64-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="26e64-132">Tenta di collocare un servizio in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="26e64-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="26e64-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="26e64-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="26e64-134">Tenta di inserire un servizio nello stato ripresa.</span><span class="sxs-lookup"><span data-stu-id="26e64-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="26e64-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="26e64-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="26e64-136">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="26e64-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="26e64-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="26e64-138">Tenta di inserire un servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="26e64-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="26e64-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="26e64-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="26e64-140">Inserisce un servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="26e64-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="26e64-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="26e64-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="26e64-142">Tenta di inviare un codice di controllo definito dall'utente a un servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="26e64-143">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26e64-143">Properties</span></span>

<span data-ttu-id="26e64-144">La classe **Win32 \_ TerminalService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26e64-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26e64-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="26e64-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26e64-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("servizio accetta pausa")</span><span class="sxs-lookup"><span data-stu-id="26e64-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-149">Indica se il servizio può essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="26e64-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="26e64-150">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="26e64-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-152">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26e64-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-154">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service accepts stop")</span><span class="sxs-lookup"><span data-stu-id="26e64-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-155">Indica se il servizio può essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="26e64-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="26e64-156">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-157">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="26e64-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-160">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="26e64-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-161">Breve descrizione del servizio una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="26e64-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="26e64-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="26e64-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-163">**CheckPoint**</span><span class="sxs-lookup"><span data-stu-id="26e64-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-164">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-166">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point count")</span><span class="sxs-lookup"><span data-stu-id="26e64-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-167">Valore che il servizio incrementa periodicamente per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione Prolong.</span><span class="sxs-lookup"><span data-stu-id="26e64-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="26e64-168">Il servizio, ad esempio, incrementa questo valore poiché completa ogni passaggio dell'inizializzazione all'avvio.</span><span class="sxs-lookup"><span data-stu-id="26e64-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="26e64-169">Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="26e64-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="26e64-170">Questo valore non è valido e deve essere zero quando il servizio non dispone di un'operazione di avvio, arresto, pausa o continuazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="26e64-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="26e64-171">Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26e64-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-175">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="26e64-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-176">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="26e64-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="26e64-177">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="26e64-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="26e64-178">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="26e64-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26e64-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-182">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Retarded \_ auto \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("avvio automatico ritardato")</span><span class="sxs-lookup"><span data-stu-id="26e64-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-183">Se **true**, il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.</span><span class="sxs-lookup"><span data-stu-id="26e64-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="26e64-184">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="26e64-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="26e64-185">Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-186">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="26e64-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-189">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="26e64-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-190">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26e64-190">Description of the object.</span></span>

<span data-ttu-id="26e64-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="26e64-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="26e64-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-193">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26e64-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-195">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagisce con il desktop")</span><span class="sxs-lookup"><span data-stu-id="26e64-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-196">Indica se il servizio è in grado di creare o comunicare con Windows sul desktop e quindi interagire in qualche modo con un utente.</span><span class="sxs-lookup"><span data-stu-id="26e64-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="26e64-197">I servizi interattivi devono essere eseguiti con l'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="26e64-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="26e64-198">La maggior parte dei servizi non è interattiva; ovvero non comunicano con l'utente in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="26e64-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="26e64-199">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-200">**DisconnectedSessions**</span><span class="sxs-lookup"><span data-stu-id="26e64-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26e64-203">Numero di sessioni disconnesse nel server corrente.</span><span class="sxs-lookup"><span data-stu-id="26e64-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="26e64-204">Queste sessioni possono continuare a usare attivamente le risorse del server, ma attualmente non hanno una connessione di rete con un client.</span><span class="sxs-lookup"><span data-stu-id="26e64-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="26e64-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="26e64-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-208">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span><span class="sxs-lookup"><span data-stu-id="26e64-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-209">Nome del servizio visualizzato nello snap-in servizi.</span><span class="sxs-lookup"><span data-stu-id="26e64-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="26e64-210">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="26e64-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="26e64-211">Si noti che il nome visualizzato e il nome del servizio (archiviati nel registro di sistema) non sono sempre gli stessi.</span><span class="sxs-lookup"><span data-stu-id="26e64-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="26e64-212">Il servizio client DHCP, ad esempio, ha il nome del servizio DHCP ma il nome visualizzato client DHCP.</span><span class="sxs-lookup"><span data-stu-id="26e64-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="26e64-213">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="26e64-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="26e64-214">Tuttavia, i confronti [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="26e64-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="26e64-215">Constraint: accetta lo stesso valore della proprietà [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="26e64-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="26e64-216">Esempio: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="26e64-216">Example: "Atdisk"</span></span>

<span data-ttu-id="26e64-217">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="26e64-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-221">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravità dell'avvio non riuscito")</span><span class="sxs-lookup"><span data-stu-id="26e64-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-222">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="26e64-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="26e64-223">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="26e64-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="26e64-224">Tutti gli errori vengono registrati dal computer.</span><span class="sxs-lookup"><span data-stu-id="26e64-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="26e64-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")</span><span class="sxs-lookup"><span data-stu-id="26e64-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-226">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="26e64-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="26e64-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")</span><span class="sxs-lookup"><span data-stu-id="26e64-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-228">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="26e64-228">User is notified.</span></span> <span data-ttu-id="26e64-229">In genere si tratta di una finestra di messaggio che informa l'utente del problema.</span><span class="sxs-lookup"><span data-stu-id="26e64-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="26e64-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="26e64-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-231">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="26e64-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="26e64-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")</span><span class="sxs-lookup"><span data-stu-id="26e64-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-233">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="26e64-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="26e64-234">Se il servizio non viene avviato una seconda volta, l'avvio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="26e64-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26e64-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="26e64-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-236">La gravità dell'errore è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="26e64-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="26e64-237">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="26e64-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-239">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-241">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita")</span><span class="sxs-lookup"><span data-stu-id="26e64-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-242">Codice di errore di Windows che definisce gli errori riscontrati durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="26e64-243">Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="26e64-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="26e64-244">Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="26e64-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="26e64-245">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="26e64-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-247">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26e64-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-249">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="26e64-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-250">L'oggetto data è installato.</span><span class="sxs-lookup"><span data-stu-id="26e64-250">Date object is installed.</span></span> <span data-ttu-id="26e64-251">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="26e64-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="26e64-252">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="26e64-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-253">**Nome**</span><span class="sxs-lookup"><span data-stu-id="26e64-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-256">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26e64-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26e64-257">Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="26e64-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="26e64-258">Questa funzionalità è descritta nella proprietà [**Description**](/windows/desktop/CIMWin32Prov/win32-service) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26e64-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="26e64-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="26e64-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="26e64-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-263">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome percorso file")</span><span class="sxs-lookup"><span data-stu-id="26e64-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-264">Percorso completo del file binario del servizio che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="26e64-265">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="26e64-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="26e64-266">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-267">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="26e64-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-268">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-270">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID processo")</span><span class="sxs-lookup"><span data-stu-id="26e64-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-271">Identificatore del processo del servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-271">Process identifier of the service.</span></span>

<span data-ttu-id="26e64-272">Esempio: 324</span><span class="sxs-lookup"><span data-stu-id="26e64-272">Example: 324</span></span>

<span data-ttu-id="26e64-273">Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-274">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="26e64-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-275">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-277">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita specifico del server")</span><span class="sxs-lookup"><span data-stu-id="26e64-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-278">Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="26e64-279">I codici di uscita sono definiti dal servizio rappresentato da questa classe.</span><span class="sxs-lookup"><span data-stu-id="26e64-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="26e64-280">Questo valore viene impostato solo quando il valore della proprietà [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) è **\_ \_ \_ errore specifico del servizio di errore** (1066).</span><span class="sxs-lookup"><span data-stu-id="26e64-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="26e64-281">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="26e64-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-285">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di servizio")</span><span class="sxs-lookup"><span data-stu-id="26e64-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-286">Tipo di servizio fornito ai processi chiamanti.</span><span class="sxs-lookup"><span data-stu-id="26e64-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="26e64-287">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="26e64-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="26e64-288">**Driver del kernel** ("driver del kernel")</span><span class="sxs-lookup"><span data-stu-id="26e64-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="26e64-289">**Driver del file System** ("driver del file System")</span><span class="sxs-lookup"><span data-stu-id="26e64-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="26e64-290">**Adapter** ("adapter")</span><span class="sxs-lookup"><span data-stu-id="26e64-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="26e64-291">**Driver di riconoscimento** ("driver di riconoscimento")</span><span class="sxs-lookup"><span data-stu-id="26e64-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="26e64-292">**Processo personale** ("processo personalizzato")</span><span class="sxs-lookup"><span data-stu-id="26e64-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="26e64-293">**Processo di condivisione** ("processo di condivisione")</span><span class="sxs-lookup"><span data-stu-id="26e64-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="26e64-294">**Processo interattivo** ("processo interattivo")</span><span class="sxs-lookup"><span data-stu-id="26e64-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="26e64-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="26e64-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="26e64-296">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-297">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="26e64-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26e64-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-300">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="26e64-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-301">Indica se il servizio è stato avviato o meno.</span><span class="sxs-lookup"><span data-stu-id="26e64-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="26e64-302">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-303">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="26e64-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-306">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="26e64-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-307">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="26e64-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="26e64-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="26e64-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-309">Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).</span><span class="sxs-lookup"><span data-stu-id="26e64-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="26e64-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="26e64-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-311">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26e64-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="26e64-312">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="26e64-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="26e64-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automatico** ("auto")</span><span class="sxs-lookup"><span data-stu-id="26e64-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-314">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="26e64-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="26e64-315">I servizi automatici vengono avviati anche se un utente non esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="26e64-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="26e64-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="26e64-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-317">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="26e64-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="26e64-318">Questi servizi non vengono avviati, a meno che un utente non esegua l'accesso e li avvii.</span><span class="sxs-lookup"><span data-stu-id="26e64-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="26e64-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="26e64-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="26e64-320">Servizio che non può essere avviato finché il relativo StartMode non viene modificato in auto o manuale.</span><span class="sxs-lookup"><span data-stu-id="26e64-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="26e64-321">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="26e64-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-325">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome account iniziale")</span><span class="sxs-lookup"><span data-stu-id="26e64-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-326">Nome dell'account con cui viene eseguito un servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-326">Account name under which a service runs.</span></span> <span data-ttu-id="26e64-327">A seconda del tipo di servizio, il nome dell'account può avere la forma di "DomainName \\ username" o del formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="26e64-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="26e64-328">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="26e64-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="26e64-329">Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="26e64-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="26e64-330">Per i driver a livello di sistema o del kernel, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene il nome dell'oggetto driver, ovvero " \\ filesystem \\ RDR" o " \\ driver \\ XNS", utilizzato dal sistema i/O per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26e64-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="26e64-331">Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="26e64-332">Esempio: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="26e64-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="26e64-333">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-334">**State**</span><span class="sxs-lookup"><span data-stu-id="26e64-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-336">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26e64-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26e64-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("state")</span><span class="sxs-lookup"><span data-stu-id="26e64-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-338">Stato corrente del servizio di base.</span><span class="sxs-lookup"><span data-stu-id="26e64-338">Current state of the base service.</span></span>

<span data-ttu-id="26e64-339">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="26e64-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="26e64-340">**Arrestato** ("arrestato")</span><span class="sxs-lookup"><span data-stu-id="26e64-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="26e64-341">**Avvio in sospeso** ("avvio in sospeso")</span><span class="sxs-lookup"><span data-stu-id="26e64-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="26e64-342">**Arresta in sospeso** ("arresta in sospeso")</span><span class="sxs-lookup"><span data-stu-id="26e64-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="26e64-343">**In esecuzione** ("Running")</span><span class="sxs-lookup"><span data-stu-id="26e64-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="26e64-344">**Continua in sospeso** ("continua in sospeso")</span><span class="sxs-lookup"><span data-stu-id="26e64-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="26e64-345">**Sospensione in sospeso** ("pausa in sospeso")</span><span class="sxs-lookup"><span data-stu-id="26e64-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="26e64-346">**Sospesa** ("sospesa")</span><span class="sxs-lookup"><span data-stu-id="26e64-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26e64-347">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="26e64-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="26e64-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="26e64-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="26e64-349">**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura prima di Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="26e64-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="26e64-350">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="26e64-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-354">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="26e64-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-355">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26e64-355">Current status of the object.</span></span> <span data-ttu-id="26e64-356">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="26e64-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="26e64-357">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="26e64-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="26e64-358">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="26e64-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="26e64-359">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="26e64-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="26e64-360">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="26e64-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="26e64-361">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="26e64-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="26e64-362">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="26e64-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="26e64-363">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="26e64-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26e64-364">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="26e64-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26e64-365">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="26e64-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="26e64-366">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="26e64-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="26e64-367">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="26e64-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="26e64-368">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="26e64-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="26e64-369">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="26e64-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="26e64-370">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="26e64-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="26e64-371">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="26e64-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="26e64-372">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="26e64-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="26e64-373">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="26e64-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="26e64-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="26e64-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="26e64-375">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="26e64-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-376">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26e64-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-377">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-379">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="26e64-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-380">Nome del tipo di sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="26e64-381">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="26e64-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-383">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26e64-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-385">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). Nome "), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="26e64-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-386">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="26e64-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="26e64-387">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="26e64-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-389">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-391">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID tag")</span><span class="sxs-lookup"><span data-stu-id="26e64-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-392">Valore di tag univoco per il servizio nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="26e64-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="26e64-393">Il valore 0 (zero) indica che il servizio non dispone di un tag.</span><span class="sxs-lookup"><span data-stu-id="26e64-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="26e64-394">Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:</span><span class="sxs-lookup"><span data-stu-id="26e64-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="26e64-395">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="26e64-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="26e64-396">I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file System con modalità avvio o sistema.</span><span class="sxs-lookup"><span data-stu-id="26e64-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="26e64-397">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="26e64-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="26e64-398">**TotalSessions**</span><span class="sxs-lookup"><span data-stu-id="26e64-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-399">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26e64-401">Numero totale di sessioni nel server corrente.</span><span class="sxs-lookup"><span data-stu-id="26e64-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="26e64-402">Sono incluse sessioni connesse e disconnesse.</span><span class="sxs-lookup"><span data-stu-id="26e64-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="26e64-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="26e64-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26e64-404">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26e64-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26e64-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26e64-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26e64-406">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo di attesa stimato")</span><span class="sxs-lookup"><span data-stu-id="26e64-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="26e64-407">Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="26e64-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="26e64-408">Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al metodo **SetServiceStatus** con un valore di [**Checkpoint**](/windows/desktop/CIMWin32Prov/win32-service) incrementato o una modifica in **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="26e64-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="26e64-409">Se la quantità di tempo specificata da **WaitHint** passa e il **Checkpoint** non è stato incrementato oppure **CurrentState** non è stato modificato, gestione controllo servizi o il programma di controllo del servizio presuppone che si sia verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="26e64-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="26e64-410">Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="26e64-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26e64-411">Commenti</span><span class="sxs-lookup"><span data-stu-id="26e64-411">Remarks</span></span>

<span data-ttu-id="26e64-412">Poiché la classe **Win32 \_ TerminalService** è una sottoclasse della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la classe eredita tutte le proprietà e i metodi del **\_ servizio Win32**.</span><span class="sxs-lookup"><span data-stu-id="26e64-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="26e64-413">[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) è associato a **Win32 \_ TerminalService** come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting di Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="26e64-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="26e64-414">[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) è associato a **Win32 \_ TerminalService** come proprietà **Setting** dell'associazione [**\_ TSSessionDirectorySetting di Win32**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="26e64-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="26e64-415">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="26e64-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26e64-416">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="26e64-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="26e64-417">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="26e64-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26e64-418">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="26e64-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="26e64-419">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26e64-419">Requirements</span></span>



| <span data-ttu-id="26e64-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e64-420">Requirement</span></span> | <span data-ttu-id="26e64-421">Valore</span><span class="sxs-lookup"><span data-stu-id="26e64-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e64-422">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26e64-422">Minimum supported client</span></span><br/> | <span data-ttu-id="26e64-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26e64-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26e64-424">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26e64-424">Minimum supported server</span></span><br/> | <span data-ttu-id="26e64-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26e64-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26e64-426">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26e64-426">Namespace</span></span><br/>                | <span data-ttu-id="26e64-427">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="26e64-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="26e64-428">MOF</span><span class="sxs-lookup"><span data-stu-id="26e64-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26e64-429"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26e64-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="26e64-430">DLL</span><span class="sxs-lookup"><span data-stu-id="26e64-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26e64-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e64-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e64-432">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26e64-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e64-433">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="26e64-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="26e64-434">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="26e64-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="26e64-435">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="26e64-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="26e64-436">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="26e64-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="26e64-437">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="26e64-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

