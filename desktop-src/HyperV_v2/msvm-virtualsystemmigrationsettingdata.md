---
description: Rappresenta le impostazioni di migrazione per la migrazione di un sistema virtuale e dello spazio di archiviazione collegato a un sistema virtuale.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878698"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="264a4-103">\_Classe MSVM VirtualSystemMigrationSettingData</span><span class="sxs-lookup"><span data-stu-id="264a4-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="264a4-104">Rappresenta le impostazioni di migrazione per la migrazione di un sistema virtuale e dello spazio di archiviazione collegato a un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="264a4-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="264a4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="264a4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="264a4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="264a4-107">Members</span><span class="sxs-lookup"><span data-stu-id="264a4-107">Members</span></span>

<span data-ttu-id="264a4-108">La **classe \_ VirtualSystemMigrationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="264a4-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="264a4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="264a4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="264a4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="264a4-110">Properties</span></span>

<span data-ttu-id="264a4-111">La **classe \_ VirtualSystemMigrationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="264a4-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="264a4-112">**AllowOverwriteExistingFile**</span><span class="sxs-lookup"><span data-stu-id="264a4-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-115">Consente all'operazione di migrazione dell'archiviazione di sovrascrivere i file. vhdx esistenti.</span><span class="sxs-lookup"><span data-stu-id="264a4-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-116">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="264a4-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="264a4-117">**AvoidRemovingVHDs**</span><span class="sxs-lookup"><span data-stu-id="264a4-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-120">Non rimuovere i VHD durante la migrazione, ad esempio i dischi rigidi virtuali nell'origine nei dischi rigidi virtuali far nella destinazione in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="264a4-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-121">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="264a4-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="264a4-122">**Larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="264a4-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="264a4-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-125">Specifica la larghezza di banda assegnata o richiesta per un'operazione di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="264a4-126">Le unità di larghezza di banda sono specificate dalla proprietà **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="264a4-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="264a4-127">All'interno di una migrazione, un valore pari a 0 indica la larghezza di banda predefinita.</span><span class="sxs-lookup"><span data-stu-id="264a4-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="264a4-128">In caso contrario, un valore pari a 0 indica che non sono supportate le larghezze di banda.</span><span class="sxs-lookup"><span data-stu-id="264a4-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="264a4-129">La **larghezza di banda** e la **priorità** possono essere utilizzate insieme.</span><span class="sxs-lookup"><span data-stu-id="264a4-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="264a4-130">I processi di migrazione con il valore di uguale priorità più alto condividono la larghezza di banda disponibile in base alla larghezza di banda richiesta.</span><span class="sxs-lookup"><span data-stu-id="264a4-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="264a4-131">Se non viene utilizzata tutta la larghezza di banda da questo set di processi, i processi di migrazione con la stessa priorità inferiore successiva condividono la larghezza di banda rimanente.</span><span class="sxs-lookup"><span data-stu-id="264a4-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="264a4-132">Se la larghezza di banda rimane ancora maggiore, vengono considerati i processi di migrazione con la priorità più bassa uguale e così via.</span><span class="sxs-lookup"><span data-stu-id="264a4-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="264a4-133">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-134">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="264a4-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-137">Specifica le unità utilizzate dalla proprietà della **larghezza di banda** .</span><span class="sxs-lookup"><span data-stu-id="264a4-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="264a4-138">Il valore di questa proprietà deve essere un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="264a4-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="264a4-139">Se il valore di questa proprietà è "percent", il valore della proprietà della **larghezza di banda** deve essere compreso tra 0 e 100, con valori più elevati che indicano una larghezza di banda maggiore.</span><span class="sxs-lookup"><span data-stu-id="264a4-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="264a4-140">Il valore 100 indica la larghezza di banda totale disponibile per l'esecuzione delle operazioni di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="264a4-141">I valori compresi tra 1 e 100 devono essere correlati in modo lineare con l'intervallo della larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="264a4-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="264a4-142">Ad esempio, il valore 50 deve richiedere metà della larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="264a4-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="264a4-143">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-144">**CancelIfBlackoutThresholdExceeded**</span><span class="sxs-lookup"><span data-stu-id="264a4-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-147">Annulla la migrazione se viene superato il tempo di soglia di blackout.</span><span class="sxs-lookup"><span data-stu-id="264a4-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-148">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="264a4-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="264a4-149">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="264a4-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-152">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="264a4-152">A short description of the object.</span></span> <span data-ttu-id="264a4-153">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="264a4-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="264a4-154">**CPUCappingMagnitude**</span><span class="sxs-lookup"><span data-stu-id="264a4-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="264a4-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="264a4-157">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span><span class="sxs-lookup"><span data-stu-id="264a4-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="264a4-158">Grado di limitazione della CPU durante la migrazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-159">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="264a4-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="264a4-160">**Normale** (0)</span><span class="sxs-lookup"><span data-stu-id="264a4-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="264a4-161">**Bassa** (1)</span><span class="sxs-lookup"><span data-stu-id="264a4-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="264a4-162">**Alta** (2)</span><span class="sxs-lookup"><span data-stu-id="264a4-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="264a4-163">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="264a4-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-166">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="264a4-166">A description of the object.</span></span> <span data-ttu-id="264a4-167">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="264a4-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="264a4-168">**DestinationIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="264a4-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-169">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="264a4-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="264a4-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-171">Questa operazione sarà **null** per la migrazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="264a4-172">Per la migrazione del sistema virtuale, può contenere un elenco di indirizzi IP dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-173">**DestinationPlannedVirtualSystemId**</span><span class="sxs-lookup"><span data-stu-id="264a4-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-176">Se nella destinazione della migrazione esiste una macchina virtuale pianificata, questa proprietà verrà impostata sul GUID della macchina virtuale di destinazione pianificata in cui deve essere eseguita la migrazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="264a4-177">Questa operazione è utile nei casi in cui un utente ha creato una macchina virtuale pianificata nella destinazione, insieme alla configurazione delle risorse e desidera che una macchina virtuale dall'origine venga migrata in questa macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="264a4-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="264a4-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-181">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="264a4-181">A display name for the object.</span></span> <span data-ttu-id="264a4-182">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="264a4-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="264a4-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="264a4-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-186">Indica se comprimere il traffico di migrazione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="264a4-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="264a4-187">**True** indica di comprimere. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="264a4-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="264a4-188">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="264a4-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="264a4-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="264a4-192">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="264a4-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="264a4-193">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="264a4-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="264a4-194">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="264a4-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="264a4-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="264a4-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="264a4-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="264a4-198">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span><span class="sxs-lookup"><span data-stu-id="264a4-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="264a4-199">Specifica il tipo di operazione di migrazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="264a4-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="264a4-200">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="264a4-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="264a4-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="264a4-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span><span class="sxs-lookup"><span data-stu-id="264a4-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-203">Esegue la migrazione del sistema virtuale all'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="264a4-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Archiviazione** (32769)</span><span class="sxs-lookup"><span data-stu-id="264a4-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-205">Esegue la migrazione solo delle risorse di archiviazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="264a4-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>Gestione **temporanea** (32770)</span><span class="sxs-lookup"><span data-stu-id="264a4-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-207">Utilizzando la configurazione del sistema virtuale, in viene creato un sistema virtuale pianificato nell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="264a4-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span><span class="sxs-lookup"><span data-stu-id="264a4-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-209">Esegue la migrazione del sistema virtuale e della relativa archiviazione nell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="264a4-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span><span class="sxs-lookup"><span data-stu-id="264a4-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-211">Esegue una verifica della capacità di migrazione delle risorse di archiviazione del sistema virtuale nell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="264a4-212">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="264a4-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="264a4-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-215">Specifica il tipo di trasporto da applicare se il valore di **TransportType** è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="264a4-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="264a4-216">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-217">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="264a4-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-218">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="264a4-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="264a4-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="264a4-220">Specifica un'importanza della migrazione relativa, che può essere usata dal sistema di migrazione per ordinare o altrimenti assegnare la preferenza tra più richieste di migrazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="264a4-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="264a4-221">Più basso è il valore, maggiore è la priorità.</span><span class="sxs-lookup"><span data-stu-id="264a4-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="264a4-222">All'interno di una migrazione, un valore pari a 0 indica la priorità predefinita.</span><span class="sxs-lookup"><span data-stu-id="264a4-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="264a4-223">In caso contrario, il valore 0 indica che le priorità non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="264a4-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="264a4-224">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-225">**RemoveSourceUnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="264a4-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-226">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-227">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-228">Rimuovere i dischi rigidi virtuali non gestiti di origine.</span><span class="sxs-lookup"><span data-stu-id="264a4-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-229">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="264a4-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="264a4-230">**RetainVhdCopiesOnSource**</span><span class="sxs-lookup"><span data-stu-id="264a4-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="264a4-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="264a4-233">Per una migrazione dell'archiviazione, specifica se i VHD di sola lettura nell'host di origine devono essere rimossi al termine della migrazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="264a4-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="264a4-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-235">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="264a4-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="264a4-236">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="264a4-237">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="264a4-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="264a4-238">Specifica il tipo di trasporto da applicare per un'operazione di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a4-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="264a4-239">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="264a4-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="264a4-240">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="264a4-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="264a4-241">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="264a4-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="264a4-242">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="264a4-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="264a4-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="264a4-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="264a4-244">**TLS Strict** (4)</span><span class="sxs-lookup"><span data-stu-id="264a4-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="264a4-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="264a4-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="264a4-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="264a4-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="264a4-247">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="264a4-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="264a4-248">**Fornitore riservato** (32768...)</span><span class="sxs-lookup"><span data-stu-id="264a4-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="264a4-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="264a4-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="264a4-250">Per la migrazione in tempo reale, questa proprietà specifica il tipo di trasporto da utilizzare per il trasferimento dello stato del sistema virtuale all'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="264a4-251">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="264a4-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="264a4-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="264a4-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-253">Indica il tipo di trasporto TCP.</span><span class="sxs-lookup"><span data-stu-id="264a4-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="264a4-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="264a4-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="264a4-255">Indica che il tipo di trasporto per il trasferimento dello stato della macchina virtuale è SMB.</span><span class="sxs-lookup"><span data-stu-id="264a4-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="264a4-256">**UnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="264a4-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264a4-257">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="264a4-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="264a4-258">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="264a4-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="264a4-259">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ MoveUnmanagedVhd")</span><span class="sxs-lookup"><span data-stu-id="264a4-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="264a4-260">Matrice di istanze di [**\_ MoveUnmanagedVhd MSVM**](msvm-moveunmanagedvhd.md) incorporate contenenti informazioni sui dischi rigidi virtuali non gestiti.</span><span class="sxs-lookup"><span data-stu-id="264a4-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-261">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="264a4-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="264a4-262">Requisiti</span><span class="sxs-lookup"><span data-stu-id="264a4-262">Requirements</span></span>



| <span data-ttu-id="264a4-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="264a4-263">Requirement</span></span> | <span data-ttu-id="264a4-264">Valore</span><span class="sxs-lookup"><span data-stu-id="264a4-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="264a4-265">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="264a4-265">Minimum supported client</span></span><br/> | <span data-ttu-id="264a4-266">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="264a4-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="264a4-267">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="264a4-267">Minimum supported server</span></span><br/> | <span data-ttu-id="264a4-268">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="264a4-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="264a4-269">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="264a4-269">Namespace</span></span><br/>                | <span data-ttu-id="264a4-270">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="264a4-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="264a4-271">MOF</span><span class="sxs-lookup"><span data-stu-id="264a4-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="264a4-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="264a4-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="264a4-273">DLL</span><span class="sxs-lookup"><span data-stu-id="264a4-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="264a4-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="264a4-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="264a4-275">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="264a4-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264a4-276">**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="264a4-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="264a4-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="264a4-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

