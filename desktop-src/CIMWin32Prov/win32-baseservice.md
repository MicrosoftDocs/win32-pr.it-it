---
description: La \_ classe WMI astratta Win32 BaseService rappresenta gli oggetti eseguibili installati in un database del registro di sistema gestito da Gestione controllo servizi.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127487"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="95d28-103">Win32 \_ BaseService (classe)</span><span class="sxs-lookup"><span data-stu-id="95d28-103">Win32\_BaseService class</span></span>

<span data-ttu-id="95d28-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta **Win32 \_ BaseService** rappresenta gli oggetti eseguibili installati in un database del registro di sistema gestito da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="95d28-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="95d28-105">Il file eseguibile associato a un servizio può essere avviato in fase di avvio da un programma di avvio o dal sistema.</span><span class="sxs-lookup"><span data-stu-id="95d28-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="95d28-106">Può anche essere avviato su richiesta da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="95d28-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="95d28-107">Qualsiasi servizio o processo non di proprietà di un utente specifico e che fornisce un'interfaccia per alcune funzionalità supportate dal computer è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="95d28-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="95d28-108">Esempio: servizio client DHCP (Dynamic Host Configuration Protocol) in un sistema di computer che esegue Windows Server.</span><span class="sxs-lookup"><span data-stu-id="95d28-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="95d28-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="95d28-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="95d28-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="95d28-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d28-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95d28-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="95d28-112">Members</span><span class="sxs-lookup"><span data-stu-id="95d28-112">Members</span></span>

<span data-ttu-id="95d28-113">La classe **Win32 \_ BaseService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="95d28-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="95d28-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="95d28-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="95d28-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="95d28-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95d28-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="95d28-116">Methods</span></span>

<span data-ttu-id="95d28-117">La classe **Win32 \_ BaseService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="95d28-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="95d28-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="95d28-118">Method</span></span>                                                                             | <span data-ttu-id="95d28-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95d28-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="95d28-120">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="95d28-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="95d28-121">Modifica un servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="95d28-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="95d28-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="95d28-123">Modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="95d28-124">**Creare**</span><span class="sxs-lookup"><span data-stu-id="95d28-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="95d28-125">Crea un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="95d28-126">**Delete**</span><span class="sxs-lookup"><span data-stu-id="95d28-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="95d28-127">Elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="95d28-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="95d28-128">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="95d28-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="95d28-129">Richiede che il servizio aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="95d28-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="95d28-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="95d28-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="95d28-131">Esegue un tentativo di sospensione del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="95d28-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="95d28-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="95d28-133">Esegue un tentativo di ripresa del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="95d28-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="95d28-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="95d28-135">Tenta di collocare il servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="95d28-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="95d28-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="95d28-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="95d28-137">Metodo della classe che inserisce il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="95d28-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="95d28-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="95d28-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="95d28-139">Tenta di inviare un codice di controllo definito dall'utente a un servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="95d28-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="95d28-140">Properties</span></span>

<span data-ttu-id="95d28-141">La classe **Win32 \_ BaseService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="95d28-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95d28-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="95d28-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95d28-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-145">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("servizio accetta pausa")</span><span class="sxs-lookup"><span data-stu-id="95d28-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-146">Il servizio può essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="95d28-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="95d28-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="95d28-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95d28-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-150">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service accepts stop")</span><span class="sxs-lookup"><span data-stu-id="95d28-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-151">Il servizio può essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="95d28-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="95d28-152">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="95d28-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-155">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="95d28-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-156">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95d28-156">Short description of the object.</span></span>

<span data-ttu-id="95d28-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95d28-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-161">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="95d28-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-162">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="95d28-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="95d28-163">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="95d28-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="95d28-164">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-165">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="95d28-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-168">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="95d28-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-169">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95d28-169">Description of the object.</span></span>

<span data-ttu-id="95d28-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="95d28-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95d28-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-174">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagisce con il desktop")</span><span class="sxs-lookup"><span data-stu-id="95d28-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-175">Il servizio può creare o comunicare con Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="95d28-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="95d28-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="95d28-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-179">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span><span class="sxs-lookup"><span data-stu-id="95d28-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-180">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-180">Display name of the service.</span></span> <span data-ttu-id="95d28-181">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="95d28-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="95d28-182">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="95d28-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="95d28-183">I confronti di **DisplayName** sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="95d28-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="95d28-184">Constraints: accetta lo stesso valore della proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="95d28-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="95d28-185">Esempio: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="95d28-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="95d28-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="95d28-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-189">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravità dell'avvio non riuscito")</span><span class="sxs-lookup"><span data-stu-id="95d28-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-190">Gravità dell'errore.</span><span class="sxs-lookup"><span data-stu-id="95d28-190">Severity of the error.</span></span> <span data-ttu-id="95d28-191">Impossibile avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-191">Service fails to start.</span></span> <span data-ttu-id="95d28-192">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="95d28-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="95d28-193">Tutti gli errori vengono registrati dal computer.</span><span class="sxs-lookup"><span data-stu-id="95d28-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="95d28-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")</span><span class="sxs-lookup"><span data-stu-id="95d28-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-195">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="95d28-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="95d28-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")</span><span class="sxs-lookup"><span data-stu-id="95d28-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-197">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="95d28-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="95d28-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="95d28-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-199">Il sistema è stato riavviato con l'ultima configurazione ben nota.</span><span class="sxs-lookup"><span data-stu-id="95d28-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="95d28-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")</span><span class="sxs-lookup"><span data-stu-id="95d28-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-201">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="95d28-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95d28-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="95d28-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-203">L'azione eseguita non è specificata.</span><span class="sxs-lookup"><span data-stu-id="95d28-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d28-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="95d28-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95d28-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-207">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita")</span><span class="sxs-lookup"><span data-stu-id="95d28-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-208">Definizione di eventuali problemi riscontrati durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="95d28-209">Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="95d28-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="95d28-210">Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="95d28-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="95d28-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95d28-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-212">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95d28-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-214">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="95d28-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-215">L'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="95d28-215">Object was installed.</span></span> <span data-ttu-id="95d28-216">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="95d28-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="95d28-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-218">**Nome**</span><span class="sxs-lookup"><span data-stu-id="95d28-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-221">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="95d28-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="95d28-222">Identificatore univoco del servizio, che fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="95d28-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="95d28-223">Questa funzionalità è descritta più dettagliatamente nella proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95d28-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="95d28-224">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="95d28-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-226">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-228">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome percorso file")</span><span class="sxs-lookup"><span data-stu-id="95d28-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-229">Percorso completo del file binario del servizio che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="95d28-230">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="95d28-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="95d28-231">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="95d28-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-232">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95d28-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-234">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita specifico del server")</span><span class="sxs-lookup"><span data-stu-id="95d28-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-235">Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="95d28-236">I codici di uscita sono definiti dal servizio rappresentato da questa classe.</span><span class="sxs-lookup"><span data-stu-id="95d28-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="95d28-237">Questo valore viene impostato solo quando il valore **ExitCodeproperty** è **\_ \_ \_ errore specifico del servizio di errore** (1066).</span><span class="sxs-lookup"><span data-stu-id="95d28-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="95d28-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-241">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di servizio")</span><span class="sxs-lookup"><span data-stu-id="95d28-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-242">Servizio fornito ai processi chiamante.</span><span class="sxs-lookup"><span data-stu-id="95d28-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="95d28-243">**Driver del kernel** ("driver del kernel")</span><span class="sxs-lookup"><span data-stu-id="95d28-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="95d28-244">**Driver del file System** ("driver del file System")</span><span class="sxs-lookup"><span data-stu-id="95d28-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="95d28-245">**Adapter** ("adapter")</span><span class="sxs-lookup"><span data-stu-id="95d28-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="95d28-246">**Driver di riconoscimento** ("driver di riconoscimento")</span><span class="sxs-lookup"><span data-stu-id="95d28-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="95d28-247">**Processo personale** ("processo personalizzato")</span><span class="sxs-lookup"><span data-stu-id="95d28-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="95d28-248">**Processo di condivisione** ("processo di condivisione")</span><span class="sxs-lookup"><span data-stu-id="95d28-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="95d28-249">**Processo interattivo** ("processo interattivo")</span><span class="sxs-lookup"><span data-stu-id="95d28-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95d28-250">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="95d28-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95d28-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-253">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="95d28-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-254">Il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="95d28-254">Service has been started.</span></span>

<span data-ttu-id="95d28-255">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-256">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="95d28-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-259">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="95d28-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-260">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="95d28-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="95d28-261">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="95d28-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="95d28-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-263">Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).</span><span class="sxs-lookup"><span data-stu-id="95d28-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="95d28-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="95d28-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-265">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="95d28-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="95d28-266">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="95d28-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="95d28-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automatico** ("auto")</span><span class="sxs-lookup"><span data-stu-id="95d28-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-268">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="95d28-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="95d28-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="95d28-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-270">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="95d28-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95d28-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="95d28-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="95d28-272">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="95d28-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d28-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="95d28-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-276">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome account iniziale")</span><span class="sxs-lookup"><span data-stu-id="95d28-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-277">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-277">Account name under which the service runs.</span></span> <span data-ttu-id="95d28-278">A seconda del tipo di servizio, il nome dell'account può avere la forma di "DomainName \\ username" o del formato UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="95d28-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="95d28-279">Il processo del servizio verrà registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="95d28-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="95d28-280">Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="95d28-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="95d28-281">Se viene specificato **null** , il servizio verrà connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="95d28-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="95d28-282">Per i driver a livello di kernel o di sistema, **StartName** contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d28-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="95d28-283">Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="95d28-284">Esempio: "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="95d28-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="95d28-285">**State**</span><span class="sxs-lookup"><span data-stu-id="95d28-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-287">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="95d28-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="95d28-288">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("state")</span><span class="sxs-lookup"><span data-stu-id="95d28-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-289">Stato corrente del servizio di base.</span><span class="sxs-lookup"><span data-stu-id="95d28-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="95d28-290">**Arrestato** ("arrestato")</span><span class="sxs-lookup"><span data-stu-id="95d28-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="95d28-291">**Avvio in sospeso** ("avvio in sospeso")</span><span class="sxs-lookup"><span data-stu-id="95d28-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="95d28-292">**Arresta in sospeso** ("arresta in sospeso")</span><span class="sxs-lookup"><span data-stu-id="95d28-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="95d28-293">**In esecuzione** ("Running")</span><span class="sxs-lookup"><span data-stu-id="95d28-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="95d28-294">**Continua in sospeso** ("continua in sospeso")</span><span class="sxs-lookup"><span data-stu-id="95d28-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="95d28-295">**Sospensione in sospeso** ("pausa in sospeso")</span><span class="sxs-lookup"><span data-stu-id="95d28-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="95d28-296">**Sospesa** ("sospesa")</span><span class="sxs-lookup"><span data-stu-id="95d28-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95d28-297">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="95d28-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="95d28-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="95d28-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="95d28-299">**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="95d28-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="95d28-300">**Status**</span><span class="sxs-lookup"><span data-stu-id="95d28-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-303">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="95d28-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-304">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95d28-304">Current status of the object.</span></span> <span data-ttu-id="95d28-305">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="95d28-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="95d28-306">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="95d28-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="95d28-307">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="95d28-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="95d28-308">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="95d28-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="95d28-309">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="95d28-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="95d28-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="95d28-311">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="95d28-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="95d28-312">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="95d28-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="95d28-313">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="95d28-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95d28-314">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="95d28-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95d28-315">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="95d28-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="95d28-316">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="95d28-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="95d28-317">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="95d28-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="95d28-318">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="95d28-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="95d28-319">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="95d28-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="95d28-320">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="95d28-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="95d28-321">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="95d28-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="95d28-322">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="95d28-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="95d28-323">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="95d28-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95d28-324">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95d28-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-327">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="95d28-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-328">Nome del tipo di sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="95d28-329">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="95d28-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95d28-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-333">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="95d28-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-334">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="95d28-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="95d28-335">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d28-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="95d28-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d28-337">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95d28-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95d28-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95d28-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d28-339">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID tag")</span><span class="sxs-lookup"><span data-stu-id="95d28-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="95d28-340">Valore di tag univoco per il servizio nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="95d28-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="95d28-341">Il valore 0 (zero) indica che al servizio non è stato assegnato un tag.</span><span class="sxs-lookup"><span data-stu-id="95d28-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="95d28-342">Un tag può essere usato per ordinare impostato a stella del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in: HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList.</span><span class="sxs-lookup"><span data-stu-id="95d28-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="95d28-343">I tag vengono valutati solo per i servizi del driver del kernel e del driver del file System di avvio con modalità di avvio o di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="95d28-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d28-344">Commenti</span><span class="sxs-lookup"><span data-stu-id="95d28-344">Remarks</span></span>

<span data-ttu-id="95d28-345">La classe **Win32 \_ BaseService** deriva dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="95d28-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95d28-346">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d28-346">Requirements</span></span>



| <span data-ttu-id="95d28-347">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d28-347">Requirement</span></span> | <span data-ttu-id="95d28-348">Valore</span><span class="sxs-lookup"><span data-stu-id="95d28-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d28-349">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d28-349">Minimum supported client</span></span><br/> | <span data-ttu-id="95d28-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d28-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95d28-351">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d28-351">Minimum supported server</span></span><br/> | <span data-ttu-id="95d28-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d28-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95d28-353">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95d28-353">Namespace</span></span><br/>                | <span data-ttu-id="95d28-354">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="95d28-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95d28-355">MOF</span><span class="sxs-lookup"><span data-stu-id="95d28-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95d28-356"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95d28-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95d28-357">DLL</span><span class="sxs-lookup"><span data-stu-id="95d28-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d28-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d28-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d28-359">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d28-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d28-360">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="95d28-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="95d28-361">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95d28-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

