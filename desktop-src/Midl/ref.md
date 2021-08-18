---
title: ref (attributo)
description: L'attributo \ ref\ identifica un puntatore di riferimento. Viene usato semplicemente per rappresentare un livello di riferimento indiretto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- Attributo ref MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916556bdee83817f512c2d86eef2d768c3f6dbddf06b39408da5c25a2ba10ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013669"
---
# <a name="ref-attribute"></a>ref (attributo)

**\[ L'attributo ref \]** identifica un puntatore di riferimento. Viene usato semplicemente per rappresentare un livello di riferimento indiretto.

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md), **\]** switch type , transmit **\[** [**\_**](switch-type.md) **\]** **\[** [**\_ as**](transmit-as.md), **\]** **\[ \]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** gli attributi puntatore ref , unique o ptr e gli attributi di utilizzo context handle , string e ignore . Separare più attributi con virgole.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione**](union.md)o un [**tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*dichiaratore standard* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*declarator-list* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore del nome di parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Specifica zero o più attributi di campo applicabili alla struttura, al membro unione o al parametro della funzione. Gli attributi di campo validi includono first è , last è , length è , max è , size è ; la stringa degli attributi di utilizzo , ignore e context handle ; l'attributo **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[ puntatore ref \]**, **\[** [**unique**](unique.md)o **\]** **\[** [**ptr**](ptr.md)e **\]** **\[** [**\_**](switch-type.md) **\]** il tipo di opzione dell'attributo union . Separare più attributi di campo con virgole.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ puntatore ref \]**, **\[** [**unique**](unique.md)o **\]** **\[** [**ptr**](ptr.md)e **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** gli attributi di utilizzo string , ignore e context handle .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui si applica **\[ l'attributo ref. \]** Un dichiaratore di puntatore è lo stesso del dichiaratore di puntatore usato in C; viene costruito dal \* designatore, dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro possono assumere gli attributi direzionali in e out; gli attributi di campo sono , last è **\[** [](in.md) **\]** , length è , max è , size è e switch **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** type **\[** [**\_**](last-is.md); **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[ \]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** l'attributo puntatore ref , unique o ptr e l'handle di contesto degli attributi di utilizzo e string . L'attributo **\[** [**di utilizzo ignore**](ignore.md) **\]** non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un attributo puntatore può essere applicato come attributo di tipo, come attributo di campo che si applica a un membro della struttura, a un membro di unione o a un parametro. o come attributo di funzione che si applica al tipo restituito della funzione. L'attributo pointer può essere visualizzato anche con la parola **\[** [**chiave pointer \_ default.**](pointer-default.md) **\]**

Un puntatore di riferimento presenta le caratteristiche seguenti:

-   Punta sempre all'archiviazione valida. non ha mai il valore **NULL**. È sempre possibile dereferenziare un puntatore di riferimento.
-   Non cambia mai durante una chiamata. Un puntatore di riferimento punta sempre alla stessa archiviazione nel client prima e dopo la chiamata.
-   Non alloca nuova memoria nel client. I dati restituiti dal server vengono scritti nell'archiviazione esistente specificata dal valore del puntatore di riferimento prima della chiamata.
-   Non causa l'aliasing. Archiviazione a cui punta un puntatore di riferimento non può essere raggiunto da qualsiasi altro nome nella funzione.

Un puntatore di riferimento non può essere usato come tipo di puntatore restituito da una funzione.

Se non viene specificato alcun attributo per un parametro puntatore di primo livello, viene considerato come puntatore di riferimento.

## <a name="examples"></a>Esempi

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
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

[**il \_ primo è**](first-is.md)
</dt> <dt>

[**Gestire**](handle.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**\_l'ultimo è**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**max \_ è**](max-is.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**tipo di \_ commutatore**](switch-type.md)
</dt> <dt>

[**trasmettere \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 