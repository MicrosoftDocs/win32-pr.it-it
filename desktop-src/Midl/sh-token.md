---
title: sh_token parola chiave
description: La parola chiave \ sh \_ token\ specifica che l'oggetto di sistema è un handle per un token.
keywords:
- sh_token parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8305a8073d03eb90bbd214f1b56cb1174ffef66953bb170fb7f28ebf1b84d35c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066773"
---
# <a name="sh_token-keyword"></a>Parola \_ chiave token sh

La **parola chiave del \_ token sh** specifica che un oggetto contiene un handle per un `system_handle` token.

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
```

## <a name="parameters"></a>Parametri

Questa parola chiave è un parametro per [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) contiene anche informazioni dettagliate sull'uso facoltativo del *parametro access-rights.* Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` in base alle specifiche della funzione [ **DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Commenti

Per usare questa parola chiave con l'attributo , il flag deve essere impostato su `system_handle` `-target` `NT100` (o superiore) durante l'esecuzione midl.exe.

## <a name="examples"></a>Esempio

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
}
```

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
|-|-|
| Client minimo supportato | Windows 10 Aggiornamento dell'anniversario (versione 1607, build 14393) |
| Server minimo supportato | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Token di accesso](../secauthz/access-tokens.md)
</dt> <dt>

[Diritti di accesso per Access-Token oggetti](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
