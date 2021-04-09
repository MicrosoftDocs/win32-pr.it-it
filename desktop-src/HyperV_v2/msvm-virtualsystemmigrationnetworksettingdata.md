---
description: Rappresenta la rete in cui il servizio migrazione del sistema virtuale è in ascolto della migrazione del sistema virtuale in ingresso.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Classe Msvm_VirtualSystemMigrationNetworkSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878702"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="6151d-103">\_Classe MSVM VirtualSystemMigrationNetworkSettingData</span><span class="sxs-lookup"><span data-stu-id="6151d-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="6151d-104">Rappresenta la rete in cui il servizio migrazione del sistema virtuale è in ascolto della migrazione del sistema virtuale in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6151d-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="6151d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6151d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6151d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6151d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="6151d-107">Members</span><span class="sxs-lookup"><span data-stu-id="6151d-107">Members</span></span>

<span data-ttu-id="6151d-108">La **classe \_ VirtualSystemMigrationNetworkSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6151d-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6151d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6151d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6151d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6151d-110">Properties</span></span>

<span data-ttu-id="6151d-111">La **classe \_ VirtualSystemMigrationNetworkSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6151d-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6151d-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6151d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6151d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6151d-115">A short description of the object.</span></span> <span data-ttu-id="6151d-116">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="6151d-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="6151d-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6151d-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6151d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="6151d-120">A description of the object.</span></span> <span data-ttu-id="6151d-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6151d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6151d-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6151d-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6151d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6151d-125">A display name for the object.</span></span> <span data-ttu-id="6151d-126">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6151d-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6151d-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6151d-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6151d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6151d-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="6151d-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6151d-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6151d-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6151d-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6151d-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6151d-133">**Metrica**</span><span class="sxs-lookup"><span data-stu-id="6151d-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6151d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-136">Metrica di priorità della rete per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="6151d-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="6151d-137">I valori più bassi hanno priorità maggiore.</span><span class="sxs-lookup"><span data-stu-id="6151d-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="6151d-138">**LunghezzaPrefisso**</span><span class="sxs-lookup"><span data-stu-id="6151d-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-139">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6151d-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-141">Lunghezza del prefisso della subnet della rete di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6151d-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="6151d-142">**SubnetNumber**</span><span class="sxs-lookup"><span data-stu-id="6151d-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6151d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6151d-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-145">Numero di subnet della rete di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6151d-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="6151d-146">**Tag**</span><span class="sxs-lookup"><span data-stu-id="6151d-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6151d-147">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6151d-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6151d-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6151d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6151d-149">Matrice di tag per rappresentare il sistema di gestione che ha impostato questa rete per il servizio migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6151d-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6151d-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6151d-150">Requirements</span></span>



| <span data-ttu-id="6151d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6151d-151">Requirement</span></span> | <span data-ttu-id="6151d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="6151d-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6151d-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6151d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6151d-154">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6151d-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6151d-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6151d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6151d-156">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6151d-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6151d-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6151d-157">Namespace</span></span><br/>                | <span data-ttu-id="6151d-158">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6151d-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6151d-159">MOF</span><span class="sxs-lookup"><span data-stu-id="6151d-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6151d-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6151d-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6151d-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6151d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6151d-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6151d-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6151d-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6151d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6151d-164">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6151d-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="6151d-165">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6151d-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

