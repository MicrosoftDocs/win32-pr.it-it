---
title: unique (attributo)
description: L'attributo \ unique\ specifica un puntatore univoco.
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
ms.openlocfilehash: 57c176c9a246329b6193c97ca5ce356c2b433cb421b77b374e103778df1b79dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822031"
---
# <a name="unique-attribute"></a>unique (attributo)

**\[ L'attributo unique \]** specifica un puntatore univoco.

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

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi applicabili al tipo. Gli attributi di tipo validi includono handle , switch type , transmit as ; l'attributo **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**puntatore ref**](ref.md) **\]** , **\[ unique \]** o **\[** [**ptr**](ptr.md)e **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** gli attributi di utilizzo context handle , string e ignore . Separare più attributi con virgole.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione,**](union.md) [**un tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*declarator e declarator-list* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore del nome di parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*struct-or-union-declarator* 
</dt> <dd>

Specifica uno [**struct**](struct.md) MIDL o un [**dichiaratore di**](union.md) unione.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Specifica zero o più attributi di campo applicabili al membro della struttura, al membro unione o al parametro della funzione. Gli attributi di campo validi includono first è , last è , length è , max **\[** [**\_**](first-is.md)è , size è ; **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[ \]** **\[ \_ \]** **\[ \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ \]** la stringa degli attributi di utilizzo , ignore e context handle ; l'attributo puntatore ref , unique o ptr e il tipo di opzione dell'attributo union . Separare più attributi di campo con virgole.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ puntatore ref \]**, **\[ unique \]** o **\[ ptr \]** e **\[ \]** **\[ \]** **\[ \_ \]** gli attributi di utilizzo string , ignore e context handle .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui si applica **\[ l'attributo \]** univoco. Un dichiaratore di puntatore è lo stesso del dichiaratore di puntatore usato in C; viene costruito dal \* designatore, dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro possono assumere gli attributi direzionali **\[ in \]** e **\[ \] out;** **\[ \]**  **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** gli attributi di campo sono , **\[ \_ \]** last è , length è , max è , size è e switch type ; l'attributo puntatore ref , unique o [**ptr**](ptr.md)e l'handle **\[ \_ \]** di contesto degli attributi di utilizzo e string . L'attributo **\[ di utilizzo ignore \]** non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli attributi del puntatore possono essere applicati come attributo di tipo. come attributo di campo che si applica a un membro della struttura, a un membro di unione o a un parametro; o come attributo di funzione che si applica al tipo restituito della funzione. L'attributo pointer può essere visualizzato anche con la parola **\[** [**chiave pointer \_ default.**](pointer-default.md) **\]**

Un puntatore univoco ha le caratteristiche seguenti:

-   Può avere il valore **NULL.**
-   Può cambiare durante una chiamata **da NULL** a non **NULL,** da non **NULL** a **NULL** o da un valore non **NULL** a un altro.
-   Può allocare nuova memoria nel client. Quando il puntatore univoco cambia **da NULL** a non **NULL,** i dati restituiti dal server vengono scritti in una nuova archiviazione.
-   Può usare la memoria esistente nel client senza allocare nuova memoria. Quando un puntatore univoco cambia durante una chiamata da un valore non **NULL** a un altro, si presuppone che il puntatore punti a un oggetto dati dello stesso tipo. I dati restituiti dal server vengono scritti nell'archiviazione esistente specificata dal valore del puntatore univoco prima della chiamata.
-   Può orfare la memoria nel client. La memoria a cui fa riferimento un puntatore univoco non **NULL** non può mai essere liberata se il puntatore univoco cambia in **NULL** durante una chiamata e il client non dispone di un altro mezzo per dereferenziare l'archiviazione.
-   Non causa l'aliasing. Analogamente all'archiviazione a cui punta un puntatore di riferimento, l'archiviazione a cui punta un puntatore univoco non può essere raggiunta da qualsiasi altro nome nella funzione.

Gli stub chiamano le funzioni di gestione della memoria fornite dall'utente [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) e [**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function) per allocare e deallocare la memoria necessaria per i puntatori univoci e i relativi riferimenti.

Le restrizioni seguenti si applicano ai puntatori univoci:

-   **\[ L'attributo \]** unique non può essere applicato ai parametri binding-handle ( [**handle \_ t**](handle-t.md)) e context-handle parameters.
-   **\[ L'attributo \]** univoco non può essere applicato ai parametri del puntatore out -only di primo **\[** [](out-idl.md) **\]** livello (parametri che hanno solo l'attributo **\[ direzionale out). \]**
-   Per impostazione predefinita, i puntatori di primo livello negli elenchi di parametri sono **\[** [**puntatori di**](ref.md) **\]** riferimento. Questo vale anche se l'interfaccia specifica **\_ default(unique) del puntatore.** I parametri di primo livello negli elenchi di parametri devono essere specificati con **\[ l'attributo univoco \]** per essere un puntatore univoco.
-   Non è possibile usare puntatori univoci per descrivere le dimensioni di una matrice o di un'unione perché i puntatori univoci possono avere il valore **NULL.** Questa restrizione impedisce l'errore che si verifica se viene usato un **valore NULL** come dimensione della matrice o della dimensione union-arm.

## <a name="examples"></a>Esempi

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**handle \_ t**](handle-t.md)
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

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**impostazione predefinita del \_ puntatore**](pointer-default.md)
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

[**tipo di \_ commutatore**](switch-type.md)
</dt> <dt>

[**trasmettere \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 