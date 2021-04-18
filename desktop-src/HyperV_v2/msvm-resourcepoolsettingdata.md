---
description: Rappresenta le impostazioni di un' \_ istanza di ResourcePool MSVM che non sono correlate all'allocazione.
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Classe Msvm_ResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37ec7dc6600dbc536ac50a2042e7d53ff8043242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312886"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="9776f-103">\_Classe MSVM ResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="9776f-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="9776f-104">Rappresenta le impostazioni di un'istanza di [**\_ ResourcePool MSVM**](msvm-resourcepool.md) che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="9776f-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="9776f-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9776f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9776f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9776f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
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

## <a name="members"></a><span data-ttu-id="9776f-107">Members</span><span class="sxs-lookup"><span data-stu-id="9776f-107">Members</span></span>

<span data-ttu-id="9776f-108">La **classe \_ ResourcePoolSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9776f-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9776f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9776f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9776f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9776f-110">Properties</span></span>

<span data-ttu-id="9776f-111">La **classe \_ ResourcePoolSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9776f-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9776f-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9776f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9776f-115">A short description of the object.</span></span> <span data-ttu-id="9776f-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9776f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9776f-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="9776f-120">A description of the object.</span></span> <span data-ttu-id="9776f-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9776f-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9776f-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9776f-125">A display name for the object.</span></span> <span data-ttu-id="9776f-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9776f-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9776f-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9776f-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9776f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9776f-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="9776f-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9776f-132">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9776f-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="9776f-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9776f-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-136">Specifica la strategia di allocazione che verrà usata dal pool di risorse per bilanciare l'utilizzo delle risorse tra le risorse aggregate.</span><span class="sxs-lookup"><span data-stu-id="9776f-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="9776f-137">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="9776f-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9776f-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="9776f-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="9776f-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distribuito** (4)</span><span class="sxs-lookup"><span data-stu-id="9776f-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidato** (5)</span><span class="sxs-lookup"><span data-stu-id="9776f-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9776f-143">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="9776f-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9776f-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-146">Specifica se il pool di risorse può tentare di usare altre risorse host per soddisfare la richiesta di allocazione se le risorse desiderate non possono essere allocate.</span><span class="sxs-lookup"><span data-stu-id="9776f-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="9776f-147">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="9776f-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9776f-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="9776f-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (3)</span><span class="sxs-lookup"><span data-stu-id="9776f-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinità Soft** (4)</span><span class="sxs-lookup"><span data-stu-id="9776f-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinità hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="9776f-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="9776f-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9776f-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9776f-155">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="9776f-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-156">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9776f-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9776f-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-158">Specifica l'ordine in cui verranno selezionate le risorse host disponibili tramite questo pool quando si tenta di soddisfare una richiesta di allocazione e la risorsa host richiesta non è disponibile o non è specificata alcuna risorsa host.</span><span class="sxs-lookup"><span data-stu-id="9776f-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="9776f-159">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-160">**Note**</span><span class="sxs-lookup"><span data-stu-id="9776f-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-163">Note fornite dall'utente finale correlate a questo pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="9776f-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="9776f-164">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-165">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="9776f-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-168">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su 0 (other).</span><span class="sxs-lookup"><span data-stu-id="9776f-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="9776f-169">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-170">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="9776f-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-173">Identificatore per il pool.</span><span class="sxs-lookup"><span data-stu-id="9776f-173">An identifier for the pool.</span></span> <span data-ttu-id="9776f-174">Questa proprietà viene utilizzata per fornire la correlazione tra il salvataggio e il ripristino dei dati di configurazione nell'archivio permanente sottostante.</span><span class="sxs-lookup"><span data-stu-id="9776f-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="9776f-175">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="9776f-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9776f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-179">Stringa che descrive un sottotipo specifico dell'implementazione per questo pool.</span><span class="sxs-lookup"><span data-stu-id="9776f-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="9776f-180">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9776f-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="9776f-181">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9776f-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9776f-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9776f-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9776f-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9776f-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9776f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9776f-185">Tipo di risorsa che questo pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="9776f-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="9776f-186">Questa proprietà viene ereditata da [**MSVM \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9776f-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="9776f-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9776f-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="9776f-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="9776f-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="9776f-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="9776f-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="9776f-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="9776f-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="9776f-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="9776f-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="9776f-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="9776f-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="9776f-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="9776f-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="9776f-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="9776f-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="9776f-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="9776f-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="9776f-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="9776f-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="9776f-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="9776f-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="9776f-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="9776f-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="9776f-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="9776f-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="9776f-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="9776f-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="9776f-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="9776f-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="9776f-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="9776f-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="9776f-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="9776f-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="9776f-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9776f-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="9776f-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9776f-222">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9776f-222">Requirements</span></span>



| <span data-ttu-id="9776f-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="9776f-223">Requirement</span></span> | <span data-ttu-id="9776f-224">Valore</span><span class="sxs-lookup"><span data-stu-id="9776f-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9776f-225">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9776f-225">Minimum supported client</span></span><br/> | <span data-ttu-id="9776f-226">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9776f-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9776f-227">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9776f-227">Minimum supported server</span></span><br/> | <span data-ttu-id="9776f-228">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9776f-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9776f-229">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9776f-229">Namespace</span></span><br/>                | <span data-ttu-id="9776f-230">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9776f-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9776f-231">MOF</span><span class="sxs-lookup"><span data-stu-id="9776f-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9776f-232"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9776f-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9776f-233">DLL</span><span class="sxs-lookup"><span data-stu-id="9776f-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9776f-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9776f-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

