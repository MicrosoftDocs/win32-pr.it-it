---
title: transmit_as (attributo)
description: L'attributo \ trasmissione \_ As \ indica al compilatore di associare Type-ID, ovvero un tipo presentato che le applicazioni client e server manipolano, con un tipo trasmesso Xmit-Type.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- attributo transmit_as MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299621"
---
# <a name="transmit_as-attribute"></a>Trasmetti \_ come attributo

L'attributo **\[ trasmissione \_ As \]** indica al compilatore di associare **Type-ID * * *,* che è un tipo presentato che le applicazioni client e server manipolano con un tipo trasmesso **Xmit-Type.**

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

*tipo di Xmit* 
</dt> <dd>

Specifica il tipo di dati trasmesso tra il client e il server.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md), **\]** il riferimento dell'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md)e **\]** la stringa degli attributi di utilizzo **\[** [](string.md) **\]** e **\[** [**ignorano**](ignore.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole. Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> <dt>

*ID tipo* 
</dt> <dd>

Specifica il nome del tipo di dati presentato alle applicazioni client e server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare l'attributo **\[ trasmissione \_ As \]** , l'utente deve fornire routine che convertono i dati tra i tipi presentati e trasmessi. tali routine devono inoltre liberare memoria utilizzata per conservare i dati convertiti. L'attributo **\[ trasmissione \_ As \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.

Il tipo trasmesso *Xmit-Type* deve essere risolto in un tipo di base MIDL, un tipo predefinito o un identificatore di tipo. Per altre informazioni, vedere [tipi di base MIDL](midl-base-types.md).

L'utente deve fornire le routine seguenti.



| Nome routine              | Descrizione                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ID-tipo * * * \_ in \_ Xmit**   | Converte i dati dal tipo presentato al tipo trasmesso. Questa routine alloca memoria per il tipo trasmesso e per tutti i dati a cui fanno riferimento i puntatori nel tipo trasmesso.                            |
| *ID-tipo * * * \_ da \_ Xmit** | Converte i dati dal tipo trasmesso al tipo presentato. Questa routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo presentato. RPC alloca memoria per il tipo stesso. |
| *ID tipo * * * \_ inst libero \_** | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo presentato. RPC libera la memoria per il tipo stesso.                                                                                               |
| *ID-tipo * * * \_ \_ Xmit gratuito** | Libera lo spazio di archiviazione usato dal chiamante per il tipo trasmesso e per i dati a cui fanno riferimento i puntatori nel tipo trasmesso.                                                                                            |



 

 

Lo stub client chiama *Type-ID * * * \_ in \_ Xmit** per allocare spazio per il tipo trasmesso e per convertire i dati in oggetti di tipo *Xmit-Type.* Lo stub del server alloca spazio per il tipo di dati originale e chiama *Type-ID * * * \_ da \_ Xmit** per tradurre i dati dal tipo trasmesso al tipo presentato.

Al ritorno dal codice dell'applicazione, lo stub del server chiama *Type-ID * * \_ * \_ inst libero** per deallocare lo spazio di archiviazione per *Type-ID* sul lato server. Lo stub client chiama *Type-ID * * * \_ Free \_ Xmit** per deallocare l'archiviazione di *tipo Xmit* sul lato client.

I tipi seguenti non possono avere un attributo **\[ trasmissione \_ As \]** :

-   Handle di contesto (tipi con l'attributo del tipo di **\[** [**\_ handle di contesto**](context-handle.md) **\]** e i tipi usati come parametri con l'attributo dell' **\[ \_ handle \] di contesto** )
-   Tipi che sono pipe o derivate da pipe
-   Tipi di dati utilizzati come tipo di base di una definizione di pipe
-   Parametri che sono puntatori o si risolvono ai puntatori
-   Parametri conformi, variabili o matrici aperte
-   Strutture che contengono matrici conformi
-   Handle di tipo predefinito [**\_ t**](handle-t.md), [**void**](void.md)

I tipi trasmessi devono essere conformi alle restrizioni seguenti:

-   Non devono essere puntatori o contenere puntatori.
-   Non devono essere pipe né contenere pipe.

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

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**gestire**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 