---
description: Rappresenta il servizio di migrazione del sistema virtuale. Viene utilizzato per la migrazione di un sistema virtuale o per la migrazione dell'archiviazione di un sistema virtuale da una piattaforma di virtualizzazione a un'altra.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750154"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="8a904-104">\_Classe MSVM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="8a904-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="8a904-105">Rappresenta il servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="8a904-106">Viene utilizzato per la migrazione di un sistema virtuale o per la migrazione dell'archiviazione di un sistema virtuale da una piattaforma di virtualizzazione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="8a904-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="8a904-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8a904-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a904-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a904-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="8a904-109">Members</span><span class="sxs-lookup"><span data-stu-id="8a904-109">Members</span></span>

<span data-ttu-id="8a904-110">La **classe \_ VirtualSystemMigrationService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8a904-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="8a904-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8a904-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8a904-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a904-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8a904-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="8a904-113">Methods</span></span>

<span data-ttu-id="8a904-114">La **classe \_ VirtualSystemMigrationService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8a904-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="8a904-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="8a904-115">Method</span></span>                                                                                                                  | <span data-ttu-id="8a904-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a904-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a904-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="8a904-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="8a904-118">Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="8a904-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="8a904-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="8a904-120">Verifica le informazioni di compatibilità per la compatibilità con il sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="8a904-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="8a904-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="8a904-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="8a904-122">Metodo per eseguire la migrazione di un sistema virtuale o l'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.</span><span class="sxs-lookup"><span data-stu-id="8a904-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="8a904-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="8a904-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="8a904-124">Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un host di destinazione specificato da un nome di rete o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="8a904-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="8a904-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="8a904-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="8a904-126">Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="8a904-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="8a904-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="8a904-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="8a904-128">Ottiene i vettori di compatibilità per una macchina virtuale o un host.</span><span class="sxs-lookup"><span data-stu-id="8a904-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="8a904-129">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8a904-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="8a904-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="8a904-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="8a904-131">Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.</span><span class="sxs-lookup"><span data-stu-id="8a904-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="8a904-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="8a904-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="8a904-133">Consente di spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8a904-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="8a904-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="8a904-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="8a904-135">Modifica le subnet della rete di migrazione del servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="8a904-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="8a904-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="8a904-137">Modifica i dati dell'impostazione per il servizio di migrazione.</span><span class="sxs-lookup"><span data-stu-id="8a904-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="8a904-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="8a904-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="8a904-139">Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="8a904-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8a904-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="8a904-141">Richiede una modifica dello stato</span><span class="sxs-lookup"><span data-stu-id="8a904-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="8a904-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="8a904-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="8a904-143">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="8a904-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="8a904-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="8a904-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="8a904-145">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="8a904-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="8a904-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a904-146">Properties</span></span>

<span data-ttu-id="8a904-147">La **classe \_ VirtualSystemMigrationService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a904-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a904-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="8a904-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a904-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-151">Il numero di migrazioni di archiviazione correnti in corso.</span><span class="sxs-lookup"><span data-stu-id="8a904-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="8a904-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a904-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-155">Il numero di migrazioni correnti del sistema virtuale in corso.</span><span class="sxs-lookup"><span data-stu-id="8a904-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8a904-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-157">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a904-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-159">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8a904-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8a904-160">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a904-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-161">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8a904-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-164">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8a904-164">A short description of the object.</span></span> <span data-ttu-id="8a904-165">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="8a904-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8a904-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-169">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="8a904-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8a904-170">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8a904-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a904-171">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a904-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a904-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-175">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="8a904-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8a904-176">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ VirtualSystemMigrationService".</span><span class="sxs-lookup"><span data-stu-id="8a904-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-177">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8a904-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-180">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="8a904-180">A description of the object.</span></span> <span data-ttu-id="8a904-181">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="8a904-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8a904-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-185">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="8a904-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8a904-186">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8a904-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a904-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a904-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8a904-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-191">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8a904-191">A display name for the object.</span></span> <span data-ttu-id="8a904-192">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="8a904-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8a904-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-194">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-196">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="8a904-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8a904-197">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="8a904-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8a904-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-201">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="8a904-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8a904-202">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="8a904-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8a904-203">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="8a904-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8a904-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-205">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-207">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8a904-207">The current health of the element.</span></span> <span data-ttu-id="8a904-208">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="8a904-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8a904-209">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="8a904-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8a904-210">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="8a904-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8a904-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-212">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a904-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-214">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8a904-215">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a904-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a904-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a904-219">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="8a904-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8a904-220">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="8a904-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8a904-221">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8a904-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="8a904-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-223">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8a904-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a904-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-225">Elenco di indirizzi IP host che possono essere utilizzati per la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a904-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8a904-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-229">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="8a904-229">The label by which the object is known.</span></span> <span data-ttu-id="8a904-230">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "migrationwmi".</span><span class="sxs-lookup"><span data-stu-id="8a904-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8a904-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-232">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-234">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8a904-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8a904-235">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8a904-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a904-236">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a904-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8a904-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-238">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a904-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-240">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8a904-240">The current statuses of the object.</span></span> <span data-ttu-id="8a904-241">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="8a904-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8a904-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-245">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="8a904-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8a904-246">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="8a904-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8a904-247">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8a904-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="8a904-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-251">Valore che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="8a904-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="8a904-252">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8a904-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="8a904-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-256">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="8a904-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="8a904-257">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="8a904-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="8a904-258">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8a904-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8a904-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-260">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-262">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="8a904-262">Provides high level status information.</span></span> <span data-ttu-id="8a904-263">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="8a904-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8a904-264">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8a904-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a904-265">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a904-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8a904-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-269">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="8a904-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="8a904-270">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8a904-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8a904-271">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8a904-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8a904-272">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8a904-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="8a904-273">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="8a904-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="8a904-274">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="8a904-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-275">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="8a904-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-276">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a904-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-278">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8a904-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="8a904-279">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a904-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-280">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="8a904-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-283">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="8a904-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="8a904-284">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8a904-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8a904-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="8a904-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="8a904-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8a904-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-290">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8a904-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a904-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-292">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8a904-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8a904-293">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e le stringhe sono sempre impostate su "OK".</span><span class="sxs-lookup"><span data-stu-id="8a904-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a904-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-297">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8a904-297">The scoping system's creation class name.</span></span> <span data-ttu-id="8a904-298">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="8a904-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="8a904-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8a904-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a904-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-302">Nome del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="8a904-302">The name of the hosting computer system.</span></span> <span data-ttu-id="8a904-303">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a904-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8a904-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-305">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a904-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-307">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8a904-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8a904-308">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a904-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a904-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8a904-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a904-310">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a904-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a904-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a904-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a904-312">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8a904-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8a904-313">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a904-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a904-314">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a904-314">Requirements</span></span>



| <span data-ttu-id="8a904-315">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a904-315">Requirement</span></span> | <span data-ttu-id="8a904-316">Valore</span><span class="sxs-lookup"><span data-stu-id="8a904-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a904-317">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a904-317">Minimum supported client</span></span><br/> | <span data-ttu-id="8a904-318">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8a904-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a904-319">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a904-319">Minimum supported server</span></span><br/> | <span data-ttu-id="8a904-320">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8a904-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a904-321">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a904-321">Namespace</span></span><br/>                | <span data-ttu-id="8a904-322">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a904-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a904-323">MOF</span><span class="sxs-lookup"><span data-stu-id="8a904-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a904-324"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a904-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a904-325">DLL</span><span class="sxs-lookup"><span data-stu-id="8a904-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a904-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a904-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

