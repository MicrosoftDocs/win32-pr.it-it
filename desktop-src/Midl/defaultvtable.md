---
title: defaultvtable (attributo)
description: L'attributo \ defaultvtable \ definisce un'interfaccia come interfaccia vtable predefinita.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- attributo MIDL di defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872461"
---
# <a name="defaultvtable-attribute"></a>defaultvtable (attributo)

L'attributo **\[ defaultvtable \]** definisce un'interfaccia come l'interfaccia vtable predefinita.

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

*coclass-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano alla classe. Gli **\[** attributi [**source**](source.md) **\]** e **\[** [**UUID**](uuid.md) **\]** sono obbligatori.

</dd> <dt>

*coclass-nome* 
</dt> <dd>

Nome della classe.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Elenco di interfacce per la classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'interfaccia vtable predefinita non può essere un'interfaccia dispatch, ma deve essere un'interfaccia dual o vtable o. Se l'interfaccia è un'interfaccia duale, i sink possono presumere che ricevano gli eventi tramite vtable.

Una classe può essere sia un'interfaccia di origine predefinita che un'interfaccia di origine vtable predefinita, come illustrato nell'esempio. In questo caso, un sink di notifica deve utilizzare \_ l'IID IDISPATCH per ricevere eventi di invio e utilizzare l'identificatore di interfaccia per ricevere eventi vtable.

### <a name="typeflag-representation"></a>Rappresentazione TYPEFLAG

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

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**origine**](source.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 