---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: Classe TcpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344551"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="cd3f3-104">\_ \_ Classe TypeGroup1 Tcpip V0</span><span class="sxs-lookup"><span data-stu-id="cd3f3-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="cd3f3-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="cd3f3-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd3f3-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="cd3f3-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd3f3-108">Members</span></span>

<span data-ttu-id="cd3f3-109">La classe **TCPIP \_ V0 \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd3f3-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cd3f3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd3f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd3f3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd3f3-111">Properties</span></span>

<span data-ttu-id="cd3f3-112">La classe **TCPIP \_ V0 \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd3f3-113">daddr</span><span class="sxs-lookup"><span data-stu-id="cd3f3-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-116">Qualificatori: WmiDataId (1), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="cd3f3-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-117">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cd3f3-118">dport</span><span class="sxs-lookup"><span data-stu-id="cd3f3-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-121">Qualificatori: WmiDataId (3), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="cd3f3-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-122">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="cd3f3-123">PID</span><span class="sxs-lookup"><span data-stu-id="cd3f3-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-126">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="cd3f3-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-127">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="cd3f3-128">saddr</span><span class="sxs-lookup"><span data-stu-id="cd3f3-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-129">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-131">Qualificatori: WmiDataId (2), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="cd3f3-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-132">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cd3f3-133">size</span><span class="sxs-lookup"><span data-stu-id="cd3f3-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-136">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="cd3f3-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-137">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="cd3f3-138">Sport</span><span class="sxs-lookup"><span data-stu-id="cd3f3-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd3f3-139">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd3f3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd3f3-141">Qualificatori: WmiDataId (4), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="cd3f3-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cd3f3-142">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="cd3f3-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd3f3-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd3f3-143">Requirements</span></span>



| <span data-ttu-id="cd3f3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd3f3-144">Requirement</span></span> | <span data-ttu-id="cd3f3-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cd3f3-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="cd3f3-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd3f3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3f3-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd3f3-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cd3f3-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd3f3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3f3-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cd3f3-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="cd3f3-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd3f3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3f3-151">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="cd3f3-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




