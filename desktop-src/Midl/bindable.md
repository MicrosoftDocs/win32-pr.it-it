---
title: bindable (attributo)
description: L'attributo \ Bindable \ indica che la proprietà supporta data binding.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- attributo MIDL associabile
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299660"
---
# <a name="bindable-attribute"></a>bindable (attributo)

L'attributo **\[ associabile \]** indica che la proprietà supporta data binding.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica zero o più attributi che si applicano al prototipo di funzione per una proprietà o un metodo in un'interfaccia o in un' [**interfaccia**](interface.md) [**Dispatch**](dispinterface.md). Gli attributi seguenti sono validi: [**\[ helpstring \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)e [**\[ vararg \]**](vararg.md). Se viene specificato **vararg** , l'ultimo parametro deve essere una matrice sicura di tipo Variant. Separare più attributi con virgole.

</dd> <dt>

*returnType* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ associabile \]** .

</dd> <dt>

*params* 
</dt> <dd>

Elenco dei parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Grazie al supporto di data binding, l'attributo **\[ associabile \]** consente al client di ricevere notifiche ogni volta che una proprietà modifica il valore. Se si desidera che il client riceva una notifica di modifiche imminenti a una proprietà, utilizzare l'attributo [**\[ requestedit \]**](requestedit.md) .

Poiché l'attributo **\[ associabile \]** si riferisce alla proprietà nel suo complesso, è necessario specificare ogni volta che la proprietà è definita. Pertanto, è necessario specificare l'attributo sia nella funzione di accesso alla proprietà che nella funzione di impostazione della proprietà.

### <a name="flags"></a>Flags

FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 