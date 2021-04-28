---
description: 'UdpIp_V1_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105409"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="3ffb9-104">Classe \_ \_ TypeGroup1 UdpIp V1</span><span class="sxs-lookup"><span data-stu-id="3ffb9-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="3ffb9-105">Questa classe è la classe del tipo di evento per gli eventi UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="3ffb9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffb9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ffb9-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="3ffb9-108">Members</span><span class="sxs-lookup"><span data-stu-id="3ffb9-108">Members</span></span>

<span data-ttu-id="3ffb9-109">La **classe \_ \_ TypeGroup1 UdpIp V1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ffb9-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="3ffb9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ffb9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ffb9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ffb9-111">Properties</span></span>

<span data-ttu-id="3ffb9-112">La **classe \_ \_ TypeGroup1 UdpIp V1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ffb9-113">daddr</span><span class="sxs-lookup"><span data-stu-id="3ffb9-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-114">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-116">Qualificatori: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="3ffb9-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-117">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3ffb9-118">dport</span><span class="sxs-lookup"><span data-stu-id="3ffb9-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-119">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-121">Qualificatori: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="3ffb9-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-122">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="3ffb9-123">PID</span><span class="sxs-lookup"><span data-stu-id="3ffb9-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-126">Qualificatori: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="3ffb9-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-127">Identificatore del processo associato alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="3ffb9-128">saddr</span><span class="sxs-lookup"><span data-stu-id="3ffb9-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-129">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-131">Qualificatori: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="3ffb9-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-132">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3ffb9-133">size</span><span class="sxs-lookup"><span data-stu-id="3ffb9-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-136">Qualificatori: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="3ffb9-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-137">Dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="3ffb9-138">sport</span><span class="sxs-lookup"><span data-stu-id="3ffb9-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffb9-139">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ffb9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffb9-141">Qualificatori: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="3ffb9-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="3ffb9-142">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="3ffb9-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ffb9-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ffb9-143">Requirements</span></span>



| <span data-ttu-id="3ffb9-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffb9-144">Requirement</span></span> | <span data-ttu-id="3ffb9-145">Valore</span><span class="sxs-lookup"><span data-stu-id="3ffb9-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ffb9-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffb9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffb9-147">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3ffb9-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3ffb9-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffb9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffb9-149">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ffb9-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ffb9-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ffb9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffb9-151">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="3ffb9-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="3ffb9-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




