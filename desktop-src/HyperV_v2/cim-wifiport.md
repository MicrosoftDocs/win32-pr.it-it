---
description: Rappresenta un dispositivo di comunicazione della rete locale wireless che è conforme alla serie IEEE 802,11 di specifiche.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: Classe CIM_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882422"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="c6b86-103">CIM \_ WiFiPort (classe)</span><span class="sxs-lookup"><span data-stu-id="c6b86-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="c6b86-104">Rappresenta un dispositivo di comunicazione della rete locale wireless che è conforme alla serie IEEE 802,11 di specifiche.</span><span class="sxs-lookup"><span data-stu-id="c6b86-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b86-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6b86-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="c6b86-106">Members</span><span class="sxs-lookup"><span data-stu-id="c6b86-106">Members</span></span>

<span data-ttu-id="c6b86-107">La classe **CIM \_ WiFiPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6b86-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c6b86-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6b86-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6b86-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6b86-109">Properties</span></span>

<span data-ttu-id="c6b86-110">La classe **CIM \_ WiFiPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6b86-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6b86-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="c6b86-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6b86-112">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b86-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6b86-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("maxspeed")</span><span class="sxs-lookup"><span data-stu-id="c6b86-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="c6b86-115">Larghezza di banda massima supportata, in bit al secondo, in base alla modalità operativa specificata nella proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="c6b86-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="c6b86-116">Ad esempio, **maxspeed** è "11 milioni" Se **PortType** contiene "71" (802.11 b).</span><span class="sxs-lookup"><span data-stu-id="c6b86-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="c6b86-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="c6b86-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6b86-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c6b86-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6b86-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="c6b86-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="c6b86-121">Matrice che contiene gli indirizzi MAC IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="c6b86-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="c6b86-122">L'indirizzo MAC è formattato come dodici cifre esadecimali, ciascuna delle quali rappresenta uno dei sei ottetti dell'indirizzo MAC nell'ordine dei bit canonico.</span><span class="sxs-lookup"><span data-stu-id="c6b86-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="c6b86-123">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="c6b86-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6b86-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6b86-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6b86-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span><span class="sxs-lookup"><span data-stu-id="c6b86-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="c6b86-127">Indirizzo MAC IEEE 802 EUI-48 della porta.</span><span class="sxs-lookup"><span data-stu-id="c6b86-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="c6b86-128">L'indirizzo MAC è formattato come dodici cifre esadecimali, ciascuna delle quali rappresenta uno dei sei ottetti dell'indirizzo MAC nell'ordine dei bit canonico.</span><span class="sxs-lookup"><span data-stu-id="c6b86-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="c6b86-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="c6b86-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6b86-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6b86-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6b86-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="c6b86-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="c6b86-133">La modalità operativa 802,11 abilitata sulla porta.</span><span class="sxs-lookup"><span data-stu-id="c6b86-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6b86-134">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c6b86-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6b86-135">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c6b86-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="c6b86-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="c6b86-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="c6b86-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="c6b86-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="c6b86-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="c6b86-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="c6b86-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="c6b86-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c6b86-140">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="c6b86-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c6b86-141">**Fornitore riservato** (16000...)</span><span class="sxs-lookup"><span data-stu-id="c6b86-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6b86-142">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="c6b86-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6b86-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b86-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6b86-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6b86-145">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span><span class="sxs-lookup"><span data-stu-id="c6b86-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="c6b86-146">Velocità dei dati a cui è stata ricevuta l'unità dati del protocollo PPDU (PLCP (Physical Layer Convergence Protocol), in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c6b86-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="c6b86-147">Questo valore viene codificato nei primi 4 bit dell'intestazione PLCP in ogni frame di PLCP.</span><span class="sxs-lookup"><span data-stu-id="c6b86-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6b86-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6b86-148">Requirements</span></span>



| <span data-ttu-id="c6b86-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b86-149">Requirement</span></span> | <span data-ttu-id="c6b86-150">Valore</span><span class="sxs-lookup"><span data-stu-id="c6b86-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b86-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b86-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b86-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6b86-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c6b86-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b86-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b86-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6b86-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c6b86-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6b86-155">Namespace</span></span><br/>                | <span data-ttu-id="c6b86-156">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c6b86-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c6b86-157">MOF</span><span class="sxs-lookup"><span data-stu-id="c6b86-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6b86-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6b86-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6b86-159">DLL</span><span class="sxs-lookup"><span data-stu-id="c6b86-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6b86-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6b86-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c6b86-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6b86-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b86-162">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="c6b86-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

