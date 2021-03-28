---
description: Questa classe è la classe del tipo di evento per gli eventi di connessione TCP/IP IPv6 e Accept. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: Classe TcpIp_TypeGroup4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754250"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="d2495-104">\_Classe TypeGroup4 Tcpip</span><span class="sxs-lookup"><span data-stu-id="d2495-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="d2495-105">Questa classe è la classe del tipo di evento per gli eventi di connessione TCP/IP IPv6 e Accept.</span><span class="sxs-lookup"><span data-stu-id="d2495-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="d2495-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d2495-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2495-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2495-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="d2495-108">Members</span><span class="sxs-lookup"><span data-stu-id="d2495-108">Members</span></span>

<span data-ttu-id="d2495-109">La classe **TCPIP \_ TypeGroup4** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2495-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="d2495-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2495-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2495-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2495-111">Properties</span></span>

<span data-ttu-id="d2495-112">La classe **TCPIP \_ TypeGroup4** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2495-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2495-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="d2495-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2495-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-116">Qualificatori: WmiDataId (15), puntatore</span><span class="sxs-lookup"><span data-stu-id="d2495-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d2495-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="d2495-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-118">daddr</span><span class="sxs-lookup"><span data-stu-id="d2495-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="d2495-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="d2495-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="d2495-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d2495-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-123">dport</span><span class="sxs-lookup"><span data-stu-id="d2495-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="d2495-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="d2495-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d2495-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d2495-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="d2495-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2495-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-131">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="d2495-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-132">Dimensioni massime del segmento.</span><span class="sxs-lookup"><span data-stu-id="d2495-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-133">PID</span><span class="sxs-lookup"><span data-stu-id="d2495-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2495-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-136">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="d2495-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-137">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="d2495-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="d2495-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2495-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-141">Qualificatori: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="d2495-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-142">Dimensioni della finestra di ricezione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="d2495-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-144">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d2495-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-146">Qualificatori: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="d2495-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-147">Fattore di scala della finestra di ricezione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="d2495-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2495-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-151">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="d2495-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-152">Opzione di riconoscimento selettiva (SACK) nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-153">saddr</span><span class="sxs-lookup"><span data-stu-id="d2495-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-154">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="d2495-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-156">Qualificatori: WmiDataId (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="d2495-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="d2495-157">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="d2495-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-158">SeqNum</span><span class="sxs-lookup"><span data-stu-id="d2495-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2495-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-161">Qualificatori: WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="d2495-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-162">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d2495-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-163">size</span><span class="sxs-lookup"><span data-stu-id="d2495-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-164">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2495-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-166">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="d2495-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-167">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d2495-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="d2495-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-169">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d2495-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-171">Qualificatori: WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="d2495-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-172">Fattore di scala della finestra di trasmissione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-173">Sport</span><span class="sxs-lookup"><span data-stu-id="d2495-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-174">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="d2495-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-176">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="d2495-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d2495-177">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="d2495-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="d2495-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2495-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-181">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="d2495-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-182">Opzione timestamp nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="d2495-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="d2495-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2495-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2495-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2495-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2495-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2495-186">Qualificatori: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="d2495-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="d2495-187">Opzione di scalabilità della finestra nell'intestazione TCP.</span><span class="sxs-lookup"><span data-stu-id="d2495-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2495-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2495-188">Requirements</span></span>



| <span data-ttu-id="d2495-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2495-189">Requirement</span></span> | <span data-ttu-id="d2495-190">Valore</span><span class="sxs-lookup"><span data-stu-id="d2495-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2495-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2495-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d2495-192">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2495-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2495-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2495-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d2495-194">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2495-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2495-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2495-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2495-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="d2495-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




