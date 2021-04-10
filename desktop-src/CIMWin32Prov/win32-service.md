---
description: Rappresenta un servizio in un sistema di computer che esegue Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Classe Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049109"
---
# <a name="win32_service-class"></a><span data-ttu-id="aeb71-103">\_Classe del servizio Win32</span><span class="sxs-lookup"><span data-stu-id="aeb71-103">Win32\_Service class</span></span>

<span data-ttu-id="aeb71-104">La [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ servizio Win32** rappresenta un servizio in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb71-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="aeb71-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aeb71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aeb71-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="aeb71-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb71-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aeb71-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="aeb71-108">Members</span><span class="sxs-lookup"><span data-stu-id="aeb71-108">Members</span></span>

<span data-ttu-id="aeb71-109">La classe del **\_ servizio Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aeb71-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="aeb71-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="aeb71-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aeb71-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aeb71-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aeb71-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="aeb71-112">Methods</span></span>

<span data-ttu-id="aeb71-113">La classe del **\_ servizio Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="aeb71-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="aeb71-114">Method</span></span>                                                                               | <span data-ttu-id="aeb71-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aeb71-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aeb71-116">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="aeb71-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="aeb71-117">Modifica un servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="aeb71-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="aeb71-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="aeb71-119">Modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="aeb71-120">**Creare**</span><span class="sxs-lookup"><span data-stu-id="aeb71-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="aeb71-121">Crea un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="aeb71-122">**Delete**</span><span class="sxs-lookup"><span data-stu-id="aeb71-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="aeb71-123">Elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="aeb71-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="aeb71-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aeb71-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="aeb71-125">Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="aeb71-126">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="aeb71-127">Richiede che un servizio aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="aeb71-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="aeb71-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="aeb71-129">Tenta di collocare un servizio in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="aeb71-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="aeb71-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="aeb71-131">Tenta di inserire un servizio nello stato ripresa.</span><span class="sxs-lookup"><span data-stu-id="aeb71-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="aeb71-132">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aeb71-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="aeb71-133">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="aeb71-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="aeb71-135">Tenta di inserire un servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="aeb71-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="aeb71-137">Inserisce un servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="aeb71-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="aeb71-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="aeb71-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="aeb71-139">Tenta di inviare un codice di controllo definito dall'utente a un servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="aeb71-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aeb71-140">Properties</span></span>

<span data-ttu-id="aeb71-141">La classe del **\_ servizio Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aeb71-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aeb71-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="aeb71-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeb71-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-145">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("servizio accetta pausa")</span><span class="sxs-lookup"><span data-stu-id="aeb71-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-146">Indica se il servizio può essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="aeb71-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="aeb71-147">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="aeb71-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeb71-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-151">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service accepts stop")</span><span class="sxs-lookup"><span data-stu-id="aeb71-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-152">Indica se il servizio può essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="aeb71-153">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-154">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="aeb71-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-157">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aeb71-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-158">Breve descrizione del servizio, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="aeb71-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="aeb71-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-160">**CheckPoint**</span><span class="sxs-lookup"><span data-stu-id="aeb71-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-163">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point count")</span><span class="sxs-lookup"><span data-stu-id="aeb71-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-164">Valore che il servizio incrementa periodicamente per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione Prolong.</span><span class="sxs-lookup"><span data-stu-id="aeb71-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="aeb71-165">Il servizio, ad esempio, incrementa questo valore poiché completa ogni passaggio dell'inizializzazione all'avvio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="aeb71-166">Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="aeb71-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="aeb71-167">Questo valore non è valido e deve essere zero quando il servizio non dispone di un'operazione di avvio, arresto, pausa o continuazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="aeb71-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-171">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="aeb71-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-172">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="aeb71-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="aeb71-173">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aeb71-174">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="aeb71-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-176">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeb71-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-178">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Retarded \_ auto \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("avvio automatico ritardato")</span><span class="sxs-lookup"><span data-stu-id="aeb71-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-179">Se **true**, il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="aeb71-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="aeb71-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-181">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aeb71-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-184">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aeb71-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-185">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aeb71-185">Description of the object.</span></span>

<span data-ttu-id="aeb71-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="aeb71-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-188">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeb71-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-190">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("interagisce con il desktop")</span><span class="sxs-lookup"><span data-stu-id="aeb71-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-191">Indica se il servizio è in grado di creare o comunicare con Windows sul desktop e quindi interagire in qualche modo con un utente.</span><span class="sxs-lookup"><span data-stu-id="aeb71-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="aeb71-192">I servizi interattivi devono essere eseguiti con l'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="aeb71-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="aeb71-193">La maggior parte dei servizi non è interattiva; ovvero non comunicano con l'utente in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="aeb71-194">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span><span class="sxs-lookup"><span data-stu-id="aeb71-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-199">Nome del servizio visualizzato nello snap-in servizi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="aeb71-200">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="aeb71-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="aeb71-201">Si noti che il nome visualizzato e il nome del servizio (archiviati nel registro di sistema) non sono sempre gli stessi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="aeb71-202">Il servizio client DHCP, ad esempio, ha il nome del servizio DHCP ma il nome visualizzato client DHCP.</span><span class="sxs-lookup"><span data-stu-id="aeb71-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="aeb71-203">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="aeb71-204">Tuttavia, i confronti **DisplayName** sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="aeb71-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="aeb71-205">Constraint: accetta lo stesso valore della proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="aeb71-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="aeb71-206">Esempio: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="aeb71-206">Example: "Atdisk"</span></span>

<span data-ttu-id="aeb71-207">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="aeb71-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-211">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravità dell'avvio non riuscito")</span><span class="sxs-lookup"><span data-stu-id="aeb71-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-212">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="aeb71-213">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="aeb71-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="aeb71-214">Tutti gli errori vengono registrati dal computer.</span><span class="sxs-lookup"><span data-stu-id="aeb71-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="aeb71-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")</span><span class="sxs-lookup"><span data-stu-id="aeb71-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-216">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="aeb71-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")</span><span class="sxs-lookup"><span data-stu-id="aeb71-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-218">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-218">User is notified.</span></span> <span data-ttu-id="aeb71-219">In genere si tratta di una finestra di messaggio che informa l'utente del problema.</span><span class="sxs-lookup"><span data-stu-id="aeb71-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="aeb71-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="aeb71-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-221">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="aeb71-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="aeb71-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")</span><span class="sxs-lookup"><span data-stu-id="aeb71-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-223">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="aeb71-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="aeb71-224">Se il servizio non viene avviato una seconda volta, l'avvio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aeb71-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-226">La gravità dell'errore è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="aeb71-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="aeb71-227">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="aeb71-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-229">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-231">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita")</span><span class="sxs-lookup"><span data-stu-id="aeb71-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-232">Codice di errore di Windows che definisce gli errori riscontrati durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="aeb71-233">Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="aeb71-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="aeb71-234">Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="aeb71-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="aeb71-235">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aeb71-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-237">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aeb71-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-239">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="aeb71-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-240">L'oggetto data è installato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-240">Date object is installed.</span></span> <span data-ttu-id="aeb71-241">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aeb71-242">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-243">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aeb71-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-246">Qualificatori: [ **chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="aeb71-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-247">Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="aeb71-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="aeb71-248">Questa funzionalità è descritta nella proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aeb71-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="aeb71-249">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-253">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome percorso file")</span><span class="sxs-lookup"><span data-stu-id="aeb71-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-254">Percorso completo del file binario del servizio che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="aeb71-255">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="aeb71-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="aeb71-256">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-257">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="aeb71-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-258">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-260">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo")</span><span class="sxs-lookup"><span data-stu-id="aeb71-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-261">Identificatore del processo del servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-261">Process identifier of the service.</span></span>

<span data-ttu-id="aeb71-262">Esempio: 324</span><span class="sxs-lookup"><span data-stu-id="aeb71-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-263">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="aeb71-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-266">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita specifico del server")</span><span class="sxs-lookup"><span data-stu-id="aeb71-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-267">Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="aeb71-268">I codici di uscita sono definiti dal servizio rappresentato da questa classe.</span><span class="sxs-lookup"><span data-stu-id="aeb71-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="aeb71-269">Questo valore viene impostato solo quando il valore della proprietà **ExitCode** è **\_ \_ \_ errore specifico del servizio di errore** (1066).</span><span class="sxs-lookup"><span data-stu-id="aeb71-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="aeb71-270">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="aeb71-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-274">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo di servizio")</span><span class="sxs-lookup"><span data-stu-id="aeb71-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-275">Tipo di servizio fornito ai processi chiamanti.</span><span class="sxs-lookup"><span data-stu-id="aeb71-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="aeb71-276">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="aeb71-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="aeb71-277">**Driver del kernel** ("driver del kernel")</span><span class="sxs-lookup"><span data-stu-id="aeb71-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="aeb71-278">**Driver del file System** ("driver del file System")</span><span class="sxs-lookup"><span data-stu-id="aeb71-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="aeb71-279">**Adapter** ("adapter")</span><span class="sxs-lookup"><span data-stu-id="aeb71-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="aeb71-280">**Driver di riconoscimento** ("driver di riconoscimento")</span><span class="sxs-lookup"><span data-stu-id="aeb71-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="aeb71-281">**Processo personale** ("processo personalizzato")</span><span class="sxs-lookup"><span data-stu-id="aeb71-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="aeb71-282">**Processo di condivisione** ("processo di condivisione")</span><span class="sxs-lookup"><span data-stu-id="aeb71-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="aeb71-283">**Processo interattivo** ("processo interattivo")</span><span class="sxs-lookup"><span data-stu-id="aeb71-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="aeb71-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aeb71-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="aeb71-285">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-286">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="aeb71-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-287">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeb71-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-289">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="aeb71-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-290">Indica se il servizio è stato avviato o meno.</span><span class="sxs-lookup"><span data-stu-id="aeb71-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="aeb71-291">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-292">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="aeb71-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-295">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="aeb71-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-296">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb71-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="aeb71-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aeb71-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-298">Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).</span><span class="sxs-lookup"><span data-stu-id="aeb71-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="aeb71-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="aeb71-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-300">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="aeb71-301">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="aeb71-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="aeb71-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automatico** ("auto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-303">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="aeb71-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="aeb71-304">I servizi automatici vengono avviati anche se un utente non esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="aeb71-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="aeb71-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="aeb71-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-306">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb71-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="aeb71-307">Questi servizi non vengono avviati, a meno che un utente non esegua l'accesso e li avvii.</span><span class="sxs-lookup"><span data-stu-id="aeb71-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aeb71-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="aeb71-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="aeb71-309">Servizio che non può essere avviato finché il relativo StartMode non viene modificato in auto o manuale.</span><span class="sxs-lookup"><span data-stu-id="aeb71-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="aeb71-310">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-314">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome account iniziale")</span><span class="sxs-lookup"><span data-stu-id="aeb71-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-315">Nome dell'account con cui viene eseguito un servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-315">Account name under which a service runs.</span></span> <span data-ttu-id="aeb71-316">A seconda del tipo di servizio, il nome dell'account può avere la forma di "DomainName \\ username" o del formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="aeb71-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="aeb71-317">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aeb71-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="aeb71-318">Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="aeb71-319">Per i driver a livello di sistema o del kernel, **StartName** contiene il nome dell'oggetto driver, ovvero " \\ filesystem \\ RDR" o " \\ driver \\ XNS", utilizzato dal sistema i/O per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="aeb71-320">Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="aeb71-321">Esempio: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="aeb71-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="aeb71-322">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-323">**State**</span><span class="sxs-lookup"><span data-stu-id="aeb71-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-325">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aeb71-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-326">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("state")</span><span class="sxs-lookup"><span data-stu-id="aeb71-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-327">Stato corrente del servizio di base.</span><span class="sxs-lookup"><span data-stu-id="aeb71-327">Current state of the base service.</span></span>

<span data-ttu-id="aeb71-328">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="aeb71-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="aeb71-329">**Arrestato** ("arrestato")</span><span class="sxs-lookup"><span data-stu-id="aeb71-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="aeb71-330">**Avvio in sospeso** ("avvio in sospeso")</span><span class="sxs-lookup"><span data-stu-id="aeb71-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="aeb71-331">**Arresta in sospeso** ("arresta in sospeso")</span><span class="sxs-lookup"><span data-stu-id="aeb71-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="aeb71-332">**In esecuzione** ("Running")</span><span class="sxs-lookup"><span data-stu-id="aeb71-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="aeb71-333">**Continua in sospeso** ("continua in sospeso")</span><span class="sxs-lookup"><span data-stu-id="aeb71-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="aeb71-334">**Sospensione in sospeso** ("pausa in sospeso")</span><span class="sxs-lookup"><span data-stu-id="aeb71-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aeb71-335">**Sospesa** ("sospesa")</span><span class="sxs-lookup"><span data-stu-id="aeb71-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aeb71-336">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="aeb71-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aeb71-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="aeb71-338">**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura prima di Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="aeb71-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="aeb71-339">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-340">**Status**</span><span class="sxs-lookup"><span data-stu-id="aeb71-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-343">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="aeb71-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-344">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aeb71-344">Current status of the object.</span></span> <span data-ttu-id="aeb71-345">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="aeb71-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aeb71-346">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="aeb71-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aeb71-347">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="aeb71-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aeb71-348">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="aeb71-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aeb71-349">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="aeb71-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aeb71-350">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aeb71-351">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="aeb71-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aeb71-352">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aeb71-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aeb71-353">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="aeb71-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aeb71-354">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="aeb71-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aeb71-355">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aeb71-356">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="aeb71-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aeb71-357">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aeb71-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aeb71-358">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aeb71-359">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="aeb71-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aeb71-360">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="aeb71-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aeb71-361">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="aeb71-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aeb71-362">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="aeb71-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aeb71-363">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="aeb71-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aeb71-364">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-367">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="aeb71-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-368">Nome del tipo di sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="aeb71-369">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aeb71-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-371">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aeb71-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-373">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="aeb71-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-374">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="aeb71-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="aeb71-375">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="aeb71-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-377">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-379">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID tag")</span><span class="sxs-lookup"><span data-stu-id="aeb71-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-380">Valore di tag univoco per il servizio nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="aeb71-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="aeb71-381">Il valore 0 (zero) indica che il servizio non dispone di un tag.</span><span class="sxs-lookup"><span data-stu-id="aeb71-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="aeb71-382">Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:</span><span class="sxs-lookup"><span data-stu-id="aeb71-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="aeb71-383">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="aeb71-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="aeb71-384">I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file System con modalità avvio o sistema.</span><span class="sxs-lookup"><span data-stu-id="aeb71-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="aeb71-385">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeb71-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="aeb71-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeb71-387">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aeb71-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeb71-389">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tempo di attesa stimato")</span><span class="sxs-lookup"><span data-stu-id="aeb71-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="aeb71-390">Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="aeb71-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="aeb71-391">Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al metodo **SetServiceStatus** con un valore di **Checkpoint** incrementato o una modifica in **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="aeb71-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="aeb71-392">Se la quantità di tempo specificata da **WaitHint** passa e il **Checkpoint** non è stato incrementato oppure **CurrentState** non è stato modificato, gestione controllo servizi o il programma di controllo del servizio presuppone che si sia verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="aeb71-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeb71-393">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeb71-393">Remarks</span></span>

<span data-ttu-id="aeb71-394">La classe del **\_ servizio Win32** è derivata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="aeb71-395">La modalità di gestione di un computer specifico dipende in larga misura dal ruolo svolto dal computer.</span><span class="sxs-lookup"><span data-stu-id="aeb71-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="aeb71-396">Ad esempio, in genere si monitorano diversi aspetti di un server DNS rispetto a un server DHCP.</span><span class="sxs-lookup"><span data-stu-id="aeb71-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="aeb71-397">Sebbene nessuna singola proprietà possa indicare se un determinato computer è un server di database, un server di posta elettronica o un server multimediale, è spesso possibile identificare il ruolo riprodotto da un computer identificando i servizi installati.</span><span class="sxs-lookup"><span data-stu-id="aeb71-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="aeb71-398">Nelle organizzazioni di grandi dimensioni è probabile che sia installato solo uno dei principali servizi, ad esempio la posta elettronica, in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="aeb71-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="aeb71-399">Sarebbe insolito che un server di posta venga eseguito anche come server per i file di Microsoft® Windows Media® Technologies Player.</span><span class="sxs-lookup"><span data-stu-id="aeb71-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="aeb71-400">Per questo motivo, l'identificazione di un servizio installato in un computer può consentire di identificare il ruolo del computer nella rete.</span><span class="sxs-lookup"><span data-stu-id="aeb71-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="aeb71-401">Se il servizio Microsoft® Exchange Server è installato e in esecuzione in un computer, è in genere preferibile che questo computer funzioni come server di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="aeb71-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="aeb71-402">È possibile utilizzare la classe **del \_ servizio WMI Win32** per enumerare i servizi installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="aeb71-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="aeb71-403">Inoltre, è possibile usare questa classe per determinare se i servizi sono attualmente in esecuzione e per restituire qualsiasi altra informazione necessaria su tale servizio e su come è stato configurato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="aeb71-404">Un'applicazione di servizio è conforme alle regole di interfaccia di gestione controllo servizi e può essere avviata automaticamente da un utente all'avvio del sistema tramite l'utilità pannello di controllo dei servizi o da un'applicazione che usa le funzioni del servizio incluse nell'API Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb71-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="aeb71-405">I servizi possono essere avviati quando nessun utente è connesso al computer.</span><span class="sxs-lookup"><span data-stu-id="aeb71-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="aeb71-406">Per poter enumerare questa classe, è necessario che un utente che si connette da un computer remoto disponga del privilegio **\_ \_ Gestione SC** .</span><span class="sxs-lookup"><span data-stu-id="aeb71-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="aeb71-407">Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="aeb71-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aeb71-408">Esempio</span><span class="sxs-lookup"><span data-stu-id="aeb71-408">Examples</span></span>

<span data-ttu-id="aeb71-409">La [query PS-WMI che restituisce il servizio "stato" in un gruppo di dispositivi esempio di](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell nella raccolta TechNet usa il **\_ servizio Win32** per creare un elenco di dispositivi da Active Directory, quindi esegue una query su ogni dispositivo che risponde con pingfor a un servizio specifico in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aeb71-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="aeb71-410">L'esempio di PowerShell per il [report del server](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) nella raccolta TechNet usa il **\_ servizio Win32** per raccogliere le informazioni sul server e pubblicarle nel documento di Word.</span><span class="sxs-lookup"><span data-stu-id="aeb71-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="aeb71-411">Nell'esempio di codice VBScript seguente vengono visualizzati tutti i servizi attualmente installati.</span><span class="sxs-lookup"><span data-stu-id="aeb71-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="aeb71-412">Nell'esempio di codice VBScript seguente vengono descritti i servizi sospesi, in esecuzione e interrotti nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="aeb71-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="aeb71-413">Nello script Perl seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze **del \_ servizio Win32**.</span><span class="sxs-lookup"><span data-stu-id="aeb71-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="aeb71-414">Nell'esempio c seguente \# viene usato [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) per recuperare tutti i servizi in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="aeb71-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="aeb71-415">Nell' \# esempio di codice C seguente viene usato lo spazio dei nomi [System. Management](/dotnet/api/system.management) per recuperare tutti i servizi in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="aeb71-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="aeb71-416">[System. Management](/dotnet/api/system.management) contiene le classi originali utilizzate per accedere a WMI. Tuttavia, sono considerate più lente e in genere non vengono ridimensionate, nonché le controparti [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aeb71-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="aeb71-417">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeb71-417">Requirements</span></span>



| <span data-ttu-id="aeb71-418">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb71-418">Requirement</span></span> | <span data-ttu-id="aeb71-419">Valore</span><span class="sxs-lookup"><span data-stu-id="aeb71-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb71-420">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb71-420">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb71-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aeb71-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aeb71-422">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb71-422">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb71-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeb71-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aeb71-424">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aeb71-424">Namespace</span></span><br/>                | <span data-ttu-id="aeb71-425">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aeb71-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aeb71-426">MOF</span><span class="sxs-lookup"><span data-stu-id="aeb71-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeb71-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aeb71-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeb71-428">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb71-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb71-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb71-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb71-430">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aeb71-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb71-431">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="aeb71-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="aeb71-432">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="aeb71-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="aeb71-433">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="aeb71-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
