---
description: Rappresenta le impostazioni di un' \_ istanza di ResourcePool MSVM che non sono correlate all'allocazione.
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Classe Msvm_AbstractResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9109bd428797c8c4f1073577e015bf4b9eddcc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967824"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="37c91-103">\_Classe MSVM AbstractResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="37c91-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="37c91-104">Rappresenta le impostazioni di un'istanza di [**\_ ResourcePool MSVM**](msvm-resourcepool.md) che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="37c91-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="37c91-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="37c91-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c91-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37c91-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="37c91-107">Members</span><span class="sxs-lookup"><span data-stu-id="37c91-107">Members</span></span>

<span data-ttu-id="37c91-108">La **classe \_ AbstractResourcePoolSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37c91-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="37c91-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37c91-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37c91-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37c91-110">Properties</span></span>

<span data-ttu-id="37c91-111">La **classe \_ AbstractResourcePoolSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37c91-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37c91-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="37c91-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37c91-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37c91-115">A short description of the object.</span></span> <span data-ttu-id="37c91-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37c91-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37c91-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="37c91-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37c91-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="37c91-120">A description of the object.</span></span> <span data-ttu-id="37c91-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37c91-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37c91-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="37c91-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37c91-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37c91-125">A display name for the object.</span></span> <span data-ttu-id="37c91-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37c91-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37c91-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37c91-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="37c91-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="37c91-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="37c91-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="37c91-132">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37c91-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37c91-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="37c91-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37c91-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37c91-136">Specifica la strategia di allocazione che verrà usata dal pool di risorse per bilanciare l'utilizzo delle risorse tra le risorse aggregate.</span><span class="sxs-lookup"><span data-stu-id="37c91-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37c91-137">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="37c91-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="37c91-138">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="37c91-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="37c91-139">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="37c91-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="37c91-140">**Distribuito** (4)</span><span class="sxs-lookup"><span data-stu-id="37c91-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="37c91-141">**Consolidato** (5)</span><span class="sxs-lookup"><span data-stu-id="37c91-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37c91-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="37c91-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37c91-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-145">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="37c91-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-146">Specifica se il pool di risorse può tentare di usare altre risorse host per soddisfare la richiesta di allocazione se le risorse desiderate non possono essere allocate.</span><span class="sxs-lookup"><span data-stu-id="37c91-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37c91-147">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="37c91-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="37c91-148">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="37c91-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="37c91-149">**Dedicato** (3)</span><span class="sxs-lookup"><span data-stu-id="37c91-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="37c91-150">**Affinità Soft** (4)</span><span class="sxs-lookup"><span data-stu-id="37c91-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="37c91-151">**Affinità hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="37c91-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="37c91-152">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="37c91-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="37c91-153">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="37c91-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37c91-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="37c91-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-155">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="37c91-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37c91-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-157">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="37c91-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-158">Specifica l'ordine in cui verranno selezionate le risorse host disponibili tramite questo pool quando si tenta di soddisfare una richiesta di allocazione e la risorsa host richiesta non è disponibile o non è specificata alcuna risorsa host.</span><span class="sxs-lookup"><span data-stu-id="37c91-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="37c91-159">**Note**</span><span class="sxs-lookup"><span data-stu-id="37c91-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37c91-162">Note fornite dall'utente finale correlate a questo pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="37c91-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="37c91-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="37c91-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-166">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span><span class="sxs-lookup"><span data-stu-id="37c91-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-167">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su 0 (other).</span><span class="sxs-lookup"><span data-stu-id="37c91-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="37c91-168">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="37c91-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-171">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolID**")</span><span class="sxs-lookup"><span data-stu-id="37c91-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-172">Identificatore per il pool.</span><span class="sxs-lookup"><span data-stu-id="37c91-172">An identifier for the pool.</span></span> <span data-ttu-id="37c91-173">Questa proprietà viene utilizzata per fornire la correlazione tra il salvataggio e il ripristino dei dati di configurazione nell'archivio permanente sottostante.</span><span class="sxs-lookup"><span data-stu-id="37c91-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="37c91-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="37c91-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37c91-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-177">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="37c91-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-178">Stringa che descrive un sottotipo specifico dell'implementazione per il pool.</span><span class="sxs-lookup"><span data-stu-id="37c91-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="37c91-179">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="37c91-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="37c91-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="37c91-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c91-181">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37c91-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37c91-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37c91-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37c91-183">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="37c91-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="37c91-184">Tipo di risorsa che questo pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="37c91-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37c91-185">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="37c91-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="37c91-186">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="37c91-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="37c91-187">**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="37c91-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="37c91-188">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="37c91-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="37c91-189">**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="37c91-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="37c91-190">**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="37c91-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="37c91-191">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="37c91-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="37c91-192">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="37c91-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="37c91-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="37c91-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="37c91-194">**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="37c91-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="37c91-195">**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="37c91-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="37c91-196">**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="37c91-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="37c91-197">**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="37c91-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="37c91-198">**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="37c91-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="37c91-199">**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="37c91-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="37c91-200">**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="37c91-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="37c91-201">**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="37c91-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="37c91-202">**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="37c91-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="37c91-203">**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="37c91-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="37c91-204">**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="37c91-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="37c91-205">**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="37c91-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="37c91-206">**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="37c91-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="37c91-207">**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="37c91-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="37c91-208">**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="37c91-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="37c91-209">**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="37c91-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="37c91-210">**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="37c91-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="37c91-211">**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="37c91-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="37c91-212">**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="37c91-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="37c91-213">**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="37c91-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="37c91-214">**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="37c91-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="37c91-215">**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="37c91-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="37c91-216">**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="37c91-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="37c91-217">**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="37c91-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="37c91-218">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="37c91-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="37c91-219">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="37c91-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="37c91-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="37c91-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="37c91-221">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37c91-221">Requirements</span></span>



| <span data-ttu-id="37c91-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c91-222">Requirement</span></span> | <span data-ttu-id="37c91-223">Valore</span><span class="sxs-lookup"><span data-stu-id="37c91-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c91-224">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37c91-224">Minimum supported client</span></span><br/> | <span data-ttu-id="37c91-225">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="37c91-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37c91-226">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37c91-226">Minimum supported server</span></span><br/> | <span data-ttu-id="37c91-227">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="37c91-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37c91-228">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37c91-228">Namespace</span></span><br/>                | <span data-ttu-id="37c91-229">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="37c91-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37c91-230">MOF</span><span class="sxs-lookup"><span data-stu-id="37c91-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37c91-231"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37c91-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37c91-232">DLL</span><span class="sxs-lookup"><span data-stu-id="37c91-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37c91-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37c91-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

