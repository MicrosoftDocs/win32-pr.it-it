---
title: parola chiave sh_pipe
description: La \_ parola chiave \ SH pipe \ specifica che l'oggetto di sistema è un handle per una pipe.
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
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320234"
---
# <a name="sh_pipe-keyword"></a>\_parola chiave pipe SH

La parola chiave della **\_ pipe SH** specifica che un oggetto `system_handle` include un handle per una pipe.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Informazioni sulle pipe](../ipc/about-pipes.md)
</dt> <dt>

[Sicurezza file e diritti di accesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**Non** (funzione)](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**CreateNamedPipe** (funzione)](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
