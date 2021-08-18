---
title: sh_reg_key parola chiave
description: La parola chiave \ sh \_ reg \_ key\ specifica che l'oggetto di sistema è un handle per una chiave del Registro di sistema.
keywords:
- sh_reg_key parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 321745879645f3f6346d1e4c5ba7047df203430041f2d8903b8ff506229bb1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013609"
---
# <a name="sh_reg_key-keyword"></a>Parola \_ chiave sh reg \_

La **parola chiave sh reg \_ \_ key** specifica che un oggetto `system_handle` contiene un handle per una chiave del Registro di sistema.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a>Parametri

Questa parola chiave è un parametro per [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) contiene anche informazioni dettagliate sull'uso facoltativo del *parametro access-rights.* Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della funzione [ **DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Commenti

Per usare questa parola chiave con l'attributo , il flag deve essere impostato su (o versione successiva) quando si `system_handle` `-target` esegue `NT100` midl.exe.

## <a name="examples"></a>Esempio

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registro](../sysinfo/registry.md)
</dt> <dt>

[Sicurezza e diritti di accesso delle chiavi del Registro di sistema](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[**Funzione RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
