---
title: ptr (attributo)
description: L'attributo \ PTR \ designa un puntatore come puntatore completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- attributo MIDL PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337030"
---
# <a name="ptr-attribute"></a>ptr (attributo)

L'attributo **\[ ptr \]** designa un puntatore come puntatore completo.

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

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md)o **\[ \] ptr** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo. Separare più attributi con virgole.

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

Specifica zero o più attributi di campo che si applicano al membro della struttura o dell'Unione o al parametro della funzione. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ \] ptr** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** . Separare più attributi di campo con virgole.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ ptr \]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica almeno un dichiaratore di puntatore a cui si applica l'attributo **\[ ptr \]** . Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

È costituito da zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi [**di**](in.md) parametro possono assumere ed [**estrarre**](out-idl.md)gli attributi direzionali; gli attributi di [**campo \_ First**](first-is.md)sono [**, Last \_ è**](last-is.md), [**length \_ is**](length-is.md), [**Max \_ is**](max-is.md), [**size \_ is**](size-is.md)e [**Switch \_ Type**](switch-type.md), l'attributo Pointer [**ref**](ref.md), [**Unique**](unique.md)o **\[ ptr \]** e la [**stringa**](string.md)e l' [**\_ handle di contesto**](context-handle.md) degli attributi Usage. L'attributo Usage [**Ignore**](ignore.md) non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il puntatore completo definito dall'attributo **\[ ptr \]** si avvicina alla funzionalità completa del puntatore del linguaggio C. Il puntatore completo può avere valore **null** e può cambiare durante la chiamata da **null** a non **null**. Lo spazio di archiviazione a cui puntano i puntatori completi può essere raggiunto da altri nomi nell'applicazione che supportano gli alias e i cicli. Questa funzionalità richiede un sovraccarico maggiore durante una chiamata di procedura remota per identificare i dati a cui fa riferimento il puntatore, determinare se il valore è **null** e per individuare se due puntatori puntano agli stessi dati.

USA puntatori completi per:

-   Valori restituiti remoti.
-   Puntatori doppi, quando la dimensione di un parametro di output non è nota.
-   Puntatori **null** .

I puntatori Full (e Unique) non possono essere usati per descrivere le dimensioni di una matrice o di un'Unione, perché questi puntatori possono avere il valore **null**. Questa restrizione di MIDL impedisce un errore che può verificarsi quando viene utilizzato un valore **null** come dimensione.

Si presuppone che il riferimento e i puntatori univoci non causino l'aliasing dei dati. Un grafico diretto ottenuto iniziando da un puntatore univoco o di riferimento e che segue solo puntatori univoci o di riferimento non contiene né riconvergenza né cicli.

Per evitare alias, è necessario ottenere tutti i valori di puntatore da un puntatore di input della stessa classe di puntatore. Se più di un puntatore punta alla stessa posizione di memoria, tutti i puntatori devono essere puntatori completi.

In alcuni casi, i puntatori completi e univoci possono essere misti. A un puntatore completo è possibile assegnare il valore di un puntatore univoco, purché l'assegnazione non violi le restrizioni relative alla modifica del valore di un puntatore univoco. Tuttavia, quando si assegna un puntatore univoco al valore di un puntatore completo, è possibile che si verifichi l'aliasing.

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

Sebbene "t->left" e "t->Right" puntino a posizioni di memoria univoche, "t->Left->pData" e "t->right->di pData" sono con alias. Per questo motivo, gli algoritmi di supporto degli alias devono seguire tutti i puntatori (inclusi i puntatori univoci e di riferimento) che potrebbero raggiungere un puntatore completo.

## <a name="examples"></a>Esempi

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
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
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 