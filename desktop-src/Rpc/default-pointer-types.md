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
# <a name="default-pointer-types"></a><span data-ttu-id="9cf82-104">Tipi di puntatore predefiniti</span><span class="sxs-lookup"><span data-stu-id="9cf82-104">Default Pointer Types</span></span>

<span data-ttu-id="9cf82-105">Non è necessario che i puntatori abbiano una descrizione esplicita dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="9cf82-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="9cf82-106">Quando non viene fornito un attributo esplicito, il compilatore MIDL usa un attributo puntatore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9cf82-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="9cf82-107">I casi predefiniti per i puntatori senza attributi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cf82-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="9cf82-108">Puntatori di primo livello visualizzati negli elenchi di parametri predefiniti per i \[ [](/windows/desktop/Midl/ref) \] puntatori Ref.</span><span class="sxs-lookup"><span data-stu-id="9cf82-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="9cf82-109">Tutti gli altri puntatori vengono predefiniti per il tipo specificato dall' \[ attributo [**\_ predefinito del puntatore**](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="9cf82-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="9cf82-110">Quando non \[ viene fornito alcun attributo **\_ predefinito del puntatore** \] , questi puntatori vengono predefiniti per l' \[ [](/windows/desktop/Midl/unique) \] attributo unique quando il compilatore MIDL si trova in modalità [Microsoft extensions](microsoft-rpc-binding-handle-extensions.md) o l' \[ [](/windows/desktop/Midl/ptr) \] attributo PTR quando il compilatore MIDL è in modalità compatibile con DCE.</span><span class="sxs-lookup"><span data-stu-id="9cf82-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="9cf82-111">Quando una procedura remota restituisce un puntatore, il valore restituito deve essere un \[ puntatore [**univoco**](/windows/desktop/Midl/unique) \] o completo ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).</span><span class="sxs-lookup"><span data-stu-id="9cf82-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="9cf82-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cf82-112">Remarks</span></span>

<span data-ttu-id="9cf82-113">Per garantire un comportamento di attributo puntatore non ambiguo, usare sempre attributi puntatore espliciti quando si definisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="9cf82-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="9cf82-114">È consigliabile **\[** **\]** usare PTR solo quando è richiesto l'aliasing del puntatore.</span><span class="sxs-lookup"><span data-stu-id="9cf82-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 