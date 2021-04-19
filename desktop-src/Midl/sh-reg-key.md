---
title: parola chiave sh_reg_key
description: La parola chiave \ sh \_ reg \_ Key \ specifica che l'oggetto di sistema è un handle per una chiave del registro di sistema.
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
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320242"
---
# <a name="sh_reg_key-keyword"></a>\_ \_ parola chiave del codice SH reg

La parola chiave del **\_ \_ codice SH reg** specifica che un oggetto `system_handle` include un handle per una chiave del registro di sistema.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
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
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registro](../sysinfo/registry.md)
</dt> <dt>

[Diritti di accesso e sicurezza della chiave del registro di sistema](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[**RegOpenKeyEx** (funzione)](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
