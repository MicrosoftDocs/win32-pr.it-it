---
title: Gestione della memoria stub server
description: Gestione della memoria stub server
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Gestione della memoria stub server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873054"
---
# <a name="server-stub-memory-management"></a>Gestione della memoria stub server

## <a name="an-introduction-to-server-stub-memory-management"></a>Introduzione alla gestione della memoria Server-Stub

Gli stub generati da MIDL fungono da interfaccia tra un processo client e un processo server. Uno Stub client esegue il marshalling di tutti i dati passati ai parametri contrassegnati con l'attributo [**\[ in \]**](../midl/in.md) e li invia allo stub del server. Lo stub del server, alla ricezione di questi dati, ricostruisce lo stack di chiamate e quindi esegue la corrispondente funzione Server implementata dall'utente. Lo stub del server esegue anche il marshalling dei dati del parametro contrassegnati con l'attributo [**\[ out \]**](../midl/out-idl.md) e li restituisce all'applicazione client.

Il formato dei dati con marshalling a 32 bit utilizzato da MSRPC è una versione conforme della sintassi di trasferimento di rappresentazione dei dati di rete (NDR). Per ulteriori informazioni su questo formato, vedere [il sito Web del gruppo Apri](https://www.opengroup.org/). Per le piattaforme a 64 bit, è possibile usare un'estensione Microsoft 64-bit per la sintassi di trasferimento di NDR denominata NDR64 per ottenere prestazioni migliori.

## <a name="unmarshaling-inbound-data"></a>Unmarshalling dei dati in ingresso

In MSRPC, lo stub client esegue il marshalling di tutti i dati dei parametri contrassegnati come [**\[ in \]**](../midl/in.md) in un buffer continuo per la trasmissione allo stub del server. Allo stesso modo, lo stub del server esegue il marshalling di tutti i dati contrassegnati con l'attributo [**\[ out \]**](../midl/out-idl.md) in un buffer continuo per tornare allo stub del client. Sebbene il livello del protocollo di rete sotto RPC possa frammentare e packetize il buffer per la trasmissione, la frammentazione è trasparente per gli stub RPC.

L'allocazione di memoria per la creazione del frame di chiamata del server può essere un'operazione costosa. Lo stub del server tenterà di ridurre al minimo l'utilizzo della memoria superflua, se possibile, e si presuppone che la routine del server non liberi o allochi i dati contrassegnati con gli attributi [**\[ in \]**](../midl/in.md) uscita o in **\[ uscita \]** . Lo stub del server tenta di riutilizzare i dati nel buffer, quando possibile, per evitare la duplicazione non necessaria. La regola generale è che se il formato dei dati di cui è stato effettuato il marshalling corrisponde al formato di memoria, RPC utilizzerà i puntatori ai dati con marshalling anziché allocare memoria aggiuntiva per i dati formattati in modo identico.

Ad esempio, la chiamata RPC seguente viene definita con una struttura il cui formato con marshalling è identico al formato in memoria.

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

In questo caso, RPC non alloca memoria aggiuntiva per i dati a cui fa riferimento *plInStructure*. bensì semplicemente passa il puntatore ai dati di cui è stato eseguito il marshalling all'implementazione della funzione lato server. Lo stub del server RPC verifica il buffer durante il processo di unmarshalling se lo stub viene compilato usando il flag "-Solid", che è un'impostazione predefinita nella versione recente nmost del compilatore MIDL. RPC garantisce che i dati passati all'implementazione della funzione lato server siano validi.

Tenere presente che la memoria è allocata per *plOutStructure*, poiché nessun dato viene passato al server.

## <a name="memory-allocation-for-inbound-data"></a>Allocazione di memoria per i dati in ingresso

Possono verificarsi casi in cui lo stub del server alloca memoria per i dati dei parametri contrassegnati con gli attributi [**\[ in \]**](../midl/in.md) o in **\[ , out \]** . Questo errore si verifica quando il formato dei dati di cui è stato effettuato il marshalling è diverso dal formato di memoria o quando le strutture che costituiscono i dati di cui è stato eseguito il marshalling sono sufficientemente complesse e devono essere lette in modo atomico dallo stub del server RPC. Di seguito sono elencati alcuni casi comuni in cui è necessario allocare memoria per i dati ricevuti dallo stub del server.

-   I dati sono una matrice variabile o una matrice variabile conforme. Si tratta di matrici (o puntatori a matrici) la cui [**\[ lunghezza \_ è () \]**](../midl/length-is.md) o il [**\[ primo attributo \_ è \]**](../midl/first-is.md) impostato su di essi. In NDR viene effettuato il marshalling e la trasmissione solo del primo elemento di queste matrici. Nel frammento di codice seguente, ad esempio, per i dati passati nel parametro *PV* verrà allocata memoria.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   I dati sono una stringa di dimensioni o non conforme. Queste stringhe sono in genere puntatori a dati di tipo carattere contrassegnati con l'attributo [**\[ size \_ is () \]**](../midl/size-is.md) . Nell'esempio seguente, alla stringa passata alla funzione lato server **SizedString** verrà allocata la memoria, mentre la stringa passata alla funzione **NormalString** verrà riutilizzata.

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   I dati sono un tipo semplice le cui dimensioni della memoria sono diverse dalle dimensioni del marshalling, ad esempio **enum16** e **\_ \_ int3264**.
-   I dati sono definiti da una struttura il cui allineamento di memoria è inferiore a quello naturale, contiene uno qualsiasi dei tipi di dati sopra indicati o con riempimento di byte finale. Ad esempio, la struttura dei dati complessa seguente ha forzato l'allineamento a 2 byte e ha la spaziatura interna alla fine.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   I dati contengono una struttura che deve essere sottoposta a marshalling Field by Field. Questi campi includono i puntatori di interfaccia definiti nelle interfacce DCOM; puntatori ignorati; valori integer impostati con l'attributo di [**\[ \] intervallo**](../midl/range.md) . gli elementi delle matrici definite con il [**\[ \_ \] marshalling di rete**](../midl/wire-marshal.md), il [**\[ \_ \] marshalling dell'utente**](../midl/user-marshal.md), la [**\[ trasmissione \_ come \]**](../midl/transmit-as.md) e [**\[ rappresentano \_ \]**](../midl/represent-as.md) gli attributi e le strutture di dati complesse incorporate.
-   I dati contengono un'Unione, una struttura contenente un'Unione o una matrice di unioni. Viene eseguito il marshalling in transito solo del ramo specifico dell'Unione.
-   I dati contengono una struttura con una matrice conforme a più dimensioni con almeno una dimensione non fissa.
-   I dati contengono una matrice di strutture complesse.
-   I dati contengono una matrice di tipi di dati semplici, ad esempio **enum16** e **\_ \_ int3264**.
-   I dati contengono una matrice di puntatori Ref e Interface.
-   Ai dati è applicato un attributo [**\[ Force \_ allocate \]**](../midl/force-allocate.md) a un puntatore.
-   Ai dati è applicato un attributo [**\[ allocate (tutti i \_ nodi) \]**](../midl/allocate.md) a un puntatore.
-   Per i dati è stato applicato un attributo di [**\[ \_ conteggio \] byte**](../midl/byte-count.md) a un puntatore.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Sintassi di NDR64 e di trasferimento dei dati a 64 bit

Come indicato in precedenza, i dati a 64 bit vengono sottoposte a marshalling mediante una specifica sintassi di trasferimento a 64 bit denominata NDR64. Questa sintassi di trasferimento è stata sviluppata per risolvere il problema specifico che si verifica quando viene effettuato il marshalling di puntatori in un rapporto di MANCAto a 32 bit e trasmesso a uno stub server in una piattaforma a 64 bit. In questo caso, un puntatore a dati a 32 bit con marshalling non corrisponde a un bit a 64 bit e l'allocazione di memoria si verificherà in modo invariabilmente. Per creare un comportamento più coerente sulle piattaforme a 64 bit, Microsoft ha sviluppato una nuova sintassi di trasferimento denominata NDR64.

Di seguito è riportato un esempio che illustra questo problema:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Questa struttura, se sottoposta a marshalling, viene riutilizzata dallo stub del server in un sistema a 32 bit. Tuttavia, se lo stub del server risiede in un sistema a 64 bit, i dati con marshalling NDR hanno una lunghezza di 4 byte, ma le dimensioni della memoria richieste saranno 8. Di conseguenza, l'allocazione di memoria viene forzata e il riutilizzo del buffer si verifica raramente. NDR64 risolve questo problema rendendo le dimensioni del marshalling di un puntatore a 64 bit.

A differenza del NDR a 32 bit, i dati semplici Tyes, ad esempio **enum16** e **\_ \_ int3264** , non rendono una struttura o una matrice complessa in NDR64. Analogamente, i valori di riempimento finali non rendono una struttura complessa. I puntatori di interfaccia vengono trattati come puntatori univoci al livello superiore; di conseguenza, le strutture e le matrici che contengono puntatori di interfaccia non sono considerate complesse e non richiedono l'allocazione di memoria specifica per l'utilizzo.

## <a name="initializing-outbound-data"></a>Inizializzazione dei dati in uscita

Dopo l'unmarshalling di tutti i dati in ingresso, lo stub del server deve inizializzare i puntatori solo in uscita contrassegnati con l'attributo [**\[ out \]**](../midl/out-idl.md) .


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



Nella chiamata precedente lo stub del server deve inizializzare *plOutStructure* perché non era presente nei dati sottoposti a marshalling ed è un puntatore di [**\[ riferimento \]**](../midl/ref.md) implicito che deve essere reso disponibile all'implementazione della funzione server. Lo stub del server RPC Inizializza e azzera tutti i puntatori di solo riferimento di primo livello con l'attributo [**\[ out \]**](../midl/out-idl.md) . Tutti i puntatori di riferimento al di sotto di esso vengono inizializzati in modo ricorsivo. **\[ \]** La ricorsione viene arrestata in corrispondenza di tutti i puntatori con attributi [**\[ Unique \]**](../midl/unique.md) o [**\[ ptr \]**](../midl/ptr.md) impostati su di essi.

L'implementazione della funzione server non può modificare direttamente i valori di puntatore di primo livello e pertanto non può riallocarli. Nell'implementazione di **ProcessRpcStructure** precedente, ad esempio, il codice seguente non è valido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* è un valore dello stack e la relativa modifica non viene propagata a RPC. L'implementazione della funzione server può tentare di evitare l'allocazione tentando di liberare *plOutStructure*, il che potrebbe causare un danneggiamento della memoria. Lo stub del server alloca quindi spazio per il puntatore di primo livello nella memoria (nel caso di puntatore a puntatore) e una struttura semplice di primo livello la cui dimensione nello stack è inferiore al previsto.

In determinate circostanze, il client può specificare le dimensioni di allocazione della memoria del lato server. Nell'esempio seguente il client specifica le dimensioni dei dati in uscita nel parametro delle *dimensioni* in ingresso.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Dopo l'unmarshalling dei dati in ingresso, incluse le *dimensioni*, lo stub del server alloca un buffer per *PV* con una dimensione di "sizeof (Char) \* size". Dopo che lo spazio è stato allocato, lo stub del server Azzera il buffer. Si noti che in questo caso specifico lo stub alloca la memoria con l' **\_ utente MIDL \_ allocate ()**, perché la dimensione del buffer è determinata in fase di esecuzione.

Si tenga presente che, nel caso di interfacce DCOM, gli stub generati da MIDL potrebbero non essere necessari se il client e il server condividono lo stesso apartment COM o se **ICallFrame** è implementato. In questo caso, il server non può dipendere dal comportamento di allocazione e deve verificare in modo indipendente la memoria di dimensioni client.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementazioni di funzioni sul lato server e marshalling dei dati in uscita

Immediatamente dopo l'unmarshalling sui dati in ingresso e l'inizializzazione della memoria allocata per contenere dati in uscita, lo stub del server RPC esegue l'implementazione lato server della funzione chiamata dal client. Al momento, il server può modificare i dati contrassegnati in modo specifico con l'attributo **\[ in \] , out** e può popolare la memoria allocata per i dati in uscita (i dati contrassegnati con [**\[ out \]**](../midl/out-idl.md)).

Le regole generali per la manipolazione dei dati dei parametri con marshalling sono semplici: il server può allocare solo la nuova memoria o modificare la memoria allocata in modo specifico dallo stub del server. La riallocazione o il rilascio della memoria esistente per i dati può influire negativamente sui risultati e sulle prestazioni della chiamata di funzione e può essere molto difficile eseguire il debug.

Logicamente, il server RPC si trova in uno spazio di indirizzi diverso rispetto a quello del client e in genere può presumere che non condividono la memoria. Di conseguenza, l'implementazione della funzione server può utilizzare i dati contrassegnati con l'attributo [**\[ in \]**](../midl/in.md) come memoria "Scratch" senza influire sugli indirizzi di memoria del client. Detto questo, il server non deve tentare di riallocare o **rilasciare \[ \] i** dati, lasciando il controllo di tali spazi allo stub del server RPC.

In genere, l'implementazione della funzione server non deve riallocare o rilasciare i dati contrassegnati con l'attributo **\[ in, out \]** . Per i dati a dimensione fissa, la logica di implementazione della funzione può modificare direttamente i dati. Analogamente, per i dati a dimensione variabile, l'implementazione della funzione non deve modificare il valore del campo fornito all'attributo [**\[ size \_ is () \]**](../midl/size-is.md) . Modificare il valore del campo utilizzato per ridimensionare i dati in un buffer più piccolo o più grande restituito al client, che potrebbe non essere in grado di gestire la lunghezza anomala.

Se si verificano situazioni in cui la routine del server deve riallocare la memoria utilizzata dai dati contrassegnati con l'attributo **\[ in, out \]** , è possibile che l'implementazione della funzione lato server non sia in grado di stabilire se il puntatore fornito dallo stub è alla memoria allocata con l' **\_ utente MIDL \_ allocato ()** o il buffer Wire di cui è stato effettuato il marshalling. Per ovviare a questo problema, MS RPC può garantire che non si verifichino perdite di memoria o danneggiamenti se l'attributo [**\[ Force \_ allocate \]**](../midl/force-allocate.md) viene impostato sui dati. Quando si imposta **\[ Force \_ allocate \]** , lo stub del server alloca sempre memoria per il puntatore, sebbene l'avvertenza riduca le prestazioni per ogni utilizzo.

Quando la chiamata viene restituita dall'implementazione della funzione lato server, lo stub del server esegue il marshalling dei dati contrassegnati con l'attributo [**\[ out \]**](../midl/out-idl.md) e li invia al client. Tenere presente che lo stub non esegue il marshalling dei dati se l'implementazione della funzione lato server genera un'eccezione.

## <a name="releasing-allocated-memory"></a>Rilascio della memoria allocata

Lo stub del server RPC rilascerà la memoria dello stack dopo che la chiamata ha restituito dalla funzione sul lato server, indipendentemente dal fatto che si verifichi un'eccezione. Lo stub del server libera tutta la memoria allocata dallo stub e la memoria allocata con **l' \_ utente MIDL \_ allocate ()**. L'implementazione della funzione sul lato server deve sempre assegnare a RPC uno stato coerente, generando un'eccezione o restituendo un codice di errore. Se la funzione ha esito negativo durante il popolamento di strutture di dati complesse, deve garantire che tutti i puntatori puntino a dati validi o siano impostati su **null**.

Durante questo passaggio, lo stub del server libera tutta la memoria che non fa parte del buffer di cui è stato eseguito il marshalling che contiene [**\[ \] i dati.**](../midl/in.md) Un'eccezione a questo comportamento è costituita dai dati con l'attributo [**\[ allocate (non \_ gratuito) \]**](../midl/allocate.md) . lo stub del server non libera alcuna memoria associata a tali puntatori.

Quando lo stub del server rilascia la memoria allocata dallo stub e dall'implementazione della funzione, lo stub chiama una funzione di notifica specifica se viene specificato l'attributo [**\[ Notify \_ flag \]**](../midl/notify-flag.md) per determinati dati.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshalling di un elenco collegato tramite RPC, ad esempio


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



Nell'esempio precedente, il formato di memoria per **LINKEDLIST** sarà identico al formato wire di cui è stato effettuato il marshalling. Di conseguenza, lo stub del server non alloca memoria per l'intera catena di puntatori dati in *pin*. Invece, RPC riutilizza il buffer di trasmissione per l'intero elenco collegato. Allo stesso modo, lo stub non alloca memoria per la *piedinatura*, ma riutilizza il buffer di rete sottoposto a marshalling dal client.

Poiché la firma della funzione contiene un parametro in uscita, il *broncio*, lo stub del server alloca memoria per contenere i dati restituiti. La memoria allocata viene inizialmente azzerata, con **pNext** impostato su **null**. L'applicazione può allocare la memoria per un nuovo elenco collegato e puntare al *broncio* -> **pNext** . il *pin* e l'elenco collegato che contiene possono essere usati come area scratch, ma l'applicazione non deve modificare i puntatori pNext.

L'applicazione può modificare liberamente il contenuto dell'elenco collegato a cui punta la *piedinatura*, ma non deve modificare alcuno dei puntatori **pNext** , tantomeno il collegamento di primo livello. Se l'applicazione decide di abbreviare l'elenco collegato, non è in grado di stabilire se un determinato puntatore **pNext** collega tto a un buffer interno RPC o a un buffer allocato in modo specifico con l' **\_ utente MIDL \_ allocate ()**. Per risolvere questo problema, aggiungere una dichiarazione di tipo specifico per i puntatori di elenco collegati che forzano l'allocazione degli utenti, come illustrato nel codice riportato di seguito.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Questo attributo impone allo stub del server di allocare separatamente ogni nodo dell'elenco collegato e l'applicazione può liberare la parte abbreviata dell'elenco collegato chiamando l' **\_ utente MIDL \_ Free ()**. L'applicazione può quindi impostare in modo sicuro il puntatore **pNext** alla fine dell'elenco collegato appena abbreviato in **null**.

 

 