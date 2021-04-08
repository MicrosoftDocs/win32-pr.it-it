---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Definizione di ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734690"
---
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="ebf38-103">Struttura ODJ_POLICY_DNS_DOMAIN_INFO</span><span class="sxs-lookup"><span data-stu-id="ebf38-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="ebf38-104">Contiene informazioni sul dominio e la foresta a cui deve essere aggiunto un client.</span><span class="sxs-lookup"><span data-stu-id="ebf38-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebf38-105">Syntax</span></span>

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a><span data-ttu-id="ebf38-106">Members</span><span class="sxs-lookup"><span data-stu-id="ebf38-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="ebf38-107">Nome</span><span class="sxs-lookup"><span data-stu-id="ebf38-107">Name</span></span>

<span data-ttu-id="ebf38-108">Deve essere impostato su un nome di dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="ebf38-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="ebf38-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="ebf38-109">DnsDomainName</span></span>

<span data-ttu-id="ebf38-110">Deve essere impostato su un nome di dominio in formato DNS.</span><span class="sxs-lookup"><span data-stu-id="ebf38-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="ebf38-111">DnsForestName</span><span class="sxs-lookup"><span data-stu-id="ebf38-111">DnsForestName</span></span>

<span data-ttu-id="ebf38-112">Deve essere impostato su un nome di foresta in formato DNS.</span><span class="sxs-lookup"><span data-stu-id="ebf38-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="ebf38-113">DomainGuid</span><span class="sxs-lookup"><span data-stu-id="ebf38-113">DomainGuid</span></span>

<span data-ttu-id="ebf38-114">Deve essere impostato sul GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="ebf38-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="ebf38-115">Sid</span><span class="sxs-lookup"><span data-stu-id="ebf38-115">Sid</span></span>

<span data-ttu-id="ebf38-116">Deve essere impostato sul SID del dominio.</span><span class="sxs-lookup"><span data-stu-id="ebf38-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebf38-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebf38-117">See also</span></span>

[<span data-ttu-id="ebf38-118">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="ebf38-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="ebf38-119">**\_stringa Unicode \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="ebf38-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="ebf38-120">**\_SID ODJ**</span><span class="sxs-lookup"><span data-stu-id="ebf38-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
