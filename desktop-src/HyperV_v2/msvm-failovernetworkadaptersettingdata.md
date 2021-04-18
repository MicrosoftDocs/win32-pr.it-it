---
description: Rappresenta le impostazioni per una scheda di rete all'interno del sistema operativo guest, che verrà applicato al momento di un failover.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Classe Msvm_FailoverNetworkAdapterSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307924"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="fa8ec-103">\_Classe MSVM FailoverNetworkAdapterSettingData</span><span class="sxs-lookup"><span data-stu-id="fa8ec-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="fa8ec-104">Rappresenta le impostazioni per una scheda di rete all'interno del sistema operativo guest, che verrà applicato al momento di un failover.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="fa8ec-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8ec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa8ec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="fa8ec-107">Members</span><span class="sxs-lookup"><span data-stu-id="fa8ec-107">Members</span></span>

<span data-ttu-id="fa8ec-108">La **classe \_ FailoverNetworkAdapterSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fa8ec-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fa8ec-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa8ec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa8ec-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa8ec-110">Properties</span></span>

<span data-ttu-id="fa8ec-111">La **classe \_ FailoverNetworkAdapterSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa8ec-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-115">A short description of the object.</span></span> <span data-ttu-id="fa8ec-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-117">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-120">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="fa8ec-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-121">Matrice di stringhe che specificano i gateway IP predefiniti configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="fa8ec-122">Il numero massimo di gateway IP predefiniti che possono essere configurati in una singola scheda di rete è cinque.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-126">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="fa8ec-126">A description of the object.</span></span> <span data-ttu-id="fa8ec-127">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-131">Specifica se DHCP è abilitato sull'interfaccia IPv4 della scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-135">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="fa8ec-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-136">Matrice di stringhe che specificano i server DNS configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-140">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-140">A display name for the object.</span></span> <span data-ttu-id="fa8ec-141">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-145">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-146">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fa8ec-147">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-149">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-151">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="fa8ec-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-152">Matrice di stringhe che specificano gli indirizzi IP configurati nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ec-153">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-156">Identifica i protocolli Internet a cui si applicano le impostazioni specificate da questa istanza.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="fa8ec-157">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa8ec-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa8ec-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="fa8ec-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="fa8ec-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="fa8ec-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="fa8ec-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="fa8ec-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa8ec-164">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8ec-165">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa8ec-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa8ec-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8ec-167">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="fa8ec-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fa8ec-168">Matrice di stringhe che specificano le subnet configurate nella scheda di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="fa8ec-169">Ogni elemento in questa matrice viene applicato all'elemento corrispondente nella matrice **IPAddresses** .</span><span class="sxs-lookup"><span data-stu-id="fa8ec-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa8ec-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa8ec-170">Requirements</span></span>



| <span data-ttu-id="fa8ec-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa8ec-171">Requirement</span></span> | <span data-ttu-id="fa8ec-172">Valore</span><span class="sxs-lookup"><span data-stu-id="fa8ec-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8ec-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa8ec-173">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8ec-174">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fa8ec-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa8ec-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa8ec-175">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8ec-176">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fa8ec-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa8ec-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa8ec-177">Namespace</span></span><br/>                | <span data-ttu-id="fa8ec-178">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa8ec-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa8ec-179">MOF</span><span class="sxs-lookup"><span data-stu-id="fa8ec-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa8ec-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa8ec-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa8ec-181">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8ec-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8ec-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa8ec-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

