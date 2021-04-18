---
description: Rappresenta le impostazioni specifiche dell'archiviazione per un sistema virtuale.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Classe Msvm_StorageSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319506"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="31b29-103">\_Classe MSVM StorageSettingData</span><span class="sxs-lookup"><span data-stu-id="31b29-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="31b29-104">Rappresenta le impostazioni specifiche dell'archiviazione per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="31b29-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="31b29-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="31b29-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b29-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31b29-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="31b29-107">Members</span><span class="sxs-lookup"><span data-stu-id="31b29-107">Members</span></span>

<span data-ttu-id="31b29-108">La **classe \_ StorageSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31b29-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="31b29-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31b29-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31b29-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31b29-110">Properties</span></span>

<span data-ttu-id="31b29-111">La **classe \_ StorageSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31b29-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31b29-112">**DisableInterruptBatching**</span><span class="sxs-lookup"><span data-stu-id="31b29-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31b29-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="31b29-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31b29-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31b29-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31b29-115">Specifica se è necessario disabilitare la suddivisione in batch degli interrupt.</span><span class="sxs-lookup"><span data-stu-id="31b29-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="31b29-116">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) della classe WMI [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="31b29-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="31b29-117">**ThreadCountPerChannel**</span><span class="sxs-lookup"><span data-stu-id="31b29-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31b29-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31b29-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31b29-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31b29-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31b29-120">Numero di thread per canale di archiviazione per l'elaborazione di IO.</span><span class="sxs-lookup"><span data-stu-id="31b29-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="31b29-121">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="31b29-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="31b29-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="31b29-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="31b29-123">Comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="31b29-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="31b29-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (1)</span><span class="sxs-lookup"><span data-stu-id="31b29-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31b29-125">Numero basso di thread per canale di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b29-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="31b29-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Media** (2)</span><span class="sxs-lookup"><span data-stu-id="31b29-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31b29-127">Numero medio di thread per canale di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b29-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="31b29-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="31b29-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31b29-129">Numero elevato di thread per canale di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b29-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31b29-130">**VirtualProcessorsPerChannel**</span><span class="sxs-lookup"><span data-stu-id="31b29-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31b29-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31b29-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31b29-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31b29-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31b29-133">Numero di processori per canale di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b29-133">The number of processors per storage channel.</span></span> <span data-ttu-id="31b29-134">Il numero di canali da aprire viene fornito da (numero di processori logici nell'host/**VirtualProcessorsPerChannel**).</span><span class="sxs-lookup"><span data-stu-id="31b29-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="31b29-135">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="31b29-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31b29-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31b29-136">Requirements</span></span>



| <span data-ttu-id="31b29-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b29-137">Requirement</span></span> | <span data-ttu-id="31b29-138">Valore</span><span class="sxs-lookup"><span data-stu-id="31b29-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b29-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b29-139">Minimum supported client</span></span><br/> | <span data-ttu-id="31b29-140">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="31b29-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="31b29-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b29-141">Minimum supported server</span></span><br/> | <span data-ttu-id="31b29-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="31b29-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="31b29-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31b29-143">Namespace</span></span><br/>                | <span data-ttu-id="31b29-144">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="31b29-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="31b29-145">MOF</span><span class="sxs-lookup"><span data-stu-id="31b29-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31b29-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31b29-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31b29-147">DLL</span><span class="sxs-lookup"><span data-stu-id="31b29-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31b29-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31b29-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="31b29-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31b29-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b29-150">**\_SystemComponentSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="31b29-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




