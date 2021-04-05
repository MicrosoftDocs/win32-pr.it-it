---
title: Tipi di puntatore predefiniti
description: Non è necessario che i puntatori abbiano una descrizione esplicita dell'attributo. Quando non viene fornito un attributo esplicito, il compilatore MIDL usa un attributo puntatore predefinito.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047059"
---
# <a name="default-pointer-types"></a>Tipi di puntatore predefiniti

Non è necessario che i puntatori abbiano una descrizione esplicita dell'attributo. Quando non viene fornito un attributo esplicito, il compilatore MIDL usa un attributo puntatore predefinito.

I casi predefiniti per i puntatori senza attributi sono i seguenti:

-   Puntatori di primo livello visualizzati negli elenchi di parametri predefiniti per i \[ [](/windows/desktop/Midl/ref) \] puntatori Ref.
-   Tutti gli altri puntatori vengono predefiniti per il tipo specificato dall' \[ attributo [**\_ predefinito del puntatore**](/windows/desktop/Midl/pointer-default) \] . Quando non \[ viene fornito alcun attributo **\_ predefinito del puntatore** \] , questi puntatori vengono predefiniti per l' \[ [](/windows/desktop/Midl/unique) \] attributo unique quando il compilatore MIDL si trova in modalità [Microsoft extensions](microsoft-rpc-binding-handle-extensions.md) o l' \[ [](/windows/desktop/Midl/ptr) \] attributo PTR quando il compilatore MIDL è in modalità compatibile con DCE.

Quando una procedura remota restituisce un puntatore, il valore restituito deve essere un \[ puntatore [**univoco**](/windows/desktop/Midl/unique) \] o completo ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).

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

Per garantire un comportamento di attributo puntatore non ambiguo, usare sempre attributi puntatore espliciti quando si definisce un puntatore.

È consigliabile **\[** **\]** usare PTR solo quando è richiesto l'aliasing del puntatore.

 

 