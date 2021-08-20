---
title: attributo ignore
description: L'attributo \ ignore\ indica che un puntatore contenuto in una struttura o in un'unione e l'oggetto indicato dal puntatore non viene trasmesso. L'attributo \ ignore\ è limitato ai membri puntatore di strutture o unioni.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- ignorare l'attributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013859"
---
# <a name="ignore-attribute"></a>attributo ignore

**\[ L'attributo ignore \]** indica che un puntatore contenuto in una struttura o in un'unione e l'oggetto indicato dal puntatore non viene trasmesso. **\[ L'attributo ignore \]** è limitato ai membri puntatore di strutture o unioni.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pointer-member-type* 
</dt> <dd>

Specifica il tipo del membro puntatore della struttura o dell'unione.

</dd> <dt>

*pointer-name* 
</dt> <dd>

Specifica il nome del membro puntatore che deve essere ignorato durante il marshalling.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore di un membro della struttura con **\[ l'attributo ignore \]** non è definito nella destinazione. Un **\[** [**parametro in**](in.md) **\]** non è definito nel computer remoto. Un **\[** [**parametro out**](out-idl.md) **\]** non è definito nel computer locale.

**\[ L'attributo ignore \]** consente di impedire la trasmissione dei dati. Ciò è utile in situazioni come un elenco collegato doppio. L'esempio seguente include un elenco collegato doppio che introduce l'alias dei dati:

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

L'aliasing si verifica nell'esempio precedente perché la stessa area di memoria è disponibile da due puntatori diversi nella funzione **p** e **p->next->precedente.**

Si noti che **\[ ignore \]** non può essere usato come attributo di tipo.

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

[**Matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 