---
description: 'TcpIp_V0_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1 classe
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
ms.openlocfilehash: 96df2214aff9b5be6f10a1f08f6e6ea2e015c6b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105789"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="880e1-104">Classe \_ TypeGroup1 TcpIp V0 \_</span><span class="sxs-lookup"><span data-stu-id="880e1-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="880e1-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="880e1-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="880e1-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="880e1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="880e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="880e1-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="880e1-108">Members</span><span class="sxs-lookup"><span data-stu-id="880e1-108">Members</span></span>

<span data-ttu-id="880e1-109">La **classe \_ \_ TypeGroup1 TcpIp V0** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="880e1-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="880e1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="880e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="880e1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="880e1-111">Properties</span></span>

<span data-ttu-id="880e1-112">La **classe \_ \_ TypeGroup1 TcpIp V0** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="880e1-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="880e1-113">tasdr</span><span class="sxs-lookup"><span data-stu-id="880e1-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-114">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="880e1-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-116">Qualificatori: WmiDataId(1), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="880e1-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="880e1-117">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="880e1-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="880e1-118">dport</span><span class="sxs-lookup"><span data-stu-id="880e1-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-119">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="880e1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-121">Qualificatori: WmiDataId(3), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="880e1-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="880e1-122">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="880e1-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="880e1-123">PID</span><span class="sxs-lookup"><span data-stu-id="880e1-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="880e1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-126">Qualificatori: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="880e1-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="880e1-127">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="880e1-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="880e1-128">saddr</span><span class="sxs-lookup"><span data-stu-id="880e1-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-129">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="880e1-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-131">Qualificatori: WmiDataId(2), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="880e1-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="880e1-132">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="880e1-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="880e1-133">size</span><span class="sxs-lookup"><span data-stu-id="880e1-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="880e1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-136">Qualificatori: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="880e1-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="880e1-137">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="880e1-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="880e1-138">sport</span><span class="sxs-lookup"><span data-stu-id="880e1-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880e1-139">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="880e1-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="880e1-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="880e1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="880e1-141">Qualificatori: WmiDataId(4), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="880e1-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="880e1-142">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="880e1-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="880e1-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="880e1-143">Requirements</span></span>



| <span data-ttu-id="880e1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="880e1-144">Requirement</span></span> | <span data-ttu-id="880e1-145">Valore</span><span class="sxs-lookup"><span data-stu-id="880e1-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="880e1-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="880e1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="880e1-147">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="880e1-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="880e1-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="880e1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="880e1-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="880e1-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="880e1-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="880e1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880e1-151">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="880e1-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




