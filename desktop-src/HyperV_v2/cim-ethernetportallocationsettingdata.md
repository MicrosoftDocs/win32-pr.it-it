---
description: Rappresenta le impostazioni per l'allocazione della porta Ethernet, oltre alle impostazioni fornite dalla \_ classe CIM EthernetPort. Queste impostazioni vengono usate per fornire informazioni specifiche della risorsa stessa.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Classe CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305674"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="584a8-104">CIM \_ EthernetPortAllocationSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="584a8-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="584a8-105">Rappresenta le impostazioni per l'allocazione della porta Ethernet, oltre alle impostazioni fornite dalla classe [**CIM \_ EthernetPort**](cim-ethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="584a8-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="584a8-106">Queste impostazioni vengono usate per fornire informazioni specifiche della risorsa stessa.</span><span class="sxs-lookup"><span data-stu-id="584a8-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="584a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="584a8-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="584a8-108">Members</span><span class="sxs-lookup"><span data-stu-id="584a8-108">Members</span></span>

<span data-ttu-id="584a8-109">La classe **CIM \_ EthernetPortAllocationSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="584a8-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="584a8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="584a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="584a8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="584a8-111">Properties</span></span>

<span data-ttu-id="584a8-112">La classe **CIM \_ EthernetPortAllocationSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="584a8-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="584a8-113">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="584a8-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584a8-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="584a8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="584a8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="584a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584a8-116">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="584a8-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="584a8-117">Modalità VLAN richiesta.</span><span class="sxs-lookup"><span data-stu-id="584a8-117">The requested VLAN mode.</span></span> <span data-ttu-id="584a8-118">Questa proprietà viene utilizzata per impostare il valore della proprietà **OperationalEndpointMode** iniziale nell'istanza di **CIM \_ VLANEndpoint** associata alla porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="584a8-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="584a8-119">**DMTF riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="584a8-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="584a8-120">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="584a8-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="584a8-121">**Accesso** (2)</span><span class="sxs-lookup"><span data-stu-id="584a8-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="584a8-122">**Auto dinamica** (3)</span><span class="sxs-lookup"><span data-stu-id="584a8-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="584a8-123">**Auspicabile dinamico** (4)</span><span class="sxs-lookup"><span data-stu-id="584a8-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="584a8-124">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="584a8-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="584a8-125">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="584a8-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="584a8-126">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="584a8-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="584a8-127">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="584a8-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="584a8-128">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="584a8-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584a8-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="584a8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="584a8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="584a8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584a8-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="584a8-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="584a8-132">Tipo di modello di endpoint VLAN supportato da questo endpoint VLAN, quando il valore della proprietà Mode è impostato su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="584a8-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="584a8-133">Questa proprietà deve essere impostata su **null** quando la proprietà Mode è un valore diverso da "1".</span><span class="sxs-lookup"><span data-stu-id="584a8-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="584a8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="584a8-134">Requirements</span></span>



| <span data-ttu-id="584a8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="584a8-135">Requirement</span></span> | <span data-ttu-id="584a8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="584a8-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584a8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584a8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="584a8-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="584a8-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="584a8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584a8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="584a8-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="584a8-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="584a8-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="584a8-141">Namespace</span></span><br/>                | <span data-ttu-id="584a8-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="584a8-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="584a8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="584a8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="584a8-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="584a8-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="584a8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="584a8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="584a8-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="584a8-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="584a8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="584a8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584a8-148">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="584a8-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

