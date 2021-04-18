---
title: unique (attributo)
description: L'attributo \ Unique \ specifica un puntatore univoco.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- attributo univoco MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299620"
---
# <a name="unique-attribute"></a>unique (attributo)

L'attributo **\[ Unique \]** specifica un puntatore univoco.

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[ univoco \]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo. Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*dichiaratore e declarator-list* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*struct-or-Union-dichiaratore* 
</dt> <dd>

Specifica una [**struttura**](struct.md) MIDL o un dichiaratore di [**Unione**](union.md) .

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano al membro della struttura, al membro di Unione o al parametro della funzione. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e il **\[ \_ tipo \] di opzione** attribute Union. Separare più attributi di campo con virgole.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui viene applicato l'attributo **\[ Unique \]** . Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi **\[ di \]** parametro possono attivare e **\[ \]** disattivare gli attributi direzionali. gli attributi di campo **\[ First \_ \]** sono, **\[ Last \_ \] è**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **Unique** o [**ptr**](ptr.md)e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage. L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile applicare gli attributi del puntatore come attributo di tipo; come attributo di campo che si applica a un membro di struttura, a un membro di Unione o a un parametro; o come attributo di funzione applicabile al tipo restituito della funzione. L'attributo pointer può essere visualizzato anche con la **\[** parola chiave [**\_ default del puntatore**](pointer-default.md) **\]** .

Un puntatore univoco presenta le caratteristiche seguenti:

-   Il valore può essere **null**.
-   Può cambiare durante una chiamata da **null** a non **null**, da un valore **diverso da****null** o da un valore non **null** a un altro.
-   Consente di allocare una nuova memoria nel client. Quando il puntatore univoco passa da **null** a non **null**, i dati restituiti dal server vengono scritti in una nuova risorsa di archiviazione.
-   Può usare la memoria esistente sul client senza allocare la nuova memoria. Quando un puntatore univoco viene modificato durante una chiamata da un valore non **null** a un altro, si presuppone che il puntatore punti a un oggetto dati dello stesso tipo. I dati restituiti dal server vengono scritti nella risorsa di archiviazione esistente specificata dal valore del puntatore univoco prima della chiamata.
-   Può avere memoria orfana sul client. La memoria a cui fa riferimento un puntatore univoco non **null** può non essere mai liberata se il puntatore univoco diventa **null** durante una chiamata e il client non dispone di un altro mezzo per dereferenziare l'archiviazione.
-   Non provoca l'aliasing. Analogamente all'archiviazione a cui punta un puntatore di riferimento, non è possibile raggiungere lo spazio di archiviazione a cui punta un puntatore univoco da un altro nome nella funzione.

Gli stub chiamano le funzioni di gestione della memoria fornite dall'utente [**MIDL \_ User \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) e [**MIDL \_ User \_ Free**](/windows/desktop/Rpc/the-midl-user-free-function) per allocare e deallocare la memoria necessaria per i puntatori univoci e i relativi riferimenti.

Ai puntatori univoci si applicano le restrizioni seguenti:

-   Non è possibile applicare l'attributo **\[ Unique \]** ai parametri dell'handle di binding ( [**handle \_ t**](handle-t.md)) e ai parametri dell'handle di contesto.
-   Non è possibile applicare l'attributo **\[ Unique \]** ai parametri del puntatore di **\[** [](out-idl.md) **\]** primo livello solo out (parametri che hanno solo l'attributo **\[ out \]** Directional).
-   Per impostazione predefinita, i puntatori di primo livello negli elenchi di parametri sono **\[** [](ref.md) **\]** puntatori Ref. Questo vale anche se l'interfaccia specifica il **puntatore \_ predefinito (univoco)**. I parametri di primo livello negli elenchi di parametri devono essere specificati con l'attributo **\[ Unique \]** come puntatore univoco.
-   Non è possibile usare i puntatori univoci per descrivere le dimensioni di una matrice o di un ARM di Unione perché i puntatori univoci possono avere il valore **null**. Questa restrizione impedisce l'errore risultante se viene usato un valore **null** come dimensione della matrice o dimensione del ARM di Unione.

## <a name="examples"></a>Esempi

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**handle \_ t**](handle-t.md)
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

[\_alloca utente \_ MIDL](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[\_utente MIDL \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**puntatore \_ predefinito**](pointer-default.md)
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

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 