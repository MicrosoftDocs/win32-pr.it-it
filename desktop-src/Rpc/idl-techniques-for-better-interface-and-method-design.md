---
title: Tecniche IDL per una migliore progettazione di interfacce e metodi
description: È consigliabile usare le tecniche specifiche di IDL seguenti per migliorare la sicurezza e le prestazioni quando si sviluppano interfacce e metodi RPC che gestiscono sia dati conformi che variant.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3608e908742d4de4b6564787c6d8faffc29efcef81549ff50414cc7716c468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929427"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Tecniche IDL per una migliore progettazione di interfacce e metodi

È consigliabile usare le tecniche specifiche di IDL seguenti per migliorare la sicurezza e le prestazioni quando si sviluppano interfacce e metodi RPC che gestiscono sia dati conformi che variant. Gli attributi a cui si fa riferimento in questo argomento sono gli attributi IDL impostati sui parametri del metodo che gestiscono i dati conformi (ad esempio, le dimensioni sono e max è attributes) o i dati \[ **\_** \] variant \[ **\_** \] (ad esempio, \[ **\_** \] \[  \] la lunghezza è e gli attributi stringa).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Uso \[ dell'attributo \] range con parametri di dati conformi

L'attributo range indica al run-time RPC di eseguire una convalida aggiuntiva delle dimensioni \[  \] durante il processo di unmarshaling dei dati. In particolare, verifica che la dimensione fornita dei dati passati come parametro associato sia all'interno dell'intervallo specificato.

\[ **L'attributo range** \] non influisce sul formato wire.

Se il valore in transito non è compreso nell'intervallo consentito, RPC genererà un'eccezione RPC X INVALID BOUND o \_ \_ RPC X BAD \_ \_ \_ \_ STUB \_ DATA. Ciò offre un livello aggiuntivo di convalida dei dati e consente di evitare errori di sicurezza comuni, ad esempio sovraccarichi del buffer. Analogamente, l'uso dell'intervallo può migliorare le prestazioni dell'applicazione, poiché i dati conformi contrassegnati con hanno vincoli chiaramente definiti che possono essere considerati \[  \] dal servizio RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Regole di gestione della memoria stub del server RPC

È importante comprendere le regole di gestione della memoria stub del server RPC quando si creano i file IDL per un'applicazione abilitata per RPC. Le applicazioni possono migliorare l'utilizzo delle risorse del server usando l'intervallo in combinazione con i dati conformi come indicato in precedenza, nonché evitando intenzionalmente l'applicazione di attributi IDL dei dati a lunghezza variabile, ad esempio la lunghezza è per i dati \[  \] \[ **\_** \] conformi.

L'applicazione \[ **della \_ lunghezza** \] ai campi della struttura di dati definiti in un file IDL non è consigliata.

## <a name="best-practices-for-variable-length-data-parameters"></a>Procedure consigliate per i parametri di dati a lunghezza variabile

Di seguito sono riportate diverse procedure consigliate da considerare quando si definiscono gli attributi IDL per strutture di dati, parametri di metodo e campi di dimensioni variabili.

-   Usare la correlazione anticipata. In genere è consigliabile definire il parametro o il campo delle dimensioni della variabile in modo che si verifichi immediatamente dopo il controllo del tipo integrale.

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

    dove **earlyCorr** dichiara il parametro size immediatamente prima del parametro di dati a lunghezza variabile e **lateCorr** dichiara il parametro size dopo di esso. L'uso della corrispondenza anticipata migliora le prestazioni complessive, soprattutto nei casi in cui il metodo viene chiamato di frequente.

-   Per i parametri contrassegnati con \[ **out, size \_** è tupla di attributi e dove la lunghezza dei dati è nota sul lato client o in cui il client ha un limite superiore ragionevole, la definizione del metodo deve essere simile alla seguente in termini di attribuzione dei parametri e \] sequenza:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    In questo caso, il client fornisce un buffer di dimensioni fisse per *pArr*, consentendo al servizio RPC sul lato server di allocare un buffer di dimensioni ragionevoli con un buon livello di garanzia. Si noti che nell'esempio i dati vengono ricevuti dal server ( \[ **out** \] ). La definizione è simile per i dati passati al server ( \[ **in** \] ).

-   Per le situazioni in cui il componente lato server di un'applicazione RPC decide la lunghezza dei dati, la definizione del metodo deve essere simile alla seguente:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **RANGED \_ LONG** è un tipo definito per gli stub client e server e di dimensioni specificate che il client può prevedere correttamente. Nell'esempio il client passa *ppArr* come **NULL** e il componente applicazione server RPC alloca la quantità corretta di memoria. Al momento della restituzione, il servizio RPC sul lato client alloca la memoria per i dati restituiti.

-   Se il client vuole inviare un subset di una matrice conforme di grandi dimensioni al server, l'applicazione può specificare le dimensioni del subset, come illustrato nell'esempio seguente:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    In questo modo RPC *trasmetterà solo gli elementi lLength* della matrice in transito. Questa definizione impone tuttavia al servizio RPC di allocare memoria *di dimensioni lSize* sul lato server.

-   Se il componente dell'applicazione client determina le dimensioni massime di una matrice che il server può restituire, ma consente al server di trasmettere un subset di tale matrice, l'applicazione può specificare tale comportamento definendo il linguaggio IDL simile all'esempio seguente:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    Il componente dell'applicazione client specifica le dimensioni massime della matrice e il server specifica il numero di elementi che trasmette al client.

-   Se il componente dell'applicazione server deve restituire una stringa al componente dell'applicazione client e se il client conosce le dimensioni massime da restituire dal server, l'applicazione può usare un tipo di stringa conforme, come illustrato nell'esempio seguente:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Se il componente dell'applicazione client non deve controllare le dimensioni della stringa, il servizio RPC può allocare in modo specifico la memoria, come illustrato nell'esempio seguente:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    Il componente dell'applicazione client deve *impostare ppStr* su **NULL** quando si chiama il metodo RPC.

 

 




