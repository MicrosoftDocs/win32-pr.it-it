---
description: 'TcpIp_V1_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1 classe
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
ms.openlocfilehash: 831dfdc228e2c8e128f328784046e833b0b45a39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105759"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="f84fb-104">Classe \_ \_ TypeGroup1 TcpIp V1</span><span class="sxs-lookup"><span data-stu-id="f84fb-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="f84fb-105">Questa classe è la classe del tipo di evento per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f84fb-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="f84fb-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f84fb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f84fb-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f84fb-108">Members</span><span class="sxs-lookup"><span data-stu-id="f84fb-108">Members</span></span>

<span data-ttu-id="f84fb-109">La **classe \_ \_ TypeGroup1 TcpIp V1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f84fb-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f84fb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f84fb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f84fb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f84fb-111">Properties</span></span>

<span data-ttu-id="f84fb-112">La **classe \_ \_ TypeGroup1 TcpIp V1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f84fb-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f84fb-113">daddr</span><span class="sxs-lookup"><span data-stu-id="f84fb-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-114">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="f84fb-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-116">Qualificatori: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="f84fb-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-117">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f84fb-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f84fb-118">dport</span><span class="sxs-lookup"><span data-stu-id="f84fb-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-119">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="f84fb-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-121">Qualificatori: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="f84fb-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-122">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f84fb-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="f84fb-123">PID</span><span class="sxs-lookup"><span data-stu-id="f84fb-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f84fb-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-126">Qualificatori: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="f84fb-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-127">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="f84fb-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="f84fb-128">saddr</span><span class="sxs-lookup"><span data-stu-id="f84fb-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-129">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="f84fb-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-131">Qualificatori: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="f84fb-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-132">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="f84fb-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f84fb-133">size</span><span class="sxs-lookup"><span data-stu-id="f84fb-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f84fb-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-136">Qualificatori: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="f84fb-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-137">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f84fb-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f84fb-138">sport</span><span class="sxs-lookup"><span data-stu-id="f84fb-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84fb-139">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="f84fb-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f84fb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84fb-141">Qualificatori: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="f84fb-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f84fb-142">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="f84fb-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f84fb-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f84fb-143">Requirements</span></span>



| <span data-ttu-id="f84fb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f84fb-144">Requirement</span></span> | <span data-ttu-id="f84fb-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f84fb-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f84fb-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f84fb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f84fb-147">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f84fb-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f84fb-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f84fb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f84fb-149">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f84fb-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f84fb-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f84fb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84fb-151">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f84fb-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




