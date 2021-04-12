---
description: Gestisce la replica per una macchina virtuale.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232081"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="b805f-103">\_Classe MSVM ReplicationService</span><span class="sxs-lookup"><span data-stu-id="b805f-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b805f-104">Gestisce la replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="b805f-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b805f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b805f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b805f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="b805f-107">Members</span><span class="sxs-lookup"><span data-stu-id="b805f-107">Members</span></span>

<span data-ttu-id="b805f-108">La **classe \_ ReplicationService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b805f-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="b805f-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="b805f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b805f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b805f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b805f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b805f-111">Methods</span></span>

<span data-ttu-id="b805f-112">La **classe \_ ReplicationService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b805f-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="b805f-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="b805f-113">Method</span></span>                                                                                                 | <span data-ttu-id="b805f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b805f-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b805f-115">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b805f-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="b805f-116">Aggiunge una voce di autorizzazione a un server.</span><span class="sxs-lookup"><span data-stu-id="b805f-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="b805f-117">**ChangeReplicationModeToPrimary**</span><span class="sxs-lookup"><span data-stu-id="b805f-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="b805f-118">Consente di modificare la relazione di replica estesa con la relazione primaria per una macchina virtuale di replica.</span><span class="sxs-lookup"><span data-stu-id="b805f-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="b805f-119">La macchina virtuale di replica deve trovarsi in uno stato di commit del failover.</span><span class="sxs-lookup"><span data-stu-id="b805f-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="b805f-120">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b805f-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="b805f-121">**CommitFailover**</span><span class="sxs-lookup"><span data-stu-id="b805f-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="b805f-122">Consente di eseguire il commit dello snapshot di recupero utilizzato dal metodo [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) per un failover.</span><span class="sxs-lookup"><span data-stu-id="b805f-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="b805f-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="b805f-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="b805f-124">Crea una nuova relazione di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="b805f-125">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="b805f-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="b805f-126">Recupera le statistiche di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="b805f-127">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="b805f-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="b805f-128">Recupera le statistiche di replica associate alla relazione di replica specificata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="b805f-129">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b805f-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="b805f-130">**GetSystemCertificates**</span><span class="sxs-lookup"><span data-stu-id="b805f-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="b805f-131">Recupera i certificati di sistema in un sistema host.</span><span class="sxs-lookup"><span data-stu-id="b805f-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="b805f-132">**ImportInitialReplica**</span><span class="sxs-lookup"><span data-stu-id="b805f-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="b805f-133">Importa la replica iniziale per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="b805f-134">**InitiateFailback**</span><span class="sxs-lookup"><span data-stu-id="b805f-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="b805f-135">Avvia il failback per una macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b805f-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="b805f-136">Ovvero, imposta il failover per la macchina virtuale su un'app o un'immagine coerente con l'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="b805f-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="b805f-137">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b805f-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="b805f-138">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="b805f-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="b805f-139">Avvia un failover per una macchina virtuale in un'immagine dell'applicazione o del punto di replica standard.</span><span class="sxs-lookup"><span data-stu-id="b805f-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="b805f-140">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b805f-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="b805f-141">Modifica una voce di autorizzazione in un server.</span><span class="sxs-lookup"><span data-stu-id="b805f-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="b805f-142">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="b805f-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="b805f-143">Modifica le impostazioni di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="b805f-144">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="b805f-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="b805f-145">Modifica le impostazioni per il servizio di replica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b805f-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="b805f-146">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b805f-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="b805f-147">Rimuove la voce di autorizzazione da un server.</span><span class="sxs-lookup"><span data-stu-id="b805f-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="b805f-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="b805f-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="b805f-149">Rimuove una relazione di replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="b805f-150">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="b805f-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="b805f-151">Rimuove la relazione di replica della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="b805f-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="b805f-152">Per una macchina virtuale di replica, non è possibile rimuovere la replica primaria se è abilitata la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="b805f-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="b805f-153">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b805f-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="b805f-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b805f-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="b805f-155">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="b805f-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="b805f-156">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="b805f-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="b805f-157">Reimposta le statistiche di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="b805f-158">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="b805f-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="b805f-159">Reimposta le statistiche di replica associate alla relazione di replica specificata di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="b805f-160">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b805f-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="b805f-161">**Risincronizzare**</span><span class="sxs-lookup"><span data-stu-id="b805f-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="b805f-162">Esegue un'operazione di risincronizzazione nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="b805f-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="b805f-163">**ReverseReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="b805f-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="b805f-164">Replica una macchina virtuale di cui è stato eseguito il failover sul server primario.</span><span class="sxs-lookup"><span data-stu-id="b805f-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="b805f-165">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="b805f-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="b805f-166">Annulla il failover corrente per una macchina virtuale ignorando il disco di failover corrente.</span><span class="sxs-lookup"><span data-stu-id="b805f-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="b805f-167">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b805f-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="b805f-168">Imposta la voce di autorizzazione di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="b805f-169">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="b805f-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="b805f-170">Configura le impostazioni IP della scheda di rete da applicare a una macchina virtuale dopo un failover.</span><span class="sxs-lookup"><span data-stu-id="b805f-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="b805f-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="b805f-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="b805f-172">Avvia la replica di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="b805f-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="b805f-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="b805f-174">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="b805f-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="b805f-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="b805f-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="b805f-176">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="b805f-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="b805f-177">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="b805f-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="b805f-178">Crea una nuova replica di una macchina virtuale con lo snapshot specificato a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="b805f-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="b805f-179">**TestReplicationConnection**</span><span class="sxs-lookup"><span data-stu-id="b805f-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="b805f-180">Verifica se la replica può essere abilitata dal sistema host corrente al sistema di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="b805f-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="b805f-181">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b805f-181">Properties</span></span>

<span data-ttu-id="b805f-182">La **classe \_ ReplicationService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b805f-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b805f-183">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b805f-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-184">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b805f-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-186">Indica i valori possibili per il parametro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="b805f-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="b805f-187">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-188">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b805f-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-191">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b805f-191">A short description of the object.</span></span> <span data-ttu-id="b805f-192">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio replica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="b805f-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b805f-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-194">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-196">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="b805f-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b805f-197">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b805f-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b805f-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b805f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b805f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b805f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="b805f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="b805f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="b805f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b805f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b805f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b805f-206">)</span><span class="sxs-lookup"><span data-stu-id="b805f-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b805f-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b805f-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-210">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="b805f-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-211">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b805f-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b805f-212">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ReplicationService".</span><span class="sxs-lookup"><span data-stu-id="b805f-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-213">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b805f-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-216">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b805f-216">A description of the object.</span></span> <span data-ttu-id="b805f-217">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Service".</span><span class="sxs-lookup"><span data-stu-id="b805f-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b805f-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-221">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="b805f-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b805f-222">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b805f-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b805f-223">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b805f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="b805f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="b805f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="b805f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b805f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="b805f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="b805f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b805f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b805f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b805f-232">)</span><span class="sxs-lookup"><span data-stu-id="b805f-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b805f-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b805f-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-236">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b805f-236">A display name for the object.</span></span> <span data-ttu-id="b805f-237">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b805f-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b805f-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-241">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b805f-242">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="b805f-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="b805f-243">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-243">Value</span></span>                                                                        | <span data-ttu-id="b805f-244">Significato</span><span class="sxs-lookup"><span data-stu-id="b805f-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="b805f-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b805f-246">Abilitato</span><span class="sxs-lookup"><span data-stu-id="b805f-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b805f-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b805f-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-248">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-250">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b805f-251">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="b805f-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b805f-252">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="b805f-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="b805f-253">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-253">Value</span></span>                                                                        | <span data-ttu-id="b805f-254">Significato</span><span class="sxs-lookup"><span data-stu-id="b805f-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="b805f-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b805f-256">Abilitato</span><span class="sxs-lookup"><span data-stu-id="b805f-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b805f-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b805f-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-258">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-260">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-260">The current health of the element.</span></span> <span data-ttu-id="b805f-261">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b805f-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b805f-262">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="b805f-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b805f-263">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="b805f-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="b805f-264">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-264">Value</span></span>                                                                        | <span data-ttu-id="b805f-265">Significato</span><span class="sxs-lookup"><span data-stu-id="b805f-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="b805f-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="b805f-267">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="b805f-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b805f-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b805f-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-269">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b805f-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-271">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b805f-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b805f-272">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b805f-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b805f-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-276">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b805f-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b805f-277">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b805f-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b805f-278">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-279">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b805f-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-282">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="b805f-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-283">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b805f-283">The label by which the object is known.</span></span> <span data-ttu-id="b805f-284">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "replicasvc".</span><span class="sxs-lookup"><span data-stu-id="b805f-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-285">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b805f-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-286">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-288">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b805f-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b805f-289">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b805f-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b805f-290">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b805f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b805f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b805f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="b805f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="b805f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="b805f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="b805f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="b805f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="b805f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="b805f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="b805f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="b805f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="b805f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="b805f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="b805f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="b805f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="b805f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="b805f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b805f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b805f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b805f-310">)</span><span class="sxs-lookup"><span data-stu-id="b805f-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b805f-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b805f-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-312">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b805f-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-314">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b805f-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="b805f-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="b805f-316">Il valore in corrispondenza dell'indice zero sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b805f-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="b805f-317">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b805f-318">Significato</span><span class="sxs-lookup"><span data-stu-id="b805f-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="b805f-319"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="b805f-320">Il servizio di replica funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="b805f-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="b805f-321"><dt>**Errore**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="b805f-322">Uno o più listener di rete di replica non sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b805f-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="b805f-323">Verificare che le impostazioni del servizio di replica siano valide.</span><span class="sxs-lookup"><span data-stu-id="b805f-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b805f-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b805f-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-327">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="b805f-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="b805f-328">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="b805f-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b805f-329">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b805f-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-333">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="b805f-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-334">Tutte le informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="b805f-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="b805f-335">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-336">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="b805f-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-339">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="b805f-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-340">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="b805f-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="b805f-341">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="b805f-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="b805f-342">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b805f-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-346">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="b805f-346">Provides high level status information.</span></span> <span data-ttu-id="b805f-347">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b805f-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b805f-348">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b805f-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b805f-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b805f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b805f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="b805f-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="b805f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="b805f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b805f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b805f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b805f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b805f-356">)</span><span class="sxs-lookup"><span data-stu-id="b805f-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b805f-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b805f-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-358">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-360">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="b805f-361">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="b805f-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b805f-362">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="b805f-363">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="b805f-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="b805f-364">In tal caso, viene utilizzato il valore 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="b805f-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="b805f-365">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b805f-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="b805f-366">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-366">Value</span></span>                                                                         | <span data-ttu-id="b805f-367">Significato</span><span class="sxs-lookup"><span data-stu-id="b805f-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="b805f-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b805f-369">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="b805f-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b805f-370">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="b805f-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-371">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b805f-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-373">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b805f-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="b805f-374">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="b805f-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-375">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="b805f-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-378">Qualificatori: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="b805f-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-379">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="b805f-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="b805f-380">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b805f-381">**Status**</span><span class="sxs-lookup"><span data-stu-id="b805f-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-384">Indica lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-384">Indicates the status of the element.</span></span> <span data-ttu-id="b805f-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="b805f-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-386">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b805f-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-387">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b805f-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b805f-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-389">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b805f-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b805f-390">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b805f-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b805f-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b805f-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-392">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-394">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="b805f-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-395">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b805f-395">The scoping system's creation class name.</span></span> <span data-ttu-id="b805f-396">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="b805f-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="b805f-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b805f-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b805f-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b805f-400">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="b805f-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b805f-401">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="b805f-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="b805f-402">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b805f-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b805f-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b805f-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-404">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b805f-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-406">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b805f-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b805f-407">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b805f-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b805f-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b805f-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b805f-409">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b805f-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b805f-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b805f-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b805f-411">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b805f-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b805f-412">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b805f-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b805f-413">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b805f-413">Requirements</span></span>



| <span data-ttu-id="b805f-414">Requisito</span><span class="sxs-lookup"><span data-stu-id="b805f-414">Requirement</span></span> | <span data-ttu-id="b805f-415">Valore</span><span class="sxs-lookup"><span data-stu-id="b805f-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b805f-416">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b805f-416">Minimum supported client</span></span><br/> | <span data-ttu-id="b805f-417">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b805f-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b805f-418">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b805f-418">Minimum supported server</span></span><br/> | <span data-ttu-id="b805f-419">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b805f-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b805f-420">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b805f-420">Namespace</span></span><br/>                | <span data-ttu-id="b805f-421">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b805f-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b805f-422">MOF</span><span class="sxs-lookup"><span data-stu-id="b805f-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b805f-423"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b805f-424">DLL</span><span class="sxs-lookup"><span data-stu-id="b805f-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b805f-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b805f-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

