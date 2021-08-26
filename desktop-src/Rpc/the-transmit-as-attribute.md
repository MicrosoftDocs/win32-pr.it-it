---
title: Attributo transmit_as
description: L'attributo \ transmit as\ consente di controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso \ 8212, senza preoccuparsi delle dimensioni dei dati o dello scambio di byte in un ambiente \_ eterogeneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Chiamata di procedura remota RPC, attributi, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617422c50bae46de72bac1e548b6f248b19d0cb2436ac0c08b265bbba4f5a6cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016641"
---
# <a name="the-transmit_as-attribute"></a>Trasmetti \_ come attributo

L'attributo transmit as consente di controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso, ovvero senza preoccuparsi delle dimensioni dei dati o dello scambio di byte in un ambiente **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** eterogeneo. Consentendo di ridurre la quantità di dati trasmessi in rete, la trasmissione **\[ \_ come \]** attributo può rendere l'applicazione più efficiente.

Usare **\[ l'attributo transmit \_ as \]** per specificare un tipo di dati che gli stub RPC trasmetteranno in rete invece di usare il tipo di dati fornito dall'applicazione. Vengono fornite routine che convertono il tipo di dati in e dal tipo utilizzato per la trasmissione. È anche necessario fornire routine per liberare la memoria usata per il tipo di dati e il tipo trasmesso. Ad esempio, l'esempio seguente **definisce il tipo xmit \_** come tipo di dati trasmesso per tutti i dati dell'applicazione specificati come di **tipo \_ spec**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

Nella tabella seguente vengono descritti i quattro nomi di routine forniti dal programmatore. **Tipo** è il tipo di dati noto all'applicazione e **il tipo xmit \_** è il tipo di dati usato per la trasmissione.



| Routine                                                 | Descrizione                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**type \_ to \_ xmit**](the-type-to-xmit-function.md)     | Alloca un oggetto del tipo trasmesso ed esegue la conversione dal tipo di applicazione al tipo trasmesso in rete (chiamante e oggetto chiamato). |
| [**Tipo \_ da \_ xmit**](the-type-from-xmit-function.md) | Esegue la conversione dal tipo trasmesso al tipo di applicazione (chiamante e oggetto chiamato).                                                                  |
| [**Digitare \_ free \_ inst**](the-type-free-inst-function.md) | Libera le risorse usate dal tipo di applicazione (solo oggetto chiamato).                                                                              |
| [**Digitare \_ free \_ xmit**](the-type-free-xmit-function.md) | Libera l'archiviazione restituita dal **tipo alla** routine _\__ *_\_ xmit_* (chiamante e oggetto chiamato).                                                      |



 

Oltre a queste quattro funzioni fornite dal programmatore, il tipo trasmesso non viene modificato dall'applicazione. Il tipo trasmesso viene definito solo per spostare i dati in rete. Dopo la conversione dei dati nel tipo usato dall'applicazione, viene liberata la memoria usata dal tipo trasmesso.

Queste routine fornite dal programmatore vengono fornite dal client o dall'applicazione server in base agli attributi direzionali. Se il parametro è **\[** [**solo in**](/windows/desktop/Midl/in) **\]** , il client trasmette al server. Il client deve avere il **tipo \_ per \_ xmit** e **le funzioni \_ \_ xmit** gratuite. Il server richiede il **tipo dalle funzioni \_ \_ inst xmit** **e \_ \_ type free.** Per un **\[** [**parametro out**](/windows/desktop/Midl/out-idl) **\]** -only, il server trasmette al client. L'applicazione server deve implementare il tipo per le funzioni xmit e **\_ \_** **\_ \_ xmit** gratuite, mentre il programma client deve fornire il **tipo dalla funzione \_ \_ xmit.** Per gli oggetti di tipo **xmit \_** temporanei, lo stub chiamerà il tipo _\__ *_\_ free xmit_* per liberare la memoria allocata da una chiamata al tipo **a \_ \_ xmit**.

Alcune linee guida si applicano all'istanza del tipo di applicazione. Se il tipo di applicazione è un puntatore o contiene un puntatore, il tipo dalla routine \_ **\_ xmit** deve allocare memoria per i dati a cui puntano i puntatori (l'oggetto tipo di applicazione stesso viene modificato dallo stub nel modo consueto).

Per **\[ out \]** e **\[ in, out \] \]** parametri o uno dei relativi **\[ \_ \]** componenti, di un tipo che contiene la trasmissione come attributo, la routine \_ **\_ inst** type free viene chiamata automaticamente per gli oggetti dati che hanno l'attributo . Per **i parametri** in , la routine  \_ **\_ inst** libera dal tipo viene chiamata solo se l'attributo transmit **\[ \_ as \]** è stato applicato al parametro . Se l'attributo è stato applicato ai componenti del parametro, **la** \_ routine **\_ inst** type free non viene chiamata. Non sono presenti chiamate di liberatura per i dati incorporati e al massimo una chiamata (correlata all'attributo di primo livello) per un solo parametro **in** .

Efficace con MIDL 2.0, sia client che server devono fornire tutte e quattro le funzioni. Ad esempio, un elenco collegato può essere trasmesso come matrice di dimensioni. Il tipo da utilizzare per la routine **\_ \_ xmit** consente di visualizzare l'elenco collegato e copiare i dati ordinati in una matrice. Gli elementi della matrice vengono ordinati in modo che non sia necessario trasmettere i numerosi puntatori associati alla struttura dell'elenco. Il tipo della routine **\_ \_ xmit** legge la matrice e inserisce i relativi elementi in una struttura di elenco collegato.

L'elenco a collegamento doppio (DOUBLE LINK LIST) include dati e \_ \_ puntatori agli elementi dell'elenco precedente e successivo:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Anziché inviare la struttura complessa, è possibile usare **\[** [**l'attributo transmit \_ as**](/windows/desktop/Midl/transmit-as) per **\]** inviarlo in rete come matrice. La sequenza di elementi nella matrice mantiene l'ordinamento degli elementi nell'elenco a un costo inferiore:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

**\[ L'attributo transmit \_ as \]** viene visualizzato nel file IDL:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

Nell'esempio seguente **ModifyListProc** definisce il parametro di tipo DOUBLE \_ LINK TYPE come parametro \_ **\[ in, out: \]**

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Le quattro funzioni definite dal programmatore usano il nome del tipo nei nomi delle funzioni e usano i tipi presentati e trasmessi come tipi di parametro, in base alle esigenze:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 