---
title: Descrittori di correlazione
description: Un descrittore di correlazione è una stringa di formato che descrive un'espressione basata su un argomento correlato a un altro argomento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872894"
---
# <a name="correlation-descriptors"></a>Descrittori di correlazione

Un descrittore di correlazione è una stringa di formato che descrive un'espressione basata su un argomento correlato a un altro argomento. È necessario un descrittore di correlazione per la gestione della semantica relativa a attributi come \[ **size \_ is ()** \] , \[ **length \_ is ()** \] , \[ **Switch \_ is ()** \] ed \[ **IID \_ è ()** \] . I descrittori di correlazione vengono utilizzati con matrici, puntatori dimensionati, unioni e puntatori di interfaccia. Il valore dell'espressione finale può essere una dimensione, una lunghezza, un discriminante di Unione o un puntatore a un IID, rispettivamente. In termini di stringhe di formato, i descrittori di correlazione vengono utilizzati con matrici, unioni e puntatori di interfaccia. Un puntatore ridimensionato viene descritto in formato stringhe come puntatore a una matrice.

Sono disponibili due routine che eseguono i calcoli delle espressioni di base: NdrpComputeConformance viene usato per le dimensioni, i commutatori e l'IID \* mentre NdrpComputeVariance viene usato per lunghezze. Esiste anche una singola routine per eseguire una convalida del valore di correlazione per la funzionalità di negazione di attacco.

I descrittori di correlazione sono stati progettati per supportare solo espressioni molto limitate. Per situazioni complesse, il compilatore genera una routine di valutazione dell'espressione che verrà chiamata dal motore quando necessario.

Un descrittore di correlazione ha il formato seguente:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

Il tipo di correlazione del descrittore di correlazione \_<1> è costituito da due stuzzichini: i 4 bit superiori descrivono dove è possibile trovare l'espressione e i 4 bit inferiori descrivono il tipo del valore dell'espressione.

Il bocconcino superiore può avere uno dei cinque valori seguenti:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformità normale \_ FC
</dt> <dd>

Un caso normale di conformità, ad esempio quello descritto in un campo di una struttura.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformità del puntatore FC \_
</dt> <dd>

Per i puntatori con attributi (**size \_ è ()**, **length \_ è ()**) che sono campi in una struttura. Ciò influiscono sul modo in cui viene impostato il puntatore di memoria di base.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformità di \_ livello \_ superiore FC
</dt> <dd>

Per la conformità di primo livello descritta da un altro parametro.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformità MULTIlivello FC di primo livello \_ \_
</dt> <dd>

Per la conformità di primo livello di una matrice multidimensionale descritta da un altro parametro.

> [!Note]  
> Le matrici e i puntatori di dimensioni multidimensionali attivano un'opzione a [**-Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>\_conformità costante \_ FC
</dt> <dd>

Per un valore costante. Il compilatore Precalcola il valore di un'espressione costante fornita dall'utente. Quando questo è il caso, i 3 byte successivi nella descrizione della conformità contengono i 3 byte inferiori di un valore Long che descrive le dimensioni della conformità. Non è necessario alcun calcolo ulteriore.

</dd> </dl>

Il morso inferiore fornisce il tipo di valore che deve essere estratto dalla memoria:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> le espressioni a 64 bit non sono supportate. FC \_ Hyper viene usato solo per **IID \_ è ()** su piattaforme a 64 bit per estrarre il valore del puntatore per IID \* .
>
> Il compilatore imposta il tipo rosicchia su zero per i casi seguenti: espressione costante menzionata sopra e quando deve essere chiamata la routine dell'espressione di valutazione, ad esempio quando \_ vengono usati la conformità della costante FC \_ e il \_ callback FC.

 

Il \_ campo dimensioni è \_ op<1> consente di applicare una delle operazioni seguenti alla variabile di conformità:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

La \_ costante di DEreferenziazione FC viene utilizzata per la correlazione di un puntatore, ad esempio per **\[ size \_ is ( \* pl) \]**. Gli operatori aritmetici usano solo la costante indicata. La \_ costante di callback FC indica che deve essere chiamata una routine di valutazione dell'espressione.

Il campo Offset<2> è in genere un offset relativo della memoria rispetto alla variabile dell'argomento Expression. Può anche essere un indice di routine di valutazione dell'espressione. Come indicato in precedenza in questo documento, per le espressioni costanti è parte del valore dell'espressione finale effettivo.

L'interpretazione dell'offset<2> campo come offset della memoria dipende dalla complessità dell'espressione, dalla posizione della variabile di espressione e, nel caso di una matrice, se la matrice è effettivamente un puntatore con attributi.

Se la matrice è un puntatore con attributi e la variabile di conformità è un campo di una struttura, il campo Offset contiene l'offset dall'inizio della struttura al campo di conformità. Se la matrice non è un puntatore con attributi e la variabile di conformità è un campo di una struttura, il campo Offset contiene l'offset dalla fine della parte non conforme della struttura al campo descrittivo di conformità. In genere, la matrice conforme è alla fine della struttura.

Per la conformità di primo livello, il campo Offset contiene l'offset dalla posizione del primo parametro dello stub nello stack al parametro che descrive la conformità. Questa operazione non viene utilizzata in modalità **-sistema operativo** . Esistono altre eccezioni all'interpretazione del campo offset. tali eccezioni sono descritte nella descrizione di tali tipi.

Quando offset<2> viene usato con il \_ callback FC, contiene un indice nella tabella di routine di valutazione dell'espressione generata dal compilatore. Il messaggio stub viene passato alla routine di valutazione, che quindi calcola il valore di conformità e lo assegna al campo MaxCount del messaggio stub.

\_È stato aggiunto il campo Solid flags<2> per Windows 2000 per il supporto di [**/robust**](/windows/desktop/Midl/-robust), ad esempio la funzionalità Denial of attacks. Il primo byte definisce i flag seguenti:

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

Il flag Early indica una correlazione anticipata rispetto alla latenza. Una correlazione anticipata è quando l'argomento dell'espressione precede l'argomento descritto, ad esempio un argomento di dimensione è precedente a un argomento del puntatore ridimensionato. Una correlazione tardiva si verifica quando l'argomento dell'espressione viene eseguito dopo l'argomento correlato. Il motore esegue immediatamente la convalida dei valori di correlazione anticipata, i valori di correlazione tardivi vengono archiviati per il controllo dopo che è stato eseguito l'annullamento del marshalling.

Il flag Split indica una suddivisione asincrona tra \[ gli \] argomenti in e \[ out \] . Un argomento di dimensione, ad esempio, può essere \[ in \] mentre il puntatore di dimensioni può essere \[ out \] . Nel contesto asincrono DCOM questi argomenti si trovano in stack diversi, quindi il motore deve essere a conoscenza di questo.

Il flag IsIidIs indica che la correlazione **IID \_ è ()** . La routine NdrComputeConformance viene ingannata per ottenere un puntatore a IID come valore di espressione, ma la routine di convalida non può confrontare tali valori (si tratta di puntatori), quindi il flag indica che è necessario confrontare il IID effettivo.

### <a name="variance-description-and-other-array-attributes"></a>Descrizione della varianza e altri attributi di matrice

Il formato del campo della descrizione della varianza è identico al campo della descrizione della conformità. La differenza consiste nel fatto che un campo di messaggio Stub diverso viene utilizzato dal motore di NDR come variabile temporanea. Nel caso della descrizione della varianza, è la lunghezza che viene valutata e il campo corrispondente è denominato ActualLength.

Con la varianza, l'offset iniziale è in genere zero e il motore viene ottimizzato di conseguenza. Se il **primo attributo \_ is ()** viene applicato a una matrice di variazione conforme, viene forzata una richiamata a una routine di valutazione dell'espressione.

 

 