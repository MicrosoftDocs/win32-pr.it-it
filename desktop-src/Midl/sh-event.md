---
title: parola chiave sh_event
description: La \_ parola chiave \ SH Event \ specifica che l'oggetto di sistema è un handle per un evento.
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
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320237"
---
# <a name="sh_event-keyword"></a>\_parola chiave evento SH

La parola chiave dell' **\_ evento SH** specifica che un oggetto `system_handle` include un handle per un evento.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
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

[Oggetti evento](../sync/event-objects.md)
</dt> <dt>

[Sicurezza e diritti di accesso degli oggetti di sincronizzazione](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateEvent** (funzione)](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**CreateEventEx** (funzione)](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
