---
description: Rappresenta le impostazioni specifiche della replica per una macchina virtuale.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Classe Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232080"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="ea91c-103">\_Classe MSVM ReplicationSettingData</span><span class="sxs-lookup"><span data-stu-id="ea91c-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="ea91c-104">Rappresenta le impostazioni specifiche della replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="ea91c-105">Il client passa un'istanza di questa classe a [**MSVM \_ ReplicationService. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) per creare una relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="ea91c-106">Il client non può modificare direttamente i valori delle proprietà di questa classe. per modificare i valori, deve chiamare il metodo [**MSVM \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ea91c-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="ea91c-107">Ogni relazione di replica dispone di una singola istanza di Settings.</span><span class="sxs-lookup"><span data-stu-id="ea91c-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="ea91c-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ea91c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea91c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea91c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="ea91c-110">Members</span><span class="sxs-lookup"><span data-stu-id="ea91c-110">Members</span></span>

<span data-ttu-id="ea91c-111">La **classe \_ ReplicationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ea91c-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ea91c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea91c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea91c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea91c-113">Properties</span></span>

<span data-ttu-id="ea91c-114">La **classe \_ ReplicationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea91c-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea91c-115">**AdditionalSettings**</span><span class="sxs-lookup"><span data-stu-id="ea91c-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-118">Impostazioni di replica aggiuntive che possono essere utilizzate dal provider di endpoint.</span><span class="sxs-lookup"><span data-stu-id="ea91c-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="ea91c-119">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea91c-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-120">**ApplicationConsistentSnapshotInterval**</span><span class="sxs-lookup"><span data-stu-id="ea91c-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-121">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-123">Intervallo di tempo tra snapshot coerenti con l'applicazione, specificato in ore.</span><span class="sxs-lookup"><span data-stu-id="ea91c-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="ea91c-124">I valori validi sono compresi tra 1 ora e 12 ore.</span><span class="sxs-lookup"><span data-stu-id="ea91c-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="ea91c-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-128">Definire la modalità di autenticazione utilizzata per la connessione al server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="ea91c-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticazione Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="ea91c-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ea91c-130">Autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ea91c-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="ea91c-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)</span><span class="sxs-lookup"><span data-stu-id="ea91c-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ea91c-132">Autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="ea91c-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea91c-133">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="ea91c-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-136">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ea91c-136">Not used.</span></span>

<span data-ttu-id="ea91c-137">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-138">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="ea91c-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-141">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ea91c-141">Not used.</span></span>

<span data-ttu-id="ea91c-142">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-143">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="ea91c-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ea91c-146">Not used.</span></span>

<span data-ttu-id="ea91c-147">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-148">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="ea91c-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-149">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea91c-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-151">Tempo di ritardo prima che la macchina virtuale venga avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ea91c-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="ea91c-152">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-153">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ea91c-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-156">Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea91c-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="ea91c-157">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-158">**AutoResynchronizeEnabled**</span><span class="sxs-lookup"><span data-stu-id="ea91c-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-159">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea91c-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-161">Specifica se le operazioni di risincronizzazione vengono attivate automaticamente quando si verifica un errore di replica a causa di problemi di alimentazione e hardware.</span><span class="sxs-lookup"><span data-stu-id="ea91c-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="ea91c-162">Le operazioni di risincronizzazione vengono attivate solo quando si verifica un errore tra le ore specificate dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea91c-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea91c-163">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="ea91c-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-164">**AutoResynchronizeIntervalEnd**</span><span class="sxs-lookup"><span data-stu-id="ea91c-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-165">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea91c-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-167">Specifica l'ora di fine per l'attivazione delle operazioni di risincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="ea91c-168">Questo valore è nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-168">This value is in local time.</span></span> <span data-ttu-id="ea91c-169">Il valore predefinito è 06:00 (6:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="ea91c-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="ea91c-170">Le operazioni di risincronizzazione vengono attivate solo quando si verifica un errore tra le ore specificate dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea91c-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea91c-171">È anche possibile pianificare le operazioni di risincronizzazione in modo che vengano attivate durante l'intervallo successivo.</span><span class="sxs-lookup"><span data-stu-id="ea91c-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-172">**AutoResynchronizeIntervalStart**</span><span class="sxs-lookup"><span data-stu-id="ea91c-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-173">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea91c-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-175">Specifica l'ora di inizio per l'attivazione delle operazioni di risincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="ea91c-176">Questo valore è nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-176">This value is in local time.</span></span> <span data-ttu-id="ea91c-177">Il valore predefinito è 18:30 (6:30).</span><span class="sxs-lookup"><span data-stu-id="ea91c-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="ea91c-178">Le operazioni di risincronizzazione vengono attivate solo quando si verifica un errore tra le ore specificate dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea91c-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea91c-179">È anche possibile pianificare le operazioni di risincronizzazione in modo che vengano attivate durante l'intervallo successivo.</span><span class="sxs-lookup"><span data-stu-id="ea91c-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-180">**BypassProxyServer**</span><span class="sxs-lookup"><span data-stu-id="ea91c-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-181">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea91c-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-183">Specifica se il server proxy deve essere ignorato durante la connessione a un server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ea91c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-187">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea91c-187">A short description of the object.</span></span> <span data-ttu-id="ea91c-188">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Settings".</span><span class="sxs-lookup"><span data-stu-id="ea91c-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="ea91c-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="ea91c-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-193">Identificazione personale del certificato da utilizzare quando la proprietà **AuthenticationType** è l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="ea91c-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-194">**CompressionEnabled**</span><span class="sxs-lookup"><span data-stu-id="ea91c-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-195">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea91c-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-197">Specifica se i dati di replica verranno compressi durante l'invio al server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-198">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea91c-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-201">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ea91c-201">Not used.</span></span>

<span data-ttu-id="ea91c-202">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-203">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="ea91c-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-206">Il percorso relativo e il nome file di un file in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="ea91c-207">Questo percorso è relativo alla proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="ea91c-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="ea91c-208">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="ea91c-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-212">Identificatore univoco della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="ea91c-213">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="ea91c-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-215">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea91c-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-217">Data e ora in cui sono state create le impostazioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="ea91c-218">Se questo oggetto rappresenta le impostazioni correnti per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato il sistema.</span><span class="sxs-lookup"><span data-stu-id="ea91c-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="ea91c-219">Se questo oggetto rappresenta le impostazioni dello snapshot per la macchina virtuale, questo valore corrisponde all'ora in cui è stato effettuato lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="ea91c-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="ea91c-220">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="ea91c-221">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ea91c-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="ea91c-222">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-223">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ea91c-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-226">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="ea91c-226">A description of the object.</span></span> <span data-ttu-id="ea91c-227">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "dati delle impostazioni di replica della macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="ea91c-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ea91c-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-231">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea91c-231">A display name for the object.</span></span> <span data-ttu-id="ea91c-232">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è impostata sul nome visualizzato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-233">**EnableWriteOrderPreservationAcrossDisks**</span><span class="sxs-lookup"><span data-stu-id="ea91c-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-234">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea91c-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-236">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="ea91c-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-237">Specifica se tutti i dischi rigidi virtuali di replica per la macchina virtuale vengono replicati nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="ea91c-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="ea91c-238">Ciò garantisce che la replica rispetta l'ordine di scrittura delle applicazioni nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="ea91c-239">**Windows 8.1:** A partire da Windows 8.1 e Windows Server 2012 R2, questa proprietà è deprecata e sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="ea91c-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-240">**IncludedDisks**</span><span class="sxs-lookup"><span data-stu-id="ea91c-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-241">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ea91c-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-243">Qualificatori: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed")</span><span class="sxs-lookup"><span data-stu-id="ea91c-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-244">Elenco di dischi rigidi virtuali (VHD) collegati al sistema che verranno replicati dal motore di replica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="ea91c-245">Si tratta di una matrice di stringhe, ognuna delle quali contiene l' **ID** istanza del [**\_ StorageAllocationSettingData MSVM**](msvm-storageallocationsettingdata.md) che rappresenta il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ea91c-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-249">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="ea91c-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-250">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ea91c-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ea91c-251">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ea91c-252">Per Windows 8, è sempre impostato su "Microsoft:*GUID macchina virtuale* \\ HVR".</span><span class="sxs-lookup"><span data-stu-id="ea91c-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="ea91c-253">Per Windows 8.1, viene impostato su "Microsoft:*GUID macchina virtuale* \\ HVR \\<0/1>".</span><span class="sxs-lookup"><span data-stu-id="ea91c-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="ea91c-254">Nel valore Windows 8.1 0 indica primario e 1 indica la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="ea91c-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="ea91c-255">Per ulteriori informazioni sulla replica estesa, vedere [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="ea91c-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-256">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea91c-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-259">Percorso di una directory in cui vengono archiviate le informazioni di log per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="ea91c-260">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-261">**Note**</span><span class="sxs-lookup"><span data-stu-id="ea91c-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-262">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ea91c-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-264">Non usato e non può essere impostato.</span><span class="sxs-lookup"><span data-stu-id="ea91c-264">Not used and can't be set.</span></span>

<span data-ttu-id="ea91c-265">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-266">**PrimaryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ea91c-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-269">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea91c-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-270">Nome del punto di connessione primario.</span><span class="sxs-lookup"><span data-stu-id="ea91c-270">The name of the primary connection point.</span></span> <span data-ttu-id="ea91c-271">Nel caso di un cluster primario, questo è il nome del CAP del broker.</span><span class="sxs-lookup"><span data-stu-id="ea91c-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="ea91c-272">Nel caso di un server primario autonomo, questo è il nome del sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea91c-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-273">**PrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="ea91c-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-276">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea91c-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-277">Nome di dominio completo del sistema host primario che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-278">**RecoveryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ea91c-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-281">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea91c-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-282">Nome del punto di connessione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-282">The name of the recovery connection point.</span></span> <span data-ttu-id="ea91c-283">Nel caso di un cluster di ripristino, questo è il nome del CAP del broker.</span><span class="sxs-lookup"><span data-stu-id="ea91c-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="ea91c-284">Nel caso di un server di ripristino autonomo, si tratta del nome del sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea91c-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-285">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="ea91c-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-288">Percorso completo di un file in cui sono archiviate le informazioni relative al ripristino per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="ea91c-289">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-290">**RecoveryHistory**</span><span class="sxs-lookup"><span data-stu-id="ea91c-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-291">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-293">Numero massimo di snapshot di ripristino che verranno archiviati nel server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="ea91c-294">I valori validi sono compresi tra 0 e 24.</span><span class="sxs-lookup"><span data-stu-id="ea91c-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-295">**RecoveryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="ea91c-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-298">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea91c-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-299">Nome di dominio completo del sistema host di ripristino che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-300">**RecoveryServerPortNumber**</span><span class="sxs-lookup"><span data-stu-id="ea91c-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-301">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-303">Numero di porta del server di ripristino da utilizzare quando si effettua una connessione sicura per la replica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-304">**ReplicateHostKvpItems**</span><span class="sxs-lookup"><span data-stu-id="ea91c-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-305">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea91c-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-307">Specifica se è necessario replicare le [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)solo host dalla macchina virtuale primaria alla macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea91c-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="ea91c-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-309">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea91c-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-311">Intervallo di replica di una relazione di replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="ea91c-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="ea91c-312">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ea91c-312">Valid values are:</span></span>

<span data-ttu-id="ea91c-313">30</span><span class="sxs-lookup"><span data-stu-id="ea91c-313">30</span></span>

<span data-ttu-id="ea91c-314">300</span><span class="sxs-lookup"><span data-stu-id="ea91c-314">300</span></span>

<span data-ttu-id="ea91c-315">900</span><span class="sxs-lookup"><span data-stu-id="ea91c-315">900</span></span>

<span data-ttu-id="ea91c-316">Il valore predefinito è 300 secondi.</span><span class="sxs-lookup"><span data-stu-id="ea91c-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="ea91c-317">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea91c-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-318">**ReplicationProvider**</span><span class="sxs-lookup"><span data-stu-id="ea91c-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-321">Percorso dell'istanza della classe [**\_ ReplicationProvider MSVM**](msvm-replicationprovider.md) che identifica l'endpoint del provider di replica.</span><span class="sxs-lookup"><span data-stu-id="ea91c-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="ea91c-322">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea91c-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-323">**RootCertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="ea91c-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-326">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="ea91c-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-327">Identificazione personale del certificato radice del certificato in uso quando **AuthenticationType** è 2 (autorizzazione basata su certificati).</span><span class="sxs-lookup"><span data-stu-id="ea91c-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-328">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea91c-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-331">Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="ea91c-332">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-333">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea91c-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-336">Percorso di una directory in cui vengono archiviate informazioni sulle informazioni relative alla sospensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="ea91c-337">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-338">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea91c-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-341">Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea91c-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="ea91c-342">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ea91c-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-343">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="ea91c-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-346">Nome dell'oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="ea91c-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="ea91c-347">Questa proprietà è una sostituzione da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea91c-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea91c-348">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="ea91c-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea91c-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ea91c-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea91c-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea91c-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea91c-351">Specifica il tipo di macchina virtuale rappresentata dai dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="ea91c-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="ea91c-352">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è sempre impostata su "Microsoft: Hyper-V: replica".</span><span class="sxs-lookup"><span data-stu-id="ea91c-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea91c-353">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea91c-353">Requirements</span></span>



| <span data-ttu-id="ea91c-354">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea91c-354">Requirement</span></span> | <span data-ttu-id="ea91c-355">Valore</span><span class="sxs-lookup"><span data-stu-id="ea91c-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea91c-356">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea91c-356">Minimum supported client</span></span><br/> | <span data-ttu-id="ea91c-357">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea91c-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea91c-358">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea91c-358">Minimum supported server</span></span><br/> | <span data-ttu-id="ea91c-359">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea91c-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea91c-360">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea91c-360">Namespace</span></span><br/>                | <span data-ttu-id="ea91c-361">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ea91c-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ea91c-362">MOF</span><span class="sxs-lookup"><span data-stu-id="ea91c-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea91c-363"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea91c-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea91c-364">DLL</span><span class="sxs-lookup"><span data-stu-id="ea91c-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea91c-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea91c-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea91c-366">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea91c-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea91c-367">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ea91c-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ea91c-368">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="ea91c-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

