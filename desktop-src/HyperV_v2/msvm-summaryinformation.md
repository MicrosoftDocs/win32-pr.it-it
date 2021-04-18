---
description: Utilizzato nei metodi GetSummaryInformation e GetDefinitionFileSummaryInformation della \_ classe MSVM VirtualSystemManagementService per recuperare rapidamente informazioni comuni relative a una macchina virtuale o a uno snapshot.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Classe Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307873"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="e756d-103">\_Classe MSVM SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="e756d-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="e756d-104">Utilizzato nei metodi [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) e [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per recuperare rapidamente informazioni comuni relative a una macchina virtuale o a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="e756d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF).</span><span class="sxs-lookup"><span data-stu-id="e756d-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e756d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e756d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="e756d-107">Members</span><span class="sxs-lookup"><span data-stu-id="e756d-107">Members</span></span>

<span data-ttu-id="e756d-108">La **classe \_ SummaryInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e756d-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="e756d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e756d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e756d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e756d-110">Properties</span></span>

<span data-ttu-id="e756d-111">La **classe \_ SummaryInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e756d-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e756d-112">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="e756d-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-115">Identificatore della GPU (Graphics Processing Unit) fisica allocata a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="e756d-116">Questa proprietà si applica solo alle macchine virtuali che usano RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="e756d-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-117">**ApplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="e756d-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-120">Stato di integrità dell'applicazione corrente per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="e756d-121">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e756d-122">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="e756d-123">**Applicazione critica** (32782)</span><span class="sxs-lookup"><span data-stu-id="e756d-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e756d-124">**Disabilitato** (32896)</span><span class="sxs-lookup"><span data-stu-id="e756d-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-125">**AsynchronousTasks**</span><span class="sxs-lookup"><span data-stu-id="e756d-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-126">Tipo di dati: **CIM \_ ConcreteJob** Array</span><span class="sxs-lookup"><span data-stu-id="e756d-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-128">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-129">Matrice di istanze [**di \_ ConcreteJob MSVM**](msvm-concretejob.md) che rappresentano le operazioni asincrone correlate alla macchina virtuale attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e756d-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="e756d-130">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-131">**AvailableMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="e756d-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e756d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-134">Percentuale di buffer di memoria disponibile per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="e756d-135">Quando la memoria dinamica è abilitata per una macchina virtuale, questa proprietà rappresenta il rapporto tra il buffer di memoria disponibile e il buffer di memoria ideale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="e756d-136">Le dimensioni di buffer di memoria ideali vengono configurate utilizzando la proprietà **TargetMemoryBuffer** della classe [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="e756d-137">Questa proprietà non è valida per le istanze della classe **MSVM \_ SummaryInformation** che rappresentano macchine virtuali per cui la memoria dinamica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e756d-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="e756d-138">Questa proprietà non è valida per le istanze della classe **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="e756d-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e756d-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-142">Ora in cui è stata creata la macchina virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e756d-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-146">Nome visualizzato per la macchina virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e756d-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-150">Stato corrente della macchina virtuale o dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="e756d-151">Per i valori possibili, vedere la proprietà **EnabledState** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-152">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="e756d-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-155">Indica se le connessioni in modalità avanzata sono consentite dall'host e, se consentito, se sono disponibili per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="e756d-156">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e756d-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="e756d-157">**Consentito e disponibile** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="e756d-158">**Non consentito** (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="e756d-159">**Consentito ma non disponibile** (6)</span><span class="sxs-lookup"><span data-stu-id="e756d-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-160">**GuestOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e756d-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-163">Nome del sistema operativo guest, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="e756d-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="e756d-164">Se queste informazioni non sono disponibili, il valore di questa proprietà è **null**.</span><span class="sxs-lookup"><span data-stu-id="e756d-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="e756d-165">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e756d-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-169">Stato di integrità corrente per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="e756d-170">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-171">**Heartbeat**</span><span class="sxs-lookup"><span data-stu-id="e756d-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-174">Stato heartbeat corrente per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="e756d-175">Per ulteriori informazioni, vedere la documentazione relativa alla proprietà [**StatusDescriptions**](msvm-heartbeatcomponent.md) della classe **MSVM \_ HeartbeatComponent** .</span><span class="sxs-lookup"><span data-stu-id="e756d-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="e756d-176">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="e756d-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e756d-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (6)</span><span class="sxs-lookup"><span data-stu-id="e756d-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e756d-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)</span><span class="sxs-lookup"><span data-stu-id="e756d-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e756d-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)</span><span class="sxs-lookup"><span data-stu-id="e756d-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e756d-181">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="e756d-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-184">Nome del computer che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-185">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e756d-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e756d-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-189">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managed. InstanceId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e756d-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e756d-190">InstanceID è una proprietà facoltativa che può essere utilizzata per identificare in modo opaco e univoco un'istanza di questa classe nell'ambito dello spazio dei nomi di creazione di istanze.</span><span class="sxs-lookup"><span data-stu-id="e756d-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="e756d-191">Varie sottoclassi di questa classe possono eseguire l'override di questa proprietà per renderla obbligatoria o una chiave.</span><span class="sxs-lookup"><span data-stu-id="e756d-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="e756d-192">Tali sottoclassi possono anche modificare gli algoritmi preferiti per garantire l'univocità definita di seguito.</span><span class="sxs-lookup"><span data-stu-id="e756d-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="e756d-193">Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente:</span><span class="sxs-lookup"><span data-stu-id="e756d-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="e756d-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="e756d-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="e756d-195">Dove <OrgID> e <LocalID> sono separati da due punti (:) e dove <OrgID> devono includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità business da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e756d-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="e756d-196">(Questo requisito è simile al <Schema Name> \_ <Class Name> struttura dei nomi delle classi dello schema. Per garantire l'univocità, inoltre, <OrgID> non deve contenere i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="e756d-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="e756d-197">Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra <OrgID> e <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="e756d-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="e756d-198"><LocalID> viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="e756d-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="e756d-199">Se non è null e l'algoritmo "preferito" precedente non viene utilizzato, l'entità di definizione deve garantire che l'ID istanza risultante non venga riutilizzato tra le InstanceID prodotte da questo o da altri provider per lo spazio dei nomi di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="e756d-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="e756d-200">Se non è impostato su null per le istanze definite da DMTF, è necessario usare l'algoritmo "preferito" con <OrgID> impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="e756d-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-201">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e756d-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-202">**IntegrationServicesVersionState**</span><span class="sxs-lookup"><span data-stu-id="e756d-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-205">Indica se i servizi di integrazione installati nella macchina virtuale sono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="e756d-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e756d-206">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="e756d-207">**Uptodate** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="e756d-208">**Mancata corrispondenza** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-209">**MemoryAvailable**</span><span class="sxs-lookup"><span data-stu-id="e756d-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-210">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e756d-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-212">Percentuale della memoria corrente disponibile per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="e756d-213">Quando la memoria dinamica è abilitata per una macchina virtuale, questa proprietà rappresenta il rapporto tra la memoria disponibile della macchina virtuale e la memoria fisica totale assegnata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="e756d-214">Quando una macchina virtuale non dispone di memoria disponibile, questa proprietà sarà negativa e conterrà il rapporto tra la memoria necessaria per la macchina virtuale e la memoria fisica totale assegnata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="e756d-215">Questa proprietà non è valida per le istanze della classe **MSVM \_ SummaryInformation** che rappresentano macchine virtuali per cui la memoria dinamica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e756d-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="e756d-216">Questa proprietà non è valida per le istanze della classe **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-217">**MemorySpansPhysicalNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="e756d-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-218">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e756d-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-220">Indica se la memoria di uno o più nodi NUMA (Virtual nonuniform Memory Access) della macchina virtuale si estende su più nodi NUMA fisici del sistema del computer host.</span><span class="sxs-lookup"><span data-stu-id="e756d-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="e756d-221">Contiene **true** se la memoria si estende su più nodi NUMA fisici o su **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e756d-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="e756d-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-223">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e756d-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-225">Utilizzo corrente della memoria, in megabyte, della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="e756d-226">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-227">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e756d-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-230">Nome univoco per la macchina virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-231">**Note**</span><span class="sxs-lookup"><span data-stu-id="e756d-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-234">Note associate alla macchina virtuale o allo snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="e756d-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-236">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-238">Numero totale di processori virtuali allocati alla macchina virtuale o allo snapshot.</span><span class="sxs-lookup"><span data-stu-id="e756d-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e756d-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-240">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-242">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-243">Stati operativi correnti della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="e756d-244">Per i valori possibili, vedere la proprietà **OperationalStatus** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-245">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e756d-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-248">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="e756d-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="e756d-249">Questa proprietà verrà impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e756d-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-250">**ProcessorLoad**</span><span class="sxs-lookup"><span data-stu-id="e756d-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-251">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-253">Utilizzo corrente del processore della macchina virtuale, in percentuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="e756d-254">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-255">**ProcessorLoadHistory**</span><span class="sxs-lookup"><span data-stu-id="e756d-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-256">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-258">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-259">Matrice dei precedenti 100 esempi di utilizzo del processore, in percentuale, per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="e756d-260">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="e756d-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-262">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-264">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationHealthEx**")</span><span class="sxs-lookup"><span data-stu-id="e756d-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-265">Stato di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="e756d-266">Per i valori possibili, vedere la proprietà **ReplicationHealth** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-267">Questa proprietà è deprecata a partire da Windows 8.1; usare invece **ReplicationHealthEx**.</span><span class="sxs-lookup"><span data-stu-id="e756d-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e756d-268">**Non applicabile** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="e756d-269">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e756d-270">**Avviso** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e756d-271">**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-272">**ReplicationHealthEx**</span><span class="sxs-lookup"><span data-stu-id="e756d-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-273">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-275">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-276">Matrice di valori di integrità della replica per le varie relazioni di replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="e756d-277">Per i valori possibili, vedere la proprietà **ReplicationHealth** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e756d-278">**Non applicabile** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="e756d-279">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e756d-280">**Avviso** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e756d-281">**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="e756d-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-285">Tipo di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="e756d-286">Per i valori possibili, vedere la proprietà **ReplicationMode** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e756d-287">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="e756d-288">**Primario** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="e756d-289">**Replica** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="e756d-290">**Replica di test** (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="e756d-291">**Replica estesa** (4)</span><span class="sxs-lookup"><span data-stu-id="e756d-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="e756d-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-293">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e756d-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-295">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-296">Per la macchina virtuale di replica primaria o estesa, questo è l'ID del provider di replica primario.</span><span class="sxs-lookup"><span data-stu-id="e756d-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="e756d-297">Per una macchina virtuale di replica e se è abilitata la replica estesa, si tratta dell'ID provider per la relazione estesa.</span><span class="sxs-lookup"><span data-stu-id="e756d-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="e756d-298">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e756d-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="e756d-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-300">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-302">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationStateEx**")</span><span class="sxs-lookup"><span data-stu-id="e756d-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-303">Stato di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="e756d-304">Per i valori possibili, vedere la proprietà **ReplicationState** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-305">Questa proprietà è deprecata a partire da Windows 8.1; usare invece **ReplicationStateEx**.</span><span class="sxs-lookup"><span data-stu-id="e756d-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e756d-306">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="e756d-307">**Pronto per la replica** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="e756d-308">**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="e756d-309">**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="e756d-310">**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="e756d-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="e756d-311">**Ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="e756d-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="e756d-312">**Commit eseguito** (6)</span><span class="sxs-lookup"><span data-stu-id="e756d-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="e756d-313">**Sospeso** (7)</span><span class="sxs-lookup"><span data-stu-id="e756d-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e756d-314">**Critico** (8)</span><span class="sxs-lookup"><span data-stu-id="e756d-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="e756d-315">**In attesa dell'avvio della risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="e756d-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="e756d-316">**Risincronizzazione** (10)</span><span class="sxs-lookup"><span data-stu-id="e756d-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="e756d-317">**Risincronizzazione sospesa** (11)</span><span class="sxs-lookup"><span data-stu-id="e756d-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="e756d-318">**Failover in corso** (12)</span><span class="sxs-lookup"><span data-stu-id="e756d-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-319">**ReplicationStateEx**</span><span class="sxs-lookup"><span data-stu-id="e756d-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-320">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-322">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-323">Matrice di valori dello stato di replica per le varie relazioni di replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="e756d-324">Per i valori possibili, vedere la proprietà **ReplicationState** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e756d-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="e756d-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="e756d-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto per la replica** (1)</span><span class="sxs-lookup"><span data-stu-id="e756d-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="e756d-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="e756d-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="e756d-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="e756d-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="e756d-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="e756d-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="e756d-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="e756d-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="e756d-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Commit eseguito** (6)</span><span class="sxs-lookup"><span data-stu-id="e756d-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="e756d-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (7)</span><span class="sxs-lookup"><span data-stu-id="e756d-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e756d-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (8)</span><span class="sxs-lookup"><span data-stu-id="e756d-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="e756d-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**In attesa dell'avvio della risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="e756d-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="e756d-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (10)</span><span class="sxs-lookup"><span data-stu-id="e756d-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="e756d-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Risincronizzazione sospesa** (11)</span><span class="sxs-lookup"><span data-stu-id="e756d-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="e756d-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in corso** (12)</span><span class="sxs-lookup"><span data-stu-id="e756d-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="e756d-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in corso** (13)</span><span class="sxs-lookup"><span data-stu-id="e756d-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="e756d-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback completato** (14)</span><span class="sxs-lookup"><span data-stu-id="e756d-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="e756d-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Aggiornamento del disco in corso** (15)</span><span class="sxs-lookup"><span data-stu-id="e756d-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-341">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="e756d-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Aggiornamento del disco critico** (16)</span><span class="sxs-lookup"><span data-stu-id="e756d-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-343">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e756d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (17)</span><span class="sxs-lookup"><span data-stu-id="e756d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-345">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="e756d-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Riutilizzo della replica in corso** (18)</span><span class="sxs-lookup"><span data-stu-id="e756d-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-347">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="e756d-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparato per la replica di sincronizzazione** (19)</span><span class="sxs-lookup"><span data-stu-id="e756d-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-349">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="e756d-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparato per la replica inversa del gruppo** (20)</span><span class="sxs-lookup"><span data-stu-id="e756d-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-351">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="e756d-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**FireDrill in corso** (21)</span><span class="sxs-lookup"><span data-stu-id="e756d-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e756d-353">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e756d-354">**Schermato**</span><span class="sxs-lookup"><span data-stu-id="e756d-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-355">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e756d-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-357">Indica se la schermatura è configurata o meno per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-358">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e756d-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-359">**Snapshot**</span><span class="sxs-lookup"><span data-stu-id="e756d-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-360">Tipo di dati: **CIM \_ VirtualSystemSettingData** Array</span><span class="sxs-lookup"><span data-stu-id="e756d-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-362">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-363">Matrice di istanze [**di \_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresentano gli snapshot per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="e756d-364">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-365">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e756d-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-366">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e756d-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-368">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-369">Stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e756d-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="e756d-370">Corrisponde alla proprietà **StatusDescriptions** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e756d-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-371">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="e756d-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-372">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e756d-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-374">Indica se il paging di secondo livello è attivo.</span><span class="sxs-lookup"><span data-stu-id="e756d-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="e756d-375">Contiene **true** se il paging di secondo livello è attivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e756d-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-376">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="e756d-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-377">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e756d-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-379">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale di replica di test per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="e756d-380">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-381">**ThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="e756d-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-382">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e756d-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-384">Qualificatori: **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**ThumbnailImageHeight**")</span><span class="sxs-lookup"><span data-stu-id="e756d-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-385">Matrice che contiene un'immagine di piccole dimensioni di anteprima del desktop per la macchina virtuale o lo snapshot nel formato RGB565.</span><span class="sxs-lookup"><span data-stu-id="e756d-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-386">**ThumbnailImageHeight**</span><span class="sxs-lookup"><span data-stu-id="e756d-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-389">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="e756d-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-390">Altezza, in pixel, dell'immagine nella proprietà ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="e756d-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-391">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e756d-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="e756d-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-393">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e756d-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-395">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="e756d-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-396">Larghezza in pixel dell'immagine nella proprietà ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="e756d-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="e756d-397">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e756d-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-398">**Tempo**</span><span class="sxs-lookup"><span data-stu-id="e756d-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-399">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e756d-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-401">Quantità di tempo trascorsa dall'ultimo avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="e756d-402">Questa proprietà non è valida per le istanze di **MSVM \_ SummaryInformation** che rappresentano uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-403">**Versione**</span><span class="sxs-lookup"><span data-stu-id="e756d-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-404">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-406">Versione del sistema virtuale in formato "Major. minor", ad esempio "2,0".</span><span class="sxs-lookup"><span data-stu-id="e756d-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="e756d-407">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e756d-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e756d-408">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="e756d-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-409">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e756d-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e756d-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e756d-411">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e756d-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e756d-412">Stringhe che specificano i nomi descrittivi dei commutatori virtuali a cui è connessa la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="e756d-413">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e756d-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e756d-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="e756d-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e756d-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e756d-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e756d-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e756d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e756d-417">Sottotipo del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="e756d-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="e756d-418">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e756d-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="e756d-419">**Microsoft: Hyper-V: sottotipo: 1** ()</span><span class="sxs-lookup"><span data-stu-id="e756d-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="e756d-420">**Microsoft: Hyper-V: sottotipo: 2** ()</span><span class="sxs-lookup"><span data-stu-id="e756d-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="e756d-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e756d-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e756d-422">Commenti</span><span class="sxs-lookup"><span data-stu-id="e756d-422">Remarks</span></span>

<span data-ttu-id="e756d-423">L'accesso alla **classe \_ SummaryInformation di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e756d-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e756d-424">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e756d-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e756d-425">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e756d-425">Requirements</span></span>



| <span data-ttu-id="e756d-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="e756d-426">Requirement</span></span> | <span data-ttu-id="e756d-427">Valore</span><span class="sxs-lookup"><span data-stu-id="e756d-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e756d-428">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e756d-428">Minimum supported client</span></span><br/> | <span data-ttu-id="e756d-429">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e756d-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e756d-430">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e756d-430">Minimum supported server</span></span><br/> | <span data-ttu-id="e756d-431">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e756d-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e756d-432">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e756d-432">Namespace</span></span><br/>                | <span data-ttu-id="e756d-433">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e756d-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e756d-434">MOF</span><span class="sxs-lookup"><span data-stu-id="e756d-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e756d-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e756d-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e756d-436">DLL</span><span class="sxs-lookup"><span data-stu-id="e756d-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e756d-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e756d-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e756d-438">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e756d-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e756d-439">**\_SummaryInformationBase MSVM**</span><span class="sxs-lookup"><span data-stu-id="e756d-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="e756d-440">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="e756d-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

