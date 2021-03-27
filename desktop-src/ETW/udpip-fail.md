---
description: Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: Classe UdpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: aef0194d296395501500022bf4cae8b9c8a8f188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980903"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="55a77-104">\_Classe UdpIp Fail</span><span class="sxs-lookup"><span data-stu-id="55a77-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="55a77-105">Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="55a77-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="55a77-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="55a77-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55a77-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="55a77-108">Members</span><span class="sxs-lookup"><span data-stu-id="55a77-108">Members</span></span>

<span data-ttu-id="55a77-109">La classe **UdpIp \_ Fail** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55a77-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="55a77-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55a77-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55a77-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55a77-111">Properties</span></span>

<span data-ttu-id="55a77-112">La classe **UdpIp \_ Fail** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55a77-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55a77-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="55a77-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a77-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55a77-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55a77-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55a77-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55a77-116">Motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="55a77-116">Reason for the failure.</span></span> <span data-ttu-id="55a77-117">Può essere uno dei seguenti codici:</span><span class="sxs-lookup"><span data-stu-id="55a77-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="55a77-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Errore \_ \_Risorse insufficienti** (1)</span><span class="sxs-lookup"><span data-stu-id="55a77-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="55a77-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Errore \_ TROPPi \_ \_ indirizzi** (2)</span><span class="sxs-lookup"><span data-stu-id="55a77-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="55a77-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Errore \_ INDIRIZZO \_ esistente** (3)</span><span class="sxs-lookup"><span data-stu-id="55a77-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="55a77-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Errore \_ \_Indirizzo non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="55a77-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="55a77-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Errore \_ ALTRO** (5)</span><span class="sxs-lookup"><span data-stu-id="55a77-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="55a77-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Errore \_ \_Indirizzo TIMEWAIT \_ esistente** (6)</span><span class="sxs-lookup"><span data-stu-id="55a77-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55a77-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="55a77-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a77-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55a77-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55a77-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55a77-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55a77-127">Identifica il protocollo.</span><span class="sxs-lookup"><span data-stu-id="55a77-127">Identifies the protocol.</span></span> <span data-ttu-id="55a77-128">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="55a77-128">Can be one of the following values:</span></span>



| <span data-ttu-id="55a77-129">Valore</span><span class="sxs-lookup"><span data-stu-id="55a77-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="55a77-130">Significato</span><span class="sxs-lookup"><span data-stu-id="55a77-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="55a77-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="55a77-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="55a77-132">Famiglia di indirizzi protocollo Internet versione 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="55a77-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="55a77-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="55a77-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="55a77-134">Famiglia di indirizzi protocollo Internet versione 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="55a77-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55a77-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55a77-135">Requirements</span></span>



| <span data-ttu-id="55a77-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a77-136">Requirement</span></span> | <span data-ttu-id="55a77-137">Valore</span><span class="sxs-lookup"><span data-stu-id="55a77-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55a77-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a77-138">Minimum supported client</span></span><br/> | <span data-ttu-id="55a77-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55a77-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55a77-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a77-140">Minimum supported server</span></span><br/> | <span data-ttu-id="55a77-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55a77-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55a77-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55a77-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a77-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="55a77-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




