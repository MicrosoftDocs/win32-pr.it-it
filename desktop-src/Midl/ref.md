---
title: ref (attributo)
description: L'attributo \ Ref \ identifica un puntatore di riferimento. Viene usato semplicemente per rappresentare un livello di riferimento indiretto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- attributo ref MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872382"
---
# <a name="ref-attribute"></a>ref (attributo)

L'attributo **\[ ref \]** identifica un puntatore di riferimento. Viene usato semplicemente per rappresentare un livello di riferimento indiretto.

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

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md), **\]** gli attributi del puntatore **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l'handle del contesto degli attributi di utilizzo **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**Ignore**](ignore.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*dichiaratore standard* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** . Separare più attributi di campo con virgole.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui si applica l'attributo **\[ ref \]** . Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro possono **\[** [](in.md) **\]** attivare e disattivare gli attributi direzionali **\[** [](out-idl.md) **\]** . gli attributi di campo **\[** [**First \_**](first-is.md)sono **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**size \_ is**](size-is.md) **\]** e **\[** [**Switch \_ Type**](switch-type.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle**](context-handle.md) **\]** e la **\[** [**stringa**](string.md)del contesto degli attributi Usage **\]** . L'attributo Usage **\[** [**Ignore**](ignore.md) **\]** non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un attributo del puntatore può essere applicato come attributo di tipo, come un attributo di campo che si applica a un membro di struttura, a un membro di Unione o a un parametro; o come attributo di funzione applicabile al tipo restituito della funzione. L'attributo pointer può essere visualizzato anche con la **\[** parola chiave [**\_ default del puntatore**](pointer-default.md) **\]** .

Un puntatore di riferimento presenta le seguenti caratteristiche:

-   Punta sempre a un archivio valido; il valore non è mai **null**. È sempre possibile dereferenziare un puntatore di riferimento.
-   Non cambia mai durante una chiamata. Un puntatore di riferimento punta sempre alla stessa risorsa di archiviazione nel client prima e dopo la chiamata.
-   Non alloca la nuova memoria nel client. I dati restituiti dal server vengono scritti nella risorsa di archiviazione esistente specificata dal valore del puntatore di riferimento prima della chiamata.
-   Non provoca l'aliasing. Non è possibile raggiungere lo spazio di archiviazione a cui punta un puntatore di riferimento da un altro nome nella funzione.

Un puntatore di riferimento non può essere utilizzato come tipo di un puntatore restituito da una funzione.

Se non è specificato alcun attributo per un parametro puntatore di primo livello, viene considerato come un puntatore di riferimento.

## <a name="examples"></a>Esempi

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
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

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[**gestire**](handle.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 