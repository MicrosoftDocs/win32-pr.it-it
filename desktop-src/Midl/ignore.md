---
title: Ignora attributo
description: L'attributo \ ignore indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dall'indicatore di misura non vengono trasmessi. L'attributo \ ignore è limitato ai membri puntatore di strutture o unioni.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- Ignora attributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872390"
---
# <a name="ignore-attribute"></a>Ignora attributo

L'attributo **\[ Ignore \]** indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dall'indicatore di misura non vengono trasmessi. L'attributo **\[ Ignore \]** è limitato ai membri puntatore di strutture o unioni.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di membro puntatore* 
</dt> <dd>

Specifica il tipo del membro del puntatore della struttura o dell'Unione.

</dd> <dt>

*nome puntatore* 
</dt> <dd>

Specifica il nome del membro del puntatore da ignorare durante il marshalling.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore di un membro della struttura con l'attributo **\[ Ignore \]** non è definito nella destinazione. Un **\[** parametro [**in**](in.md) **\]** non è definito nel computer remoto. Un **\[** parametro [**out**](out-idl.md) **\]** non è definito nel computer locale.

L'attributo **\[ Ignore \]** consente di impedire la trasmissione di dati. Questa operazione è utile in situazioni come un elenco con collegamento doppio. L'esempio seguente include un elenco a doppio collegamento che introduce l'aliasing dei dati:

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

L'aliasing si verifica nell'esempio precedente perché la stessa area di memoria è disponibile in due puntatori diversi della funzione **p** e **p->Next->precedente**.

Si noti che **\[ Ignore \]** non può essere utilizzato come attributo di tipo.

## <a name="examples"></a>Esempi

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 