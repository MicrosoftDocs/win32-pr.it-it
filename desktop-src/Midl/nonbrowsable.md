---
title: nonbrowsable (attributo)
description: Usare l'attributo \ nonbrowsable\ per contrassegnare un membro di interfaccia o interfaccia dispatch che non deve essere visualizzato in un visualizzatore proprietà.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- attributo non esplorabile MIDL
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6349683c3a3c591752036d9a5e2995d368460a049a79d2e1cf4123beb2b0ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066951"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable (attributo)

Usare **\[ l'attributo \] nonbrowsable** per contrassegnare un membro di interfaccia o interfaccia dispatch che non deve essere visualizzato in un visualizzatore proprietà.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*property-attribute-list* 
</dt> <dd>

Altri attributi che si applicano alla proprietà .

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo dei dati restituiti dal metodo .

</dd> <dt>

*property-name* 
</dt> <dd>

Nome della proprietà o del metodo.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Zero o più parametri da passare al metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune proprietà non devono essere visualizzate in un visualizzatore proprietà. Ciò può essere dovuto al fatto che il recupero del valore potrebbe richiedere molto tempo. L'esempio impedisce all'utente di tentare di recuperare la *proprietà Count,* che restituisce il numero di righe nel dynaset. Questo numero può rappresentare i risultati di una query di dimensioni molto grandi.

Altre proprietà possono avere effetti imprevisti sul browser. Si consideri ad esempio un controllo con la proprietà "IsSelected" per indicare se il controllo è selezionato. Se l'opzione "IsSelected" è impostata su false, un browser delle proprietà basato sulla selezione esplora un oggetto diverso.

Si noti che una proprietà contrassegnata come **\[ non esplorabile \]** verrà comunque visualizzata in un visualizzatore oggetti, che non mostra i valori delle proprietà.

### <a name="typeflag-representation"></a>Rappresentazione del flag di tipo

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

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 