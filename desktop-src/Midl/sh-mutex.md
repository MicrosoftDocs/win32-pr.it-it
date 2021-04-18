---
title: parola chiave sh_mutex
description: La \_ parola chiave \ SH mutex \ specifica che l'oggetto di sistema è un handle per un mutex.
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
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321026"
---
# <a name="sh_mutex-keyword"></a>SH \_ mutex (parola chiave)

La parola chiave del **\_ mutex SH** specifica che un oggetto `system_handle` include un handle per un mutex.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a>Parametri

Questa parola chiave è un parametro per [**system_handle**](system-handle.md).

La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* . Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Commenti

Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.

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
| Client minimo supportato | Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393) |
| Server minimo supportato | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Oggetti mutex](../sync/mutex-objects.md)
</dt> <dt>

[Sicurezza e diritti di accesso degli oggetti di sincronizzazione](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateMutex** (funzione)](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**CreateMutexEx** (funzione)](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>