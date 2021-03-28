---
description: Questa classe è la classe del tipo di evento per gli eventi di trasmissione TCP/IP IPv6. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: Classe TcpIp_SendIPV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978258"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="56b0e-104">\_Classe SendIPV6 Tcpip</span><span class="sxs-lookup"><span data-stu-id="56b0e-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="56b0e-105">Questa classe è la classe del tipo di evento per gli eventi di trasmissione TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="56b0e-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="56b0e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="56b0e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b0e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56b0e-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="56b0e-108">Members</span><span class="sxs-lookup"><span data-stu-id="56b0e-108">Members</span></span>

<span data-ttu-id="56b0e-109">La classe **TCPIP \_ SendIPV6** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56b0e-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="56b0e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56b0e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56b0e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56b0e-111">Properties</span></span>

<span data-ttu-id="56b0e-112">La classe **TCPIP \_ SendIPV6** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56b0e-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56b0e-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="56b0e-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-116">Qualificatori: WmiDataId (10), puntatore</span><span class="sxs-lookup"><span data-stu-id="56b0e-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="56b0e-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-118">daddr</span><span class="sxs-lookup"><span data-stu-id="56b0e-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="56b0e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="56b0e-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56b0e-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-123">dport</span><span class="sxs-lookup"><span data-stu-id="56b0e-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="56b0e-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="56b0e-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56b0e-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="56b0e-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-131">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="56b0e-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-132">Termina tempo richiesta di invio.</span><span class="sxs-lookup"><span data-stu-id="56b0e-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-133">PID</span><span class="sxs-lookup"><span data-stu-id="56b0e-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-136">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="56b0e-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-137">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="56b0e-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-138">saddr</span><span class="sxs-lookup"><span data-stu-id="56b0e-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-139">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="56b0e-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-141">Qualificatori: WmiDataId (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="56b0e-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-142">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="56b0e-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-143">SeqNum</span><span class="sxs-lookup"><span data-stu-id="56b0e-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-146">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="56b0e-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-147">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="56b0e-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-148">size</span><span class="sxs-lookup"><span data-stu-id="56b0e-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-151">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="56b0e-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-152">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="56b0e-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-153">Sport</span><span class="sxs-lookup"><span data-stu-id="56b0e-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-154">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="56b0e-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-156">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="56b0e-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-157">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="56b0e-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="56b0e-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="56b0e-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56b0e-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56b0e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56b0e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56b0e-161">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="56b0e-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="56b0e-162">Ora di inizio della richiesta di invio.</span><span class="sxs-lookup"><span data-stu-id="56b0e-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56b0e-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56b0e-163">Requirements</span></span>



| <span data-ttu-id="56b0e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b0e-164">Requirement</span></span> | <span data-ttu-id="56b0e-165">Valore</span><span class="sxs-lookup"><span data-stu-id="56b0e-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56b0e-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b0e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="56b0e-167">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56b0e-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56b0e-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b0e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="56b0e-169">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56b0e-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56b0e-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56b0e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b0e-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="56b0e-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




