---
description: Questa classe è la classe del tipo di evento per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Classe UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968111"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="af5ac-104">\_Classe UdpIp V0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="af5ac-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="af5ac-105">Questa classe è la classe del tipo di evento per gli eventi UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="af5ac-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="af5ac-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="af5ac-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af5ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af5ac-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="af5ac-108">Members</span><span class="sxs-lookup"><span data-stu-id="af5ac-108">Members</span></span>

<span data-ttu-id="af5ac-109">La classe **UdpIp \_ V0 \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af5ac-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="af5ac-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af5ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af5ac-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af5ac-111">Properties</span></span>

<span data-ttu-id="af5ac-112">La classe **UdpIp \_ V0 \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af5ac-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af5ac-113">contesto</span><span class="sxs-lookup"><span data-stu-id="af5ac-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af5ac-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-116">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="af5ac-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-117">Identificatore del processo per l'oggetto Address che ha effettuato o ricevuto la richiesta.</span><span class="sxs-lookup"><span data-stu-id="af5ac-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-118">daddr</span><span class="sxs-lookup"><span data-stu-id="af5ac-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="af5ac-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-121">Qualificatori: WmiDataId (5), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="af5ac-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af5ac-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-123">dport</span><span class="sxs-lookup"><span data-stu-id="af5ac-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="af5ac-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-126">Qualificatori: WmiDataId (6), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="af5ac-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af5ac-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-128">dsize</span><span class="sxs-lookup"><span data-stu-id="af5ac-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af5ac-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-131">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="af5ac-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-132">Dimensioni del pacchetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af5ac-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-133">saddr</span><span class="sxs-lookup"><span data-stu-id="af5ac-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="af5ac-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-136">Qualificatori: WmiDataId (2), Extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="af5ac-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="af5ac-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-138">size</span><span class="sxs-lookup"><span data-stu-id="af5ac-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af5ac-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-141">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="af5ac-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-142">Dimensioni del pacchetto di origine.</span><span class="sxs-lookup"><span data-stu-id="af5ac-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="af5ac-143">Sport</span><span class="sxs-lookup"><span data-stu-id="af5ac-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af5ac-144">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="af5ac-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af5ac-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af5ac-146">Qualificatori: WmiDataId (3), Extension ("Port")</span><span class="sxs-lookup"><span data-stu-id="af5ac-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="af5ac-147">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="af5ac-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af5ac-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af5ac-148">Requirements</span></span>



| <span data-ttu-id="af5ac-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="af5ac-149">Requirement</span></span> | <span data-ttu-id="af5ac-150">Valore</span><span class="sxs-lookup"><span data-stu-id="af5ac-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="af5ac-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af5ac-151">Minimum supported client</span></span><br/> | <span data-ttu-id="af5ac-152">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af5ac-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="af5ac-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af5ac-153">Minimum supported server</span></span><br/> | <span data-ttu-id="af5ac-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af5ac-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="af5ac-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af5ac-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5ac-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="af5ac-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




