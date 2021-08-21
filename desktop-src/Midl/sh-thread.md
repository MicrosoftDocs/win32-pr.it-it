---
title: sh_thread parola chiave
description: La parola chiave \sh \_ thread\ specifica che l'oggetto di sistema è un handle per un thread.
keywords:
- sh_thread parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5cd3f5458e54ccd266f5ef0920b1cc79e1c0b42e35fac51f7ac353d22409aaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641333"
---
# <a name="sh_thread-keyword"></a>Parola \_ chiave sh thread

La **parola chiave sh \_ thread** specifica che un `system_handle` oggetto contiene un handle per un thread.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
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
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
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

[Informazioni su processi e thread](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Sicurezza dei thread e diritti di accesso](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[**Funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[**Funzione OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>