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
# <a name="ignore-attribute"></a><span data-ttu-id="1a814-105">Ignora attributo</span><span class="sxs-lookup"><span data-stu-id="1a814-105">ignore attribute</span></span>

<span data-ttu-id="1a814-106">L'attributo **\[ Ignore \]** indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dall'indicatore di misura non vengono trasmessi.</span><span class="sxs-lookup"><span data-stu-id="1a814-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="1a814-107">L'attributo **\[ Ignore \]** è limitato ai membri puntatore di strutture o unioni.</span><span class="sxs-lookup"><span data-stu-id="1a814-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="1a814-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a814-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a814-109">*tipo di membro puntatore*</span><span class="sxs-lookup"><span data-stu-id="1a814-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1a814-110">Specifica il tipo del membro del puntatore della struttura o dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="1a814-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="1a814-111">*nome puntatore*</span><span class="sxs-lookup"><span data-stu-id="1a814-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a814-112">Specifica il nome del membro del puntatore da ignorare durante il marshalling.</span><span class="sxs-lookup"><span data-stu-id="1a814-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a814-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a814-113">Remarks</span></span>

<span data-ttu-id="1a814-114">Il valore di un membro della struttura con l'attributo **\[ Ignore \]** non è definito nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="1a814-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="1a814-115">Un **\[** parametro [**in**](in.md) **\]** non è definito nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="1a814-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="1a814-116">Un **\[** parametro [**out**](out-idl.md) **\]** non è definito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a814-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="1a814-117">L'attributo **\[ Ignore \]** consente di impedire la trasmissione di dati.</span><span class="sxs-lookup"><span data-stu-id="1a814-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="1a814-118">Questa operazione è utile in situazioni come un elenco con collegamento doppio.</span><span class="sxs-lookup"><span data-stu-id="1a814-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="1a814-119">L'esempio seguente include un elenco a doppio collegamento che introduce l'aliasing dei dati:</span><span class="sxs-lookup"><span data-stu-id="1a814-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

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

<span data-ttu-id="1a814-120">L'aliasing si verifica nell'esempio precedente perché la stessa area di memoria è disponibile in due puntatori diversi della funzione **p** e **p->Next->precedente**.</span><span class="sxs-lookup"><span data-stu-id="1a814-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="1a814-121">Si noti che **\[ Ignore \]** non può essere utilizzato come attributo di tipo.</span><span class="sxs-lookup"><span data-stu-id="1a814-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="1a814-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="1a814-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="1a814-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1a814-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a814-124">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="1a814-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="1a814-125">**matrici**</span><span class="sxs-lookup"><span data-stu-id="1a814-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="1a814-126">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="1a814-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="1a814-127">**in**</span><span class="sxs-lookup"><span data-stu-id="1a814-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="1a814-128">**out**</span><span class="sxs-lookup"><span data-stu-id="1a814-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="1a814-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="1a814-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="1a814-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="1a814-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="1a814-131">**unico**</span><span class="sxs-lookup"><span data-stu-id="1a814-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 