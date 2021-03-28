---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv6. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: Classe TcpIp_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978247"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="9d75f-104">\_Classe TypeGroup3 Tcpip</span><span class="sxs-lookup"><span data-stu-id="9d75f-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="9d75f-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="9d75f-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="9d75f-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="9d75f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d75f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d75f-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="9d75f-108">Members</span><span class="sxs-lookup"><span data-stu-id="9d75f-108">Members</span></span>

<span data-ttu-id="9d75f-109">La classe **TCPIP \_ TypeGroup3** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d75f-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="9d75f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d75f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d75f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d75f-111">Properties</span></span>

<span data-ttu-id="9d75f-112">La classe **TCPIP \_ TypeGroup3** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d75f-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d75f-113">ConnID</span><span class="sxs-lookup"><span data-stu-id="9d75f-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d75f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-116">Qualificatori: WmiDataId (6), puntatore</span><span class="sxs-lookup"><span data-stu-id="9d75f-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-117">Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="9d75f-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-118">daddr</span><span class="sxs-lookup"><span data-stu-id="9d75f-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="9d75f-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-121">Qualificatori: WmiDataId (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="9d75f-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d75f-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-123">dport</span><span class="sxs-lookup"><span data-stu-id="9d75f-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="9d75f-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-126">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="9d75f-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d75f-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-128">PID</span><span class="sxs-lookup"><span data-stu-id="9d75f-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d75f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9d75f-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-132">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="9d75f-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-133">saddr</span><span class="sxs-lookup"><span data-stu-id="9d75f-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="9d75f-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-136">Qualificatori: WmiDataId (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="9d75f-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="9d75f-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="9d75f-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d75f-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-141">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="9d75f-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-142">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="9d75f-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-143">size</span><span class="sxs-lookup"><span data-stu-id="9d75f-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d75f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-146">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9d75f-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-147">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9d75f-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="9d75f-148">Sport</span><span class="sxs-lookup"><span data-stu-id="9d75f-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d75f-149">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="9d75f-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d75f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d75f-151">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="9d75f-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="9d75f-152">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="9d75f-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d75f-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d75f-153">Requirements</span></span>



| <span data-ttu-id="9d75f-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d75f-154">Requirement</span></span> | <span data-ttu-id="9d75f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="9d75f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d75f-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d75f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="9d75f-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d75f-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d75f-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d75f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="9d75f-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d75f-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d75f-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d75f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d75f-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="9d75f-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




