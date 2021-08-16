---
title: sh_mutex parola chiave
description: La parola chiave \ sh \_ mutex\ specifica che l'oggetto di sistema è un handle per un mutex.
keywords:
- sh_mutex parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a355eb0121875e186a485ee6f7f96519a4fa0cfb1c75c806e1baea895691c914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641366"
---
# <a name="sh_mutex-keyword"></a>Parola \_ chiave mutex sh

La **parola chiave sh \_ mutex** specifica che un oggetto `system_handle` contiene un handle per un mutex.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a>Parametri

Questa parola chiave è un parametro per [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) documentazione contiene anche informazioni dettagliate sull'uso facoltativo del *parametro access-rights.* Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della funzione [ **DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Commenti

Per usare questa parola chiave con l'attributo , il flag deve essere impostato su (o versione successiva) quando si `system_handle` `-target` esegue `NT100` midl.exe.

## <a name="examples"></a>Esempio

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
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

[Oggetti Mutex](../sync/mutex-objects.md)
</dt> <dt>

[Sicurezza degli oggetti di sincronizzazione e diritti di accesso](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Funzione CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**Funzione CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>