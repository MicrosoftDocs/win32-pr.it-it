---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Classe SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980551"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="22dde-103">\_Classe SystemConfig V0 \_ NIC</span><span class="sxs-lookup"><span data-stu-id="22dde-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="22dde-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22dde-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="22dde-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="22dde-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="22dde-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22dde-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="22dde-107">Members</span><span class="sxs-lookup"><span data-stu-id="22dde-107">Members</span></span>

<span data-ttu-id="22dde-108">La classe **SystemConfig \_ V0 \_ NIC** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="22dde-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="22dde-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22dde-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22dde-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22dde-110">Properties</span></span>

<span data-ttu-id="22dde-111">La classe **SystemConfig \_ V0 \_ NIC** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="22dde-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22dde-112">**Dati**</span><span class="sxs-lookup"><span data-stu-id="22dde-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22dde-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-115">Qualificatori: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="22dde-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-116">Campo dati.</span><span class="sxs-lookup"><span data-stu-id="22dde-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="22dde-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-120">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="22dde-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-121">Indirizzo IP del server DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="22dde-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="22dde-122">Il valore 255.255.255.255 indica che non è stato possibile raggiungere il server DHCP oppure è in corso il raggiungimento.</span><span class="sxs-lookup"><span data-stu-id="22dde-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="22dde-123">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-124">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="22dde-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-128">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="22dde-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-129">Primi indirizzi IP del server da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="22dde-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="22dde-130">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-131">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="22dde-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-133">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-135">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="22dde-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-136">Secondi indirizzi IP del server da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="22dde-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="22dde-137">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-138">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="22dde-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-140">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-142">Qualificatori: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="22dde-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-143">Indirizzi IP del terzo server da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="22dde-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="22dde-144">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-145">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="22dde-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-149">Qualificatori: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="22dde-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-150">Quarto indirizzo IP del server da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="22dde-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="22dde-151">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-152">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-153">**Gateway**</span><span class="sxs-lookup"><span data-stu-id="22dde-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-154">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-156">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="22dde-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-157">Indirizzo IP del gateway predefinito utilizzato dal computer.</span><span class="sxs-lookup"><span data-stu-id="22dde-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="22dde-158">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-159">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="22dde-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22dde-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-163">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="22dde-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-164">Indice dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="22dde-164">Adapter index.</span></span> <span data-ttu-id="22dde-165">È possibile che l'indice dell'adapter venga modificato quando un adapter viene disabilitato e quindi abilitato oppure in altre circostanze e non deve essere considerato persistente.</span><span class="sxs-lookup"><span data-stu-id="22dde-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-166">**IpAddress**</span><span class="sxs-lookup"><span data-stu-id="22dde-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-167">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-169">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="22dde-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-170">Indirizzi IP associati alla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22dde-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="22dde-171">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-172">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="22dde-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-174">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="22dde-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="22dde-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-176">Qualificatori: **WmiDataId** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="22dde-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-177">Nome della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22dde-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-178">**PhysicalAddr**</span><span class="sxs-lookup"><span data-stu-id="22dde-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-179">Tipo di dati: **Char16**</span><span class="sxs-lookup"><span data-stu-id="22dde-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-181">Qualificatori: **WmiDataId** (4), **Max** (8)</span><span class="sxs-lookup"><span data-stu-id="22dde-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-182">Indirizzo hardware per la scheda.</span><span class="sxs-lookup"><span data-stu-id="22dde-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-183">**PhysicalAddrLen**</span><span class="sxs-lookup"><span data-stu-id="22dde-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-184">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22dde-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-186">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="22dde-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-187">Lunghezza dell'indirizzo hardware per la scheda.</span><span class="sxs-lookup"><span data-stu-id="22dde-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-188">**PrimaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="22dde-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-189">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-191">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="22dde-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-192">Indirizzo IP del server WINS primario.</span><span class="sxs-lookup"><span data-stu-id="22dde-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="22dde-193">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-194">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-195">**SecondaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="22dde-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-196">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-198">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="22dde-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-199">Indirizzo IP del server WINS secondario.</span><span class="sxs-lookup"><span data-stu-id="22dde-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="22dde-200">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-201">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-202">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="22dde-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22dde-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-205">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="22dde-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-206">Dimensione, in byte, della proprietà dei dati.</span><span class="sxs-lookup"><span data-stu-id="22dde-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="22dde-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22dde-208">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22dde-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22dde-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="22dde-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22dde-210">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="22dde-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="22dde-211">Subnet mask associata alla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22dde-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="22dde-212">Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="22dde-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="22dde-213">Il byte di ordine inferiore contiene il valore per P1, il byte successivo contiene il valore per P2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22dde-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22dde-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22dde-214">Requirements</span></span>



| <span data-ttu-id="22dde-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="22dde-215">Requirement</span></span> | <span data-ttu-id="22dde-216">Valore</span><span class="sxs-lookup"><span data-stu-id="22dde-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22dde-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22dde-217">Minimum supported client</span></span><br/> | <span data-ttu-id="22dde-218">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="22dde-218">None supported</span></span><br/>                            |
| <span data-ttu-id="22dde-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22dde-219">Minimum supported server</span></span><br/> | <span data-ttu-id="22dde-220">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22dde-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22dde-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22dde-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22dde-222">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="22dde-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




