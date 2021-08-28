---
title: sh_event parola chiave
description: La parola chiave \ sh \_ event\ specifica che l'oggetto di sistema è un handle per un evento.
keywords:
- sh_event parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b2f489c27d32c40f80cef326b99131158df92cad2183cee1dc5a3dd74310cf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013649"
---
# <a name="sh_event-keyword"></a>Parola chiave \_ event sh

La **parola \_ chiave dell'evento sh** specifica che un oggetto contiene un handle per un `system_handle` evento.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a>Parametri

Questa parola chiave è un parametro per [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) contiene anche informazioni dettagliate sull'uso facoltativo del *parametro access-rights.* Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` in base alle specifiche della funzione [ **DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Commenti

Per usare questa parola chiave con l'attributo , il flag deve essere impostato `system_handle` `-target` su `NT100` (o superiore) durante l'esecuzione midl.exe.

## <a name="examples"></a>Esempio

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
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

[Oggetti evento](../sync/event-objects.md)
</dt> <dt>

[Sicurezza degli oggetti di sincronizzazione e diritti di accesso](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Funzione CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**Funzione CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
