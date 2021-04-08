---
description: Rappresenta il driver di sistema per un servizio di base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748402"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="a06cb-103">Win32 \_ SystemDriver (classe)</span><span class="sxs-lookup"><span data-stu-id="a06cb-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="a06cb-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriver Win32** rappresenta il driver di sistema per un servizio di base.</span><span class="sxs-lookup"><span data-stu-id="a06cb-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="a06cb-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a06cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a06cb-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a06cb-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a06cb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a06cb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="a06cb-108">Members</span><span class="sxs-lookup"><span data-stu-id="a06cb-108">Members</span></span>

<span data-ttu-id="a06cb-109">La classe **Win32 \_ SystemDriver** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a06cb-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="a06cb-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a06cb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a06cb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a06cb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a06cb-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a06cb-112">Methods</span></span>

<span data-ttu-id="a06cb-113">La classe **Win32 \_ SystemDriver** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a06cb-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="a06cb-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a06cb-114">Method</span></span>                                                                              | <span data-ttu-id="a06cb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a06cb-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a06cb-116">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="a06cb-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="a06cb-117">Metodo della classe che modifica un servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="a06cb-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="a06cb-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="a06cb-119">Metodo della classe che modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="a06cb-120">**Creare**</span><span class="sxs-lookup"><span data-stu-id="a06cb-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="a06cb-121">Metodo della classe che crea un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="a06cb-122">**Delete**</span><span class="sxs-lookup"><span data-stu-id="a06cb-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="a06cb-123">Metodo della classe che elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="a06cb-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="a06cb-124">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="a06cb-125">Metodo della classe che richiede che il servizio aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="a06cb-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="a06cb-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="a06cb-127">Metodo della classe che tenta di collocare il servizio nello stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="a06cb-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="a06cb-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="a06cb-129">Metodo della classe che tenta di collocare il servizio nello stato ripreso.</span><span class="sxs-lookup"><span data-stu-id="a06cb-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="a06cb-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="a06cb-131">Metodo della classe che tenta di collocare il servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="a06cb-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="a06cb-133">Metodo della classe che inserisce il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="a06cb-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="a06cb-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="a06cb-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="a06cb-135">Metodo della classe che tenta di inviare un codice di controllo definito dall'utente a un servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="a06cb-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a06cb-136">Properties</span></span>

<span data-ttu-id="a06cb-137">La classe **Win32 \_ SystemDriver** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a06cb-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a06cb-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="a06cb-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a06cb-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-141">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("servizio accetta pausa")</span><span class="sxs-lookup"><span data-stu-id="a06cb-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-142">Il servizio può essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="a06cb-142">Service can be paused.</span></span>

<span data-ttu-id="a06cb-143">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="a06cb-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a06cb-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-147">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service accepts stop")</span><span class="sxs-lookup"><span data-stu-id="a06cb-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-148">Il servizio può essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-148">Service can be stopped.</span></span>

<span data-ttu-id="a06cb-149">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-150">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a06cb-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-153">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a06cb-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-154">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a06cb-154">Short description of the object.</span></span>

<span data-ttu-id="a06cb-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-159">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="a06cb-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-160">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a06cb-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a06cb-161">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a06cb-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a06cb-162">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-163">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a06cb-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-166">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a06cb-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-167">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a06cb-167">Description of the object.</span></span>

<span data-ttu-id="a06cb-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="a06cb-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a06cb-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-172">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("interagisce con il desktop")</span><span class="sxs-lookup"><span data-stu-id="a06cb-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-173">Questo servizio può creare o comunicare con Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="a06cb-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="a06cb-174">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-178">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span><span class="sxs-lookup"><span data-stu-id="a06cb-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-179">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-179">Display name of the service.</span></span> <span data-ttu-id="a06cb-180">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a06cb-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="a06cb-181">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="a06cb-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="a06cb-182">I confronti **DisplayName** sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a06cb-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="a06cb-183">Constraints: accetta lo stesso valore della proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="a06cb-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="a06cb-184">Esempio: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="a06cb-184">Example: "Atdisk"</span></span>

<span data-ttu-id="a06cb-185">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="a06cb-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-189">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravità dell'avvio non riuscito")</span><span class="sxs-lookup"><span data-stu-id="a06cb-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-190">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="a06cb-191">Questo valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a06cb-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="a06cb-192">Tutti gli errori vengono registrati dal computer.</span><span class="sxs-lookup"><span data-stu-id="a06cb-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="a06cb-193">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="a06cb-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")</span><span class="sxs-lookup"><span data-stu-id="a06cb-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-195">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="a06cb-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")</span><span class="sxs-lookup"><span data-stu-id="a06cb-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-197">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="a06cb-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="a06cb-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-199">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="a06cb-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a06cb-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")</span><span class="sxs-lookup"><span data-stu-id="a06cb-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-201">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="a06cb-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a06cb-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-203">La cause dell'errore è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="a06cb-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a06cb-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="a06cb-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a06cb-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-207">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita")</span><span class="sxs-lookup"><span data-stu-id="a06cb-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-208">Codice di errore di Windows che definisce eventuali problemi riscontrati durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="a06cb-209">Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="a06cb-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="a06cb-210">Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="a06cb-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="a06cb-211">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a06cb-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-213">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a06cb-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-215">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a06cb-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-216">L'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-216">Object was installed.</span></span> <span data-ttu-id="a06cb-217">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a06cb-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-219">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a06cb-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-222">Qualificatori: [ **chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="a06cb-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-223">Identificatore univoco per il servizio che fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="a06cb-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="a06cb-224">Questa funzionalità è descritta più dettagliatamente nella proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a06cb-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="a06cb-225">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-229">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome percorso file")</span><span class="sxs-lookup"><span data-stu-id="a06cb-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-230">Percorso completo del file binario del servizio che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="a06cb-231">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="a06cb-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="a06cb-232">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-233">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="a06cb-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-234">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a06cb-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-236">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita specifico del server")</span><span class="sxs-lookup"><span data-stu-id="a06cb-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-237">Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="a06cb-238">I codici di uscita sono definiti dal servizio rappresentato da questa classe.</span><span class="sxs-lookup"><span data-stu-id="a06cb-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="a06cb-239">Questo valore viene impostato solo quando il valore della proprietà **ExitCode** è **\_ \_ \_ errore specifico del servizio di errore** (1066).</span><span class="sxs-lookup"><span data-stu-id="a06cb-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="a06cb-240">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="a06cb-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-244">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo di servizio")</span><span class="sxs-lookup"><span data-stu-id="a06cb-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-245">Tipo di servizio fornito ai processi chiamanti.</span><span class="sxs-lookup"><span data-stu-id="a06cb-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="a06cb-246">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="a06cb-247">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a06cb-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="a06cb-248">**Driver del kernel** ("driver del kernel")</span><span class="sxs-lookup"><span data-stu-id="a06cb-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="a06cb-249">**Driver del file System** ("driver del file System")</span><span class="sxs-lookup"><span data-stu-id="a06cb-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="a06cb-250">**Adapter** ("adapter")</span><span class="sxs-lookup"><span data-stu-id="a06cb-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="a06cb-251">**Driver di riconoscimento** ("driver di riconoscimento")</span><span class="sxs-lookup"><span data-stu-id="a06cb-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="a06cb-252">**Processo personale** ("processo personalizzato")</span><span class="sxs-lookup"><span data-stu-id="a06cb-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="a06cb-253">**Processo di condivisione** ("processo di condivisione")</span><span class="sxs-lookup"><span data-stu-id="a06cb-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="a06cb-254">**Processo interattivo** ("processo interattivo")</span><span class="sxs-lookup"><span data-stu-id="a06cb-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a06cb-255">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="a06cb-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-256">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a06cb-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-258">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="a06cb-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-259">Il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-259">Service has been started.</span></span>

<span data-ttu-id="a06cb-260">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-261">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="a06cb-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-264">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="a06cb-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-265">Modalità di avvio del driver di sistema.</span><span class="sxs-lookup"><span data-stu-id="a06cb-265">Start mode of the system driver.</span></span>

<span data-ttu-id="a06cb-266">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="a06cb-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a06cb-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-268">Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).</span><span class="sxs-lookup"><span data-stu-id="a06cb-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="a06cb-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="a06cb-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-270">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a06cb-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="a06cb-271">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="a06cb-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="a06cb-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automatico** ("auto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-273">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a06cb-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="a06cb-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="a06cb-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-275">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="a06cb-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a06cb-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="a06cb-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="a06cb-277">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="a06cb-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a06cb-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-281">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome account iniziale")</span><span class="sxs-lookup"><span data-stu-id="a06cb-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-282">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-282">Account name under which the service runs.</span></span> <span data-ttu-id="a06cb-283">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username.</span><span class="sxs-lookup"><span data-stu-id="a06cb-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="a06cb-284">Il processo del servizio verrà registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a06cb-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="a06cb-285">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="a06cb-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="a06cb-286">Se viene specificato **null** , il servizio verrà connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a06cb-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="a06cb-287">Per i driver a livello di kernel o di sistema, **StartName** contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a06cb-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="a06cb-288">Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="a06cb-289">Esempio: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="a06cb-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="a06cb-290">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-291">**State**</span><span class="sxs-lookup"><span data-stu-id="a06cb-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-293">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a06cb-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-294">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("state")</span><span class="sxs-lookup"><span data-stu-id="a06cb-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-295">Stato corrente del servizio di base.</span><span class="sxs-lookup"><span data-stu-id="a06cb-295">Current state of the base service.</span></span>

<span data-ttu-id="a06cb-296">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="a06cb-297">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a06cb-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="a06cb-298">**Arrestato** ("arrestato")</span><span class="sxs-lookup"><span data-stu-id="a06cb-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="a06cb-299">**Avvio in sospeso** ("avvio in sospeso")</span><span class="sxs-lookup"><span data-stu-id="a06cb-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="a06cb-300">**Arresta in sospeso** ("arresta in sospeso")</span><span class="sxs-lookup"><span data-stu-id="a06cb-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a06cb-301">**In esecuzione** ("Running")</span><span class="sxs-lookup"><span data-stu-id="a06cb-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="a06cb-302">**Continua in sospeso** ("continua in sospeso")</span><span class="sxs-lookup"><span data-stu-id="a06cb-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="a06cb-303">**Sospensione in sospeso** ("pausa in sospeso")</span><span class="sxs-lookup"><span data-stu-id="a06cb-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a06cb-304">**Sospesa** ("sospesa")</span><span class="sxs-lookup"><span data-stu-id="a06cb-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a06cb-305">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a06cb-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="a06cb-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-309">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a06cb-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-310">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a06cb-310">Current status of the object.</span></span> <span data-ttu-id="a06cb-311">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="a06cb-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a06cb-312">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="a06cb-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a06cb-313">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a06cb-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a06cb-314">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a06cb-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a06cb-315">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a06cb-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a06cb-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a06cb-317">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a06cb-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a06cb-318">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a06cb-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a06cb-319">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a06cb-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a06cb-320">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a06cb-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a06cb-321">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a06cb-322">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a06cb-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a06cb-323">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a06cb-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a06cb-324">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a06cb-325">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a06cb-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a06cb-326">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a06cb-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a06cb-327">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a06cb-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a06cb-328">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a06cb-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a06cb-329">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a06cb-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a06cb-330">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-333">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="a06cb-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-334">Nome del tipo di sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="a06cb-335">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a06cb-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a06cb-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-339">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="a06cb-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-340">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="a06cb-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="a06cb-341">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a06cb-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="a06cb-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a06cb-343">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a06cb-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a06cb-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a06cb-345">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID tag")</span><span class="sxs-lookup"><span data-stu-id="a06cb-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="a06cb-346">Valore di tag univoco per il servizio nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="a06cb-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="a06cb-347">Il valore 0 (zero) indica che al servizio non è stato assegnato un tag.</span><span class="sxs-lookup"><span data-stu-id="a06cb-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="a06cb-348">Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:</span><span class="sxs-lookup"><span data-stu-id="a06cb-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="a06cb-349">Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="a06cb-350">**HKEY \_ \_GroupOrderList del \\ \\ \\ \\ controllo del sistema CurrentControlSet del computer locale**.</span><span class="sxs-lookup"><span data-stu-id="a06cb-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="a06cb-351">I tag vengono valutati solo per i servizi del driver del kernel e del driver del file System di avvio con modalità di avvio o di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a06cb-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a06cb-352">Commenti</span><span class="sxs-lookup"><span data-stu-id="a06cb-352">Remarks</span></span>

<span data-ttu-id="a06cb-353">La classe **Win32 \_ SystemDriver** è derivata da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="a06cb-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a06cb-354">Esempio</span><span class="sxs-lookup"><span data-stu-id="a06cb-354">Examples</span></span>

<span data-ttu-id="a06cb-355">Nell'esempio [elenco driver di sistema](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript vengono visualizzati i driver di sistema installati in un file HTML.</span><span class="sxs-lookup"><span data-stu-id="a06cb-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="a06cb-356">Nell'esempio di PowerShell seguente vengono recuperate alcune proprietà dai driver di sistema in esecuzione in un computer.</span><span class="sxs-lookup"><span data-stu-id="a06cb-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="a06cb-357">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a06cb-357">Requirements</span></span>



| <span data-ttu-id="a06cb-358">Requisito</span><span class="sxs-lookup"><span data-stu-id="a06cb-358">Requirement</span></span> | <span data-ttu-id="a06cb-359">Valore</span><span class="sxs-lookup"><span data-stu-id="a06cb-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a06cb-360">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06cb-360">Minimum supported client</span></span><br/> | <span data-ttu-id="a06cb-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a06cb-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a06cb-362">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06cb-362">Minimum supported server</span></span><br/> | <span data-ttu-id="a06cb-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a06cb-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a06cb-364">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a06cb-364">Namespace</span></span><br/>                | <span data-ttu-id="a06cb-365">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a06cb-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a06cb-366">MOF</span><span class="sxs-lookup"><span data-stu-id="a06cb-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a06cb-367"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a06cb-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a06cb-368">DLL</span><span class="sxs-lookup"><span data-stu-id="a06cb-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a06cb-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a06cb-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06cb-370">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a06cb-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a06cb-371">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="a06cb-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="a06cb-372">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a06cb-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
