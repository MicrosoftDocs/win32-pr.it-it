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
# <a name="odj_policy_dns_domain_info-structure"></a>Struttura ODJ_POLICY_DNS_DOMAIN_INFO

Contiene informazioni sul dominio e la foresta a cui deve essere aggiunto un client.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

### <a name="name"></a>Nome

Deve essere impostato su un nome di dominio NetBIOS.

### <a name="dnsdomainname"></a>DnsDomainName

Deve essere impostato su un nome di dominio in formato DNS.

### <a name="dnsforestname"></a>DnsForestName

Deve essere impostato su un nome di foresta in formato DNS.

### <a name="domainguid"></a>DomainGuid

Deve essere impostato sul GUID del dominio.

### <a name="sid"></a>Sid

Deve essere impostato sul SID del dominio.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_stringa Unicode \_ ODJ**](odj-odj_unicode_string.md)

[**\_SID ODJ**](odj-odj_sid.md)
