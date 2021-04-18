---
description: Fornisce le statistiche di replica per una macchina virtuale.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Classe Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313852"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="7697d-103">\_Classe MSVM ReplicationStatistics</span><span class="sxs-lookup"><span data-stu-id="7697d-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="7697d-104">Fornisce le statistiche di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7697d-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="7697d-105">Queste statistiche coprono la durata specificata dalle proprietà **MonitoringStartTime** e **MonitoringInterval** della classe [**MSVM \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="7697d-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="7697d-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7697d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7697d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7697d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="7697d-108">Members</span><span class="sxs-lookup"><span data-stu-id="7697d-108">Members</span></span>

<span data-ttu-id="7697d-109">La **classe \_ ReplicationStatistics di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7697d-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="7697d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7697d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7697d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7697d-111">Properties</span></span>

<span data-ttu-id="7697d-112">La **classe \_ ReplicationStatistics di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7697d-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7697d-113">**ApplicationConsistentSnapshotFailureCount**</span><span class="sxs-lookup"><span data-stu-id="7697d-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-116">Numero totale di errori di snapshot VSS.</span><span class="sxs-lookup"><span data-stu-id="7697d-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7697d-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7697d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-120">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7697d-120">A short description of the object.</span></span> <span data-ttu-id="7697d-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7697d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7697d-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7697d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-125">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7697d-125">A description of the object.</span></span> <span data-ttu-id="7697d-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7697d-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7697d-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7697d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-130">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7697d-130">A display name for the object.</span></span> <span data-ttu-id="7697d-131">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7697d-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-132">**EndStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-135">Ora, in formato UTC, in cui il servizio di replica Hyper-V ha interrotto la raccolta dei dati delle statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="7697d-136">A questo punto, viene avviato un nuovo ciclo di statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7697d-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7697d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7697d-140">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7697d-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7697d-141">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7697d-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7697d-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7697d-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-143">**LastTestFailoverTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-144">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-146">Indica l'ultima volta in cui è stato creato un sistema di replica di test per una macchina virtuale abilitata per la replica nel server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7697d-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-147">**MaxReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="7697d-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-150">Quantità massima di tempo impiegato per completare un singolo ciclo di replica, in secondi.</span><span class="sxs-lookup"><span data-stu-id="7697d-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-151">**MaxReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="7697d-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-152">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7697d-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-154">Numero massimo di dati di replica trasferiti in byte al sistema host di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7697d-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="7697d-155">Rappresenta le dimensioni massime dei dati di replica inviati in un singolo ciclo per questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="7697d-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-156">**NetworkFailureCount**</span><span class="sxs-lookup"><span data-stu-id="7697d-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-159">Numero totale di errori di rete rilevati per il canale di replica con sistema host di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7697d-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-160">**PendingReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="7697d-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-161">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7697d-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-163">Dimensioni in byte dei dati per una replica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7697d-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-164">**ReplicationFailureCount**</span><span class="sxs-lookup"><span data-stu-id="7697d-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-167">Numero totale di errori di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-167">The total number of replication failures.</span></span> <span data-ttu-id="7697d-168">Sono inclusi gli errori per l'operazione di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="7697d-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-172">Stato di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7697d-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="7697d-173">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7697d-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7697d-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (0)</span><span class="sxs-lookup"><span data-stu-id="7697d-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7697d-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="7697d-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7697d-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (2)</span><span class="sxs-lookup"><span data-stu-id="7697d-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7697d-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="7697d-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7697d-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="7697d-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-179">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-181">Latenza di replica totale durante il trasferimento dei dati al sistema host di ripristino, in secondi.</span><span class="sxs-lookup"><span data-stu-id="7697d-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-182">**ReplicationMissCount**</span><span class="sxs-lookup"><span data-stu-id="7697d-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-185">Numero di cicli di replica mancanti.</span><span class="sxs-lookup"><span data-stu-id="7697d-185">The number of missed replication cycles.</span></span> <span data-ttu-id="7697d-186">Ciò può essere dovuto a carichi di lavoro gravosi, problemi di rete o errori di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-187">**ReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="7697d-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-188">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7697d-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-190">Quantità totale di dati di replica trasferiti in byte al sistema host di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7697d-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-191">**ReplicationSuccessCount**</span><span class="sxs-lookup"><span data-stu-id="7697d-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-192">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7697d-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-194">Numero totale di repliche riuscite per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7697d-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7697d-195">**StartStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7697d-196">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7697d-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7697d-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7697d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7697d-198">Ora, in formato UTC, in cui il servizio di replica Hyper-V ha iniziato a raccogliere i dati delle statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="7697d-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7697d-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7697d-199">Requirements</span></span>



| <span data-ttu-id="7697d-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="7697d-200">Requirement</span></span> | <span data-ttu-id="7697d-201">Valore</span><span class="sxs-lookup"><span data-stu-id="7697d-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7697d-202">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7697d-202">Minimum supported client</span></span><br/> | <span data-ttu-id="7697d-203">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7697d-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7697d-204">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7697d-204">Minimum supported server</span></span><br/> | <span data-ttu-id="7697d-205">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7697d-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7697d-206">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7697d-206">Namespace</span></span><br/>                | <span data-ttu-id="7697d-207">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7697d-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7697d-208">MOF</span><span class="sxs-lookup"><span data-stu-id="7697d-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7697d-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7697d-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7697d-210">DLL</span><span class="sxs-lookup"><span data-stu-id="7697d-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7697d-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7697d-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

