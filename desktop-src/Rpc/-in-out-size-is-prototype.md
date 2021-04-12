---
title: " in, out, size_is prototipo"
description: '\ in, out, Size \_ is \ Prototype usa una matrice di caratteri a valore singolo che viene passata da client a server e da server a client.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337791"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="985ff-103">\[in, out, dimensioni \_ è un \] prototipo</span><span class="sxs-lookup"><span data-stu-id="985ff-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="985ff-104">Il prototipo di funzione seguente usa una matrice di caratteri a conteggio singolo che viene passata in entrambi i modi: da client a server e da server a client:</span><span class="sxs-lookup"><span data-stu-id="985ff-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="985ff-105">Come parametro \[ [**in**](/windows/desktop/Midl/in) \] , *achInOut* deve puntare a un archivio valido sul lato client.</span><span class="sxs-lookup"><span data-stu-id="985ff-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="985ff-106">Prima di eseguire la chiamata di procedura remota, lo sviluppatore alloca memoria associata alla matrice sul lato client.</span><span class="sxs-lookup"><span data-stu-id="985ff-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="985ff-107">Gli stub utilizzano le \[ [**dimensioni \_**](/windows/desktop/Midl/size-is) del \] parametro *strsize* per allocare la memoria sul server e quindi utilizzano la \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) il \] parametro *pcbSize* per trasmettere gli elementi della matrice in questa memoria.</span><span class="sxs-lookup"><span data-stu-id="985ff-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="985ff-108">Lo sviluppatore deve assicurarsi che il codice client imposti la **\[ lunghezza \_ sia \]** variabile prima di chiamare la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="985ff-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="985ff-109">In alcune situazioni, l'uso di parametri distinti anziché di una singola stringa per l'input e l'output è più efficiente e garantisce flessibilità.</span><span class="sxs-lookup"><span data-stu-id="985ff-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="985ff-110">Questa operazione è illustrata nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="985ff-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="985ff-111">Nell'esempio precedente, la matrice di caratteri achInOut viene usata anche come parametro \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="985ff-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="985ff-112">In C, il nome della matrice è equivalente all'utilizzo di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="985ff-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="985ff-113">Per impostazione predefinita, tutti i puntatori di primo livello sono puntatori di riferimento, ma non cambiano nel valore e puntano alla stessa area di memoria sul client prima e dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="985ff-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="985ff-114">Tutta la memoria a cui accede la procedura remota deve adattarsi alla dimensione specificata dal client prima della chiamata. in alternativa, gli stub genereranno un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="985ff-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="985ff-115">Prima di restituire, la funzione Analyze sul server deve reimpostare il parametro *pcbSize* per indicare il numero di elementi che il server trasmetterà al client, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="985ff-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 