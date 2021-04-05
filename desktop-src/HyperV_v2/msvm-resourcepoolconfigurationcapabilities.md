---
description: Descrive le funzionalità della \_ classe MSVM ResourcePoolConfigurationService associata.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Classe Msvm_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882754"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="51950-103">\_Classe MSVM ResourcePoolConfigurationCapabilities</span><span class="sxs-lookup"><span data-stu-id="51950-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="51950-104">Descrive le funzionalità della classe [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) associata.</span><span class="sxs-lookup"><span data-stu-id="51950-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="51950-105">I client possono usare le istanze di questa classe per determinare quali metodi sono supportati in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="51950-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="51950-106">Lo stesso metodo non deve essere presente in entrambi gli elenchi.</span><span class="sxs-lookup"><span data-stu-id="51950-106">The same method must not be in both lists.</span></span> <span data-ttu-id="51950-107">Le implementazioni del metodo devono essere sincrone o asincrone.</span><span class="sxs-lookup"><span data-stu-id="51950-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="51950-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="51950-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51950-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51950-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="51950-110">Members</span><span class="sxs-lookup"><span data-stu-id="51950-110">Members</span></span>

<span data-ttu-id="51950-111">La **classe \_ ResourcePoolConfigurationCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51950-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="51950-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51950-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51950-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51950-113">Properties</span></span>

<span data-ttu-id="51950-114">La **classe \_ ResourcePoolConfigurationCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51950-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51950-115">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="51950-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-116">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51950-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="51950-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51950-118">Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ ResourcePoolConfigurationService MSVM**](msvm-resourcepoolconfigurationservice.md) supportata in modo asincrono dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="51950-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="51950-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="51950-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="51950-120">**CreatePool è supportato** (32768)</span><span class="sxs-lookup"><span data-stu-id="51950-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="51950-121">**ChangePoolResources è supportato** (32769)</span><span class="sxs-lookup"><span data-stu-id="51950-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="51950-122">**ChangePoolSettings è supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="51950-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="51950-123">**Deletepool è supportato** (32771)</span><span class="sxs-lookup"><span data-stu-id="51950-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="51950-124">**Fornitore riservato** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="51950-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51950-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="51950-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51950-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51950-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51950-128">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51950-128">A short description of the object.</span></span> <span data-ttu-id="51950-129">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità di configurazione del pool di risorse".</span><span class="sxs-lookup"><span data-stu-id="51950-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="51950-130">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="51950-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51950-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51950-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51950-133">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="51950-133">A description of the object.</span></span> <span data-ttu-id="51950-134">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità di configurazione del pool di risorse Microsoft".</span><span class="sxs-lookup"><span data-stu-id="51950-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="51950-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="51950-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51950-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51950-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51950-138">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51950-138">A display name for the object.</span></span> <span data-ttu-id="51950-139">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità di configurazione del pool di risorse".</span><span class="sxs-lookup"><span data-stu-id="51950-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="51950-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51950-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51950-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51950-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51950-143">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="51950-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="51950-144">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="51950-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="51950-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="51950-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51950-146">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="51950-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51950-147">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51950-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="51950-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51950-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51950-149">Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ ResourcePoolConfigurationService MSVM**](msvm-resourcepoolconfigurationservice.md) supportata in modo sincrono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="51950-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="51950-150">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="51950-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="51950-151">**CreatePool è supportato** (32768)</span><span class="sxs-lookup"><span data-stu-id="51950-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="51950-152">**ChangePoolResources è supportato** (32769)</span><span class="sxs-lookup"><span data-stu-id="51950-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="51950-153">**ChangePoolSettings è supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="51950-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="51950-154">**Deletepool è supportato** (32771)</span><span class="sxs-lookup"><span data-stu-id="51950-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="51950-155">**Fornitore riservato** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="51950-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="51950-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="51950-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="51950-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51950-157">Requirements</span></span>



| <span data-ttu-id="51950-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="51950-158">Requirement</span></span> | <span data-ttu-id="51950-159">Valore</span><span class="sxs-lookup"><span data-stu-id="51950-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51950-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51950-160">Minimum supported client</span></span><br/> | <span data-ttu-id="51950-161">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51950-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="51950-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51950-162">Minimum supported server</span></span><br/> | <span data-ttu-id="51950-163">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="51950-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="51950-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51950-164">Namespace</span></span><br/>                | <span data-ttu-id="51950-165">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="51950-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51950-166">MOF</span><span class="sxs-lookup"><span data-stu-id="51950-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51950-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51950-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51950-168">DLL</span><span class="sxs-lookup"><span data-stu-id="51950-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51950-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51950-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

