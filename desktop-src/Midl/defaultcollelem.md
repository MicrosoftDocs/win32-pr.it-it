---
title: defaultcollelem (attributo)
description: L'attributo \ defaultcollelem \ contrassegna una proprietà come funzione di accesso per un elemento della raccolta predefinita.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- attributo MIDL di defaultcollelem
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046690"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem (attributo)

L'attributo **\[ defaultcollelem \]** contrassegna una proprietà come funzione di accesso per un elemento della raccolta predefinita.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano alla proprietà.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*nome proprietà* 
</dt> <dd>

Nome della proprietà.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Elenco di zero o più parametri associati alla proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ defaultcollelem \]** viene usato per l'ottimizzazione del codice® Visual BasicÂ. Se un membro di un'interfaccia o di un'interfaccia dispatch viene contrassegnato come funzione di accesso, la chiamata passerà direttamente a tale membro.

L'uso di **\[ defaultcollelem \]** deve essere coerente per una proprietà. Se ad esempio si usa l'attributo in una proprietà *Get* , deve essere presente anche in una proprietà *Let* .

### <a name="typeflags-representation"></a>Rappresentazione TYPEFLAGS

Presenza di FUNCFLAG \_ FDEFAULTCOLLELEM o VARFLAG \_ FDEFAULTCOLLELEM.

## <a name="examples"></a>Esempi

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 