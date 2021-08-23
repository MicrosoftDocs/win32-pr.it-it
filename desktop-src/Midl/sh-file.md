---
title: sh_file parola chiave
description: La parola chiave \ sh \_ file\ specifica che l'oggetto di sistema è un handle per un file.
keywords:
- sh_file parola chiave MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 05b76ad772ca628a28677d9b0da06252d0fec70251a4a197d39b50b9760ef931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013629"
---
# <a name="sh_file-keyword"></a>Parola \_ chiave sh file

La **parola chiave sh \_ file** specifica che un `system_handle` oggetto contiene un handle per un file.

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
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
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
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

[Sicurezza dei file e diritti di accesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**Funzione DCompositionCreateSurfaceHandle**](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
