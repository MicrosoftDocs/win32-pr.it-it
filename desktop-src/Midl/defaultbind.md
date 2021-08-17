---
title: defaultbind (attributo)
description: L'attributo \ defaultbind\ indica la singola proprietà associabile che meglio rappresenta l'oggetto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- Attributo defaultbind MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807297"
---
# <a name="defaultbind-attribute"></a>defaultbind (attributo)

**\[ L'attributo \] defaultbind** indica la singola proprietà associabile che meglio rappresenta l'oggetto.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'intera interfaccia. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano alla funzione. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Returntype* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato **\[ l'attributo defaultbind. \]**

</dd> <dt>

*params* 
</dt> <dd>

Elenco di parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Anche le proprietà con **\[ l'attributo defaultbind \]** devono avere l'attributo **\[** [**associabile.**](bindable.md) **\]** Solo una proprietà in un'interfaccia o un'interfaccia dispatch può avere **\[ l'attributo defaultbind. \]**

Questo attributo viene usato dai contenitori che hanno un modello utente che prevede l'associazione a un oggetto anziché l'associazione a una proprietà di un oggetto. Un oggetto può supportare data binding ma non dispone di questo attributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 