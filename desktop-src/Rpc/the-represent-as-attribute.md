---
title: Attributo represent_as
description: L'attributo \ rappresenta \_ come \ consente di specificare la modalità di rappresentazione di un particolare tipo di dati transmittable nell'applicazione.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, attributi, represent_as di procedura remota
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118334"
---
# <a name="the-represent_as-attribute"></a>Rappresenta \_ come attributo

L' \[ attributo [rappresenta \_ come](/windows/desktop/Midl/represent-as) \] consente di specificare il modo in cui un particolare tipo di dati transmittable viene rappresentato nell'applicazione. Questa operazione viene eseguita specificando il nome del tipo rappresentato per un tipo transmittable noto e fornendo le routine di conversione. È inoltre necessario specificare le routine per liberare la memoria utilizzata dagli oggetti del tipo di dati.

Utilizzare l'attributo **\[ rappresenta \_ come \]** per presentare un'applicazione con un tipo di dati diverso, possibilmente untransmittable, anziché il tipo effettivamente trasmesso tra il client e il server. È anche possibile che il tipo modificato dall'applicazione possa essere sconosciuto al momento della compilazione MIDL. Quando si sceglie un tipo transmittable ben definito, non è necessario preoccuparsi della rappresentazione dei dati nell'ambiente eterogeneo. L'attributo **\[ rappresenta \_ come \]** può migliorare l'efficienza dell'applicazione riducendo la quantità di dati trasmessi in rete.

L'attributo **\[ rappresenta \_ \] come** è simile all'attributo \[ [trasmissione \_ come](/windows/desktop/Midl/transmit-as) \] . Tuttavia, mentre **\[ trasmette \_ come \]** consente di specificare un tipo di dati che verrà usato per la trasmissione, **\[ rappresenta \_ come \]** consente di specificare la modalità di rappresentazione di un tipo di dati per l'applicazione. Non è necessario definire il tipo rappresentato nei file elaborati MIDL; può essere definito nel momento in cui gli stub vengono compilati con il compilatore C. A tale scopo, usare la direttiva include nel [file di configurazione dell'applicazione (ACF)](the-application-configuration-file-acf-.md) per compilare il file di intestazione appropriato. Ad esempio, l'ACF seguente definisce un tipo locale per l'applicazione, **repr \_ Type**, per il tipo transmittable Type **denominato \_ :**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

Nella tabella seguente vengono descritte le quattro routine fornite dal programmatore.



| Routine                      | Descrizione                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **\_tipo denominato \_ da \_ local** | Alloca un'istanza del tipo di rete e la converte dal tipo locale al tipo di rete.      |
| **\_tipo denominato \_ in \_ locale**   | Esegue la conversione dal tipo di rete al tipo locale.                                                    |
| **\_tipo denominato \_ Free \_ local** | Libera la memoria allocata da una chiamata al **\_ tipo denominato \_ alla routine \_ locale** , ma non al tipo stesso. |
| **\_ \_ inst libero del tipo denominato \_**  | Libera lo spazio di archiviazione per il tipo di rete (entrambi i lati).                                                     |



 

Ad eccezione di queste quattro routine fornite dal programmatore, il tipo denominato non viene modificato dall'applicazione. L'unico tipo visibile all'applicazione è il tipo rappresentato. L'applicazione usa il nome del tipo rappresentato anziché il nome del tipo trasmesso nei prototipi e negli stub generati dal compilatore. È necessario fornire il set di routine per entrambi i lati.

Per gli oggetti di **\_ tipo denominato** temporaneo, lo stub chiamerà il **\_ tipo denominato \_ \_ inst Free** per liberare la memoria allocata da una chiamata al **\_ tipo denominato \_ da \_ local**.

Se il tipo rappresentato è un puntatore o contiene un puntatore, il **\_ tipo denominato \_ alla routine \_ locale** deve allocare memoria per i dati a cui puntatori (l'oggetto di tipo rappresentato stesso viene modificato dallo stub nel modo consueto). Per \[ [out](/windows/desktop/Midl/out-idl) \] e \[ [in](/windows/desktop/Midl/in), \] i parametri out di un tipo che contengono **\[ rappresentano \_ come** o uno dei suoi componenti, **il \_ tipo denominato \_ Free \_ local** routine viene chiamato automaticamente per gli oggetti dati che contengono l'attributo. Per i parametri **\[ in \]** , **il \_ tipo denominato \_ Free \_ local** routine viene chiamato solo se l'attributo **\[ rappresenta \_ come \]** è stato applicato al parametro. Se l'attributo è stato applicato ai componenti del parametro, la routine *\* *** \_ \_ locale gratuita** non viene chiamata. Le routine di liberazione non vengono chiamate per i dati incorporati e la chiamata at-most-once (correlata all'attributo di primo livello) **\[ \] per un solo** parametro.

> [!Note]  
> È possibile applicare sia la **\[ trasmissione \_ che \]** la **\[ rappresentazione \_ come \]** attributi allo stesso tipo. Quando si effettua il marshalling dei dati, l'oggetto **\[ rappresenta \_ come \]** conversione del tipo viene applicato per primo e quindi viene applicata la **\[ trasmissione \_ come \]** conversione. L'ordine viene invertito durante l'annullamento del marshalling dei dati. Pertanto, quando si effettua il marshalling, \* **\_ da \_ local** alloca un'istanza di un tipo denominato e la converte da un oggetto di tipo locale all'oggetto di tipo denominato temporaneo. Questo oggetto è l'oggetto tipo presentato usato per la \* routine **\_ to \_ Xmit** . La \* routine **\_ to \_ Xmit** quindi alloca un oggetto tipo trasmesso e lo converte dall'oggetto presentato (denominato) all'oggetto trasmesso.

 

Una matrice di valori long integer può essere usata per rappresentare un elenco collegato. In questo modo, l'applicazione modifica l'elenco e la trasmissione usa una matrice di valori long integer quando viene trasmesso un elenco di questo tipo. È possibile iniziare con una matrice, ma è più facile usare un costrutto con una matrice aperta di valori long integer. L'esempio seguente illustra come farlo.

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

Si noti che i prototipi delle routine che usano il tipo **LONGARR** vengono effettivamente visualizzati nei file stub. h come **ploc \_ Box** al posto del tipo **LONGARR** . Lo stesso vale per gli stub appropriati nel \_ file c. c dello stub.

È necessario fornire le quattro funzioni seguenti:

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

Le routine illustrate in precedenza eseguono le operazioni seguenti:

-   **LONGARR \_ dalla routine \_ locale** conta i nodi dell'elenco, alloca un oggetto LONGARR con le dimensioni **sizeof**(**LONGARR**) + Count \* **sizeof**(**Long**), imposta il campo delle **dimensioni** su Count e copia i dati nel campo **DataArr** .
-   La routine **LONGARR \_ to \_ local** crea un elenco con nodi di dimensioni e trasferisce la matrice ai nodi appropriati.
-   In questo caso la routine **\_ \_ inst Free di LONGARR** non consente di liberare nulla.
-   La **routine \_ \_ locale gratuita LONGARR** libera tutti i nodi dell'elenco.

 

 