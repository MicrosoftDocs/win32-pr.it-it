---
title: attributo midl_user_allocate
description: La \_ \_ funzione di allocazione utente MIDL è una funzione fornita dalle applicazioni client e server per allocare memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- attributo midl_user_allocate MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337375"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="37e98-104">\_attributo di \_ allocazione utente MIDL</span><span class="sxs-lookup"><span data-stu-id="37e98-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="37e98-105">La funzione di **\_ \_ allocazione utente MIDL** è una funzione fornita dalle applicazioni client e server per allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="37e98-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="37e98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37e98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e98-107">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="37e98-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="37e98-108">Specifica il numero di byte da allocare.</span><span class="sxs-lookup"><span data-stu-id="37e98-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37e98-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="37e98-109">Remarks</span></span>

<span data-ttu-id="37e98-110">Sia le applicazioni client che le applicazioni server devono implementare la funzione di **\_ \_ allocazione utente MIDL** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="37e98-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="37e98-111">Le applicazioni e gli stub generati chiamano l' **\_ utente MIDL \_ allocato** quando si gestiscono oggetti a cui fanno riferimento i puntatori:</span><span class="sxs-lookup"><span data-stu-id="37e98-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="37e98-112">L'applicazione server deve chiamare **MIDL \_ User \_ allocate** per allocare memoria per ApplicationA, ad esempio quando si crea un nuovo nodo.</span><span class="sxs-lookup"><span data-stu-id="37e98-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="37e98-113">Lo stub del server chiama l' **\_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati puntati nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="37e98-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="37e98-114">Lo stub client chiama **l' \_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati dal server a cui fa riferimento un puntatore [**out**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="37e98-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="37e98-115">Si noti che per i **\[** [](in.md) **\]** puntatori univoci in, **\[ out \]** e **\[** [**Unique**](unique.md) **\]** , lo stub client chiama l' **\_ utente MIDL \_ allocare** solo se il valore del puntatore **\[ univoco \]** è **null** per l'input e viene modificato in un valore non **null** durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="37e98-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="37e98-116">Se per l'input il puntatore **\[ \] univoco** è diverso da **null** , lo stub client scrive i dati associati nella memoria esistente.</span><span class="sxs-lookup"><span data-stu-id="37e98-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="37e98-117">Se **\_ \_ allocare l'utente MIDL** non riesce ad allocare memoria, deve restituire un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="37e98-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="37e98-118">È consigliabile che **MIDL \_ User \_ allocate** restituisca un puntatore a 8 byte allineato.</span><span class="sxs-lookup"><span data-stu-id="37e98-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="37e98-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="37e98-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="37e98-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="37e98-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e98-121">**allocare**</span><span class="sxs-lookup"><span data-stu-id="37e98-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="37e98-122">**matrici**</span><span class="sxs-lookup"><span data-stu-id="37e98-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="37e98-123">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="37e98-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="37e98-124">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="37e98-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="37e98-125">**in**</span><span class="sxs-lookup"><span data-stu-id="37e98-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="37e98-126">**\_utente MIDL \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="37e98-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="37e98-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="37e98-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="37e98-128">**out**</span><span class="sxs-lookup"><span data-stu-id="37e98-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="37e98-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="37e98-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="37e98-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="37e98-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="37e98-131">**unico**</span><span class="sxs-lookup"><span data-stu-id="37e98-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 