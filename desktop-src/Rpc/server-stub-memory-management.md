---
title: Gestione della memoria dello stub del server
description: Gestione della memoria dello stub del server
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Gestione della memoria dello stub del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c772678e28a51c4d5162472bc7b0ef73e19888feefbd0e1890cb13f65650425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925188"
---
# <a name="server-stub-memory-management"></a>Gestione della memoria dello stub del server

## <a name="an-introduction-to-server-stub-memory-management"></a>Introduzione alla gestione Server-Stub memoria

Gli stub generati da MIDL fungono da interfaccia tra un processo client e un processo server. Uno stub client effettua il marshalling di tutti i dati passati ai parametri contrassegnati con l'attributo [**\[ in \]**](../midl/in.md) e li invia al server stub. Lo stub del server, alla ricezione di questi dati, ricostruisce lo stack di chiamate e quindi esegue la funzione server implementata dall'utente corrispondente. Lo stub del server effettua anche il marshalling dei dati dei parametri contrassegnati con [**\[ l'attributo out \]**](../midl/out-idl.md) e lo restituisce all'applicazione client.

Il formato dei dati con marshalling a 32 bit usato da MSRPC è una versione conforme della sintassi di trasferimento NDR (Network Data Representation). Per altre informazioni su questo formato, vedere [Il sito Web open group](https://www.opengroup.org/). Per le piattaforme a 64 bit, è possibile usare un'estensione Microsoft a 64 bit per la sintassi di trasferimento NDR denominata NDR64 per prestazioni migliori.

## <a name="unmarshaling-inbound-data"></a>Annullamento delmarsaling dei dati in ingresso

In MSRPC, lo stub client effettua il marshalling di tutti i dati dei parametri contrassegnati [**\[ come in in un \]**](../midl/in.md) buffer continuo per la trasmissione nello stub del server. Analogamente, lo stub del server effettua il marshalling di tutti i dati contrassegnati con [**\[ l'attributo out \]**](../midl/out-idl.md) in un buffer continuo per la restituzione allo stub client. Mentre il livello del protocollo di rete sotto RPC può frammentare e in pacchetto il buffer per la trasmissione, la frammentazione è trasparente agli stub RPC.

L'allocazione di memoria per la creazione del frame di chiamata del server può essere un'operazione costosa. Lo stub del server tenterà di ridurre al minimo l'utilizzo della memoria non necessario quando possibile e si presuppone che la routine del server non libera o rialloci i dati contrassegnati con gli attributi [**\[ in \]**](../midl/in.md) o **\[ in \]** out. Lo stub del server tenta di riutilizzare i dati nel buffer ogni volta che è possibile per evitare inutili duplicazioni. La regola generale è che se il formato dei dati di cui è stato effettuato il marshalling è lo stesso del formato di memoria, RPC userà puntatori ai dati sottoposti a marshalling anziché allocare memoria aggiuntiva per i dati formattati in modo identico.

Ad esempio, la chiamata RPC seguente viene definita con una struttura il cui formato di marshalling è identico al formato in memoria.

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

In questo caso, RPC non alloca memoria aggiuntiva per i dati a cui fa riferimento *plInStructure*; al contrario, passa semplicemente il puntatore ai dati di cui è stato effettuato il marshalling all'implementazione della funzione sul lato server. Lo stub del server RPC verifica il buffer durante il processo di unmarshaling se lo stub viene compilato usando il flag "-robust", ovvero un'impostazione predefinita nella versione più recente del compilatore MIDL. RPC garantisce che i dati passati all'implementazione della funzione sul lato server siano validi.

Tenere presente che la memoria viene allocata per *plOutStructure*, poiché non viene passato alcun dato al server.

## <a name="memory-allocation-for-inbound-data"></a>Allocazione di memoria per i dati in ingresso

Possono verificarsi casi in cui lo stub del server alloca memoria per i dati dei parametri contrassegnati con gli attributi [**\[ in \]**](../midl/in.md) o **\[ in out. \]** Ciò si verifica quando il formato dei dati di cui è stato effettuato il marshalling è diverso dal formato di memoria o quando le strutture che costituiscono i dati sottoposti a marshalling sono sufficientemente complesse e devono essere lette atomicamente dallo stub del server RPC. Di seguito sono elencati diversi casi comuni in cui la memoria deve essere allocata per i dati ricevuti dallo stub del server.

-   I dati sono una matrice variabile o una matrice variabile conforme. Si tratta di matrici (o puntatori alle matrici) con l'attributo [**\[ \_ length is() \]**](../midl/length-is.md) o il primo attributo [**\[ \_ is() \]**](../midl/first-is.md) impostato su di esse. Nel rapporto di mancato recapito viene effettuato il marshalling e la trasmissione solo del primo elemento di queste matrici. Nel frammento di codice seguente, ad esempio, i dati passati nel parametro *pv* avranno memoria allocata.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   I dati sono una stringa di dimensioni o una stringa non conforme. Queste stringhe sono in genere puntatori a dati di tipo carattere contrassegnati con [**\[ \_ \] l'attributo size is().**](../midl/size-is.md) Nell'esempio seguente la stringa passata alla funzione lato server **SizedString** avrà memoria allocata, mentre la stringa passata alla **funzione NormalString** verrà riutilizzata.

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

-   I dati sono un tipo semplice le cui dimensioni di memoria differiscono dalle dimensioni di cui è stato effettuato il marshalling, ad esempio **enum16** e **\_ \_ int3264.**
-   I dati sono definiti da una struttura il cui allineamento della memoria è inferiore all'allineamento naturale, contiene uno dei tipi di dati precedenti o ha una spaziatura interna in byte finale. Ad esempio, la struttura di dati complessa seguente ha forzato l'allineamento a 2 byte e ha spaziatura interna alla fine.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   I dati contengono una struttura di cui è necessario effettuare il marshalling campo per campo. Questi campi includono puntatori a interfaccia definiti nelle interfacce DCOM. puntatori ignorati; Valori integer impostati con l'attributo [**\[ \] range;**](../midl/range.md) [**\[ \_ \]**](../midl/wire-marshal.md)elementi di matrici definite con il marshalling wire, [**\[ il \_ marshalling \]**](../midl/user-marshal.md)dell'utente, [**\[ \_ \]**](../midl/transmit-as.md) la trasmissione come e la [**\[ rappresentazione \_ come \]**](../midl/represent-as.md) attributi e le strutture di dati complesse incorporate.
-   I dati contengono un'unione, una struttura contenente un'unione o una matrice di unioni. Viene effettuato il marshalling in transito solo del ramo specifico dell'unione.
-   I dati contengono una struttura con una matrice conforme multidimensionale con almeno una dimensione non fissa.
-   I dati contengono una matrice di strutture complesse.
-   I dati contengono una matrice di tipi di dati semplici, ad esempio **enum16** e **\_ \_ int3264.**
-   I dati contengono una matrice di puntatori di riferimento e di interfaccia.
-   Ai dati è applicato un [**\[ attributo force \_ allocate \]**](../midl/force-allocate.md) a un puntatore.
-   Ai dati è applicato un [**\[ attributo allocate(all \_ nodes) \]**](../midl/allocate.md) a un puntatore.
-   Ai dati è applicato un [**\[ attributo byte \_ count \]**](../midl/byte-count.md) a un puntatore.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Sintassi di trasferimento di dati e NDR64 a 64 bit

Come accennato in precedenza, i dati a 64 bit vengono marshalling usando una sintassi di trasferimento a 64 bit specifica denominata NDR64. Questa sintassi di trasferimento è stata sviluppata per risolvere il problema specifico che si verifica quando i puntatori vengono sottoposti a marshalling in NDR a 32 bit e trasmessi a uno stub server in una piattaforma a 64 bit. In questo caso, un puntatore dati a 32 bit sottoposto a marshalling non corrisponde a uno a 64 bit e l'allocazione di memoria si verificherà invariabilmente. Per creare un comportamento più coerente nelle piattaforme a 64 bit, Microsoft ha sviluppato una nuova sintassi di trasferimento denominata NDR64.

Un esempio che illustra questo problema è il seguente:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Questa struttura, in caso di marshalling, verrà riutilizzata dallo stub del server in un sistema a 32 bit. Tuttavia, se lo stub del server risiede in un sistema a 64 bit, i dati con marshalling NDR hanno una lunghezza di 4 byte, ma le dimensioni della memoria richieste saranno 8. Di conseguenza, l'allocazione di memoria viene forzata e raramente si verifica il riutilizzo del buffer. NDR64 risolve questo problema rendendo le dimensioni di marshalling di un puntatore a 64 bit.

A differenza del rapporto di mancato recapito a 32 bit, i dati semplici, ad esempio **enum16** e **\_ \_ int3264,** non rendono complessa una struttura o una matrice in NDR64. Analogamente, i valori del riquadro finale non rendono complessa una struttura. I puntatori a interfaccia vengono considerati come puntatori univoci al livello superiore. Di conseguenza, le strutture e le matrici contenenti puntatori a interfaccia non sono considerate complesse e non richiedono un'allocazione di memoria specifica per l'uso.

## <a name="initializing-outbound-data"></a>Inizializzazione dei dati in uscita

Dopo l'unmarshalling di tutti i dati in ingresso, lo stub del server deve inizializzare i puntatori solo in uscita contrassegnati con [**\[ l'attributo out. \]**](../midl/out-idl.md)


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



Nella chiamata precedente, lo stub del server deve inizializzare *plOutStructure* perché non era presente [**\[ \]**](../midl/ref.md) nei dati sottoposti a marshalling ed è un puntatore di riferimento implicito che deve essere reso disponibile per l'implementazione della funzione server. Lo stub del server RPC inizializza e azzera tutti i puntatori di primo livello solo riferimento con [**\[ l'attributo out. \]**](../midl/out-idl.md) Anche **\[ i puntatori \]** di riferimento out sottostanti vengono inizializzati in modo ricorsivo. La ricorsione si arresta in corrispondenza di qualsiasi puntatore con gli attributi [**\[ univoci \]**](../midl/unique.md) [**\[ o ptr \]**](../midl/ptr.md) impostati su di essi.

L'implementazione della funzione server non può modificare direttamente i valori dei puntatori di primo livello e pertanto non può riallocarli. Ad esempio, nell'implementazione di **ProcessRpcStructure** precedente, il codice seguente non è valido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* è un valore dello stack e la relativa modifica non viene propagata a RPC. L'implementazione della funzione server può tentare di evitare l'allocazione provando a liberare *plOutStructure*, che può causare il danneggiamento della memoria. Lo stub del server alloca quindi spazio per il puntatore di primo livello in memoria (nel caso di puntatore a puntatore) e una struttura semplice di primo livello le cui dimensioni nello stack sono inferiori al previsto.

Il client può, in determinate circostanze, specificare le dimensioni di allocazione della memoria sul lato server. Nell'esempio seguente il client specifica le dimensioni dei dati in uscita nel parametro delle *dimensioni* in ingresso.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Dopo l'unmarshalling dei dati in ingresso, incluse le dimensioni *,* lo stub del server alloca un buffer per *pv* con dimensioni "sizeof(char) \* size". Dopo l'allocazione dello spazio, lo stub del server azzera il buffer. Si noti che in questo caso specifico, lo stub alloca la memoria con **MIDL \_ user \_ allocate()**, poiché le dimensioni del buffer vengono determinate in fase di esecuzione.

Tenere presente che nel caso delle interfacce DCOM, gli stub generati da MIDL potrebbero non essere coinvolti affatto se il client e il server condividono lo stesso apartment COM o se viene implementato **ICallFrame.** In questo caso, il server non può dipendere dal comportamento di allocazione e deve verificare in modo indipendente la memoria di dimensioni client.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementazioni di funzioni lato server e marshalling dei dati in uscita

Immediatamente dopo l'unmarshalling sui dati in ingresso e l'inizializzazione della memoria allocata per contenere i dati in uscita, lo stub del server RPC esegue l'implementazione lato server della funzione chiamata dal client. Al momento, il server può modificare i dati contrassegnati in modo specifico con l'attributo **\[ in, out \]** e popolare la memoria allocata per i dati solo in uscita (i dati contrassegnati con [**\[ out \]**](../midl/out-idl.md)).

Le regole generali per la manipolazione dei dati dei parametri di marshalling sono semplici: il server può allocare solo nuova memoria o modificare la memoria allocata in modo specifico dallo stub del server. La riallocazione o il rilascio della memoria esistente per i dati può avere un impatto negativo sui risultati e sulle prestazioni della chiamata di funzione e può essere molto difficile eseguire il debug.

Logicamente, il server RPC risiede in uno spazio di indirizzi diverso rispetto al client e in genere si può presumere che non condividono memoria. Di conseguenza, l'implementazione della funzione server può usare i dati contrassegnati con [**\[ l'attributo in \]**](../midl/in.md) come memoria "scratch" senza influire sugli indirizzi di memoria del client. Detto questo, il server non deve tentare **\[ \]** di riallocare o rilasciare nei dati, lasciando il controllo di tali spazi allo stub del server RPC stesso.

In genere, l'implementazione della funzione server non deve riallocare o rilasciare i dati contrassegnati con **\[ l'attributo in, \] out.** Per i dati a dimensione fissa, la logica di implementazione della funzione può modificare direttamente i dati. Analogamente, per i dati di dimensioni variabili, l'implementazione della funzione non deve modificare il valore del campo fornito all'attributo [**\[ \_ \] size is().**](../midl/size-is.md) Modificare il valore del campo usato per ridimensionare i dati in un buffer più piccolo o più grande restituito al client che potrebbe non essere dotato per gestire la lunghezza anomala.

Se si verificano circostanze in cui la routine del server deve riallocare la memoria usata dai dati contrassegnati con l'attributo **\[ in, out, \]** è del tutto possibile che l'implementazione della funzione sul lato server non sappia se il puntatore fornito dallo stub è alla memoria allocata con **MIDL user \_ \_ allocate()** o il buffer cab sottoposto a marshalling. Per risolvere questo problema, MS RPC può garantire che non si verifichino perdite di memoria o danneggiamenti se l'attributo [**\[ \_ force allocate \]**](../midl/force-allocate.md) è impostato sui dati. Quando **\[ è \_ impostata \] l'allocazione** forzata, lo stub del server alloca sempre memoria per il puntatore, anche se l'avvertenza è che le prestazioni diminuiscono per ogni utilizzo.

Quando la chiamata viene restituita dall'implementazione della funzione sul lato server, lo stub del server effettua il marshalling dei dati contrassegnati con [**\[ l'attributo out \]**](../midl/out-idl.md) e li invia al client. Tenere presente che lo stub non effettua il marshalling dei dati se l'implementazione della funzione sul lato server genera un'eccezione.

## <a name="releasing-allocated-memory"></a>Rilascio della memoria allocata

Lo stub del server RPC rilascerà la memoria dello stack dopo che la chiamata è stata restituita dalla funzione sul lato server, indipendentemente dal fatto che si verifichi o meno un'eccezione. Lo stub del server libera tutta la memoria allocata dallo stub, nonché la memoria allocata con **midl \_ user \_ allocate()**. L'implementazione della funzione lato server deve sempre fornire a RPC uno stato coerente, generando un'eccezione o restituisce un codice di errore. Se la funzione ha esito negativo durante il popolamento di strutture di dati complesse, deve garantire che tutti i puntatori puntino a dati validi o siano impostati su **NULL.**

Durante questo passaggio, lo stub del server libera tutta la memoria che non fa parte del buffer sottoposto a marshalling contenente [**\[ \] nei**](../midl/in.md) dati. Un'eccezione a questo comportamento è data con [**\[ l'attributo allocate(don't \_ free) \]**](../midl/allocate.md) impostato su di essi. Lo stub del server non libera memoria associata a questi puntatori.

Dopo che lo stub del server rilascia la memoria allocata dallo stub e dall'implementazione della funzione, lo stub chiama una funzione di notifica specifica se l'attributo [**\[ \_ del flag \]**](../midl/notify-flag.md) di notifica è specificato per dati specifici.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshalling di un elenco collegato su RPC - Esempio


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



Nell'esempio precedente il formato di memoria per **LINKEDLIST** sarà identico al formato di rete sottoposto a marshalling. Di conseguenza, lo stub del server non alloca memoria per l'intera catena di puntatori ai dati in *pIn*. Rpc riutilizza invece il buffer di collegamento per l'intero elenco collegato. Analogamente, lo stub non alloca memoria per *pInOut*, ma riutilizza il buffer di collegamento sottoposto a marshalling dal client.

Poiché la firma della funzione contiene un parametro in uscita, *pOut*, lo stub del server alloca memoria per contenere i dati restituiti. La memoria allocata viene inizialmente azzerato, con **pNext** impostato su **NULL.** L'applicazione può allocare la memoria per un nuovo elenco collegato e puntare *pOut* -> **pNext** a esso. *pIn* e l'elenco collegato che contiene possono essere usati come area scratch, ma l'applicazione non deve modificare i puntatori pNext.

L'applicazione può modificare liberamente il contenuto dell'elenco collegato a cui punta *pInOut*, ma non deve modificare i puntatori **pNext,** ma solo il collegamento di primo livello stesso. Se l'applicazione decide di abbreviare l'elenco collegato, non può sapere se un dato puntatore **pNext** collega un buffer interno RPC o un buffer allocato in modo specifico con **midl \_ user \_ allocate().** Per risolvere questo problema, aggiungere una dichiarazione di tipo specifica per i puntatori a elenchi collegati che forzano l'allocazione dell'utente, come illustrato nel codice seguente.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Questo attributo forza lo stub del server ad allocare separatamente ogni nodo dell'elenco collegato e l'applicazione può liberare la parte abbreviata dell'elenco collegato chiamando **l'utente MIDL \_ \_ free().** L'applicazione può quindi impostare in modo sicuro il puntatore **pNext** alla fine dell'elenco collegato appena abbreviato su **NULL.**

 

 