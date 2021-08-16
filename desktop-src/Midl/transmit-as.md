---
title: transmit_as (attributo)
description: L'attributo \ transmit as\ indica al compilatore di associare type-id, ovvero un tipo presentato manipolato dalle applicazioni client e server, a un tipo \_ trasmesso xmit-type.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as attributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382831"
---
# <a name="transmit_as-attribute"></a>\_trasmetti come attributo

**\[ L'attributo transmit \_ as \]** indica al compilatore di associare **type-id**_,_ ovvero un tipo presentato manipolato dalle applicazioni client e server, a un tipo **trasmesso xmit-type.**

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*xmit-type* 
</dt> <dd>

Specifica il tipo di dati trasmesso tra client e server.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono handle , tipo switch , riferimento dell'attributo del puntatore , univoco o ptr , e la **\[** [](handle.md) **\]** stringa degli attributi **\[** [**\_**](switch-type.md) **\]** di utilizzo **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** e **\[** [](ptr.md) **\]** **\[** [](string.md) **\]** **\[** [**ignorano**](ignore.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione,**](union.md) [**un tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers) *Declarator-list* è costituito da uno o più dichiaratori separati da virgole. Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> <dt>

*type-id* 
</dt> <dd>

Specifica il nome del tipo di dati presentato alle applicazioni client e server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare l'attributo **\[ transmit \_ \] as,** l'utente deve fornire routine che convertono i dati tra i tipi presentati e trasmessi. Queste routine devono anche liberare la memoria utilizzata per contenere i dati convertiti. **\[ L'attributo transmit \_ as \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.

Il tipo trasmesso *xmit-type* deve essere risolto in un tipo di base MIDL, in un tipo predefinito o in un identificatore di tipo. Per altre informazioni, vedere [MidL Base Types](midl-base-types.md).

L'utente deve fornire le routine seguenti.



| Nome routine              | Descrizione                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *type-id*** \_ to \_ xmit**   | Converte i dati dal tipo presentato al tipo trasmesso. Questa routine alloca memoria per il tipo trasmesso e per tutti i dati a cui fanno riferimento i puntatori nel tipo trasmesso.                            |
| *type-id*** \_ from \_ xmit** | Converte i dati dal tipo trasmesso al tipo presentato. Questa routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo presentato. RPC alloca memoria per il tipo stesso. |
| *type-id*** \_ free \_ inst** | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo presentato. RPC libera memoria per il tipo stesso.                                                                                               |
| *type-id*** \_ \_ free xmit** | Libera lo spazio di archiviazione usato dal chiamante per il tipo trasmesso e per i dati a cui fanno riferimento i puntatori nel tipo trasmesso.                                                                                            |



 

 

Lo stub client chiama *type-id*** per \_ \_ xmit** per allocare spazio per il tipo trasmesso e convertire i dati in oggetti di *tipo xmit-type.* Lo stub del server alloca spazio per il tipo di dati originale e chiama *type-id*** da \_ \_ xmit** per convertire i dati dal tipo trasmesso al tipo presentato.

Al ritorno dal codice dell'applicazione, lo stub del server chiama *type-id*** \_ free \_ inst** per deallocare lo spazio di archiviazione per *type-id* sul lato server. Lo stub client chiama *type-id*** \_ \_ free xmit** per deallocare l'archiviazione *di tipo xmit* sul lato client.

I tipi seguenti non possono avere un **\[ attributo transmit \_ as: \]**

-   Handle di contesto (tipi con l'attributo del tipo di handle di contesto e tipi usati come parametri con **\[** [**\_**](context-handle.md) **\]** l'attributo **\[ \_ dell'handle di \]** contesto)
-   Tipi che sono pipe o derivati da pipe
-   Tipi di dati utilizzati come tipo di base di una definizione di pipe
-   Parametri che sono puntatori o si risolvono in puntatori
-   Parametri conformi, variabili o matrici aperte
-   Strutture che contengono matrici conformi
-   Handle di tipo predefinito [**\_ t**](handle-t.md), [**void**](void.md)

I tipi trasmessi devono essere conformi alle restrizioni seguenti:

-   Non devono essere puntatori o contenere puntatori.
-   Non devono essere pipe o contenere pipe.

## <a name="examples"></a>Esempi

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**Gestire**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**tipo \_ di opzione**](switch-type.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 