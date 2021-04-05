---
description: Rappresenta la configurazione di una scheda di rete all'interno del sistema operativo guest.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Classe Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129750"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="bb052-103">\_Classe MSVM GuestNetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb052-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="bb052-104">Rappresenta la configurazione di una scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="bb052-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bb052-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb052-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb052-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="bb052-107">Members</span><span class="sxs-lookup"><span data-stu-id="bb052-107">Members</span></span>

<span data-ttu-id="bb052-108">La **classe \_ GuestNetworkAdapterConfiguration di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bb052-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="bb052-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb052-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb052-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb052-110">Properties</span></span>

<span data-ttu-id="bb052-111">La **classe \_ GuestNetworkAdapterConfiguration di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb052-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb052-112">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="bb052-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bb052-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb052-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-115">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="bb052-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bb052-116">Matrice di stringhe che contengono i gateway IP predefiniti configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="bb052-117">Il numero massimo di gateway IP predefiniti che possono essere configurati in una singola scheda di rete è cinque.</span><span class="sxs-lookup"><span data-stu-id="bb052-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="bb052-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb052-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb052-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb052-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb052-121">Specifica se DHCP è abilitato nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bb052-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="bb052-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-123">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bb052-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb052-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-125">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="bb052-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bb052-126">Matrice di stringhe che contiene i server DNS configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bb052-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb052-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb052-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb052-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb052-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb052-131">Identificatore univoco per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb052-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="bb052-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="bb052-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bb052-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb052-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-135">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="bb052-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bb052-136">Matrice di stringhe che contengono gli indirizzi IP configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bb052-137">**IPAddressOrigins**</span><span class="sxs-lookup"><span data-stu-id="bb052-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb052-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb052-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-140">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="bb052-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bb052-141">Origine degli indirizzi IP configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb052-142">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bb052-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb052-143">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb052-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="bb052-144">**Statico** (2)</span><span class="sxs-lookup"><span data-stu-id="bb052-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb052-145">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="bb052-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb052-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb052-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb052-148">Identifica i protocolli IP a cui si applicano le impostazioni specificate da questa istanza.</span><span class="sxs-lookup"><span data-stu-id="bb052-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb052-149">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bb052-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb052-150">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb052-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="bb052-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="bb052-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="bb052-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="bb052-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="bb052-153">**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="bb052-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb052-154">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="bb052-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb052-155">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bb052-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb052-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb052-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb052-157">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="bb052-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bb052-158">Matrice di stringhe che contengono le subnet configurate nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="bb052-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="bb052-159">Ogni elemento in questa matrice viene applicato all'elemento corrispondente nella matrice **IPAddresses** .</span><span class="sxs-lookup"><span data-stu-id="bb052-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb052-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb052-160">Requirements</span></span>



| <span data-ttu-id="bb052-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb052-161">Requirement</span></span> | <span data-ttu-id="bb052-162">Valore</span><span class="sxs-lookup"><span data-stu-id="bb052-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb052-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb052-163">Minimum supported client</span></span><br/> | <span data-ttu-id="bb052-164">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb052-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb052-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb052-165">Minimum supported server</span></span><br/> | <span data-ttu-id="bb052-166">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb052-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb052-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb052-167">Namespace</span></span><br/>                | <span data-ttu-id="bb052-168">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb052-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb052-169">MOF</span><span class="sxs-lookup"><span data-stu-id="bb052-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb052-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb052-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb052-171">DLL</span><span class="sxs-lookup"><span data-stu-id="bb052-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb052-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb052-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

