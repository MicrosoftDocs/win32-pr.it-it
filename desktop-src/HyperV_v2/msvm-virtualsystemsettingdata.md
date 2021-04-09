---
description: Rappresenta le impostazioni specifiche della virtualizzazione per una macchina virtuale.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Classe Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966493"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="889e0-103">\_Classe MSVM VirtualSystemSettingData</span><span class="sxs-lookup"><span data-stu-id="889e0-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="889e0-104">Rappresenta le impostazioni specifiche della virtualizzazione per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="889e0-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="889e0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="889e0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="889e0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="889e0-107">Members</span><span class="sxs-lookup"><span data-stu-id="889e0-107">Members</span></span>

<span data-ttu-id="889e0-108">La **classe \_ VirtualSystemSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="889e0-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="889e0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="889e0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="889e0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="889e0-110">Properties</span></span>

<span data-ttu-id="889e0-111">La **classe \_ VirtualSystemSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="889e0-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="889e0-112">**AdditionalRecoveryInformation**</span><span class="sxs-lookup"><span data-stu-id="889e0-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-115">Eventuali informazioni aggiuntive fornite all'azione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="889e0-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="889e0-116">Il significato di questa proprietà è definito dall'azione in **AutomaticRecoveryAction**.</span><span class="sxs-lookup"><span data-stu-id="889e0-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="889e0-117">Se **AutomaticRecoveryAction** è 0 ("None") o 1 ("Restart"), questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="889e0-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="889e0-118">Se **AutomaticRecoveryAction** è 2 ("Ripristina snapshot"), si tratta del percorso dell'oggetto per uno snapshot da applicare in caso di errore del processo di lavoro della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-119">**AllowFullSCSICommandSet**</span><span class="sxs-lookup"><span data-stu-id="889e0-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-122">**True** se i comandi SCSI dal sistema operativo guest vengono passati a dischi pass-through. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="889e0-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="889e0-123">Se **true**, i comandi SCSI emessi dal sistema operativo guest per i dischi pass-through non vengono filtrati.</span><span class="sxs-lookup"><span data-stu-id="889e0-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="889e0-124">È consigliabile che i filtri SCSI rimangano abilitati per le distribuzioni di produzione.</span><span class="sxs-lookup"><span data-stu-id="889e0-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-125">**AllowReducedFcRedundancy**</span><span class="sxs-lookup"><span data-stu-id="889e0-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-128">Specifica se la migrazione in tempo reale di una macchina virtuale configurata con una scheda di Fibre Channel virtuale è consentita a un computer di destinazione che potrebbe non avere percorsi o ridotti ai dispositivi di Fibre Channel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="889e0-129">Questa proprietà deve essere cancellata dopo una migrazione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="889e0-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="889e0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-130">Value</span></span>                                                                            | <span data-ttu-id="889e0-131">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="889e0-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="889e0-133">Non è possibile eseguire la migrazione in tempo reale della macchina virtuale a un computer di destinazione che potrebbe non avere percorsi o ridotti per i dispositivi Fibre Channel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="889e0-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="889e0-135">È possibile eseguire la migrazione in tempo reale della macchina virtuale a un computer di destinazione che potrebbe non avere o ridotti percorsi per i dispositivi Fibre Channel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="889e0-136">Il sistema operativo guest potrebbe perdere la connettività alla risorsa di archiviazione e potrebbe comportarsi in modo imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="889e0-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="889e0-137">**Architettura**</span><span class="sxs-lookup"><span data-stu-id="889e0-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-140">Architettura del sistema.</span><span class="sxs-lookup"><span data-stu-id="889e0-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-141">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="889e0-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="889e0-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="889e0-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="889e0-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="889e0-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-144">**AutomaticCriticalErrorAction**</span><span class="sxs-lookup"><span data-stu-id="889e0-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-147">Identifica l'azione da eseguire sulla macchina virtuale quando si verifica un errore critico, come la disconnessione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-148">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="889e0-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="889e0-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-150">Non verranno intraprese azioni specifiche per le condizioni di errore critiche.</span><span class="sxs-lookup"><span data-stu-id="889e0-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="889e0-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Sospendi ripresa** (1)</span><span class="sxs-lookup"><span data-stu-id="889e0-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-152">Fa in modo che la macchina virtuale venga sospesa e ripresa automaticamente quando la condizione di errore critico viene risolta.</span><span class="sxs-lookup"><span data-stu-id="889e0-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-153">**AutomaticCriticalErrorActionTimeout**</span><span class="sxs-lookup"><span data-stu-id="889e0-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-154">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="889e0-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="889e0-156">Qualificatori: [**sottotipo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Interval")</span><span class="sxs-lookup"><span data-stu-id="889e0-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="889e0-157">Identifica la durata massima per cui verrà eseguito **AutomaticCriticalErrorAction** per risolvere l'errore critico.</span><span class="sxs-lookup"><span data-stu-id="889e0-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="889e0-158">Si applica solo quando il valore della proprietà **AutomaticCriticalErrorAction** non è 0 (nessuno).</span><span class="sxs-lookup"><span data-stu-id="889e0-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="889e0-159">Una volta scaduto il timeout, la macchina virtuale verrà spenta.</span><span class="sxs-lookup"><span data-stu-id="889e0-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="889e0-160">Il valore verrà arrotondato per eccesso al minuto più vicino.</span><span class="sxs-lookup"><span data-stu-id="889e0-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="889e0-161">Il valore 0 implica che la macchina virtuale deve essere spenta immediatamente quando rileva una condizione di errore critico.</span><span class="sxs-lookup"><span data-stu-id="889e0-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-162">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-163">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="889e0-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-166">Azione da eseguire per la macchina virtuale quando il software eseguito dalla macchina virtuale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="889e0-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="889e0-167">Gli errori in questo caso indicano un errore rilevabile dalla piattaforma host, ad esempio una condizione di stato di attesa interrotti.</span><span class="sxs-lookup"><span data-stu-id="889e0-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="889e0-168">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="889e0-169">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-169">This can be one of the following values.</span></span>



| <span data-ttu-id="889e0-170">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-170">Value</span></span>                                                                               | <span data-ttu-id="889e0-171">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="889e0-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="889e0-173">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="889e0-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="889e0-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="889e0-175">Riavvia.</span><span class="sxs-lookup"><span data-stu-id="889e0-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="889e0-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="889e0-177">Ripristina snapshot.</span><span class="sxs-lookup"><span data-stu-id="889e0-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="889e0-179">Riservato.</span><span class="sxs-lookup"><span data-stu-id="889e0-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="889e0-180">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="889e0-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-181">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-183">Azione da eseguire per la macchina virtuale quando l'host viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="889e0-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="889e0-184">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="889e0-185">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-185">This can be one of the following values.</span></span>



| <span data-ttu-id="889e0-186">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-186">Value</span></span>                                                                               | <span data-ttu-id="889e0-187">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="889e0-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="889e0-189">Spegni.</span><span class="sxs-lookup"><span data-stu-id="889e0-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="889e0-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="889e0-191">Salvare lo stato.</span><span class="sxs-lookup"><span data-stu-id="889e0-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="889e0-193">Arresto.</span><span class="sxs-lookup"><span data-stu-id="889e0-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="889e0-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="889e0-195">Riservato.</span><span class="sxs-lookup"><span data-stu-id="889e0-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="889e0-196">**AutomaticSnapshotsEnabled**</span><span class="sxs-lookup"><span data-stu-id="889e0-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-197">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-199">Indica se la macchina virtuale deve avere snapshot automatici abilitati.</span><span class="sxs-lookup"><span data-stu-id="889e0-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-200">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="889e0-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-201">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="889e0-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-204">Azione da eseguire per la macchina virtuale all'avvio dell'host.</span><span class="sxs-lookup"><span data-stu-id="889e0-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="889e0-205">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="889e0-206">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-206">This can be one of the following values.</span></span>



| <span data-ttu-id="889e0-207">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-207">Value</span></span>                                                                               | <span data-ttu-id="889e0-208">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="889e0-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="889e0-210">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="889e0-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="889e0-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="889e0-212">Riavviare se precedentemente attivo.</span><span class="sxs-lookup"><span data-stu-id="889e0-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="889e0-214">Avviare sempre.</span><span class="sxs-lookup"><span data-stu-id="889e0-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="889e0-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="889e0-216">Riservato.</span><span class="sxs-lookup"><span data-stu-id="889e0-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="889e0-217">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="889e0-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-218">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="889e0-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-220">Tempo di ritardo prima che la macchina virtuale venga avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="889e0-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="889e0-221">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-222">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="889e0-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-225">Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host.</span><span class="sxs-lookup"><span data-stu-id="889e0-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="889e0-226">Un numero inferiore indica l'attivazione precedente.</span><span class="sxs-lookup"><span data-stu-id="889e0-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="889e0-227">Se una o più configurazioni mostrano lo stesso valore, la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="889e0-228">Il valore 0 indica che la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="889e0-229">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-230">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="889e0-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-233">Il numero di serie della lavagna di base per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-234">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="889e0-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-236">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-237">Identificatore univoco globale per il BIOS della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-238">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="889e0-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-240">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-241">**True** se il tasto BLOC NUM è impostato su on dal BIOS; **False** se il tasto BLOC NUM è impostato su off dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="889e0-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="889e0-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-245">Il numero di serie del BIOS per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="889e0-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-247">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="889e0-248">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="889e0-249">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="889e0-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="889e0-250">Ordine di avvio impostato all'interno del BIOS della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="889e0-251">Questa proprietà è una matrice di valori, **BootOrder** \[ da 0 a \] **BootOrder** \[ 3 \] , incluso, in cui ogni valore indica un dispositivo da cui eseguire l'avvio.</span><span class="sxs-lookup"><span data-stu-id="889e0-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="889e0-252">Ognuno dei 4 valori nella matrice deve essere impostato e non deve corrispondere a un altro valore nella matrice.</span><span class="sxs-lookup"><span data-stu-id="889e0-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="889e0-253">La macchina virtuale tenterà innanzitutto di eseguire l'avvio dal dispositivo indicato dal primo valore all'interno della matrice.</span><span class="sxs-lookup"><span data-stu-id="889e0-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="889e0-254">Se il dispositivo non contiene un settore di avvio, la macchina virtuale tenterà di eseguire l'avvio dal dispositivo successivo specificato dalla proprietà **BootOrder** e così via.</span><span class="sxs-lookup"><span data-stu-id="889e0-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="889e0-255">Se nessun dispositivo specificato all'interno di **BootOrder** contiene un settore di avvio, la macchina virtuale non verrà avviata.</span><span class="sxs-lookup"><span data-stu-id="889e0-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="889e0-256">Il valore predefinito per una macchina virtuale è \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="889e0-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="889e0-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span><span class="sxs-lookup"><span data-stu-id="889e0-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-258">La macchina virtuale tenterà di eseguire l'avvio dal disco floppy all'interno dell'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="889e0-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="889e0-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span><span class="sxs-lookup"><span data-stu-id="889e0-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-260">La macchina virtuale tenterà di eseguire l'avvio dal primo disco CD o DVD trovato con un settore di avvio.</span><span class="sxs-lookup"><span data-stu-id="889e0-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="889e0-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disco rigido IDE** (2)</span><span class="sxs-lookup"><span data-stu-id="889e0-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-262">La macchina virtuale tenterà di eseguire l'avvio dalla prima unità disco rigido trovata con un settore di avvio.</span><span class="sxs-lookup"><span data-stu-id="889e0-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="889e0-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Avvio PXE** (3)</span><span class="sxs-lookup"><span data-stu-id="889e0-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-264">La macchina virtuale tenterà l'avvio PXE dalla rete.</span><span class="sxs-lookup"><span data-stu-id="889e0-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="889e0-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Unità disco rigido SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="889e0-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="889e0-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="889e0-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-267">**BootSourceOrder**</span><span class="sxs-lookup"><span data-stu-id="889e0-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-268">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="889e0-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="889e0-269">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-270">Ordine dell'origine di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="889e0-271">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-272">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="889e0-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-275">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="889e0-275">A short description of the object.</span></span> <span data-ttu-id="889e0-276">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="889e0-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-277">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="889e0-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-279">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-280">Tag asset dello chassis per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-281">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="889e0-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-283">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-284">Il numero di serie dello chassis per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-285">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-288">Percorso di una directory in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="889e0-289">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-290">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="889e0-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-293">Il percorso relativo e il nome file di un file in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="889e0-294">Questo percorso è relativo alla proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="889e0-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="889e0-295">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="889e0-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-299">Identificatore univoco della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="889e0-300">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-301">**ConsoleMode**</span><span class="sxs-lookup"><span data-stu-id="889e0-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-302">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-303">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-304">Identifica la modalità della console per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-305">Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="889e0-306">**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="889e0-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="889e0-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="889e0-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="889e0-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="889e0-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="889e0-309">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="889e0-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="889e0-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-311">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="889e0-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-313">Data e ora in cui sono state create le impostazioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="889e0-314">Se questo oggetto rappresenta le impostazioni correnti per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato il sistema.</span><span class="sxs-lookup"><span data-stu-id="889e0-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="889e0-315">Se questo oggetto rappresenta le impostazioni dello snapshot per la macchina virtuale, questo valore corrisponde all'ora in cui è stato effettuato lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="889e0-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="889e0-316">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-317">**DebugChannelId**</span><span class="sxs-lookup"><span data-stu-id="889e0-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="889e0-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-319">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-320">Identificatore del canale utilizzato per eseguire il debug della macchina virtuale utilizzando il debugger unificato.</span><span class="sxs-lookup"><span data-stu-id="889e0-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-321">**DebugPort**</span><span class="sxs-lookup"><span data-stu-id="889e0-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-322">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="889e0-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-323">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-324">Porta TCP/IP utilizzata per eseguire il debug della macchina virtuale utilizzando il debug sintetico.</span><span class="sxs-lookup"><span data-stu-id="889e0-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-325">**DebugPortEnabled**</span><span class="sxs-lookup"><span data-stu-id="889e0-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-326">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-327">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-328">Specifica se la macchina virtuale utilizza il debug sintetico.</span><span class="sxs-lookup"><span data-stu-id="889e0-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="889e0-329">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="889e0-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Disattivato** (0)</span><span class="sxs-lookup"><span data-stu-id="889e0-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="889e0-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span><span class="sxs-lookup"><span data-stu-id="889e0-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="889e0-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span><span class="sxs-lookup"><span data-stu-id="889e0-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-333">Assegnazione automatica</span><span class="sxs-lookup"><span data-stu-id="889e0-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-334">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="889e0-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-337">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="889e0-337">A description of the object.</span></span> <span data-ttu-id="889e0-338">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="889e0-339">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-339">Value</span></span>                                                                                                                  | <span data-ttu-id="889e0-340">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="889e0-341"><dt>"Impostazioni attive per la macchina virtuale"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="889e0-342">Questa istanza fa riferimento a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-343"><dt>"Impostazioni snapshot per la macchina virtuale"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="889e0-344">Questa istanza fa riferimento a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="889e0-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="889e0-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="889e0-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-348">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="889e0-348">A display name for the object.</span></span> <span data-ttu-id="889e0-349">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è sempre impostata sul nome visualizzato del computer.</span><span class="sxs-lookup"><span data-stu-id="889e0-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="889e0-350">Il nome non può superare i 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="889e0-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-351">**EnhancedSessionTransportType**</span><span class="sxs-lookup"><span data-stu-id="889e0-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-352">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-353">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-354">Indica il tipo di trasporto da utilizzare per la connessione a una sessione avanzata.</span><span class="sxs-lookup"><span data-stu-id="889e0-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-355">Questa proprietà è stata aggiunta in Windows 10, versione 1803.</span><span class="sxs-lookup"><span data-stu-id="889e0-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="889e0-356">**Pipe VMBus** (0)</span><span class="sxs-lookup"><span data-stu-id="889e0-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="889e0-357">**Socket di Hyper-V** (1)</span><span class="sxs-lookup"><span data-stu-id="889e0-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-358">**GuestControlledCacheTypes**</span><span class="sxs-lookup"><span data-stu-id="889e0-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-359">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-360">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-361">Indica se il Guest può controllare i tipi di cache.</span><span class="sxs-lookup"><span data-stu-id="889e0-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-362">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-363">**GuestStateDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-366">FilePath di una directory in cui vengono archiviate le informazioni sullo stato di runtime Guest.</span><span class="sxs-lookup"><span data-stu-id="889e0-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-367">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="889e0-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-368">**GuestStateFile**</span><span class="sxs-lookup"><span data-stu-id="889e0-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-371">FilePath di un file in cui vengono archiviate le informazioni sullo stato di runtime Guest.</span><span class="sxs-lookup"><span data-stu-id="889e0-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="889e0-372">Un percorso relativo viene accodato al valore della proprietà **GuestStateDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="889e0-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-373">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="889e0-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-374">**HighMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="889e0-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-375">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="889e0-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-376">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-377">Dimensioni massime (sopra 4 GB) Memory-Mapped Gap i/o in MB</span><span class="sxs-lookup"><span data-stu-id="889e0-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="889e0-378">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="889e0-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-379">**IncrementalBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="889e0-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-380">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-381">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-382">Indica se il VSS writer Hyper-V supporta l'esecuzione di backup incrementali della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="889e0-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-384">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="889e0-386">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="889e0-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="889e0-387">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="889e0-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="889e0-388">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-389">**IsAutomaticSnapshot**</span><span class="sxs-lookup"><span data-stu-id="889e0-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-390">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-392">Indica se si tratta di uno snapshot creato automaticamente per l'utente.</span><span class="sxs-lookup"><span data-stu-id="889e0-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-393">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="889e0-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="889e0-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-395">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-397">**True** se la configurazione contiene un riferimento a un file di stato salvato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="889e0-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="889e0-398">Questa operazione non indica la presenza di un file di questo tipo, ma solo che la configurazione ne specifichi uno.</span><span class="sxs-lookup"><span data-stu-id="889e0-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-399">**LockOnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="889e0-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-400">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-401">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-402">Blocca la console quando si disconnette da vmconnect.</span><span class="sxs-lookup"><span data-stu-id="889e0-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-403">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-404">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-407">Percorso di una directory in cui vengono archiviate le informazioni di log per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="889e0-408">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-409">**LowMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="889e0-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-410">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="889e0-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-411">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-412">Configura le dimensioni in megabyte del primo gap MMIO per una macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="889e0-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="889e0-413">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="889e0-414">Intervallo: 128 3584</span><span class="sxs-lookup"><span data-stu-id="889e0-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="889e0-415">**NetworkBootPreferredProtocol**</span><span class="sxs-lookup"><span data-stu-id="889e0-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-416">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-417">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-418">Determina se il protocollo preferito per l'avvio PXE è IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="889e0-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="889e0-419">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="889e0-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="889e0-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="889e0-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="889e0-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-422">**Note**</span><span class="sxs-lookup"><span data-stu-id="889e0-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-423">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="889e0-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="889e0-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-425">Note fornite dall'utente correlate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="889e0-426">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-427">**Parent**</span><span class="sxs-lookup"><span data-stu-id="889e0-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-430">Se questa istanza non rappresenta un sistema basato su uno snapshot di una macchina virtuale, questa proprietà è **null**.</span><span class="sxs-lookup"><span data-stu-id="889e0-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="889e0-431">In caso contrario, la proprietà contenga il percorso dell'oggetto **MSVM \_ VirtualSystemSettingData** su cui è basata l'istanza.</span><span class="sxs-lookup"><span data-stu-id="889e0-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="889e0-432">Quando si compila una gerarchia della struttura ad albero dello snapshot per la macchina virtuale, questa proprietà fa riferimento all'oggetto da cui viene derivata l'istanza corrente (l'istanza corrente è il nodo figlio e l'oggetto a cui si fa riferimento in questa proprietà è il nodo padre).</span><span class="sxs-lookup"><span data-stu-id="889e0-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="889e0-433">**ParentPackage**</span><span class="sxs-lookup"><span data-stu-id="889e0-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-435">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-436">Se il sistema è un contenitore, il percorso dell'ContainerPackage MSVM \_ da cui si basa questo sistema.</span><span class="sxs-lookup"><span data-stu-id="889e0-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-437">Aggiunta in Windows 10; rimosso in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="889e0-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-438">**PauseAfterBootFailure**</span><span class="sxs-lookup"><span data-stu-id="889e0-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-439">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-440">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-441">Indica se il BIOS viene sospeso dopo ogni errore della voce di avvio in attesa che l'utente prema un tasto.</span><span class="sxs-lookup"><span data-stu-id="889e0-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="889e0-442">**True** se il BIOS viene sospeso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="889e0-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="889e0-443">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-444">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="889e0-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-447">Percorso completo di un file in cui sono archiviate le informazioni relative al ripristino per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="889e0-448">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-449">**Della securebootenabled**</span><span class="sxs-lookup"><span data-stu-id="889e0-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-450">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-451">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-452">Indica se l'avvio protetto è abilitato per la macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="889e0-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="889e0-453">**True** se abilitata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="889e0-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-454">L'avvio protetto può essere abilitato solo per le macchine virtuali di seconda generazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="889e0-455">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-456">**SecureBootTemplateId**</span><span class="sxs-lookup"><span data-stu-id="889e0-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-457">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-458">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-459">Identificatore univoco globale del modello di valori iniziali delle variabili correlate all'avvio protetto UEFI.</span><span class="sxs-lookup"><span data-stu-id="889e0-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="889e0-460">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="889e0-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-461">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="889e0-462">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-465">Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="889e0-466">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-467">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-468">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-470">Percorso di una directory in cui vengono archiviate informazioni sulle informazioni relative alla sospensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="889e0-471">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-472">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="889e0-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-473">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-474">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-475">Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="889e0-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="889e0-476">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-477">**UserSnapshotType**</span><span class="sxs-lookup"><span data-stu-id="889e0-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-478">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="889e0-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-479">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="889e0-480">Indica il tipo di snapshot definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="889e0-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="889e0-481">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="889e0-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="889e0-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (2)</span><span class="sxs-lookup"><span data-stu-id="889e0-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-483">Disabilitare la creazione di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="889e0-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="889e0-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span><span class="sxs-lookup"><span data-stu-id="889e0-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-485">Snapshot coerente con i dati da usare nell'ambiente di produzione. Esegue uno snapshot con lo stato dell'applicazione quando non è disponibile la possibilità di creare snapshot coerenti con i dati.</span><span class="sxs-lookup"><span data-stu-id="889e0-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="889e0-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span><span class="sxs-lookup"><span data-stu-id="889e0-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-487">Snapshot coerente con i dati da usare nell'ambiente di produzione. Non crea uno snapshot con lo stato dell'applicazione se non è possibile creare uno snapshot coerente con i dati.</span><span class="sxs-lookup"><span data-stu-id="889e0-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="889e0-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span><span class="sxs-lookup"><span data-stu-id="889e0-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="889e0-489">Snapshot che contiene informazioni sulla memoria e sul dispositivo a scopo di test e sviluppo.</span><span class="sxs-lookup"><span data-stu-id="889e0-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-490">**Versione**</span><span class="sxs-lookup"><span data-stu-id="889e0-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-491">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-493">Versione della macchina virtuale in formato "Major. minor", ad esempio "2,0".</span><span class="sxs-lookup"><span data-stu-id="889e0-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="889e0-494">**VirtualNumaEnabled**</span><span class="sxs-lookup"><span data-stu-id="889e0-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-495">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="889e0-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-496">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="889e0-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="889e0-497">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span><span class="sxs-lookup"><span data-stu-id="889e0-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="889e0-498">**True** se i nodi NUMA (non-Uniform Memory Access) virtuali sono proiettati nella macchina virtuale; **False** se la macchina virtuale avrà un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="889e0-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="889e0-499">Se **true**, il numero di nodi NUMA virtuali proiettati nella macchina virtuale è determinato dai valori delle proprietà [**MSVM ProcessorSettingData. \_ MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) e [**MSVM \_ MemorySettingData. MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="889e0-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="889e0-500">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="889e0-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-501">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-502">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="889e0-503">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="889e0-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="889e0-504">Nome dell'oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="889e0-505">Questa proprietà è una sostituzione da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="889e0-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="889e0-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="889e0-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-507">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-508">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-509">I valori validi per questa proprietà sono Microsoft: Hyper-V: sottotipo: 1 e Microsoft: Hyper-V: sottotipo: 2.</span><span class="sxs-lookup"><span data-stu-id="889e0-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="889e0-510">Una macchina virtuale di prima generazione è sottotipo 1.</span><span class="sxs-lookup"><span data-stu-id="889e0-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="889e0-511">Una macchina virtuale di seconda generazione è sottotipo 2.</span><span class="sxs-lookup"><span data-stu-id="889e0-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="889e0-512">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="889e0-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="889e0-513">**Microsoft: Hyper-v: sottotipo: 1** ("Microsoft: Hyper-v: sottotipo: 1")</span><span class="sxs-lookup"><span data-stu-id="889e0-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="889e0-514">**Microsoft: Hyper-v: sottotipo: 2** ("Microsoft: Hyper-v: sottotipo: 2")</span><span class="sxs-lookup"><span data-stu-id="889e0-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="889e0-515">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="889e0-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889e0-516">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="889e0-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="889e0-517">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="889e0-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="889e0-518">Specifica il tipo di macchina virtuale rappresentata dai dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="889e0-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="889e0-519">Questa proprietà viene ereditata dalla classe [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="889e0-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="889e0-520">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="889e0-520">This will be one of the following values.</span></span>



| <span data-ttu-id="889e0-521">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="889e0-522">Significato</span><span class="sxs-lookup"><span data-stu-id="889e0-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="889e0-523"><dt>"Microsoft: Hyper-V: System: realizzato"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="889e0-524">Una macchina virtuale realizzata.</span><span class="sxs-lookup"><span data-stu-id="889e0-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="889e0-525"><dt>"Microsoft: Hyper-V: System: planned"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="889e0-526">Una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="889e0-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="889e0-527"><dt>"Microsoft: Hyper-V: snapshot: realizzato"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="889e0-528">Snapshot di una macchina virtuale realizzata.</span><span class="sxs-lookup"><span data-stu-id="889e0-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-529"><dt>"Microsoft: Hyper-V: snapshot: Recovery"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="889e0-530">Snapshot di una macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="889e0-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="889e0-531"><dt>"Microsoft: Hyper-V: snapshot: pianificato"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="889e0-532">Snapshot di una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="889e0-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="889e0-533"><dt>"Microsoft: Hyper-V: snapshot: Missing"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="889e0-534">Uno snapshot mancante.</span><span class="sxs-lookup"><span data-stu-id="889e0-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="889e0-535"><dt>"Microsoft: Hyper-V: snapshot: replica: standard"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="889e0-536">Snapshot del punto di replica basato sul tempo.</span><span class="sxs-lookup"><span data-stu-id="889e0-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="889e0-537"><dt>"Microsoft: Hyper-V: snapshot: replica: ApplicationConsistent"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="889e0-538">Snapshot del punto di replica VSS.</span><span class="sxs-lookup"><span data-stu-id="889e0-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="889e0-539"><dt>"Microsoft: Hyper-V: snapshot: replica: PlannedFailover"</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="889e0-540">Snapshot di replica pianificato.</span><span class="sxs-lookup"><span data-stu-id="889e0-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="889e0-541">Commenti</span><span class="sxs-lookup"><span data-stu-id="889e0-541">Remarks</span></span>

<span data-ttu-id="889e0-542">L'accesso alla **classe \_ VirtualSystemSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="889e0-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="889e0-543">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="889e0-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="889e0-544">Requisiti</span><span class="sxs-lookup"><span data-stu-id="889e0-544">Requirements</span></span>



| <span data-ttu-id="889e0-545">Requisito</span><span class="sxs-lookup"><span data-stu-id="889e0-545">Requirement</span></span> | <span data-ttu-id="889e0-546">Valore</span><span class="sxs-lookup"><span data-stu-id="889e0-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="889e0-547">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="889e0-547">Minimum supported client</span></span><br/> | <span data-ttu-id="889e0-548">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="889e0-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="889e0-549">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="889e0-549">Minimum supported server</span></span><br/> | <span data-ttu-id="889e0-550">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="889e0-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="889e0-551">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="889e0-551">Namespace</span></span><br/>                | <span data-ttu-id="889e0-552">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="889e0-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="889e0-553">MOF</span><span class="sxs-lookup"><span data-stu-id="889e0-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="889e0-554"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="889e0-555">DLL</span><span class="sxs-lookup"><span data-stu-id="889e0-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="889e0-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="889e0-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="889e0-557">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="889e0-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889e0-558">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="889e0-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="889e0-559">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="889e0-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="889e0-560">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="889e0-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

