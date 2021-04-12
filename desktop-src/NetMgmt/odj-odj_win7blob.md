---
title: ODJ_WIN7BLOB
description: Definizione di ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104339563"
---
# <a name="odj_win7blob-structure"></a>Struttura ODJ_WIN7BLOB

Contiene le informazioni di base necessarie per aggiungere un client a un dominio.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Members

### <a name="lpdomain"></a>lpDomain

Deve essere impostato sul nome di dominio.

### <a name="lpmachinename"></a>lpMachineName

Deve essere impostato sul nome del computer.

### <a name="lpmachinepassword"></a>lpMachinePassword

Deve essere impostato su una password non crittografata per l'account del computer identificato da lpMachineName

### <a name="dnsdomaininfo"></a>DnsDomainInfo

Contiene informazioni sul dominio da unire.

### <a name="dcinfo"></a>DcInfo

Contiene informazioni sulla denominazione e sull'indirizzamento del controller di dominio utilizzato per creare l'account del computer Active Directory.

### <a name="options"></a>Opzioni

Deve essere impostato su zero.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_informazioni sul \_ \_ dominio DNS del criterio \_ ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



