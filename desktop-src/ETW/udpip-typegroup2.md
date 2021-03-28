---
description: Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv6 UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: Classe UdpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978866"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="c5649-104">\_Classe UdpIp TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="c5649-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="c5649-105">Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv6 UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="c5649-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="c5649-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c5649-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5649-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5649-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="c5649-108">Members</span><span class="sxs-lookup"><span data-stu-id="c5649-108">Members</span></span>

<span data-ttu-id="c5649-109">La **classe \_ TypeGroup2 di UdpIp** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c5649-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="c5649-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5649-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5649-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5649-111">Properties</span></span>

<span data-ttu-id="c5649-112">La **classe \_ TypeGroup2 di UdpIp** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5649-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5649-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="c5649-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5649-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-116">Qualificatori: WmiDataId (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="c5649-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c5649-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="c5649-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-118">daddr</span><span class="sxs-lookup"><span data-stu-id="c5649-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5649-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="c5649-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="c5649-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5649-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-123">dport</span><span class="sxs-lookup"><span data-stu-id="c5649-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5649-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="c5649-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="c5649-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5649-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-128">PID</span><span class="sxs-lookup"><span data-stu-id="c5649-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5649-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="c5649-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c5649-132">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5649-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-133">saddr</span><span class="sxs-lookup"><span data-stu-id="c5649-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5649-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-136">Qualificatori: WmiDataId (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="c5649-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="c5649-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="c5649-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="c5649-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5649-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-141">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="c5649-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="c5649-142">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="c5649-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-143">size</span><span class="sxs-lookup"><span data-stu-id="c5649-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5649-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-146">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="c5649-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c5649-147">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c5649-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="c5649-148">Sport</span><span class="sxs-lookup"><span data-stu-id="c5649-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5649-149">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5649-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5649-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5649-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5649-151">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="c5649-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="c5649-152">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="c5649-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5649-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5649-153">Requirements</span></span>



| <span data-ttu-id="c5649-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5649-154">Requirement</span></span> | <span data-ttu-id="c5649-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c5649-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5649-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5649-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c5649-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5649-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5649-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5649-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c5649-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5649-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5649-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5649-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5649-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="c5649-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




