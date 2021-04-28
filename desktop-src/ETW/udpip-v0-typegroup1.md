---
description: 'UdpIp_V0_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1 classe
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
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105499"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="82ab9-104">Classe \_ TypeGroup1 UdpIp V0 \_</span><span class="sxs-lookup"><span data-stu-id="82ab9-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="82ab9-105">Questa classe è la classe del tipo di evento per gli eventi UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="82ab9-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="82ab9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="82ab9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ab9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82ab9-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="82ab9-108">Members</span><span class="sxs-lookup"><span data-stu-id="82ab9-108">Members</span></span>

<span data-ttu-id="82ab9-109">La **classe \_ \_ TypeGroup1 UdpIp V0** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="82ab9-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="82ab9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82ab9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82ab9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82ab9-111">Properties</span></span>

<span data-ttu-id="82ab9-112">La **classe \_ \_ TypeGroup1 UdpIp V0** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="82ab9-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82ab9-113">contesto</span><span class="sxs-lookup"><span data-stu-id="82ab9-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-114">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="82ab9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-116">Qualificatori: WmiDataId(1), puntatore</span><span class="sxs-lookup"><span data-stu-id="82ab9-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-117">Identificatore del processo per l'oggetto Address che ha effettuato o ricevuto la richiesta.</span><span class="sxs-lookup"><span data-stu-id="82ab9-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-118">tasdr</span><span class="sxs-lookup"><span data-stu-id="82ab9-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-119">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="82ab9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-121">Qualificatori: WmiDataId(5), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="82ab9-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-122">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82ab9-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-123">dport</span><span class="sxs-lookup"><span data-stu-id="82ab9-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-124">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="82ab9-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-126">Qualificatori: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="82ab9-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-127">Numero di porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82ab9-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-128">dsize</span><span class="sxs-lookup"><span data-stu-id="82ab9-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-129">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="82ab9-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-131">Qualificatori: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="82ab9-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-132">Dimensioni del pacchetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82ab9-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-133">saddr</span><span class="sxs-lookup"><span data-stu-id="82ab9-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-134">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="82ab9-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-136">Qualificatori: WmiDataId(2), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="82ab9-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-137">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="82ab9-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-138">size</span><span class="sxs-lookup"><span data-stu-id="82ab9-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-139">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="82ab9-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-141">Qualificatori: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="82ab9-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-142">Dimensioni del pacchetto di origine.</span><span class="sxs-lookup"><span data-stu-id="82ab9-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="82ab9-143">sport</span><span class="sxs-lookup"><span data-stu-id="82ab9-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82ab9-144">Tipo di dati: **object**</span><span class="sxs-lookup"><span data-stu-id="82ab9-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82ab9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82ab9-146">Qualificatori: WmiDataId(3), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="82ab9-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="82ab9-147">Numero di porta di origine.</span><span class="sxs-lookup"><span data-stu-id="82ab9-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82ab9-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82ab9-148">Requirements</span></span>



| <span data-ttu-id="82ab9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ab9-149">Requirement</span></span> | <span data-ttu-id="82ab9-150">Valore</span><span class="sxs-lookup"><span data-stu-id="82ab9-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="82ab9-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82ab9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="82ab9-152">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="82ab9-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="82ab9-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82ab9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="82ab9-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="82ab9-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="82ab9-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82ab9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ab9-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="82ab9-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




