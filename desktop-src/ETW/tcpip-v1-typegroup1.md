---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: Classe TcpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978234"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="32b41-104">\_ \_ Classe TypeGroup1 di Tcpip V1</span><span class="sxs-lookup"><span data-stu-id="32b41-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="32b41-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="32b41-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="32b41-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="32b41-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32b41-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="32b41-108">Members</span><span class="sxs-lookup"><span data-stu-id="32b41-108">Members</span></span>

<span data-ttu-id="32b41-109">La classe **TCPIP \_ V1 \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32b41-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="32b41-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32b41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32b41-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32b41-111">Properties</span></span>

<span data-ttu-id="32b41-112">La classe **TCPIP \_ V1 \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="32b41-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32b41-113">daddr</span><span class="sxs-lookup"><span data-stu-id="32b41-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="32b41-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-116">Qualificatori: WmiDataId (3), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="32b41-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="32b41-117">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="32b41-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32b41-118">dport</span><span class="sxs-lookup"><span data-stu-id="32b41-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="32b41-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-121">Qualificatori: WmiDataId (5), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="32b41-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="32b41-122">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="32b41-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="32b41-123">PID</span><span class="sxs-lookup"><span data-stu-id="32b41-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32b41-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-126">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="32b41-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="32b41-127">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="32b41-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="32b41-128">saddr</span><span class="sxs-lookup"><span data-stu-id="32b41-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-129">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="32b41-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-131">Qualificatori: WmiDataId (4), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="32b41-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="32b41-132">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="32b41-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32b41-133">size</span><span class="sxs-lookup"><span data-stu-id="32b41-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32b41-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-136">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="32b41-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="32b41-137">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="32b41-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="32b41-138">Sport</span><span class="sxs-lookup"><span data-stu-id="32b41-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b41-139">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="32b41-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="32b41-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32b41-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b41-141">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="32b41-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="32b41-142">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="32b41-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32b41-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32b41-143">Requirements</span></span>



| <span data-ttu-id="32b41-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b41-144">Requirement</span></span> | <span data-ttu-id="32b41-145">Valore</span><span class="sxs-lookup"><span data-stu-id="32b41-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32b41-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32b41-146">Minimum supported client</span></span><br/> | <span data-ttu-id="32b41-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="32b41-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="32b41-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32b41-148">Minimum supported server</span></span><br/> | <span data-ttu-id="32b41-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32b41-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32b41-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32b41-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b41-151">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="32b41-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




