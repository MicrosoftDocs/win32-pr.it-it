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
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Tecniche IDL per una migliore progettazione di interfacce e metodi

Si consiglia di utilizzare le seguenti tecniche specifiche di IDL per migliorare la sicurezza e le prestazioni quando si sviluppano interfacce e metodi RPC che gestiscono dati sia conformi che Variant. Gli attributi a cui si fa riferimento in questo argomento sono gli attributi IDL impostati nei parametri del metodo che gestiscono dati conformi (ad esempio, la \[ **dimensione \_ è** \] e il \[ **numero massimo \_ è** \] attributi) o i dati Variant (ad esempio, la \[ **lunghezza \_ è** \] e \[  \] gli attributi stringa).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Utilizzo dell' \[ \] attributo Range con parametri dati conformi

L' \[  \] attributo Range indica al runtime RPC di eseguire la convalida delle dimensioni aggiuntiva durante il processo di unmarshalling dei dati. In particolare, verifica che le dimensioni fornite dei dati passati come parametro associato siano comprese nell'intervallo specificato.

L' \[ attributo di **intervallo** non \] influisce sul formato wire.

Se il valore in transito non è compreso nell'intervallo consentito, RPC genererà un' \_ eccezione RPC \_ x \_ binding non valido o un'eccezione di \_ \_ \_ dati stub non corretti RPC \_ . Questo fornisce un livello aggiuntivo di convalida dei dati e consente di evitare errori di sicurezza comuni, come i sovraccarichi del buffer. Analogamente, \[  \] l'utilizzo di range può migliorare le prestazioni dell'applicazione, poiché i dati conformi contrassegnati con esso hanno vincoli chiaramente definiti, disponibili per la considerazione da parte del servizio RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Regole di gestione della memoria stub del server RPC

Quando si creano i file IDL per un'applicazione abilitata per RPC, è importante comprendere le regole di gestione della memoria stub del server RPC. Le applicazioni possono migliorare l'utilizzo delle risorse del server usando l' \[ **intervallo** insieme \] ai dati conformi come indicato in precedenza, oltre a evitare intenzionalmente che l'applicazione di attributi IDL di dati a lunghezza variabile, ad esempio la \[ **lunghezza, \_ sia** \] conforme ai dati.

L'applicazione di \[ **lunghezza \_ è** \] per i campi della struttura di dati definiti in un file IDL non è consigliata.

## <a name="best-practices-for-variable-length-data-parameters"></a>Procedure consigliate per i parametri dei dati a lunghezza variabile

Di seguito sono riportate alcune procedure consigliate da considerare quando si definiscono gli attributi IDL per strutture di dati di dimensioni variabili, parametri di metodo e campi.

-   Usare la correlazione anticipata. In genere, è preferibile definire il parametro o il campo di dimensioni variabili in modo che si verifichi immediatamente dopo il tipo integrale di controllo.

    Ad esempio,

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    è meglio di

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    wherein **earlyCorr** dichiara il parametro size immediatamente prima del parametro dati a lunghezza variabile e **lateCorr** dichiara il parametro Size dopo di esso. L'utilizzo della corrispondenza anticipata consente di migliorare le prestazioni complessive, soprattutto nei casi in cui il metodo viene chiamato di frequente.

-   Per i parametri contrassegnati con \[ **out, Size \_ è** la \] tupla degli attributi e, in cui la lunghezza dei dati è nota sul lato client o in cui il client ha un limite superiore ragionevole, la definizione del metodo deve essere simile alla seguente in termini di attribuzione e sequenza dei parametri:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    In questo caso, il client fornisce un buffer a dimensione fissa per *Parr*, consentendo al servizio RPC sul lato server di allocare un buffer di dimensioni ragionevolmente con un buon livello di sicurezza. Si noti che nell'esempio i dati vengono ricevuti dal server ( \[ **out** \] ). La definizione è simile per i dati passati al server ( \[ **in** \] ).

-   Per le situazioni in cui il componente lato server di un'applicazione RPC decide la lunghezza dei dati, la definizione del metodo dovrebbe essere simile alla seguente:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **Con \_ intervallo LONG** è un tipo definito per gli stub client e server e di una dimensione specificata che il client può prevedere correttamente. Nell'esempio, il client passa *ppArr* come **null** e il componente applicazione server RPC alloca la quantità di memoria corretta. Al momento della restituzione, il servizio RPC sul lato client alloca la memoria per i dati restituiti.

-   Se il client vuole inviare al server un subset di una matrice conforme di grandi dimensioni, l'applicazione può specificare le dimensioni del subset come illustrato nell'esempio seguente:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    In questo modo, RPC trasmette solo gli elementi *lLength* della matrice attraverso la rete. Questa definizione impone tuttavia al servizio RPC di allocare memoria di dimensioni *lSize* sul lato server.

-   Se il componente dell'applicazione client determina la dimensione massima di una matrice che il server può restituire, ma consente al server di trasmettere un subset di tale matrice, l'applicazione può specificare tale comportamento definendo l'IDL simile all'esempio seguente:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    Il componente dell'applicazione client specifica la dimensione massima della matrice e il server specifica il numero di elementi trasmessi al client.

-   Se il componente dell'applicazione server deve restituire una stringa al componente dell'applicazione client e se il client conosce le dimensioni massime che devono essere restituite dal server, l'applicazione può usare un tipo di stringa conforme, come illustrato nell'esempio seguente:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Se il componente dell'applicazione client non deve controllare la dimensione della stringa, il servizio RPC può allocare la memoria in modo specifico, come illustrato nell'esempio seguente:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    Quando si chiama il metodo RPC, il componente dell'applicazione client deve impostare *ppStr* su **null** .

 

 




