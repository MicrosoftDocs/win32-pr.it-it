---
title: out (attributo)
description: L'attributo \ out\ identifica i parametri del puntatore restituiti dalla procedura chiamata alla procedura chiamante (dal server al client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- Attributo out MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32bdbd18c6412f943a124a62badb9c154fa9aeb64573919970ffc1dc4af17798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066801"
---
# <a name="out-attribute"></a>out (attributo)

L'attributo out identifica i parametri del puntatore restituiti dalla procedura chiamata \[  \] alla procedura chiamante (dal server al client).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo puntatore ref , unique o ptr e la stringa degli attributi di utilizzo \[ [](callback.md) \] \[ [](local.md) \] \[ [](ref.md) \] \[ [](unique.md) \] , \[ [](ptr.md) \] \[ [](string.md) \] \[ [**ignorano**](ignore.md) \] e \[ [**l'handle di \_ contesto**](context-handle.md) \] .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di \_ base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*pointer-declarator* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore di puntatore usato in C; viene costruito \* dall'designatore , dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Specifica zero o più attributi appropriati per un tipo di parametro specificato. Gli attributi di parametro con l'attributo out possono anche rimuovere l'attributo direzionale . Gli attributi del campo sono , last è , length è , max è , size è e il tipo switch , l'attributo puntatore ref , unique o \[  \] \[  \] \[ [**\_**](first-is.md) \] \[ [**\_**](last-is.md) \] \[ [**\_**](length-is.md) \] \[ [**\_**](max-is.md) \] \[ [**\_**](size-is.md) \] \[ [**\_**](switch-type.md) \] \[ [](ref.md) \] \[ [](unique.md) \] \[ [**ptr**](ptr.md) \] e \[ [**\_ l'handle**](context-handle.md) \] \[ [](string.md) \] di contesto e la stringa degli attributi di utilizzo . L'attributo \[ [**di utilizzo ignore**](ignore.md) \] non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*Dichiaratore* 
</dt> <dd>

Specifica i dichiaratori standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers) Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo out indica che un parametro che funge da puntatore e i dati associati in memoria devono essere passati nuovamente dalla routine chiamata \[  \] alla routine chiamante.

\[ **L'attributo out** \] deve essere un puntatore. I compilatori IDL DCE richiedono la presenza di un \* esplicito come dichiaratore di puntatore nella dichiarazione di parametro. Microsoft IDL offre un'estensione che elimina questo requisito e consente una matrice o un tipo di puntatore definito in precedenza.

Un attributo correlato, \[ [**in**](in.md) \] , indica che il parametro viene passato dalla routine chiamante alla routine chiamata. Gli \[ **attributi in** \] e \[ **out** \] specificano la direzione in cui vengono passati i parametri. Un parametro può essere definito come \[ **in** \] -only, \[ **out** \] -only o \[ **in**, **out** \] .

Si presuppone che un parametro out-only non sia definito quando viene chiamata la procedura remota e la memoria per l'oggetto viene \[  \] allocata dal server. Poiché i puntatori/parametri di primo livello devono sempre puntare a una risorsa di archiviazione valida e pertanto non possono essere **NULL,** non è possibile applicare out ai puntatori univoci \[  \] \[ [](unique.md) \] \[ [**o ptr di**](ptr.md) primo \] livello. I parametri che \[ **sono puntatori** \] \[ **univoci o ptr** devono essere \] \[ [**in**](in.md) \] o \[ **in**, parametri **out.** \]

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**first \_ è**](first-is.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**tipo \_ di opzione**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 