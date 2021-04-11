---
description: Un endpoint su un'opzione o una stazione finale assegnata a una VLAN oppure accetta il traffico da una o più VLAN.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Classe CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128123"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="50b47-103">CIM \_ VLANEndpoint (classe)</span><span class="sxs-lookup"><span data-stu-id="50b47-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="50b47-104">Un endpoint su un'opzione o una stazione finale assegnata a una VLAN oppure accetta il traffico da una o più VLAN.</span><span class="sxs-lookup"><span data-stu-id="50b47-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b47-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50b47-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="50b47-106">Members</span><span class="sxs-lookup"><span data-stu-id="50b47-106">Members</span></span>

<span data-ttu-id="50b47-107">La classe **CIM \_ VLANEndpoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="50b47-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="50b47-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50b47-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50b47-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50b47-109">Properties</span></span>

<span data-ttu-id="50b47-110">La classe **CIM \_ VLANEndpoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="50b47-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50b47-111">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="50b47-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50b47-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-113">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50b47-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50b47-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="50b47-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-115">La modalità VLAN richiesta per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50b47-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-116">**DMTF riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="50b47-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50b47-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="50b47-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="50b47-118">**Accesso** (2)</span><span class="sxs-lookup"><span data-stu-id="50b47-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="50b47-119">**Auto dinamica** (3)</span><span class="sxs-lookup"><span data-stu-id="50b47-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="50b47-120">**Auspicabile dinamico** (4)</span><span class="sxs-lookup"><span data-stu-id="50b47-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="50b47-121">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="50b47-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="50b47-122">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="50b47-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-123">**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="50b47-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="50b47-124">**Fornitore riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="50b47-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50b47-125">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="50b47-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50b47-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50b47-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50b47-128">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="50b47-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-129">Tipo di incapsulamento VLAN richiesto.</span><span class="sxs-lookup"><span data-stu-id="50b47-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="50b47-130">Questa proprietà viene usata solo quando l'endpoint VLAN è in modalità trunk.</span><span class="sxs-lookup"><span data-stu-id="50b47-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-131">**DMTF riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="50b47-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50b47-132">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="50b47-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="50b47-133">**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="50b47-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="50b47-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="50b47-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="50b47-135">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="50b47-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="50b47-136">**Negoziazione** (5)</span><span class="sxs-lookup"><span data-stu-id="50b47-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-137">**DMTF riservato** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="50b47-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="50b47-138">**Fornitore riservato** (32768...)</span><span class="sxs-lookup"><span data-stu-id="50b47-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50b47-139">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="50b47-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50b47-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50b47-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50b47-142">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="50b47-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-143">Indica se il protocollo di registrazione VLAN GARP (GVRP) è abilitato o disabilitato nell'endpoint del trunk.</span><span class="sxs-lookup"><span data-stu-id="50b47-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="50b47-144">Questa proprietà viene utilizzata solo quando GVRP è supportato dall'endpoint e la modalità di trunking è abilitata.</span><span class="sxs-lookup"><span data-stu-id="50b47-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50b47-145">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="50b47-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="50b47-146">**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="50b47-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="50b47-147">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="50b47-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="50b47-148">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="50b47-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50b47-149">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="50b47-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50b47-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50b47-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50b47-152">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="50b47-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-153">La modalità VLAN corrente per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50b47-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-154">**DMTF riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="50b47-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50b47-155">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="50b47-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="50b47-156">**Accesso** (2)</span><span class="sxs-lookup"><span data-stu-id="50b47-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="50b47-157">**Auto dinamica** (3)</span><span class="sxs-lookup"><span data-stu-id="50b47-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="50b47-158">**Auspicabile dinamico** (4)</span><span class="sxs-lookup"><span data-stu-id="50b47-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="50b47-159">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="50b47-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="50b47-160">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="50b47-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-161">**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="50b47-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="50b47-162">**Fornitore riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="50b47-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50b47-163">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="50b47-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50b47-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50b47-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50b47-166">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="50b47-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-167">Tipo di incapsulamento VLAN corrente.</span><span class="sxs-lookup"><span data-stu-id="50b47-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="50b47-168">Questa proprietà viene usata solo quando l'endpoint VLAN è in modalità trunk.</span><span class="sxs-lookup"><span data-stu-id="50b47-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50b47-169">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="50b47-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50b47-170">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="50b47-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="50b47-171">**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="50b47-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="50b47-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="50b47-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="50b47-173">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="50b47-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="50b47-174">**Negoziazione** (5)</span><span class="sxs-lookup"><span data-stu-id="50b47-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50b47-175">**DMTF riservato** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="50b47-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="50b47-176">**Fornitore riservato** (32768...)</span><span class="sxs-lookup"><span data-stu-id="50b47-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50b47-177">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="50b47-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50b47-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50b47-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50b47-180">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="50b47-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-181">Tipo di modello di endpoint VLAN supportato da VLANEndpoint quando il valore di **DesiredEndpointMode** è impostato su "1" (other); in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="50b47-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50b47-182">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="50b47-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50b47-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50b47-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50b47-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50b47-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50b47-185">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="50b47-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="50b47-186">Tipo di incapsulamento VLAN supportato dall'endpoint VLAN quando il valore della proprietà **DesiredVLANTrunkEncapsulation** è impostato su 1 (other); in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="50b47-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50b47-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50b47-187">Requirements</span></span>



| <span data-ttu-id="50b47-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b47-188">Requirement</span></span> | <span data-ttu-id="50b47-189">Valore</span><span class="sxs-lookup"><span data-stu-id="50b47-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b47-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50b47-190">Minimum supported client</span></span><br/> | <span data-ttu-id="50b47-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50b47-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="50b47-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50b47-192">Minimum supported server</span></span><br/> | <span data-ttu-id="50b47-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50b47-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="50b47-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50b47-194">Namespace</span></span><br/>                | <span data-ttu-id="50b47-195">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="50b47-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50b47-196">MOF</span><span class="sxs-lookup"><span data-stu-id="50b47-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50b47-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50b47-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50b47-198">DLL</span><span class="sxs-lookup"><span data-stu-id="50b47-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50b47-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50b47-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50b47-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50b47-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b47-201">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="50b47-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

