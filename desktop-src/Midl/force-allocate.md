---
title: attributo force_allocate
description: L'attributo ACF \ Force \_ allocate \ forza l'allocazione di un parametro del puntatore usando l' \_ utente MIDL \_ allocate anziché ottimizzare l'allocazione.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- attributo force_allocate MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472843"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="54050-104">Force \_ alloca attributo</span><span class="sxs-lookup"><span data-stu-id="54050-104">force\_allocate attribute</span></span>

<span data-ttu-id="54050-105">L'attributo di allocazione forzata degli attributi di ACF impone l'allocazione di \[ **\_** \] un parametro del puntatore usando l' [**\_ utente MIDL \_ allocato**](midl-user-allocate-1.md) anziché ottimizzare l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="54050-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="54050-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54050-106">Parameters</span></span>

<span data-ttu-id="54050-107">Questo attributo non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="54050-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="54050-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="54050-108">Remarks</span></span>

<span data-ttu-id="54050-109">RPC tenta di ridurre al minimo le allocazioni di memoria nel server fornendo puntatori ai buffer di memoria interni.</span><span class="sxs-lookup"><span data-stu-id="54050-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="54050-110">Questo approccio può causare problemi per le applicazioni che tentano di chiamare direttamente l' [**\_ utente MIDL \_ senza**](midl-user-free-1.md) i puntatori forniti da RPC, perché un puntatore ottimizzato non può essere liberato.</span><span class="sxs-lookup"><span data-stu-id="54050-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="54050-111">Contrassegnando un parametro con **\[ Force \_ allocate \]** si eviterà questa ottimizzazione per tutti i puntatori che lo derivano.</span><span class="sxs-lookup"><span data-stu-id="54050-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="54050-112">Un altro uso comune di **\[ Force \_ allocate \]** consiste nel garantire l'allineamento della memoria a cui si fa riferimento se un'applicazione richiede un allineamento maggiore di quello della memoria a cui punta.</span><span class="sxs-lookup"><span data-stu-id="54050-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="54050-113">Ad esempio, le applicazioni passano spesso dati in una matrice generica di byte anziché utilizzare il tipo effettivo, ma un byte è garantito solo per essere allineato a 1, che può causare problemi per le applicazioni che presuppongono un allineamento più grande.</span><span class="sxs-lookup"><span data-stu-id="54050-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="54050-114">Contrassegnando il parametro con **\[ Force \_ allocate \]**, l'applicazione può garantire che tutte le memoria a cui puntano avranno un allineamento uguale a quello garantito dall' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="54050-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54050-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="54050-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="54050-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="54050-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54050-117">Evitare le informazioni nascoste</span><span class="sxs-lookup"><span data-stu-id="54050-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="54050-118">Progettazione di interfacce compatibili con 64 bit</span><span class="sxs-lookup"><span data-stu-id="54050-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="54050-119">**\_alloca utente \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="54050-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="54050-120">**\_utente MIDL \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="54050-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="54050-121">**allocare**</span><span class="sxs-lookup"><span data-stu-id="54050-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 