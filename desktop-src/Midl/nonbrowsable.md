---
title: nonbrowsable (attributo)
description: Usare l'attributo \ nonbrowsable \ per contrassegnare un'interfaccia o un membro dispatch che non deve essere visualizzato in un browser delle proprietà.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- attributo MIDL non esplorabile
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956395"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable (attributo)

Usare l'attributo **\[ nonbrowsable \]** per contrassegnare un'interfaccia o un membro dispatch che non deve essere visualizzato in un browser delle proprietà.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano alla proprietà.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Tipo dei dati restituiti dal metodo.

</dd> <dt>

*nome proprietà* 
</dt> <dd>

Nome della proprietà o del metodo.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Zero o più parametri da passare al metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune proprietà non devono essere visualizzate in un browser delle proprietà. Questo può essere dovuto al fatto che il recupero del valore richiede molto tempo. Nell'esempio viene impedito all'utente di tentare di recuperare la proprietà *count* , che restituisce il numero di righe nel dynaset. Questo numero può rappresentare i risultati di una query di dimensioni molto grandi.

Altre proprietà possono avere effetti imprevisti sul browser. Si consideri, ad esempio, un controllo con la proprietà "IsSelected" per indicare se il controllo è selezionato. Se "IsSelected" è impostato su false, un visualizzatore di proprietà basate sulla selezione esplorerà un oggetto diverso.

Si noti che una proprietà contrassegnata come non **\[ esplorabile \]** verrà comunque visualizzata in un Visualizzatore oggetti, che non Mostra i valori delle proprietà.

### <a name="typeflag-representation"></a>Rappresentazione TYPEFLAG

Presenza di FUNCFLAG \_ FNONBROWSABLE o VARFLAG \_ FNONBROWSABLE.

## <a name="examples"></a>Esempi

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 