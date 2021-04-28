---
description: 'UdpIp_Fail classe: questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: UdpIp_Fail classe
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
ms.openlocfilehash: f923f26e1371d11e27bfd58bcb69c053bfb5f1a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105509"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="f413c-104">Classe UdpIp \_ Fail</span><span class="sxs-lookup"><span data-stu-id="f413c-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="f413c-105">Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f413c-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="f413c-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f413c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f413c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f413c-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="f413c-108">Members</span><span class="sxs-lookup"><span data-stu-id="f413c-108">Members</span></span>

<span data-ttu-id="f413c-109">La **classe UdpIp \_ Fail** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f413c-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="f413c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f413c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f413c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f413c-111">Properties</span></span>

<span data-ttu-id="f413c-112">La **classe UdpIp \_ Fail** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f413c-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f413c-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="f413c-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f413c-114">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="f413c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f413c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f413c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f413c-116">Motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="f413c-116">Reason for the failure.</span></span> <span data-ttu-id="f413c-117">Può essere uno dei codici seguenti:</span><span class="sxs-lookup"><span data-stu-id="f413c-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="f413c-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERRORE \_ RISORSE \_ INSUFFICIENTI** (1)</span><span class="sxs-lookup"><span data-stu-id="f413c-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f413c-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERRORE \_ TROPPI \_ \_ INDIRIZZI** (2)</span><span class="sxs-lookup"><span data-stu-id="f413c-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f413c-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERRORE \_ \_L'INDIRIZZO ESISTE** (3)</span><span class="sxs-lookup"><span data-stu-id="f413c-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f413c-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ INDIRIZZO \_ NON VALIDO** (4)</span><span class="sxs-lookup"><span data-stu-id="f413c-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f413c-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERRORE \_ OTHER** (5)</span><span class="sxs-lookup"><span data-stu-id="f413c-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f413c-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERRORE \_ L'INDIRIZZO \_ \_ TIMEWAIT ESISTE** (6)</span><span class="sxs-lookup"><span data-stu-id="f413c-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f413c-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="f413c-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f413c-125">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="f413c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f413c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f413c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f413c-127">Identifica il protocollo.</span><span class="sxs-lookup"><span data-stu-id="f413c-127">Identifies the protocol.</span></span> <span data-ttu-id="f413c-128">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f413c-128">Can be one of the following values:</span></span>



| <span data-ttu-id="f413c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f413c-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="f413c-130">Significato</span><span class="sxs-lookup"><span data-stu-id="f413c-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="f413c-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f413c-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f413c-132">Famiglia protocollo IP versione 4 di indirizzi (IPv4).</span><span class="sxs-lookup"><span data-stu-id="f413c-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="f413c-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="f413c-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="f413c-134">Famiglia di indirizzi IPv6 (Internet Protocol versione 6).</span><span class="sxs-lookup"><span data-stu-id="f413c-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f413c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f413c-135">Requirements</span></span>



| <span data-ttu-id="f413c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f413c-136">Requirement</span></span> | <span data-ttu-id="f413c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f413c-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f413c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f413c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f413c-139">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f413c-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f413c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f413c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f413c-141">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f413c-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f413c-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f413c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f413c-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="f413c-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




