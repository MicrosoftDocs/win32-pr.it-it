---
title: defaultvtable (attributo)
description: L'attributo \ defaultvtable\ definisce un'interfaccia come interfaccia Vtable predefinita.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- attributo defaultvtable MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffebc5907072f7fdfc539bbc2b06bf1e4ad9fb667826c6c3c5a96121b106326e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067341"
---
# <a name="defaultvtable-attribute"></a>defaultvtable (attributo)

**\[ L'attributo \] defaultvtable** definisce un'interfaccia come interfaccia Vtable predefinita.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Altri attributi che si applicano alla classe . Gli **\[** [**attributi di**](source.md) **\]** origine e **\[** [**uuid**](uuid.md) sono **\]** obbligatori.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Nome della classe.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Elenco di interfacce per la classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'interfaccia Vtable predefinita non può essere un'interfaccia dispatch, ma deve essere un'interfaccia duale o Vtable o un'interfaccia. Se l'interfaccia è un'interfaccia duale, i sink possono presupporre che riceveranno eventi tramite Vtable.

Una classe può essere sia un'interfaccia di origine predefinita che un'interfaccia di origine Vtable predefinita, come illustrato nell'esempio. In questo caso un sink di consulenza deve usare IDISPATCH IID per ricevere eventi di invio e usare l'identificatore di interfaccia \_ per ricevere eventi Vtable.

### <a name="typeflag-representation"></a>Rappresentazione typeflag

Presenza di IMPLTYPEFLAG \_ FDEFAULTVTABLE.

## <a name="examples"></a>Esempi

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**fonte**](source.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 