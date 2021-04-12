---
title: Tecniche IDL per una migliore progettazione di interfacce e metodi
description: Si consiglia di utilizzare le seguenti tecniche specifiche di IDL per migliorare la sicurezza e le prestazioni quando si sviluppano interfacce e metodi RPC che gestiscono dati sia conformi che Variant.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395822"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="498a5-103">Tecniche IDL per una migliore progettazione di interfacce e metodi</span><span class="sxs-lookup"><span data-stu-id="498a5-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="498a5-104">Si consiglia di utilizzare le seguenti tecniche specifiche di IDL per migliorare la sicurezza e le prestazioni quando si sviluppano interfacce e metodi RPC che gestiscono dati sia conformi che Variant.</span><span class="sxs-lookup"><span data-stu-id="498a5-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="498a5-105">Gli attributi a cui si fa riferimento in questo argomento sono gli attributi IDL impostati nei parametri del metodo che gestiscono dati conformi (ad esempio, la \[ **dimensione \_ è** \] e il \[ **numero massimo \_ è** \] attributi) o i dati Variant (ad esempio, la \[ **lunghezza \_ è** \] e \[  \] gli attributi stringa).</span><span class="sxs-lookup"><span data-stu-id="498a5-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="498a5-106">Utilizzo dell' \[ \] attributo Range con parametri dati conformi</span><span class="sxs-lookup"><span data-stu-id="498a5-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="498a5-107">L' \[  \] attributo Range indica al runtime RPC di eseguire la convalida delle dimensioni aggiuntiva durante il processo di unmarshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="498a5-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="498a5-108">In particolare, verifica che le dimensioni fornite dei dati passati come parametro associato siano comprese nell'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="498a5-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="498a5-109">L' \[ attributo di **intervallo** non \] influisce sul formato wire.</span><span class="sxs-lookup"><span data-stu-id="498a5-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="498a5-110">Se il valore in transito non è compreso nell'intervallo consentito, RPC genererà un' \_ eccezione RPC \_ x \_ binding non valido o un'eccezione di \_ \_ \_ dati stub non corretti RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="498a5-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="498a5-111">Questo fornisce un livello aggiuntivo di convalida dei dati e consente di evitare errori di sicurezza comuni, come i sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="498a5-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="498a5-112">Analogamente, \[  \] l'utilizzo di range può migliorare le prestazioni dell'applicazione, poiché i dati conformi contrassegnati con esso hanno vincoli chiaramente definiti, disponibili per la considerazione da parte del servizio RPC.</span><span class="sxs-lookup"><span data-stu-id="498a5-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="498a5-113">Regole di gestione della memoria stub del server RPC</span><span class="sxs-lookup"><span data-stu-id="498a5-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="498a5-114">Quando si creano i file IDL per un'applicazione abilitata per RPC, è importante comprendere le regole di gestione della memoria stub del server RPC.</span><span class="sxs-lookup"><span data-stu-id="498a5-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="498a5-115">Le applicazioni possono migliorare l'utilizzo delle risorse del server usando l' \[ **intervallo** insieme \] ai dati conformi come indicato in precedenza, oltre a evitare intenzionalmente che l'applicazione di attributi IDL di dati a lunghezza variabile, ad esempio la \[ **lunghezza, \_ sia** \] conforme ai dati.</span><span class="sxs-lookup"><span data-stu-id="498a5-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="498a5-116">L'applicazione di \[ **lunghezza \_ è** \] per i campi della struttura di dati definiti in un file IDL non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="498a5-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="498a5-117">Procedure consigliate per i parametri dei dati a lunghezza variabile</span><span class="sxs-lookup"><span data-stu-id="498a5-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="498a5-118">Di seguito sono riportate alcune procedure consigliate da considerare quando si definiscono gli attributi IDL per strutture di dati di dimensioni variabili, parametri di metodo e campi.</span><span class="sxs-lookup"><span data-stu-id="498a5-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="498a5-119">Usare la correlazione anticipata.</span><span class="sxs-lookup"><span data-stu-id="498a5-119">Use early correlation.</span></span> <span data-ttu-id="498a5-120">In genere, è preferibile definire il parametro o il campo di dimensioni variabili in modo che si verifichi immediatamente dopo il tipo integrale di controllo.</span><span class="sxs-lookup"><span data-stu-id="498a5-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="498a5-121">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="498a5-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="498a5-122">è meglio di</span><span class="sxs-lookup"><span data-stu-id="498a5-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="498a5-123">wherein **earlyCorr** dichiara il parametro size immediatamente prima del parametro dati a lunghezza variabile e **lateCorr** dichiara il parametro Size dopo di esso.</span><span class="sxs-lookup"><span data-stu-id="498a5-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="498a5-124">L'utilizzo della corrispondenza anticipata consente di migliorare le prestazioni complessive, soprattutto nei casi in cui il metodo viene chiamato di frequente.</span><span class="sxs-lookup"><span data-stu-id="498a5-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="498a5-125">Per i parametri contrassegnati con \[ **out, Size \_ è** la \] tupla degli attributi e, in cui la lunghezza dei dati è nota sul lato client o in cui il client ha un limite superiore ragionevole, la definizione del metodo deve essere simile alla seguente in termini di attribuzione e sequenza dei parametri:</span><span class="sxs-lookup"><span data-stu-id="498a5-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="498a5-126">In questo caso, il client fornisce un buffer a dimensione fissa per *Parr*, consentendo al servizio RPC sul lato server di allocare un buffer di dimensioni ragionevolmente con un buon livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="498a5-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="498a5-127">Si noti che nell'esempio i dati vengono ricevuti dal server ( \[ **out** \] ).</span><span class="sxs-lookup"><span data-stu-id="498a5-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="498a5-128">La definizione è simile per i dati passati al server ( \[ **in** \] ).</span><span class="sxs-lookup"><span data-stu-id="498a5-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="498a5-129">Per le situazioni in cui il componente lato server di un'applicazione RPC decide la lunghezza dei dati, la definizione del metodo dovrebbe essere simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="498a5-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="498a5-130">**Con \_ intervallo LONG** è un tipo definito per gli stub client e server e di una dimensione specificata che il client può prevedere correttamente.</span><span class="sxs-lookup"><span data-stu-id="498a5-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="498a5-131">Nell'esempio, il client passa *ppArr* come **null** e il componente applicazione server RPC alloca la quantità di memoria corretta.</span><span class="sxs-lookup"><span data-stu-id="498a5-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="498a5-132">Al momento della restituzione, il servizio RPC sul lato client alloca la memoria per i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="498a5-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="498a5-133">Se il client vuole inviare al server un subset di una matrice conforme di grandi dimensioni, l'applicazione può specificare le dimensioni del subset come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="498a5-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="498a5-134">In questo modo, RPC trasmette solo gli elementi *lLength* della matrice attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="498a5-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="498a5-135">Questa definizione impone tuttavia al servizio RPC di allocare memoria di dimensioni *lSize* sul lato server.</span><span class="sxs-lookup"><span data-stu-id="498a5-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="498a5-136">Se il componente dell'applicazione client determina la dimensione massima di una matrice che il server può restituire, ma consente al server di trasmettere un subset di tale matrice, l'applicazione può specificare tale comportamento definendo l'IDL simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="498a5-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="498a5-137">Il componente dell'applicazione client specifica la dimensione massima della matrice e il server specifica il numero di elementi trasmessi al client.</span><span class="sxs-lookup"><span data-stu-id="498a5-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="498a5-138">Se il componente dell'applicazione server deve restituire una stringa al componente dell'applicazione client e se il client conosce le dimensioni massime che devono essere restituite dal server, l'applicazione può usare un tipo di stringa conforme, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="498a5-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="498a5-139">Se il componente dell'applicazione client non deve controllare la dimensione della stringa, il servizio RPC può allocare la memoria in modo specifico, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="498a5-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="498a5-140">Quando si chiama il metodo RPC, il componente dell'applicazione client deve impostare *ppStr* su **null** .</span><span class="sxs-lookup"><span data-stu-id="498a5-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




