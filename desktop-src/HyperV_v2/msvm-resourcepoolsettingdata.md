---
description: "Msvm_ResourcePoolSettingData classe: rappresenta le impostazioni di un'istanza \\_ di Msvm ResourcePool che non sono correlate all'allocazione."
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Msvm_ResourcePoolSettingData classe
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
ms.openlocfilehash: 4fba27ec5c12e0c3cb18b8a6dfd4a863e59cad62
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111509"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="7a79c-103">Classe \_ Msvm ResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="7a79c-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="7a79c-104">Rappresenta le impostazioni di [**un'istanza di Msvm \_ ResourcePool**](msvm-resourcepool.md) che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="7a79c-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="7a79c-105">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7a79c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a79c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a79c-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7a79c-107">Members</span><span class="sxs-lookup"><span data-stu-id="7a79c-107">Members</span></span>

<span data-ttu-id="7a79c-108">La **classe Msvm \_ ResourcePoolSettingData** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7a79c-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7a79c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7a79c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a79c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7a79c-110">Properties</span></span>

<span data-ttu-id="7a79c-111">La **classe Msvm \_ ResourcePoolSettingData** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a79c-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a79c-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7a79c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-113">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a79c-115">A short description of the object.</span></span> <span data-ttu-id="7a79c-116">Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="7a79c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7a79c-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-118">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7a79c-120">A description of the object.</span></span> <span data-ttu-id="7a79c-121">Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="7a79c-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7a79c-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-123">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a79c-125">A display name for the object.</span></span> <span data-ttu-id="7a79c-126">Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="7a79c-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7a79c-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-128">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7a79c-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7a79c-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7a79c-132">Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7a79c-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="7a79c-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-134">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="7a79c-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-136">Specifica la strategia di allocazione che deve essere usata dal pool di risorse per bilanciare l'utilizzo delle risorse tra le risorse aggregate.</span><span class="sxs-lookup"><span data-stu-id="7a79c-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="7a79c-137">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="7a79c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7a79c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="7a79c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="7a79c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distribuito** (4)</span><span class="sxs-lookup"><span data-stu-id="7a79c-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidato** (5 )</span><span class="sxs-lookup"><span data-stu-id="7a79c-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7a79c-143">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="7a79c-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-144">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="7a79c-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-146">Specifica se il pool di risorse può tentare di usare altre risorse host per soddisfare la richiesta di allocazione se non è possibile allocare le risorse desiderate.</span><span class="sxs-lookup"><span data-stu-id="7a79c-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="7a79c-147">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="7a79c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7a79c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="7a79c-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (3)</span><span class="sxs-lookup"><span data-stu-id="7a79c-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinità soft** (4)</span><span class="sxs-lookup"><span data-stu-id="7a79c-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinità rigida** (5)</span><span class="sxs-lookup"><span data-stu-id="7a79c-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="7a79c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span><span class="sxs-lookup"><span data-stu-id="7a79c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7a79c-155">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="7a79c-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-156">Tipo di dati: **matrice di** stringhe</span><span class="sxs-lookup"><span data-stu-id="7a79c-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-158">Specifica l'ordine in cui verranno selezionate le risorse host disponibili tramite questo pool quando si tenta di soddisfare una richiesta di allocazione e la risorsa host richiesta non è disponibile o non viene specificata alcuna risorsa host.</span><span class="sxs-lookup"><span data-stu-id="7a79c-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="7a79c-159">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-160">**Note**</span><span class="sxs-lookup"><span data-stu-id="7a79c-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-161">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-163">Note fornite dall'utente finale correlate a questo pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a79c-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="7a79c-164">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-165">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="7a79c-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-166">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-168">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su 0 (Altro).</span><span class="sxs-lookup"><span data-stu-id="7a79c-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="7a79c-169">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-170">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="7a79c-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-171">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-173">Identificatore per il pool.</span><span class="sxs-lookup"><span data-stu-id="7a79c-173">An identifier for the pool.</span></span> <span data-ttu-id="7a79c-174">Questa proprietà viene usata per fornire la correlazione tra il salvataggio e il ripristino dei dati di configurazione nell'archiviazione permanente sottostante.</span><span class="sxs-lookup"><span data-stu-id="7a79c-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="7a79c-175">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="7a79c-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-177">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="7a79c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-179">Stringa che descrive un sottotipo specifico dell'implementazione per questo pool.</span><span class="sxs-lookup"><span data-stu-id="7a79c-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="7a79c-180">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7a79c-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="7a79c-181">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79c-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="7a79c-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a79c-183">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="7a79c-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a79c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a79c-185">Tipo di risorsa che il pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="7a79c-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="7a79c-186">Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="7a79c-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="7a79c-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7a79c-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="7a79c-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="7a79c-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="7a79c-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="7a79c-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallela** (6)</span><span class="sxs-lookup"><span data-stu-id="7a79c-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="7a79c-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="7a79c-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="7a79c-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="7a79c-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di** rete (11)</span><span class="sxs-lookup"><span data-stu-id="7a79c-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot di I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="7a79c-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo di I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="7a79c-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="7a79c-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="7a79c-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="7a79c-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="7a79c-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="7a79c-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di** archiviazione (19)</span><span class="sxs-lookup"><span data-stu-id="7a79c-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di** archiviazione (20)</span><span class="sxs-lookup"><span data-stu-id="7a79c-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="7a79c-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="7a79c-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="7a79c-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafico** (24)</span><span class="sxs-lookup"><span data-stu-id="7a79c-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span><span class="sxs-lookup"><span data-stu-id="7a79c-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="7a79c-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="7a79c-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Alimentazione** (28)</span><span class="sxs-lookup"><span data-stu-id="7a79c-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="7a79c-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta commutatore Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="7a79c-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="7a79c-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="7a79c-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="7a79c-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7a79c-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7a79c-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF )</span><span class="sxs-lookup"><span data-stu-id="7a79c-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a79c-222">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a79c-222">Requirements</span></span>



| <span data-ttu-id="7a79c-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a79c-223">Requirement</span></span> | <span data-ttu-id="7a79c-224">Valore</span><span class="sxs-lookup"><span data-stu-id="7a79c-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a79c-225">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a79c-225">Minimum supported client</span></span><br/> | <span data-ttu-id="7a79c-226">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a79c-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7a79c-227">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a79c-227">Minimum supported server</span></span><br/> | <span data-ttu-id="7a79c-228">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a79c-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a79c-229">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7a79c-229">Namespace</span></span><br/>                | <span data-ttu-id="7a79c-230">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="7a79c-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7a79c-231">MOF</span><span class="sxs-lookup"><span data-stu-id="7a79c-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a79c-232"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a79c-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a79c-233">DLL</span><span class="sxs-lookup"><span data-stu-id="7a79c-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a79c-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a79c-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

