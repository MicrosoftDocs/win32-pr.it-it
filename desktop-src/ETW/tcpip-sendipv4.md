---
description: Questa classe è la classe del tipo di evento per gli eventi di invio TCP/IP IPv4. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: Classe TcpIp_SendIPV4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967034"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="89633-104">\_Classe SendIPV4 Tcpip</span><span class="sxs-lookup"><span data-stu-id="89633-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="89633-105">Questa classe è la classe del tipo di evento per gli eventi di invio TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="89633-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="89633-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="89633-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="89633-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89633-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="89633-108">Members</span><span class="sxs-lookup"><span data-stu-id="89633-108">Members</span></span>

<span data-ttu-id="89633-109">La classe **TCPIP \_ SendIPV4** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89633-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="89633-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89633-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89633-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89633-111">Properties</span></span>

<span data-ttu-id="89633-112">La classe **TCPIP \_ SendIPV4** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89633-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89633-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="89633-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-116">Qualificatori: WmiDataId (10), puntatore</span><span class="sxs-lookup"><span data-stu-id="89633-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="89633-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="89633-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="89633-118">daddr</span><span class="sxs-lookup"><span data-stu-id="89633-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="89633-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="89633-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="89633-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="89633-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89633-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89633-123">dport</span><span class="sxs-lookup"><span data-stu-id="89633-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="89633-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="89633-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="89633-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="89633-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89633-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="89633-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="89633-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-131">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="89633-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="89633-132">Termina tempo richiesta di invio.</span><span class="sxs-lookup"><span data-stu-id="89633-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="89633-133">PID</span><span class="sxs-lookup"><span data-stu-id="89633-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-136">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="89633-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="89633-137">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="89633-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="89633-138">saddr</span><span class="sxs-lookup"><span data-stu-id="89633-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-139">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="89633-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="89633-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-141">Qualificatori: WmiDataId (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="89633-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="89633-142">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="89633-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89633-143">SeqNum</span><span class="sxs-lookup"><span data-stu-id="89633-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-146">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="89633-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="89633-147">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="89633-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="89633-148">size</span><span class="sxs-lookup"><span data-stu-id="89633-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-151">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="89633-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="89633-152">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="89633-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="89633-153">Sport</span><span class="sxs-lookup"><span data-stu-id="89633-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-154">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="89633-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="89633-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-156">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="89633-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="89633-157">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="89633-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="89633-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="89633-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89633-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89633-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89633-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89633-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89633-161">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="89633-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="89633-162">Ora di inizio della richiesta di invio.</span><span class="sxs-lookup"><span data-stu-id="89633-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89633-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89633-163">Requirements</span></span>



| <span data-ttu-id="89633-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="89633-164">Requirement</span></span> | <span data-ttu-id="89633-165">Valore</span><span class="sxs-lookup"><span data-stu-id="89633-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89633-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89633-166">Minimum supported client</span></span><br/> | <span data-ttu-id="89633-167">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89633-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="89633-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89633-168">Minimum supported server</span></span><br/> | <span data-ttu-id="89633-169">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89633-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89633-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89633-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89633-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="89633-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




