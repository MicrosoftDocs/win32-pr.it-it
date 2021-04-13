---
title: attributo partial_ignore
description: L'attributo ACF \ partial \_ Ignore \ definisce una versione specializzata di \ Unique \ puntatori che fornisce la semantica facoltativa.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- attributo partial_ignore MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397923"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="19601-104">\_attributo parziale ignore</span><span class="sxs-lookup"><span data-stu-id="19601-104">partial\_ignore attribute</span></span>

<span data-ttu-id="19601-105">L'attributo ACF **\[ partial \_ Ignore \]** definisce una versione specializzata di puntatori **\[ univoci \]** che fornisce la semantica facoltativa.</span><span class="sxs-lookup"><span data-stu-id="19601-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="19601-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="19601-106">Remarks</span></span>

<span data-ttu-id="19601-107">Quando si crea una funzione, è comune consentire agli utenti di specificare un puntatore non **null** ai dati restituiti facoltativi, spesso definito come un puntatore out facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19601-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="19601-108">Non è in genere necessario inizializzare la memoria a cui fa riferimento l'utente.</span><span class="sxs-lookup"><span data-stu-id="19601-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="19601-109">Questa tecnica rappresenta un problema quando la funzione viene utilizzata tramite RPC.</span><span class="sxs-lookup"><span data-stu-id="19601-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="19601-110">Se il puntatore facoltativo-out è valido, ma punta a dati non inizializzati, RPC tenta di effettuare il marshalling dei dati e di inviarli al server, il che può causare la mancata riuscita del marshalling e l'interruzione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="19601-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="19601-111">Anche in caso di esito positivo del marshalling, una quantità potenzialmente elevata di dati inutili viene inviata al server.</span><span class="sxs-lookup"><span data-stu-id="19601-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="19601-112">Questi problemi vengono risolti contrassegnando il puntatore come **\[ in, out, Unique, partial \_ Ignore \]**.</span><span class="sxs-lookup"><span data-stu-id="19601-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="19601-113">Devono essere presenti tutti e quattro gli attributi.</span><span class="sxs-lookup"><span data-stu-id="19601-113">All four attributes must be present.</span></span> <span data-ttu-id="19601-114">Quando viene effettuato il marshalling di un puntatore di **\[ \_ Ignora \] parziale** sul lato client, gli unici dati inviati al server sono un indicatore che indica se il puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="19601-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="19601-115">Se il puntatore è diverso da **null**, la routine lato server riceve un puntatore valido a un blocco di memoria inizializzato con zeri.</span><span class="sxs-lookup"><span data-stu-id="19601-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="19601-116">Se il puntatore è **null**, la routine lato server riceve un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="19601-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="19601-117">In questa situazione, la dimensione massima del puntatore deve essere definita correttamente in fase di compilazione o in base ai parametri di input, perché il server deve allocare spazio per la posizione di memoria a cui punta.</span><span class="sxs-lookup"><span data-stu-id="19601-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="19601-118">Un puntatore di **\[ stringa \]** semplice, ad esempio, non ha una dimensione ben definita perché la stringa viene terminata in modo implicito da un carattere null.</span><span class="sxs-lookup"><span data-stu-id="19601-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="19601-119">In questo caso, se **\[ \_ si \]** specificano le dimensioni massime della stringa aggiungendo una dimensione, l'attributo otterrà il requisito di dimensione ben definito.</span><span class="sxs-lookup"><span data-stu-id="19601-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="19601-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="19601-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="19601-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="19601-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19601-122">**unico**</span><span class="sxs-lookup"><span data-stu-id="19601-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




