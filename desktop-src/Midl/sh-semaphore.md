---
title: sh_semaphore parola chiave
description: La parola chiave \ sh \_ semaphore\ specifica che l'oggetto di sistema è un handle per un semaforo.
keywords:
- sh_semaphore parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a48d0b085f3653679c7399ad0f234e7b7a1ecf1b1532480c003923967ac4830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383221"
---
# <a name="sh_semaphore-keyword"></a>Parola chiave sh \_ semaphore

La **parola chiave sh \_ semaphore** specifica che un oggetto `system_handle` contiene un handle per un semaforo.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[Oggetti semaforo](../sync/semaphore-objects.md)
</dt> <dt>

[Sicurezza degli oggetti di sincronizzazione e diritti di accesso](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Funzione CreateSemaphore**](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**Funzione CreateSemaphoreEx**](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
