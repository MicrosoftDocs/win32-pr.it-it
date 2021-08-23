---
title: Tipi di puntatore predefiniti
description: I puntatori non devono avere una descrizione esplicita dell'attributo. Quando non viene fornito un attributo esplicito, il compilatore MIDL usa un attributo puntatore predefinito.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3020f17af6e24778c0fa5090009650f3c0832df528ba148e0a6a91928dd1dc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930978"
---
# <a name="default-pointer-types"></a>Tipi di puntatore predefiniti

I puntatori non devono avere una descrizione esplicita dell'attributo. Quando non viene fornito un attributo esplicito, il compilatore MIDL usa un attributo puntatore predefinito.

I casi predefiniti per i puntatori senza attributi sono i seguenti:

-   Per impostazione predefinita, i puntatori di primo livello visualizzati negli elenchi di parametri sono \[ [**puntatori di**](/windows/desktop/Midl/ref) \] riferimento.
-   Tutti gli altri puntatori vengono predefiniti al tipo specificato \[ [**dall'attributo predefinito \_ del**](/windows/desktop/Midl/pointer-default) \] puntatore. Quando non viene fornito alcun attributo predefinito del puntatore, questi puntatori impostano per impostazione predefinita l'attributo univoco quando il compilatore MIDL è in modalità estensioni Microsoft o l'attributo ptr quando il compilatore MIDL è in modalità \[ **\_** \] compatibile con \[ [](/windows/desktop/Midl/unique) \] [](microsoft-rpc-binding-handle-extensions.md) \[ [](/windows/desktop/Midl/ptr) \] DCE.

Quando una procedura remota restituisce un puntatore, il valore restituito deve essere un \[ [**puntatore**](/windows/desktop/Midl/unique) univoco o \] completo ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a>Commenti

Per garantire un comportamento non ambiguo dell'attributo di puntatore, usare sempre attributi di puntatore espliciti durante la definizione di un puntatore.

È consigliabile usare ptr solo quando è necessario **\[** **\]** l'alias del puntatore.

 

 