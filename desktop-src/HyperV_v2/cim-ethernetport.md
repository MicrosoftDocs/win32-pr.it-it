---
description: Rappresenta una porta Ethernet.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: Classe CIM_EthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524924"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="af9cc-103">CIM \_ EthernetPort (classe)</span><span class="sxs-lookup"><span data-stu-id="af9cc-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="af9cc-104">Rappresenta una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af9cc-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af9cc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="af9cc-106">Members</span><span class="sxs-lookup"><span data-stu-id="af9cc-106">Members</span></span>

<span data-ttu-id="af9cc-107">La classe **CIM \_ EthernetPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af9cc-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="af9cc-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af9cc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af9cc-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af9cc-109">Properties</span></span>

<span data-ttu-id="af9cc-110">La classe **CIM \_ EthernetPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af9cc-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af9cc-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="af9cc-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af9cc-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-114">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="af9cc-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-115">Funzionalità della porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af9cc-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="af9cc-116">Se sono abilitate le funzionalità di failover o bilanciamento del carico, è necessario definire anche un oggetto [**CIM \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) o [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (Load Balancing) per descrivere completamente la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af9cc-117">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af9cc-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af9cc-118">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af9cc-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="af9cc-119">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="af9cc-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="af9cc-120">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="af9cc-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="af9cc-121">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="af9cc-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="af9cc-122">**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="af9cc-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af9cc-123">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="af9cc-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-124">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="af9cc-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-126">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="af9cc-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-127">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità indicate nella matrice delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="af9cc-128">Gli elementi in questa matrice corrispondono agli elementi nella matrice delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="af9cc-129">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="af9cc-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-130">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af9cc-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-132">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**Funzionalità**","**CIM \_ EthernetPort**.**OtherEnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="af9cc-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-133">Indica quali funzionalità sono abilitate nella matrice di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="af9cc-134">Gli elementi in questa matrice corrispondono agli elementi nella matrice delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af9cc-135">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af9cc-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af9cc-136">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af9cc-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="af9cc-137">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="af9cc-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="af9cc-138">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="af9cc-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="af9cc-139">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="af9cc-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="af9cc-140">**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="af9cc-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af9cc-141">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="af9cc-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9cc-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpPortMaxInfo ")</span><span class="sxs-lookup"><span data-stu-id="af9cc-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-145">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="af9cc-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="af9cc-146">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="af9cc-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-147">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="af9cc-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-149">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="af9cc-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-150">Indirizzi di rete assegnati alla porta.</span><span class="sxs-lookup"><span data-stu-id="af9cc-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="af9cc-151">L'indirizzo è un MAC 802,3 formattato come dodici cifre esadecimali (ad esempio, "010203040506"), in cui ogni coppia di cifre rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico.</span><span class="sxs-lookup"><span data-stu-id="af9cc-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="af9cc-152">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="af9cc-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-153">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="af9cc-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-155">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**EnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="af9cc-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-156">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per gli elementi della matrice **EnabledCapabilities** impostati su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="af9cc-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="af9cc-157">Gli elementi in questa matrice corrispondono agli elementi nella matrice **EnabledCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="af9cc-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="af9cc-158">**PortType**</span><span class="sxs-lookup"><span data-stu-id="af9cc-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9cc-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af9cc-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af9cc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9cc-161">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="af9cc-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="af9cc-162">Modalità abilitata sulla porta.</span><span class="sxs-lookup"><span data-stu-id="af9cc-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="af9cc-163">Quando è impostata su 1 (other), la proprietà **OtherPortType** descrive la modalità.</span><span class="sxs-lookup"><span data-stu-id="af9cc-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af9cc-164">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af9cc-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af9cc-165">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af9cc-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="af9cc-166">**10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="af9cc-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="af9cc-167">**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="af9cc-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="af9cc-168">**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="af9cc-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="af9cc-169">**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="af9cc-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="af9cc-170">**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="af9cc-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="af9cc-171">**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="af9cc-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="af9cc-172">**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="af9cc-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="af9cc-173">**100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="af9cc-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="af9cc-174">**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="af9cc-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="af9cc-175">**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="af9cc-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="af9cc-176">**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="af9cc-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="af9cc-177">**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="af9cc-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="af9cc-178">**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="af9cc-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="af9cc-179">**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="af9cc-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="af9cc-180">**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="af9cc-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="af9cc-181">**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="af9cc-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="af9cc-182">**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="af9cc-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="af9cc-183">**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="af9cc-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="af9cc-184">**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="af9cc-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="af9cc-185">**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="af9cc-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="af9cc-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="af9cc-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="af9cc-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af9cc-187">Requirements</span></span>



| <span data-ttu-id="af9cc-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9cc-188">Requirement</span></span> | <span data-ttu-id="af9cc-189">Valore</span><span class="sxs-lookup"><span data-stu-id="af9cc-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9cc-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9cc-190">Minimum supported client</span></span><br/> | <span data-ttu-id="af9cc-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="af9cc-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="af9cc-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9cc-192">Minimum supported server</span></span><br/> | <span data-ttu-id="af9cc-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af9cc-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="af9cc-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af9cc-194">Namespace</span></span><br/>                | <span data-ttu-id="af9cc-195">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="af9cc-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="af9cc-196">MOF</span><span class="sxs-lookup"><span data-stu-id="af9cc-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af9cc-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af9cc-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af9cc-198">DLL</span><span class="sxs-lookup"><span data-stu-id="af9cc-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9cc-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af9cc-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af9cc-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af9cc-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9cc-201">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="af9cc-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

