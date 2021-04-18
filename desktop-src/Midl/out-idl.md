---
title: out (attributo)
description: L'attributo \ out \ identifica i parametri del puntatore restituiti dalla routine chiamata alla procedura chiamante (dal server al client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- attributo out MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299737"
---
# <a name="out-attribute"></a>out (attributo)

L' \[ attributo **out** \] identifica i parametri del puntatore restituiti dalla routine chiamata alla procedura chiamante (dal server al client).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono \[ [**callback**](callback.md) \] , \[ [**local**](local.md), \] l'attributo Pointer \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] e gli attributi Usage \[ [**String**](string.md) \] , \[ [**Ignore**](ignore.md) \] e \[ [**Context \_ handle**](context-handle.md) \] .

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*puntatore-dichiaratore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi appropriati per un tipo di parametro specificato. Gli attributi di parametro con l' \[ attributo **out** \] possono anche prendere l'attributo Directional \[ **out** \] . gli attributi di campo \[ [**First \_ sono**](first-is.md) \] , \[ [**Last \_ is**](last-is.md) \] , \[ [**length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**size \_ is**](size-is.md) \] e \[ [**Switch \_ Type**](switch-type.md), \] l'attributo Pointer \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] e l' \[ [**\_ handle**](context-handle.md) \] e la \[ [**stringa**](string.md)del contesto degli attributi Usage \] . L'attributo Usage \[ [**Ignore**](ignore.md) \] non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*dichiaratore* 
</dt> <dd>

Specifica i dichiaratori standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L' \[ attributo **out** \] indica che un parametro che funge da puntatore e i dati associati in memoria devono essere passati di nuovo dalla procedura chiamata alla procedura chiamante.

L' \[ attributo **out** \] deve essere un puntatore. I compilatori IDL DCE richiedono la presenza di un \* dichiaratore esplicito come puntatore nella dichiarazione di parametro. Microsoft IDL offre un'estensione che elimina questo requisito e consente una matrice o un tipo di puntatore definito in precedenza.

Un attributo correlato, \[ [**in**](in.md) \] , indica che il parametro viene passato dalla routine chiamante alla routine chiamata. Gli \[  \] attributi in e \[ **out** \] specificano la direzione in cui vengono passati i parametri. Un parametro può essere definito solo \[ **in**, solo in uscita o in uscita \] \[  \] \[   \] .

\[  \] Si presuppone che un parametro out-only non sia definito quando viene chiamata la procedura remota e che la memoria per l'oggetto venga allocata dal server. Poiché il puntatore/parametri di primo livello deve sempre puntare a una risorsa di archiviazione valida e pertanto non può essere **null**, \[ **out** \] non può essere applicato ai \[ puntatori [**univoci**](unique.md) \] o \[ [**ptr**](ptr.md) di primo livello \] . I parametri che corrispondono \[  \] a puntatori univoci o \[ **ptr** \] devono essere \[ [**in**](in.md) \] o \[ **in**, **out** \] Parameters.

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 