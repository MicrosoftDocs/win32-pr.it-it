---
description: 'TcpIp_Fail: questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105849"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="3686b-104">Classe TcpIp \_ Fail</span><span class="sxs-lookup"><span data-stu-id="3686b-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="3686b-105">Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3686b-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="3686b-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3686b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3686b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3686b-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="3686b-108">Members</span><span class="sxs-lookup"><span data-stu-id="3686b-108">Members</span></span>

<span data-ttu-id="3686b-109">La **classe TcpIp \_ Fail** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3686b-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="3686b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3686b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3686b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3686b-111">Properties</span></span>

<span data-ttu-id="3686b-112">La **classe TcpIp \_ Fail** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3686b-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3686b-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="3686b-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3686b-114">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="3686b-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3686b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3686b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3686b-116">Motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="3686b-116">Reason for the failure.</span></span> <span data-ttu-id="3686b-117">Può essere uno dei codici seguenti:</span><span class="sxs-lookup"><span data-stu-id="3686b-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="3686b-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERRORE \_ RISORSE \_ INSUFFICIENTI** (1)</span><span class="sxs-lookup"><span data-stu-id="3686b-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3686b-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERRORE \_ TROPPI \_ \_ INDIRIZZI** (2)</span><span class="sxs-lookup"><span data-stu-id="3686b-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3686b-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERRORE \_ ADDRESS \_ EXISTS** (3)</span><span class="sxs-lookup"><span data-stu-id="3686b-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3686b-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ INDIRIZZO \_ NON VALIDO** (4)</span><span class="sxs-lookup"><span data-stu-id="3686b-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3686b-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERRORE \_ OTHER** (5)</span><span class="sxs-lookup"><span data-stu-id="3686b-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3686b-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERRORE \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)</span><span class="sxs-lookup"><span data-stu-id="3686b-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3686b-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="3686b-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3686b-125">Tipo di dati: **uint16**</span><span class="sxs-lookup"><span data-stu-id="3686b-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3686b-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3686b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3686b-127">Identifica il protocollo.</span><span class="sxs-lookup"><span data-stu-id="3686b-127">Identifies the protocol.</span></span> <span data-ttu-id="3686b-128">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3686b-128">Can be one of the following values:</span></span>



| <span data-ttu-id="3686b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3686b-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="3686b-130">Significato</span><span class="sxs-lookup"><span data-stu-id="3686b-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="3686b-131"><dt>**Af \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3686b-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="3686b-132">Famiglia protocollo IP versione 4 indirizzi di rete (IPv4).</span><span class="sxs-lookup"><span data-stu-id="3686b-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="3686b-133"><dt>**Af \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="3686b-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="3686b-134">Famiglia di indirizzi IPv6 (Internet Protocol versione 6).</span><span class="sxs-lookup"><span data-stu-id="3686b-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3686b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3686b-135">Requirements</span></span>



| <span data-ttu-id="3686b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3686b-136">Requirement</span></span> | <span data-ttu-id="3686b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3686b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3686b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3686b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3686b-139">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3686b-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3686b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3686b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3686b-141">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3686b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3686b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3686b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3686b-143">**Tcpip**</span><span class="sxs-lookup"><span data-stu-id="3686b-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




