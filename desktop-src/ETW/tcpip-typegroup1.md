---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv4. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: Classe TcpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978263"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="da829-104">\_Classe TypeGroup1 Tcpip</span><span class="sxs-lookup"><span data-stu-id="da829-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="da829-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="da829-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="da829-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="da829-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="da829-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da829-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
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

## <a name="members"></a><span data-ttu-id="da829-108">Members</span><span class="sxs-lookup"><span data-stu-id="da829-108">Members</span></span>

<span data-ttu-id="da829-109">La classe **TCPIP \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da829-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="da829-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da829-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da829-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da829-111">Properties</span></span>

<span data-ttu-id="da829-112">La classe **TCPIP \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da829-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da829-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="da829-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da829-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da829-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-116">Qualificatori: WmiDataId (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="da829-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="da829-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="da829-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="da829-118">daddr</span><span class="sxs-lookup"><span data-stu-id="da829-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="da829-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da829-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="da829-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="da829-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da829-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da829-123">dport</span><span class="sxs-lookup"><span data-stu-id="da829-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="da829-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da829-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="da829-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="da829-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da829-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="da829-128">PID</span><span class="sxs-lookup"><span data-stu-id="da829-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da829-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da829-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="da829-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="da829-132">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="da829-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="da829-133">saddr</span><span class="sxs-lookup"><span data-stu-id="da829-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="da829-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da829-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-136">Qualificatori: WmiDataId (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="da829-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="da829-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="da829-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da829-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="da829-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da829-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da829-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-141">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="da829-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="da829-142">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="da829-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="da829-143">size</span><span class="sxs-lookup"><span data-stu-id="da829-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da829-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da829-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-146">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="da829-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="da829-147">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="da829-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="da829-148">Sport</span><span class="sxs-lookup"><span data-stu-id="da829-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da829-149">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="da829-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da829-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da829-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da829-151">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="da829-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="da829-152">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="da829-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da829-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da829-153">Requirements</span></span>



| <span data-ttu-id="da829-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="da829-154">Requirement</span></span> | <span data-ttu-id="da829-155">Valore</span><span class="sxs-lookup"><span data-stu-id="da829-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da829-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da829-156">Minimum supported client</span></span><br/> | <span data-ttu-id="da829-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da829-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da829-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da829-158">Minimum supported server</span></span><br/> | <span data-ttu-id="da829-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da829-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da829-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da829-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da829-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="da829-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




