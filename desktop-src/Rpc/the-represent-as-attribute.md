---
title: Attributo represent_as
description: L'attributo \ represent as\ consente di specificare come viene rappresentato un particolare tipo di dati trasmettibile \_ nell'applicazione.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC Remote Procedure Call , attributi e represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbf217260f3d23f7390a2295d7db5a36174ae01a94f7368f8e7d2085d19ae0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924000"
---
# <a name="the-represent_as-attribute"></a>Rappresenta \_ come attributo

L'attributo represent as consente di specificare la modalità di rappresentazione di un particolare tipo di dati trasmettibile \[ [ \_ ](/windows/desktop/Midl/represent-as) \] nell'applicazione. Questa operazione viene eseguita specificando il nome del tipo rappresentato per un tipo trasmettibile noto e fornendo le routine di conversione. È inoltre necessario fornire le routine per liberare la memoria utilizzata dagli oggetti tipo di dati.

Usare **\[ l'attributo represent \_ \]** as per presentare a un'applicazione un tipo di dati diverso, possibilmente non ritrasmettibile, anziché il tipo effettivamente trasmesso tra il client e il server. È anche possibile che il tipo modificato dall'applicazione sia sconosciuto al momento della compilazione MIDL. Quando si sceglie un tipo trasmettibile ben definito, non è necessario preoccuparsi della rappresentazione dei dati nell'ambiente eterogeneo. **\[ \_ L'attributo \] rappresenta** come può rendere l'applicazione più efficiente riducendo la quantità di dati trasmessi in rete.

**\[ \_ L'attributo \] rappresenta** come è simile all'attributo \[ [transmit \_ as.](/windows/desktop/Midl/transmit-as) \] Tuttavia, mentre **\[ \_ \] trasmetti** come consente di specificare un tipo di dati che verrà utilizzato per la trasmissione, **\[ \_ \]** rappresentare come consente di specificare come viene rappresentato un tipo di dati per l'applicazione. Il tipo rappresentato non deve essere definito nei file elaborati MIDL. può essere definito nel momento in cui gli stub vengono compilati con il compilatore C. A tale scopo, usare la direttiva include nel [file di configurazione dell'applicazione (ACF)](the-application-configuration-file-acf-.md) per compilare il file di intestazione appropriato. Ad esempio, l'ACF seguente definisce un tipo locale per l'applicazione, **repr \_ type**, per il tipo trasmettibile **denominato \_ type:**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

Nella tabella seguente vengono descritte le quattro routine fornite dal programmatore.



| Routine                      | Descrizione                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **tipo \_ denominato \_ da \_ local** | Alloca un'istanza del tipo di rete ed esegue la conversione dal tipo locale al tipo di rete.      |
| **da tipo \_ denominato \_ a \_ locale**   | Converte dal tipo di rete al tipo locale.                                                    |
| **tipo \_ denominato \_ free \_ local** | Libera la memoria allocata da una chiamata al **tipo \_ denominato \_ alla \_** routine locale, ma non al tipo stesso. |
| **tipo \_ denominato \_ free \_ inst**  | Libera spazio di archiviazione per il tipo di rete (entrambi i lati).                                                     |



 

A differenza di queste quattro routine fornite dal programmatore, il tipo denominato non viene modificato dall'applicazione. L'unico tipo visibile all'applicazione è il tipo rappresentato. L'applicazione usa il nome del tipo rappresentato anziché il nome del tipo trasmesso nei prototipi e negli stub generati dal compilatore. È necessario fornire il set di routine per entrambi i lati.

Per gli **oggetti \_ di tipo** denominato temporanei, lo stub chiamerà il tipo denominato free **\_ \_ \_ inst** per liberare la memoria allocata da una chiamata al **tipo denominato \_ \_ \_ dall'oggetto locale.**

Se il tipo rappresentato è un puntatore o contiene un puntatore, il tipo denominato alla routine locale deve allocare memoria per i dati a cui puntano i puntatori (l'oggetto tipo rappresentato stesso viene modificato dallo stub nel modo consueto). **\_ \_ \_** Per out e in , i parametri out di un tipo che contengono rappresentano come o uno dei relativi componenti, la routine locale senza tipo denominato viene chiamata automaticamente per gli oggetti dati che \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in) \] contengono l'attributo **\[ \_** **\_ \_ \_** . Per **\[ i parametri \]** in , la routine locale senza **\_ \_ \_ tipi** denominati viene chiamata solo se l'attributo represent **\[ \_ as \]** è stato applicato al parametro . Se l'attributo è stato applicato ai componenti del parametro , la routine * locale libera non viene chiamata. *\* *** \_ \_* Le routine di liberatura non vengono chiamate per i dati incorporati e la chiamata at-most-once (correlata all'attributo di primo livello) per un solo parametro **\[ in \]** .

> [!Note]  
> È possibile applicare sia la **\[ trasmissione \_ \] che** la **\[ rappresentazione \_ come \]** attributi allo stesso tipo. Quando si effettua il marshalling dei dati, **\[ l'oggetto rappresenta \_ \]** come conversione del tipo viene applicato per primo e quindi viene applicata la **\[ \_ trasmissione \]** come conversione. L'ordine viene invertito quando si esegue l'unmarsshaling dei dati. Pertanto, durante il marshalling, da local alloca un'istanza di un tipo denominato e la converte da un oggetto tipo locale \* *_\_ \__* all'oggetto tipo denominato temporaneo. Questo oggetto è l'oggetto di tipo presentato usato per la routine \* *_\_ \_ da xmit._* La \* *_\_ routine \_ to xmit_* alloca quindi un oggetto di tipo trasmesso e lo converte dall'oggetto presentato (denominato) all'oggetto trasmesso.

 

È possibile usare una matrice di valori long integer per rappresentare un elenco collegato. In questo modo, l'applicazione modifica l'elenco e la trasmissione usa una matrice di valori long integer quando viene trasmesso un elenco di questo tipo. È possibile iniziare con una matrice, ma è più pratico usare un costrutto con una matrice aperta di valori long integer. L'esempio seguente illustra come farlo.

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

Si noti che i prototipi delle routine che usano il tipo **LONGARR** vengono effettivamente visualizzati nei file Stub.h come **PLOC \_ BOX** al posto del **tipo LONGARR.** Lo stesso vale per gli stub appropriati nel file Stub \_ c.c.

È necessario specificare le quattro funzioni seguenti:

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

Le routine illustrate in precedenza ese indicato di seguito:

-   **LONGARR \_ \_** dalla routine locale conta i nodi dell'elenco, alloca un oggetto LONGARR con **sizeof**(**LONGARR**) + Count sizeof ( long ), imposta il campo Size su Count e copia i dati nel \* ** **campo DataArr.**  
-   La routine **da LONGARR a \_ \_ locale** crea un elenco con nodi Size e trasferisce la matrice ai nodi appropriati.
-   In questo caso, la routine **\_ \_ inst gratuita LONGARR** non libera nulla.
-   La routine **locale \_ \_ longarr** free libera tutti i nodi dell'elenco.

 

 