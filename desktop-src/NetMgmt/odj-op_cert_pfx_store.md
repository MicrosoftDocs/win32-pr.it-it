---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL Definition
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911541"
---
# <a name="op_cert_pfx_store-structure"></a>OP_CERT_PFX_STORE struttura

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

Deve essere impostato sul nome del modello di certificato usato per creare il certificato.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contiene un valore [**dell'enumerazione X509PrivateKeyExportFlags.**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags)

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Deve essere impostato l'URL del server dei criteri.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contiene un valore [**dell'enumerazione PolicyServerUrlFlags.**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags)

### <a name="ppolicyserverid"></a>pPolicyServerId

Contiene una stringa che identifica in modo univoco il server dei criteri

### <a name="cbpfx"></a>cbPfx

Contiene le dimensioni di pPfx in byte.

### <a name="ppfx"></a>pPfx

Contiene una struttura PFX serializzata (vedere [**RFC 7292).**](https://tools.ietf.org/html/rfc7292)

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)
