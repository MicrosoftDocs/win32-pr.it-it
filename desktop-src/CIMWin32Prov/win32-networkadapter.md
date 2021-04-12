---
description: La \_ classe Win32 NetworkAdapter è deprecata. Usare invece la \_ classe MSFT NetAdapter. La \_ classe Win32 NetworkAdapterWMI rappresenta una scheda di rete di un computer che esegue un sistema operativo Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483797"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="e5afb-105">Win32 \_ NetworkAdapter (classe)</span><span class="sxs-lookup"><span data-stu-id="e5afb-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="e5afb-106">La classe **Win32 \_ NetworkAdapter** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="e5afb-107">Usare invece la classe [**MSFT \_ NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e5afb-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="e5afb-108">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapter Win32** rappresenta una scheda di rete di un computer che esegue un sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="e5afb-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="e5afb-109">**Win32 \_ NetworkAdapter** fornisce solo i dati IPv4.</span><span class="sxs-lookup"><span data-stu-id="e5afb-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="e5afb-110">Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="e5afb-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e5afb-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e5afb-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e5afb-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5afb-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5afb-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="e5afb-114">Members</span><span class="sxs-lookup"><span data-stu-id="e5afb-114">Members</span></span>

<span data-ttu-id="e5afb-115">La classe **Win32 \_ NetworkAdapter** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e5afb-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="e5afb-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="e5afb-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5afb-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5afb-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5afb-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="e5afb-118">Methods</span></span>

<span data-ttu-id="e5afb-119">La classe **Win32 \_ NetworkAdapter** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e5afb-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="e5afb-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="e5afb-120">Method</span></span>                                                          | <span data-ttu-id="e5afb-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5afb-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5afb-122">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="e5afb-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="e5afb-123">Disabilita la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="e5afb-124">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="e5afb-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="e5afb-125">Abilita la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="e5afb-126">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="e5afb-126">**Reset**</span></span>                                                       | <span data-ttu-id="e5afb-127">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-127">Not implemented.</span></span> <span data-ttu-id="e5afb-128">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="e5afb-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e5afb-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="e5afb-130">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-130">Not implemented.</span></span> <span data-ttu-id="e5afb-131">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e5afb-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5afb-132">Properties</span></span>

<span data-ttu-id="e5afb-133">La classe **Win32 \_ NetworkAdapter** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e5afb-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5afb-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="e5afb-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen \_ media \_ in \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="e5afb-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-138">Supporto di rete in uso.</span><span class="sxs-lookup"><span data-stu-id="e5afb-138">Network medium in use.</span></span> <span data-ttu-id="e5afb-139">Le schede di rete sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5afb-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="e5afb-140">**Ethernet 802,3** ("Ethernet 802,3")</span><span class="sxs-lookup"><span data-stu-id="e5afb-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="e5afb-141">**Token ring 802,5** ("token ring 802,5")</span><span class="sxs-lookup"><span data-stu-id="e5afb-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="e5afb-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span><span class="sxs-lookup"><span data-stu-id="e5afb-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="e5afb-143">**WAN** (Wide Area Network) (WAN)</span><span class="sxs-lookup"><span data-stu-id="e5afb-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="e5afb-144">**LocalTalk** ("LocalTalk")</span><span class="sxs-lookup"><span data-stu-id="e5afb-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="e5afb-145">**Ethernet con formato di intestazione Dix** ("Ethernet con formato di intestazione Dix")</span><span class="sxs-lookup"><span data-stu-id="e5afb-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="e5afb-146">**ARCNET** ("ARCNET")</span><span class="sxs-lookup"><span data-stu-id="e5afb-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="e5afb-147">**ARCNET (878,2)** ("ARCNET (878,2)")</span><span class="sxs-lookup"><span data-stu-id="e5afb-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="e5afb-148">**ATM** ("ATM")</span><span class="sxs-lookup"><span data-stu-id="e5afb-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="e5afb-149">**Wireless** ("wireless")</span><span class="sxs-lookup"><span data-stu-id="e5afb-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="e5afb-150">**Wireless a infrarossi** ("wireless infrarossi")</span><span class="sxs-lookup"><span data-stu-id="e5afb-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="e5afb-151">**Bpc** ("BPC")</span><span class="sxs-lookup"><span data-stu-id="e5afb-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="e5afb-152">**Cowan** ("Cowan")</span><span class="sxs-lookup"><span data-stu-id="e5afb-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="e5afb-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="e5afb-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-154">**AdapterTypeID**</span><span class="sxs-lookup"><span data-stu-id="e5afb-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5afb-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-157">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen \_ media \_ in \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="e5afb-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-158">Supporto di rete in uso.</span><span class="sxs-lookup"><span data-stu-id="e5afb-158">Network medium in use.</span></span> <span data-ttu-id="e5afb-159">Restituisce le stesse informazioni della proprietà **AdapterType** , ad eccezione del fatto che le informazioni sono nel formato di un numero intero.</span><span class="sxs-lookup"><span data-stu-id="e5afb-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="e5afb-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="e5afb-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="e5afb-161">**Token Ring 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="e5afb-162">**FDDI (Fiber Distributed Data Interface)** (2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="e5afb-163">**WAN (Wide Area Network)** (3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="e5afb-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="e5afb-165">**Ethernet con formato di intestazione Dix** (5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="e5afb-166">**ARCNET** (6)</span><span class="sxs-lookup"><span data-stu-id="e5afb-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="e5afb-167">**ARCNET (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="e5afb-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="e5afb-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="e5afb-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="e5afb-169">**Wireless** (9)</span><span class="sxs-lookup"><span data-stu-id="e5afb-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="e5afb-170">**Wireless a infrarossi** (10)</span><span class="sxs-lookup"><span data-stu-id="e5afb-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="e5afb-171">**Bpc** (11)</span><span class="sxs-lookup"><span data-stu-id="e5afb-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="e5afb-172">**Cowan** (12)</span><span class="sxs-lookup"><span data-stu-id="e5afb-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="e5afb-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="e5afb-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-174">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="e5afb-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-175">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-177">Se **true**, la scheda di rete è in grado di determinare automaticamente la velocità del supporto collegato o di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="e5afb-178">Questa proprietà viene ereditata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-179">Questa proprietà non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-179">This property has not been implemented yet.</span></span> <span data-ttu-id="e5afb-180">Per impostazione predefinita, viene restituito un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-181">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="e5afb-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5afb-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-184">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-185">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-185">Availability and status of the device.</span></span>

<span data-ttu-id="e5afb-186">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e5afb-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5afb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e5afb-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-190">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="e5afb-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e5afb-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e5afb-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e5afb-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="e5afb-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e5afb-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="e5afb-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e5afb-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="e5afb-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e5afb-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="e5afb-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e5afb-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="e5afb-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e5afb-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="e5afb-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e5afb-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="e5afb-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e5afb-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="e5afb-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-201">Il dispositivo è noto come stato di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e5afb-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="e5afb-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-203">Il dispositivo è in uno stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="e5afb-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e5afb-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="e5afb-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-205">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e5afb-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="e5afb-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e5afb-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="e5afb-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-208">Il dispositivo è in uno stato di avviso, anche se in stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="e5afb-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e5afb-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e5afb-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-210">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="e5afb-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e5afb-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="e5afb-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-212">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e5afb-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="e5afb-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-214">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e5afb-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="e5afb-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-216">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="e5afb-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-217">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e5afb-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-220">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e5afb-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-221">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="e5afb-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="e5afb-222">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-223">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e5afb-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-224">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-226">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5afb-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-227">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e5afb-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="e5afb-228">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e5afb-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e5afb-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="e5afb-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-231">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e5afb-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e5afb-233">(1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-234">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e5afb-236">(2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e5afb-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e5afb-238">(3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-239">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="e5afb-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e5afb-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e5afb-241">(4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-242">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-242">Device is not working properly.</span></span> <span data-ttu-id="e5afb-243">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e5afb-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e5afb-245">(5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-246">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="e5afb-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e5afb-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e5afb-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="e5afb-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-249">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5afb-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e5afb-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e5afb-251">(7)</span><span class="sxs-lookup"><span data-stu-id="e5afb-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e5afb-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e5afb-253">(8)</span><span class="sxs-lookup"><span data-stu-id="e5afb-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-254">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="e5afb-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e5afb-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e5afb-256">(9)</span><span class="sxs-lookup"><span data-stu-id="e5afb-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-257">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-257">Device is not working properly.</span></span> <span data-ttu-id="e5afb-258">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e5afb-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e5afb-260">(10)</span><span class="sxs-lookup"><span data-stu-id="e5afb-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-261">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e5afb-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e5afb-263">(11)</span><span class="sxs-lookup"><span data-stu-id="e5afb-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-264">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e5afb-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e5afb-266">12</span><span class="sxs-lookup"><span data-stu-id="e5afb-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-267">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="e5afb-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e5afb-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e5afb-269">(13)</span><span class="sxs-lookup"><span data-stu-id="e5afb-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-270">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e5afb-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e5afb-272">(14)</span><span class="sxs-lookup"><span data-stu-id="e5afb-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-273">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e5afb-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e5afb-275">(15)</span><span class="sxs-lookup"><span data-stu-id="e5afb-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-276">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="e5afb-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e5afb-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e5afb-278">(16)</span><span class="sxs-lookup"><span data-stu-id="e5afb-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-279">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e5afb-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e5afb-281">(17)</span><span class="sxs-lookup"><span data-stu-id="e5afb-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-282">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e5afb-284">(18)</span><span class="sxs-lookup"><span data-stu-id="e5afb-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-285">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e5afb-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e5afb-287">(19)</span><span class="sxs-lookup"><span data-stu-id="e5afb-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e5afb-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e5afb-289">(20)</span><span class="sxs-lookup"><span data-stu-id="e5afb-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-290">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e5afb-292">(21)</span><span class="sxs-lookup"><span data-stu-id="e5afb-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-293">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5afb-293">System failure.</span></span> <span data-ttu-id="e5afb-294">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e5afb-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e5afb-295">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e5afb-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e5afb-297">(22)</span><span class="sxs-lookup"><span data-stu-id="e5afb-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-298">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e5afb-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e5afb-300">(23)</span><span class="sxs-lookup"><span data-stu-id="e5afb-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-301">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5afb-301">System failure.</span></span> <span data-ttu-id="e5afb-302">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e5afb-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e5afb-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e5afb-304">(24)</span><span class="sxs-lookup"><span data-stu-id="e5afb-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-305">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="e5afb-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e5afb-307">(25)</span><span class="sxs-lookup"><span data-stu-id="e5afb-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-308">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e5afb-310">(26)</span><span class="sxs-lookup"><span data-stu-id="e5afb-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-311">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e5afb-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e5afb-313">(27)</span><span class="sxs-lookup"><span data-stu-id="e5afb-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-314">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="e5afb-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e5afb-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e5afb-316">(28)</span><span class="sxs-lookup"><span data-stu-id="e5afb-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-317">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="e5afb-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e5afb-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e5afb-319">(29)</span><span class="sxs-lookup"><span data-stu-id="e5afb-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-320">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-320">Device is disabled.</span></span> <span data-ttu-id="e5afb-321">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="e5afb-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e5afb-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e5afb-323">(30)</span><span class="sxs-lookup"><span data-stu-id="e5afb-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-324">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5afb-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e5afb-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e5afb-326">31</span><span class="sxs-lookup"><span data-stu-id="e5afb-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-327">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-327">Device is not working properly.</span></span> <span data-ttu-id="e5afb-328">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="e5afb-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-329">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e5afb-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-330">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-332">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5afb-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-333">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e5afb-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e5afb-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5afb-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-338">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e5afb-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-339">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="e5afb-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e5afb-340">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="e5afb-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e5afb-341">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-342">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e5afb-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-345">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e5afb-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-346">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-346">Description of the object.</span></span>

<span data-ttu-id="e5afb-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5afb-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-351">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="e5afb-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-352">Identificatore univoco della scheda di rete di altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e5afb-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="e5afb-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-354">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e5afb-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-355">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-357">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e5afb-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e5afb-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-362">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="e5afb-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="e5afb-363">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e5afb-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-367">Identificatore univoco globale per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e5afb-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="e5afb-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-369">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-371">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="e5afb-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-372">Numero di indice della scheda di rete, archiviato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5afb-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="e5afb-373">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="e5afb-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e5afb-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-375">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5afb-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-377">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-378">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-378">Date and time the object was installed.</span></span> <span data-ttu-id="e5afb-379">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e5afb-380">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e5afb-381">Questa proprietà non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-381">This property has not been implemented yet.</span></span> <span data-ttu-id="e5afb-382">Per impostazione predefinita, viene restituito un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-383">**Installato**</span><span class="sxs-lookup"><span data-stu-id="e5afb-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-384">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-386">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32REGISTRY \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="e5afb-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-387">Se **true**, la scheda di rete viene installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e5afb-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-388">**IndiceInterfaccia**</span><span class="sxs-lookup"><span data-stu-id="e5afb-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-389">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-391">Valore di indice che identifica in modo univoco l'interfaccia di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e5afb-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="e5afb-392">Il valore in questa proprietà corrisponde al valore della proprietà **IndiceInterfaccia** nell'istanza di [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) che rappresenta l'interfaccia di rete nella tabella di route.</span><span class="sxs-lookup"><span data-stu-id="e5afb-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e5afb-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-394">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-396">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5afb-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e5afb-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="e5afb-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-401">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="e5afb-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-402">Indirizzo del controllo di accesso multimediale per questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="e5afb-403">Un indirizzo MAC è un numero univoco a 48 bit assegnato alla scheda di rete dal produttore.</span><span class="sxs-lookup"><span data-stu-id="e5afb-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="e5afb-404">Identifica in modo univoco questa scheda di rete e viene utilizzata per il mapping delle comunicazioni di rete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e5afb-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-405">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="e5afb-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-408">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="e5afb-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-409">Nome del produttore della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="e5afb-410">Esempio: "3COM"</span><span class="sxs-lookup"><span data-stu-id="e5afb-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-411">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="e5afb-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-412">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-414">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,9 \| numero massimo di allegati ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-415">Numero massimo di porte indirizzabili direttamente supportate da questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="e5afb-416">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e5afb-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-417">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="e5afb-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-418">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5afb-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-420">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="e5afb-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-421">Velocità massima, in bit al secondo, per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="e5afb-422">Questa proprietà viene ereditata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-423">Questa proprietà non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-423">This property has not been implemented yet.</span></span> <span data-ttu-id="e5afb-424">Per impostazione predefinita, viene restituito un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="e5afb-425">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5afb-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-426">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e5afb-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-429">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e5afb-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-430">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-430">Label by which the object is known.</span></span> <span data-ttu-id="e5afb-431">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e5afb-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e5afb-432">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="e5afb-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-435">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e5afb-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-436">Nome della connessione di rete visualizzato nel programma del pannello di controllo **connessioni di rete** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="e5afb-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-438">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5afb-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-440">Stato della connessione della scheda di rete alla rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="e5afb-441">**Disconnesso** (0)</span><span class="sxs-lookup"><span data-stu-id="e5afb-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="e5afb-442">**Connessione** (1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="e5afb-443">**Connessione interconnessa** (2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="e5afb-444">**Disconnessione** (3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="e5afb-445">**Hardware non presente** (4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="e5afb-446">**Hardware disabilitato** (5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="e5afb-447">**Malfunzionamento hardware** (6)</span><span class="sxs-lookup"><span data-stu-id="e5afb-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="e5afb-448">**Supporti disconnessi** (7)</span><span class="sxs-lookup"><span data-stu-id="e5afb-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="e5afb-449">**Autenticazione** (8)</span><span class="sxs-lookup"><span data-stu-id="e5afb-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="e5afb-450">**Autenticazione riuscita** (9)</span><span class="sxs-lookup"><span data-stu-id="e5afb-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="e5afb-451">**Autenticazione non riuscita** (10)</span><span class="sxs-lookup"><span data-stu-id="e5afb-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="e5afb-452">**Indirizzo non valido** (11)</span><span class="sxs-lookup"><span data-stu-id="e5afb-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="e5afb-453">**Credenziali richieste** (12)</span><span class="sxs-lookup"><span data-stu-id="e5afb-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e5afb-454">**Altri**</span><span class="sxs-lookup"><span data-stu-id="e5afb-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="e5afb-455">13-65535</span><span class="sxs-lookup"><span data-stu-id="e5afb-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="e5afb-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-457">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-459">Indica se l'adapter è abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="e5afb-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="e5afb-460">Se **true**, l'adapter è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="e5afb-461">È possibile abilitare o disabilitare la scheda di interfaccia di rete usando i metodi [**Enable**](enable-method-in-class-win32-networkadapter.md) e [**Disable**](disable-method-in-class-win32-networkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="e5afb-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="e5afb-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-463">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e5afb-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-465">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-466">Matrice di indirizzi di rete per un adapter.</span><span class="sxs-lookup"><span data-stu-id="e5afb-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="e5afb-467">Questa proprietà viene ereditata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-468">Questa proprietà non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-468">This property has not been implemented yet.</span></span> <span data-ttu-id="e5afb-469">Per impostazione predefinita, viene restituito un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-470">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="e5afb-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-471">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-473">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-474">Indirizzo di rete hardcoded in un adapter.</span><span class="sxs-lookup"><span data-stu-id="e5afb-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="e5afb-475">Questo indirizzo hardcoded può essere modificato dall'aggiornamento del firmware o dalla configurazione del software.</span><span class="sxs-lookup"><span data-stu-id="e5afb-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="e5afb-476">In tal caso, questo campo deve essere aggiornato quando viene apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="e5afb-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="e5afb-477">Se non esiste alcun indirizzo hardcoded per la scheda di rete, la proprietà deve essere lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="e5afb-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="e5afb-478">Questa proprietà viene ereditata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-479">Questa proprietà non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-479">This property has not been implemented yet.</span></span> <span data-ttu-id="e5afb-480">Per impostazione predefinita, viene restituito un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5afb-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="e5afb-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-482">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-484">Indica se l'adapter è una scheda fisica o logica.</span><span class="sxs-lookup"><span data-stu-id="e5afb-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="e5afb-485">Se **true**, l'adapter è fisico.</span><span class="sxs-lookup"><span data-stu-id="e5afb-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5afb-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-489">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5afb-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-490">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5afb-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e5afb-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e5afb-492">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e5afb-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-493">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e5afb-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-494">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5afb-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-496">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5afb-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e5afb-497">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5afb-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e5afb-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e5afb-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e5afb-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e5afb-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-502">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5afb-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e5afb-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-504">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="e5afb-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e5afb-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-506">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e5afb-507">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="e5afb-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="e5afb-508">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e5afb-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="e5afb-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-510">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="e5afb-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e5afb-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="e5afb-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e5afb-512">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="e5afb-512">Timed Power-On Supported</span></span>

<span data-ttu-id="e5afb-513">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="e5afb-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-514">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e5afb-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-515">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5afb-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-516">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-517">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="e5afb-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="e5afb-518">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="e5afb-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e5afb-519">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="e5afb-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-521">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-523">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="e5afb-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-524">Nome del prodotto della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-524">Product name of the network adapter.</span></span>

<span data-ttu-id="e5afb-525">Esempio: "Fast EtherLink XL"</span><span class="sxs-lookup"><span data-stu-id="e5afb-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-526">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="e5afb-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-527">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-528">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-529">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="e5afb-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-530">Nome del servizio della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-530">Service name of the network adapter.</span></span> <span data-ttu-id="e5afb-531">Questo nome è in genere più breve del nome completo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="e5afb-532">Esempio: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="e5afb-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-533">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="e5afb-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-534">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5afb-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-535">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-536">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Scheda di rete DMTF 802 porta \| 001,5 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bit al secondo ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-537">Stima della larghezza di banda corrente in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e5afb-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="e5afb-538">Per gli endpoint che variano a seconda della larghezza di banda o per quelli in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="e5afb-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="e5afb-539">Questa proprietà viene ereditata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-540">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5afb-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-541">**Status**</span><span class="sxs-lookup"><span data-stu-id="e5afb-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-542">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-543">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-544">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="e5afb-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-545">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-545">Current status of the object.</span></span> <span data-ttu-id="e5afb-546">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e5afb-547">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5afb-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e5afb-548">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e5afb-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e5afb-549">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e5afb-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e5afb-550">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e5afb-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5afb-551">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e5afb-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e5afb-552">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e5afb-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e5afb-553">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e5afb-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e5afb-554">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e5afb-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e5afb-555">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e5afb-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e5afb-556">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e5afb-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e5afb-557">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e5afb-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e5afb-558">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e5afb-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e5afb-559">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e5afb-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e5afb-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-561">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5afb-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-562">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-563">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e5afb-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-564">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5afb-564">State of the logical device.</span></span> <span data-ttu-id="e5afb-565">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e5afb-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e5afb-566">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e5afb-567">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e5afb-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5afb-568">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="e5afb-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e5afb-569">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e5afb-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e5afb-570">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="e5afb-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e5afb-571">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="e5afb-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5afb-572">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5afb-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-573">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-574">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-575">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e5afb-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-576">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="e5afb-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e5afb-577">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e5afb-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-579">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5afb-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-580">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-581">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e5afb-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-582">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e5afb-582">Name of the scoping system.</span></span>

<span data-ttu-id="e5afb-583">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5afb-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="e5afb-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5afb-585">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5afb-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-586">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5afb-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5afb-587">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System Up Time")</span><span class="sxs-lookup"><span data-stu-id="e5afb-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="e5afb-588">Data e ora dell'ultima reimpostazione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5afb-589">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5afb-589">Remarks</span></span>

<span data-ttu-id="e5afb-590">La classe **Win32 \_ NetworkAdapter** è derivata da [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="e5afb-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="e5afb-591">Nell'elenco seguente vengono descritte le classi associater per **Win32 \_ NetworkAdapter**:</span><span class="sxs-lookup"><span data-stu-id="e5afb-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="e5afb-592">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="e5afb-593">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="e5afb-594">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="e5afb-595">**\_IRQResource Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="e5afb-596">**\_DeviceMemoryAddress Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="e5afb-597">**\_PortResource Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="e5afb-598">**\_NetworkProtocol Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="e5afb-599">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="e5afb-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="e5afb-600">Molti sistemi hanno un certo numero di schede di rete.</span><span class="sxs-lookup"><span data-stu-id="e5afb-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="e5afb-601">Per trovare le schede correnti, provare a utilizzare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e5afb-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="e5afb-602">Anche usando i qualificatori precedenti, è probabile che vengano recuperate più schede di rete valide.</span><span class="sxs-lookup"><span data-stu-id="e5afb-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="e5afb-603">In tal caso, è possibile usare le informazioni seguenti per qualificare ulteriormente la ricerca di Win32 \_ NetworkAdapterConfiguration:</span><span class="sxs-lookup"><span data-stu-id="e5afb-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="e5afb-604">Una volta eseguita questa operazione, è probabile che l'elenco sia stato ridotto a uno o due adattatori configurati.</span><span class="sxs-lookup"><span data-stu-id="e5afb-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="e5afb-605">È inoltre possibile utilizzare la procedura seguente per trovare l'adattatore predefinito:</span><span class="sxs-lookup"><span data-stu-id="e5afb-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="e5afb-606">Eseguire la query seguente:</span><span class="sxs-lookup"><span data-stu-id="e5afb-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="e5afb-607">È necessario avere una sola destinazione di rete predefinita 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="e5afb-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="e5afb-608">Usare **IndiceInterfaccia** per recuperare la scheda di rete desiderata.</span><span class="sxs-lookup"><span data-stu-id="e5afb-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="e5afb-609">Esempio</span><span class="sxs-lookup"><span data-stu-id="e5afb-609">Examples</span></span>

<span data-ttu-id="e5afb-610">L'esempio di codice PowerShell per le [due funzioni WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) della raccolta TechNet USA **Win32 \_ NetworkAdapter** per ricreare il cmdlet [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) di Windows.</span><span class="sxs-lookup"><span data-stu-id="e5afb-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="e5afb-611">L'esempio relativo a [Get-ComputerInfo-query computer da computer locale/remoto-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell nella raccolta TechNet usa una serie di chiamate a hardware e software, tra cui **Win32 \_ NetworkAdapter**, per visualizzare informazioni su un sistema locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="e5afb-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="e5afb-612">Nell' \# esempio di codice C seguente viene usato lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) per recuperare le schede di rete correnti nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e5afb-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="e5afb-613">Nell' \# esempio di codice C seguente viene usato lo https://msdn.microsoft.com/library/system.management.aspx spazio dei nomi per recuperare le schede di rete correnti nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e5afb-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="e5afb-614"> https://msdn.microsoft.com/library/system.management.aspx contiene le classi originali utilizzate per accedere a WMI. Tuttavia, sono considerate più lente e in genere non vengono ridimensionate, nonché le controparti [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e5afb-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="e5afb-615">Nell'esempio di codice VBScript seguente viene descritto come recuperare le schede di rete correnti nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e5afb-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="e5afb-616">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5afb-616">Requirements</span></span>



| <span data-ttu-id="e5afb-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5afb-617">Requirement</span></span> | <span data-ttu-id="e5afb-618">Valore</span><span class="sxs-lookup"><span data-stu-id="e5afb-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5afb-619">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5afb-619">Minimum supported client</span></span><br/> | <span data-ttu-id="e5afb-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5afb-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5afb-621">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5afb-621">Minimum supported server</span></span><br/> | <span data-ttu-id="e5afb-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5afb-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5afb-623">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5afb-623">Namespace</span></span><br/>                | <span data-ttu-id="e5afb-624">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e5afb-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5afb-625">MOF</span><span class="sxs-lookup"><span data-stu-id="e5afb-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5afb-626"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5afb-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5afb-627">DLL</span><span class="sxs-lookup"><span data-stu-id="e5afb-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5afb-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5afb-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5afb-629">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5afb-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5afb-630">**\_NETWORKADAPTER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5afb-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="e5afb-631">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e5afb-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e5afb-632">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="e5afb-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="e5afb-633">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="e5afb-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
