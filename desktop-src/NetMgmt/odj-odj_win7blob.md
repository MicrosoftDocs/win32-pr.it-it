---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL Definition
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ab6f6582b23d6e65866ba1380b696fab6d8313578fab47ad5dda999b09a1caa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911596"
---
# <a name="odj_win7blob-structure"></a>ODJ_WIN7BLOB struttura

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

Contiene informazioni sul dominio aggiunto.

### <a name="dcinfo"></a>DcInfo

Contiene informazioni di denominazione e indirizzamento sul controller di dominio utilizzato per creare l'account computer Active Directory.

### <a name="options"></a>Opzioni

Deve essere impostato su zero.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)

[**INFORMAZIONI SUL DOMINIO \_ \_ DNS DEI CRITERI \_ ODJ \_**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



