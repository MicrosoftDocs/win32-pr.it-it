---
title: string (attributo)
description: L'attributo \ string \ indica che la matrice unidimensionale char, WCHAR \_ t, byte (o equivalente) o il puntatore a una matrice di questo tipo devono essere considerati come una stringa.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- attributo stringa MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963033"
---
# <a name="string-attribute"></a>string (attributo)

L' **\[ attributo \] stringa** indica che la matrice unidimensionale [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o il puntatore a tale matrice deve essere considerata come una stringa. La stringa può anche essere una matrice (o un puntatore a una matrice) di costrutti i cui campi sono tutti di tipo **byte**.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano a un tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[ stringa \]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo. Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), un tipo di [**struct**](struct.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*dichiaratore standard* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice. Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione. I due attributi di campo validi sono **\[** [**Max \_**](max-is.md) **\]** e **\[** [**size \_ è**](size-is.md) **\]** ; gli attributi di utilizzo **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**, l'attributo puntatore **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** e il **\[ \_ tipo \] di opzione** attribute Union. Separare più attributi di campo con virgole.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica un dichiaratore di puntatore facoltativo a cui si applica l'attributo **\[ stringa \]** . Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro possono assumere ed **\[ \] escludere** gli attributi direzionali. gli attributi **\[ \] di** campo **\[** [**Max \_ è**](max-is.md) **\]** e **\[** [**size \_ sono**](size-is.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi di utilizzo. L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se l'attributo **\[ stringa \]** viene usato con una matrice i cui limiti vengono determinati in fase di esecuzione, è necessario specificare anche **\[ \_ \] una dimensione** oppure il valore **\[ Max \_ è \]** attributo, come nell'esempio seguente:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

Impossibile utilizzare l'attributo **\[ stringa \]** con attributi che specificano l'intervallo di elementi trasmessi, ad esempio **\[ First \_ è \]**, **\[ Last \_ è \]** e **\[ length \_ è \]**.

Quando viene utilizzato su matrici multidimensionali, l'attributo **\[ stringa \]** viene applicato alla matrice più a destra.

Per definire una stringa calcolata, non usare l'attributo **\[ String \]** . Utilizzare una matrice di caratteri o un puntatore basato su caratteri come il seguente:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

L'attributo **\[ String \]** specifica che lo stub deve usare un metodo fornito dal linguaggio per determinare la lunghezza delle stringhe.

Quando si dichiarano stringhe in C, è necessario allocare spazio per un carattere aggiuntivo che contrassegna la fine della stringa.

## <a name="examples"></a>Esempi

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
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

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
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

[**puntatore \_ predefinito**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
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
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 