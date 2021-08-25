---
title: ptr (attributo)
description: L'attributo \ ptr\ definisce un puntatore come puntatore completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- Attributo ptr MIDL
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53e9b85be5e9073a272dafd63a2a01ba64f440f90cc5d9c41f44260f235f9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927421"
---
# <a name="ptr-attribute"></a>ptr (attributo)

**\[ L'attributo \] ptr** definisce un puntatore come puntatore completo.

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono handle , tipo switch , trasmissione come ; riferimento dell'attributo del puntatore , univoco o **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\[ ptr \]** e **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** handle di contesto degli attributi di utilizzo , stringa e ignorare . Separare più attributi con virgole.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione**](union.md)o un [**tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*dichiaratore standard* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers)

</dd> <dt>

*declarator-list* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers) *Declarator-list* è costituito da uno o più dichiaratori separati da virgole. L'identificatore del nome del parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano alla struttura, al membro unione o al parametro della funzione. Gli attributi di campo validi includono first è , last è , length è , max è , size è , la stringa degli attributi di utilizzo , ignora e **\[** [**\_**](first-is.md)l'handle di contesto , l'attributo puntatore ref , unique o **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[ ptr \]** e **\[** [**\_**](switch-type.md) **\]** il tipo di opzione dell'attributo di unione . Separare più attributi di campo con virgole.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo puntatore ref , unique o **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[ ptr \]** e **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** la stringa degli attributi di utilizzo , ignorano e l'handle di contesto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui si applica **\[ l'attributo ptr. \]** Un dichiaratore di puntatore è uguale al dichiaratore di puntatore usato in C; viene costruito \* dall'designatore , dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi dei parametri possono prendere gli attributi direzionali [**in**](in.md) e [**out;**](out-idl.md) Gli attributi di campo sono , last è , length è [**, \_**](length-is.md) [**\_**](last-is.md) [**\_**](first-is.md)max è , [**size \_**](size-is.md)è e il tipo [**switch \_**](switch-type.md), l'attributo puntatore [**ref**](ref.md), [**unique**](unique.md)o **\[ \] ptr** e l'handle di contesto e la stringa degli attributi di [**utilizzo**](string.md). [**\_**](max-is.md) [**\_**](context-handle.md) L'attributo [**di utilizzo ignore**](ignore.md) non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il puntatore completo designato **\[ dall'attributo ptr \]** si avvicina alla funzionalità completa del puntatore del linguaggio C. Il puntatore completo può avere il **valore NULL** e può cambiare durante la chiamata da **NULL** a non **NULL.** Archiviazione a cui puntano i puntatori completi possono essere raggiunti da altri nomi nell'applicazione che supportano l'aliasing e i cicli. Questa funzionalità richiede un sovraccarico maggiore durante una chiamata di procedura remota per identificare i dati a cui fa riferimento il puntatore, determinare se il valore è **NULL** e individuare se due puntatori puntano agli stessi dati.

Usare puntatori completi per:

-   Valori restituiti remoti.
-   Puntatori doppi, quando le dimensioni di un parametro di output non sono note.
-   **Puntatori NULL.**

Non è possibile usare puntatori completi (e univoci) per descrivere le dimensioni di una matrice o di un'unione perché questi puntatori possono avere il **valore NULL.** Questa restrizione da MIDL impedisce un errore che può verificarsi quando viene usato un **valore NULL** come dimensione.

Si presuppone che i puntatori di riferimento e univoci non causeranno l'aliasing dei dati. Un grafo diretto ottenuto a partire da un puntatore univoco o di riferimento e seguendo solo puntatori univoci o di riferimento non contiene né reconvergenza né cicli.

Per evitare l'aliasing, tutti i valori del puntatore devono essere ottenuti da un puntatore di input della stessa classe di puntatore. Se più puntatori puntano alla stessa posizione di memoria, tutti questi puntatori devono essere puntatori completi.

In alcuni casi, i puntatori completi e univoci possono essere misti. A un puntatore completo può essere assegnato il valore di un puntatore univoco, purché l'assegnazione non violi le restrizioni relative alla modifica del valore di un puntatore univoco. Tuttavia, quando si assegna a un puntatore univoco il valore di un puntatore completo, è possibile che si causerà l'aliasing.

La combinazione di puntatori completi e univoci può causare l'aliasing, come illustrato nell'esempio seguente:

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

Anche se "t->left" e "t->right" puntano a posizioni di memoria univoche, "t->left->pdata" e "t->right->pdata" sono alias. Per questo motivo, gli algoritmi di supporto degli alias devono seguire tutti i puntatori (inclusi i puntatori univoci e di riferimento) che possono raggiungere un puntatore completo.

## <a name="examples"></a>Esempi

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi di matrice Sized-Pointer matrice](array-and-sized-pointer-attributes.md)
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

[**Gestire**](handle.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**impostazione predefinita del \_ puntatore**](pointer-default.md)
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

[**\_trasmetti come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 