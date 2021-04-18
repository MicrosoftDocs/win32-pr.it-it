---
title: Attributo transmit_as
description: L'attributo \ trasmette \_ come \ consente di controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso, ovvero senza doversi preoccupare delle dimensioni dei dati o dello scambio di byte in un ambiente eterogeneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, attributi, transmit_as di procedura remota
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399421"
---
# <a name="the-transmit_as-attribute"></a>Attributo trasmissione \_ As

L' **\[** attributo [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) **\]** offre un modo per controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso, ovvero senza preoccuparsi delle dimensioni dei dati o dello scambio di byte in un ambiente eterogeneo. Consentendo di ridurre la quantità di dati trasmessi in rete, l'attributo **\[ trasmissione \_ come \]** può rendere più efficiente l'applicazione.

Utilizzare l'attributo **\[ trasmissione \_ As \]** per specificare un tipo di dati che gli stub RPC trasmetteranno sulla rete anziché utilizzare il tipo di dati fornito dall'applicazione. Vengono fornite routine che convertono il tipo di dati da e verso il tipo utilizzato per la trasmissione. È inoltre necessario specificare routine per liberare la memoria utilizzata per il tipo di dati e il tipo trasmesso. Ad esempio, di seguito viene definito il **\_ tipo Xmit** come tipo di dati trasmesso per tutti i dati dell'applicazione specificati come tipo **\_ spec**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

Nella tabella seguente vengono descritti i quattro nomi di routine forniti dal programmatore. Il **tipo è il** tipo di dati noto all'applicazione e **Xmit \_ tipo** è il tipo di dati utilizzato per la trasmissione.



| Routine                                                 | Descrizione                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Digitare \_ per \_ Xmit**](the-type-to-xmit-function.md)     | Alloca un oggetto del tipo trasmesso e viene convertito dal tipo di applicazione al tipo trasmesso sulla rete (chiamante e oggetto chiamato). |
| [**Digitare \_ da \_ Xmit**](the-type-from-xmit-function.md) | Esegue la conversione dal tipo trasmesso al tipo di applicazione (chiamante e oggetto denominato).                                                                  |
| [**Digitare \_ Free \_ inst**](the-type-free-inst-function.md) | Libera le risorse utilizzate dal tipo di applicazione (solo oggetto chiamato).                                                                              |
| [**Digitare \_ Free \_ Xmit**](the-type-free-xmit-function.md) | Libera lo spazio di archiviazione restituito dal **tipo ***\_*** alla routine \_ Xmit** (chiamante e oggetto chiamato).                                                      |



 

Oltre a queste quattro funzioni fornite dal programmatore, il tipo trasmesso non viene modificato dall'applicazione. Il tipo trasmesso viene definito solo per lo spostamento dei dati sulla rete. Dopo la conversione dei dati nel tipo utilizzato dall'applicazione, la memoria utilizzata dal tipo trasmesso viene liberata.

Queste routine fornite dal programmatore vengono fornite dal client o dall'applicazione server basata sugli attributi direzionali. Se il parametro è **\[** solo [**in**](/windows/desktop/Midl/in) **\]** , il client trasmette al server. Il client richiede **che il \_ tipo \_ Xmit** e **digiti le funzioni \_ \_ Xmit gratuite** . Il server richiede il **tipo \_ di \_ Xmit** e **digita le funzioni \_ \_ inst gratuite** . Per un **\[** [](/windows/desktop/Midl/out-idl) **\]** parametro di sola uscita, il server trasmette al client. L'applicazione server deve implementare il **tipo \_ in \_ Xmit** e **digitare \_ funzioni \_ Xmit gratuite** , mentre il programma client deve fornire il **tipo \_ dalla funzione \_ Xmit** . Per gli oggetti **di \_ tipo Xmit** temporaneo, lo stub chiamerà **il ***\_*** tipo Free \_ Xmit** per liberare la memoria allocata da una chiamata al **tipo \_ a \_ Xmit**.

Alcune linee guida si applicano all'istanza del tipo di applicazione. Se il tipo di applicazione è un puntatore o contiene un puntatore, il **tipo** \_ **dalla routine \_ Xmit** deve allocare memoria per i dati a cui puntano i puntatori (l'oggetto del tipo di applicazione stesso viene modificato dallo stub nel modo consueto).

Per **\[ out \]** e **\[ in, parametri \] out \]** out o uno dei rispettivi componenti di un tipo che contiene l'attributo **\[ trasmissione \_ As \]** , la routine  \_ **\_ inst gratuita** del tipo viene chiamata automaticamente per gli oggetti dati che hanno l'attributo. Per i parametri **in** , la \_ **routine \_ inst Free** del tipo viene chiamata solo se l'attributo **\[ trasmissione \_ \] As** è stato applicato al parametro. Se l'attributo è stato applicato ai componenti del parametro, la  \_ routine **\_ inst Free** del tipo non viene chiamata. Non sono disponibili chiamate gratuite per i dati incorporati e una chiamata al massimo uno (correlato all'attributo di primo livello) **per un solo** parametro.

A partire da MIDL 2,0, sia il client che il server devono fornire tutte e quattro le funzioni. Un elenco collegato, ad esempio, può essere trasmesso come matrice di dimensioni. Il **tipo \_ per \_** la routine Xmit esamina l'elenco collegato e copia i dati ordinati in una matrice. Gli elementi della matrice vengono ordinati in modo che i molti puntatori associati alla struttura elenco non debbano essere trasmessi. Il **tipo \_ dalla routine \_ Xmit** legge la matrice e inserisce i relativi elementi in una struttura di elenco collegato.

L'elenco \_ a collegamento doppio ( \_ elenco di collegamenti doppi) include i dati e i puntatori agli elementi elenco precedente e successivo:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Anziché spedire la struttura complessa, l' **\[** attributo [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) **\]** può essere usato per inviarlo tramite la rete come matrice. La sequenza di elementi nella matrice mantiene l'ordine degli elementi nell'elenco a un costo inferiore:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

L'attributo **\[ trasmissione \_ come \]** viene visualizzato nel file IDL:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

Nell'esempio seguente **ModifyListProc** definisce il parametro di tipo Double \_ link \_ come parametro **\[ in, out \]** :

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Le quattro funzioni definite dal programmatore utilizzano il nome del tipo nei nomi di funzione e utilizzano i tipi presentati e trasmessi come tipi di parametro, come richiesto:

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

 

 