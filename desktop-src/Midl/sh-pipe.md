---
title: sh_pipe parola chiave
description: La parola chiave \ sh \_ pipe\ specifica che l'oggetto di sistema è un handle per una pipe.
keywords:
- sh_pipe parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 15bee0e34525d83af10e5c42199116dc6080a6a7b7f4e2af3de565f62a9c6a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383346"
---
# <a name="sh_pipe-keyword"></a>Parola \_ chiave sh pipe

La **parola chiave sh \_ pipe** specifica che un `system_handle` oggetto contiene un handle per una pipe.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Informazioni sulle pipe](../ipc/about-pipes.md)
</dt> <dt>

[Sicurezza dei file e diritti di accesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**Funzione CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**Funzione CreateNamedPipe**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
