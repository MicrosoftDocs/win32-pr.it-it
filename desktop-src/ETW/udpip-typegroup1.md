---
description: Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv4 UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: Classe UdpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978871"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="a8c37-104">\_Classe UdpIp TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="a8c37-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="a8c37-105">Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv4 UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="a8c37-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="a8c37-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a8c37-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c37-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8c37-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
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

## <a name="members"></a><span data-ttu-id="a8c37-108">Members</span><span class="sxs-lookup"><span data-stu-id="a8c37-108">Members</span></span>

<span data-ttu-id="a8c37-109">La **classe \_ TypeGroup1 di UdpIp** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a8c37-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a8c37-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8c37-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8c37-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8c37-111">Properties</span></span>

<span data-ttu-id="a8c37-112">La **classe \_ TypeGroup1 di UdpIp** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8c37-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8c37-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="a8c37-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8c37-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-116">Qualificatori: WmiDataId (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="a8c37-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="a8c37-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a8c37-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="a8c37-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="a8c37-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a8c37-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-123">dport</span><span class="sxs-lookup"><span data-stu-id="a8c37-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="a8c37-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="a8c37-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a8c37-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-128">PID</span><span class="sxs-lookup"><span data-stu-id="a8c37-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8c37-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="a8c37-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-132">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8c37-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-133">saddr</span><span class="sxs-lookup"><span data-stu-id="a8c37-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="a8c37-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-136">Qualificatori: WmiDataId (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="a8c37-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="a8c37-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="a8c37-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8c37-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-141">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="a8c37-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-142">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="a8c37-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-143">size</span><span class="sxs-lookup"><span data-stu-id="a8c37-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8c37-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-146">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a8c37-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-147">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a8c37-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a8c37-148">Sport</span><span class="sxs-lookup"><span data-stu-id="a8c37-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c37-149">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="a8c37-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8c37-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c37-151">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="a8c37-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a8c37-152">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="a8c37-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8c37-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8c37-153">Requirements</span></span>



| <span data-ttu-id="a8c37-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c37-154">Requirement</span></span> | <span data-ttu-id="a8c37-155">Valore</span><span class="sxs-lookup"><span data-stu-id="a8c37-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8c37-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8c37-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c37-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8c37-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8c37-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8c37-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c37-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8c37-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8c37-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8c37-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c37-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="a8c37-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




