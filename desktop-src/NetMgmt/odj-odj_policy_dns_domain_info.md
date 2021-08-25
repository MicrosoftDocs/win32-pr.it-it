---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO definizione IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d0a83ccade72a11449ca0cc9b35b9fc58e9c53d48f8248a9f6074cdb087cc0c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911597"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO struttura

Contiene informazioni sul dominio e sulla foresta a cui deve essere aggiunto un client.

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

Deve essere impostato su un nome di dominio Netbios.

### <a name="dnsdomainname"></a>DnsDomainName

Deve essere impostato su un nome di dominio in formato DNS.

### <a name="dnsforestname"></a>DnsForestName

Deve essere impostato su un nome di foresta in formato DNS.

### <a name="domainguid"></a>DomainGuid

Deve essere impostato sul GUID di dominio.

### <a name="sid"></a>Sid

Deve essere impostato sul SID del dominio.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)

[**STRINGA \_ UNICODE \_ ODJ**](odj-odj_unicode_string.md)

[**ODJ \_ SID**](odj-odj_sid.md)
