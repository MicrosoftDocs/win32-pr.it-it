---
title: OP_CERT_PFX_STORE
description: Definizione di OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300650"
---
# <a name="op_cert_pfx_store-structure"></a>Struttura OP_CERT_PFX_STORE

Contiene una struttura PFX serializzata.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Members

### <a name="ptemplatename"></a>pTemplateName

Deve essere impostato sul nome del modello di certificato utilizzato per creare il certificato.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contiene un valore dell'enumerazione [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

È necessario impostare l'URL del server dei criteri.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contiene un valore dell'enumerazione [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .

### <a name="ppolicyserverid"></a>pPolicyServerId

Contiene una stringa che identifica in modo univoco il server dei criteri

### <a name="cbpfx"></a>cbPfx

Contiene la dimensione di pPfx in byte.

### <a name="ppfx"></a>pPfx

Contiene una struttura PFX serializzata (vedere [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
