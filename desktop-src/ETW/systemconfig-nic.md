---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Classe SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966713"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="09a28-104">\_Classe NIC SystemConfig</span><span class="sxs-lookup"><span data-stu-id="09a28-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="09a28-105">Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="09a28-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="09a28-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="09a28-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a28-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09a28-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="09a28-108">Members</span><span class="sxs-lookup"><span data-stu-id="09a28-108">Members</span></span>

<span data-ttu-id="09a28-109">La **classe \_ NIC SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="09a28-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="09a28-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09a28-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09a28-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09a28-111">Properties</span></span>

<span data-ttu-id="09a28-112">La **classe \_ NIC SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="09a28-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09a28-113">DnsServerAddresses</span><span class="sxs-lookup"><span data-stu-id="09a28-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09a28-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-116">Qualificatori: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="09a28-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="09a28-117">Indirizzi IP da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="09a28-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="09a28-118">L'elenco di indirizzi è delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="09a28-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="09a28-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09a28-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-122">Qualificatori: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="09a28-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="09a28-123">Indirizzi IP associati alla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="09a28-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="09a28-124">L'elenco di indirizzi è delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="09a28-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="09a28-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09a28-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-128">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="09a28-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="09a28-129">Indice dell'adapter per la scheda di interfaccia di rete IPv4.</span><span class="sxs-lookup"><span data-stu-id="09a28-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="09a28-130">È possibile che l'indice dell'adapter venga modificato quando un adapter viene disabilitato e quindi abilitato oppure in altre circostanze e non deve essere considerato persistente.</span><span class="sxs-lookup"><span data-stu-id="09a28-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="09a28-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09a28-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-134">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="09a28-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="09a28-135">Indice dell'adapter per la scheda di interfaccia di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="09a28-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="09a28-136">È possibile che l'indice dell'adapter venga modificato quando un adapter viene disabilitato e quindi abilitato oppure in altre circostanze e non deve essere considerato persistente.</span><span class="sxs-lookup"><span data-stu-id="09a28-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-137">NICDescription</span><span class="sxs-lookup"><span data-stu-id="09a28-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09a28-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-140">Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="09a28-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="09a28-141">Descrizione della scheda.</span><span class="sxs-lookup"><span data-stu-id="09a28-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-142">PhysicalAddr</span><span class="sxs-lookup"><span data-stu-id="09a28-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09a28-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-145">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="09a28-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="09a28-146">Indirizzo hardware per la scheda.</span><span class="sxs-lookup"><span data-stu-id="09a28-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="09a28-147">PhysicalAddrLen</span><span class="sxs-lookup"><span data-stu-id="09a28-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09a28-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09a28-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09a28-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09a28-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09a28-150">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="09a28-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="09a28-151">Lunghezza dell'indirizzo hardware per la scheda.</span><span class="sxs-lookup"><span data-stu-id="09a28-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09a28-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09a28-152">Requirements</span></span>



| <span data-ttu-id="09a28-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a28-153">Requirement</span></span> | <span data-ttu-id="09a28-154">Valore</span><span class="sxs-lookup"><span data-stu-id="09a28-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09a28-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09a28-155">Minimum supported client</span></span><br/> | <span data-ttu-id="09a28-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09a28-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09a28-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09a28-157">Minimum supported server</span></span><br/> | <span data-ttu-id="09a28-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09a28-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09a28-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09a28-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a28-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="09a28-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




