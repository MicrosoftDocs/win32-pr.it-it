---
description: Questa classe è la classe del tipo di evento per gli eventi di connessione TCP/IP IPv4 e Accept. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Classe TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528219"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="2460c-104">\_Classe TypeGroup2 Tcpip</span><span class="sxs-lookup"><span data-stu-id="2460c-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="2460c-105">Questa classe è la classe del tipo di evento per gli eventi di connessione TCP/IP IPv4 e Accept.</span><span class="sxs-lookup"><span data-stu-id="2460c-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="2460c-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2460c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2460c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2460c-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="2460c-108">Members</span><span class="sxs-lookup"><span data-stu-id="2460c-108">Members</span></span>

<span data-ttu-id="2460c-109">La classe **TCPIP \_ TypeGroup2** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2460c-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="2460c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2460c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2460c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2460c-111">Properties</span></span>

<span data-ttu-id="2460c-112">La classe **TCPIP \_ TypeGroup2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2460c-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2460c-113">**ConnID**</span><span class="sxs-lookup"><span data-stu-id="2460c-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2460c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-116">Qualificatori: **WmiDataId (15)**, **puntatore**</span><span class="sxs-lookup"><span data-stu-id="2460c-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="2460c-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="2460c-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2460c-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-121">Qualificatori: **WmiDataId (3)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="2460c-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2460c-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="2460c-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2460c-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-126">Qualificatori: **WmiDataId (5)**, **Extension ("Port")**</span><span class="sxs-lookup"><span data-stu-id="2460c-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2460c-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="2460c-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2460c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-131">Qualificatori: **WmiDataId (7)**</span><span class="sxs-lookup"><span data-stu-id="2460c-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-132">Dimensioni massime del segmento.</span><span class="sxs-lookup"><span data-stu-id="2460c-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-133">**PID**</span><span class="sxs-lookup"><span data-stu-id="2460c-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2460c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-136">Qualificatori: **WmiDataId (1)**</span><span class="sxs-lookup"><span data-stu-id="2460c-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-137">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="2460c-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="2460c-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2460c-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-141">Qualificatori: **WmiDataId (11)**</span><span class="sxs-lookup"><span data-stu-id="2460c-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-142">Dimensioni della finestra di ricezione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="2460c-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-144">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2460c-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-146">Qualificatori: **WmiDataId (12)**</span><span class="sxs-lookup"><span data-stu-id="2460c-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-147">Fattore di scala della finestra di ricezione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="2460c-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2460c-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-151">Qualificatori: **WmiDataId (8)**</span><span class="sxs-lookup"><span data-stu-id="2460c-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-152">Opzione di riconoscimento selettiva (SACK) nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="2460c-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-154">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2460c-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-156">Qualificatori: **WmiDataId (4)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="2460c-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-157">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="2460c-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-158">**SeqNum**</span><span class="sxs-lookup"><span data-stu-id="2460c-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2460c-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-161">Qualificatori: **WmiDataId (14)**</span><span class="sxs-lookup"><span data-stu-id="2460c-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-162">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="2460c-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-163">**size**</span><span class="sxs-lookup"><span data-stu-id="2460c-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-164">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2460c-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-166">Qualificatori: **WmiDataId (2)**</span><span class="sxs-lookup"><span data-stu-id="2460c-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-167">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2460c-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="2460c-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-169">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2460c-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-171">Qualificatori: **WmiDataId (13)**</span><span class="sxs-lookup"><span data-stu-id="2460c-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-172">Fattore di scala della finestra di trasmissione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-173">**Sport**</span><span class="sxs-lookup"><span data-stu-id="2460c-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-174">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2460c-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-176">Qualificatori: **WmiDataId (6)**, **Extension ("Port")**</span><span class="sxs-lookup"><span data-stu-id="2460c-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-177">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="2460c-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="2460c-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2460c-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-181">Qualificatori: **WmiDataId (9)**</span><span class="sxs-lookup"><span data-stu-id="2460c-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-182">Opzione timestamp nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="2460c-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="2460c-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2460c-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2460c-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2460c-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2460c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2460c-186">Qualificatori: **WmiDataId (10)**</span><span class="sxs-lookup"><span data-stu-id="2460c-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="2460c-187">Opzione di scalabilità della finestra nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="2460c-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2460c-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2460c-188">Requirements</span></span>



| <span data-ttu-id="2460c-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="2460c-189">Requirement</span></span> | <span data-ttu-id="2460c-190">Valore</span><span class="sxs-lookup"><span data-stu-id="2460c-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2460c-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2460c-191">Minimum supported client</span></span><br/> | <span data-ttu-id="2460c-192">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2460c-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2460c-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2460c-193">Minimum supported server</span></span><br/> | <span data-ttu-id="2460c-194">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2460c-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2460c-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2460c-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2460c-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="2460c-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




