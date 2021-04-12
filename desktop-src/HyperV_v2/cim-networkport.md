---
description: Rappresentazione logica di una porta di rete in un dispositivo di rete.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Classe CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233319"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="e9928-103">CIM \_ NetworkPort (classe)</span><span class="sxs-lookup"><span data-stu-id="e9928-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="e9928-104">Rappresentazione logica di una porta di rete in un dispositivo di rete.</span><span class="sxs-lookup"><span data-stu-id="e9928-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9928-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9928-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="e9928-106">Members</span><span class="sxs-lookup"><span data-stu-id="e9928-106">Members</span></span>

<span data-ttu-id="e9928-107">La classe **CIM \_ NetworkPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9928-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e9928-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9928-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9928-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9928-109">Properties</span></span>

<span data-ttu-id="e9928-110">La classe **CIM \_ NetworkPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9928-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9928-111">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e9928-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-112">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9928-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="e9928-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-115">Unità di trasmissione massima (MTU) attiva o negoziata supportata dalla porta.</span><span class="sxs-lookup"><span data-stu-id="e9928-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-116">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="e9928-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9928-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9928-119">**true** se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9928-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-120">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="e9928-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9928-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9928-123">**true** se la porta funziona in modalità full duplex; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9928-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-124">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e9928-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9928-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-127">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="e9928-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-128">Tecnologia di collegamento utilizzata dalla porta.</span><span class="sxs-lookup"><span data-stu-id="e9928-128">The link technology used by the port.</span></span> <span data-ttu-id="e9928-129">Se impostato su "1" (altro), la proprietà **OtherLinkTechnology** contiene una descrizione del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="e9928-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9928-130">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e9928-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9928-131">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e9928-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="e9928-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="e9928-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="e9928-133">**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="e9928-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="e9928-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="e9928-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="e9928-135">**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="e9928-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="e9928-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="e9928-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="e9928-137">**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="e9928-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="e9928-138">**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="e9928-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="e9928-139">**Infrarossi** (9)</span><span class="sxs-lookup"><span data-stu-id="e9928-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="e9928-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="e9928-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="e9928-141">**LAN wireless** (11)</span><span class="sxs-lookup"><span data-stu-id="e9928-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9928-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="e9928-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-143">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e9928-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9928-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-145">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="e9928-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-146">Matrice che contiene gli indirizzi di rete per la porta.</span><span class="sxs-lookup"><span data-stu-id="e9928-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-147">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e9928-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9928-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-150">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="e9928-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-151">La tecnologia di collegamento quando **LinkTechnology** è impostata su "1", (other).</span><span class="sxs-lookup"><span data-stu-id="e9928-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="e9928-152">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="e9928-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9928-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-155">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")</span><span class="sxs-lookup"><span data-stu-id="e9928-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="e9928-156">Descrizione deprecata: tipo di modulo della porta, quando la proprietà **portType** contiene 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e9928-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="e9928-157">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e9928-157">This property is deprecated.</span></span> <span data-ttu-id="e9928-158">È invece consigliabile usare la proprietà **portType** nella classe [**CIM \_ LogicalPort**](cim-logicalport.md) .</span><span class="sxs-lookup"><span data-stu-id="e9928-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-159">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="e9928-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9928-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="e9928-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-163">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="e9928-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="e9928-164">È possibile modificare l'indirizzo hardcoded usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="e9928-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="e9928-165">Quando questa modifica viene apportata, questa proprietà deve essere aggiornata nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="e9928-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="e9928-166">Se l'indirizzo non esiste, **PermanentAddress** deve essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="e9928-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-167">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="e9928-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9928-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9928-170">Numero di porta della porta di rete.</span><span class="sxs-lookup"><span data-stu-id="e9928-170">The port number of the network port.</span></span> <span data-ttu-id="e9928-171">Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete.</span><span class="sxs-lookup"><span data-stu-id="e9928-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-172">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="e9928-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-173">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9928-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-175">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits al secondo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ifSpeed "," MIF. \|Scheda di rete DMTF 802 porta \| 001,5 "), **punito** (" bit/secondo ")</span><span class="sxs-lookup"><span data-stu-id="e9928-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-176">Larghezza di banda corrente della porta in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e9928-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="e9928-177">Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="e9928-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="e9928-178">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e9928-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9928-179">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9928-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9928-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9928-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9928-181">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="e9928-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="e9928-182">Unità di trasmissione massima (MTU) supportata dalla porta.</span><span class="sxs-lookup"><span data-stu-id="e9928-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9928-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9928-183">Requirements</span></span>



| <span data-ttu-id="e9928-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9928-184">Requirement</span></span> | <span data-ttu-id="e9928-185">Valore</span><span class="sxs-lookup"><span data-stu-id="e9928-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9928-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9928-186">Minimum supported client</span></span><br/> | <span data-ttu-id="e9928-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9928-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e9928-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9928-188">Minimum supported server</span></span><br/> | <span data-ttu-id="e9928-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9928-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e9928-190">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9928-190">Namespace</span></span><br/>                | <span data-ttu-id="e9928-191">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e9928-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e9928-192">MOF</span><span class="sxs-lookup"><span data-stu-id="e9928-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9928-193"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9928-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9928-194">DLL</span><span class="sxs-lookup"><span data-stu-id="e9928-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9928-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9928-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9928-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9928-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9928-197">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="e9928-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

