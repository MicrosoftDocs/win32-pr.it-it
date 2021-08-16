---
title: displaybind (attributo)
description: L'attributo \ displaybind\ indica una proprietà che deve essere visualizzata all'utente come associabile.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- Attributo displaybind MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f331ee62128501237671d01524c0f74df5ebc3b9da37dbf6ba3f71f9a5df460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384605"
---
# <a name="displaybind-attribute"></a>displaybind (attributo)

**\[ L'attributo \] displaybind** indica una proprietà che deve essere visualizzata all'utente come associabile.

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco facoltativo di attributi di interfaccia.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo restituito dalla funzione.

</dd> <dt>

*Returntype* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato **\[ l'attributo displaybind. \]**

</dd> <dt>

*params* 
</dt> <dd>

Elenco di parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Anche le proprietà con **\[ l'attributo displaybind \]** devono avere l'attributo **\[** [**associabile.**](bindable.md) **\]** Un oggetto può supportare data binding ma non dispone di questo attributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 