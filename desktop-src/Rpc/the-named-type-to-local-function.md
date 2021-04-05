---
title: Funzione named_type_to_local
description: Gli stub chiamano il \_ tipo denominato \_ nella \_ funzione locale per convertire i dati da un tipo trasmesso al tipo che sono presenti nell'applicazione.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044713"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="32394-104">Tipo denominato \_ \_ per la \_ funzione locale</span><span class="sxs-lookup"><span data-stu-id="32394-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="32394-105">Gli stub chiamano il **tipo denominato nella funzione \_ \_ \_ locale** per convertire i dati da un tipo trasmesso al tipo che sono presenti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32394-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="32394-106">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="32394-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="32394-107">Il primo parametro punta ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="32394-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="32394-108">La funzione imposta il secondo parametro in modo che punti ai dati presentati.</span><span class="sxs-lookup"><span data-stu-id="32394-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="32394-109">Il **\_ tipo denominato \_ per \_** la funzione locale deve gestire la memoria per il tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="32394-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="32394-110">La funzione deve allocare memoria per l'intera struttura di dati che inizia dall'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e la passa alla funzione).</span><span class="sxs-lookup"><span data-stu-id="32394-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="32394-111">Il valore del secondo parametro non può essere modificato durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="32394-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="32394-112">La funzione può modificare il contenuto in corrispondenza di tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="32394-112">The function can change the contents at that address.</span></span>

 

 




