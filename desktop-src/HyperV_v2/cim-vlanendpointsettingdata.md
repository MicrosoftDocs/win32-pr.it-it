---
description: Rappresenta i dati di configurazione per un endpoint VLAN.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Classe CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885868"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="d716e-103">CIM \_ VLANEndpointSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="d716e-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="d716e-104">Rappresenta i dati di configurazione per un endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="d716e-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="d716e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d716e-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="d716e-106">Members</span><span class="sxs-lookup"><span data-stu-id="d716e-106">Members</span></span>

<span data-ttu-id="d716e-107">La classe **CIM \_ VLANEndpointSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d716e-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d716e-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d716e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d716e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d716e-109">Properties</span></span>

<span data-ttu-id="d716e-110">La classe **CIM \_ VLANEndpointSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d716e-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d716e-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="d716e-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d716e-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d716e-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d716e-113">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d716e-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d716e-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="d716e-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="d716e-115">VLAN di accesso per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d716e-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="d716e-116">**DefaultVLAN**</span><span class="sxs-lookup"><span data-stu-id="d716e-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d716e-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d716e-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d716e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d716e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d716e-119">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="d716e-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="d716e-120">Valore predefinito per la VLAN nativa sull'endpoint trunk.</span><span class="sxs-lookup"><span data-stu-id="d716e-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="d716e-121">Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="d716e-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="d716e-122">**NativeVLAN**</span><span class="sxs-lookup"><span data-stu-id="d716e-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d716e-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d716e-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d716e-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d716e-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d716e-125">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="d716e-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="d716e-126">ID VLAN usato per contrassegnare il traffico non contrassegnato ricevuto sull'endpoint trunk.</span><span class="sxs-lookup"><span data-stu-id="d716e-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="d716e-127">Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **SwitchEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="d716e-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="d716e-128">**PruneEligibleVLANList**</span><span class="sxs-lookup"><span data-stu-id="d716e-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d716e-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d716e-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d716e-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d716e-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d716e-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="d716e-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="d716e-132">Matrice che contiene gli ID di VLAN che il sistema può rimuovere dall'endpoint del trunk.</span><span class="sxs-lookup"><span data-stu-id="d716e-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="d716e-133">Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="d716e-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="d716e-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="d716e-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d716e-135">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d716e-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d716e-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d716e-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d716e-137">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="d716e-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="d716e-138">Matrice che contiene gli ID degli endpoint VLAN con trunking abilitato.</span><span class="sxs-lookup"><span data-stu-id="d716e-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="d716e-139">Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="d716e-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d716e-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d716e-140">Requirements</span></span>



| <span data-ttu-id="d716e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d716e-141">Requirement</span></span> | <span data-ttu-id="d716e-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d716e-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d716e-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d716e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d716e-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d716e-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d716e-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d716e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d716e-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d716e-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d716e-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d716e-147">Namespace</span></span><br/>                | <span data-ttu-id="d716e-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d716e-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d716e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d716e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d716e-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d716e-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d716e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d716e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d716e-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d716e-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d716e-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d716e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d716e-154">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d716e-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

