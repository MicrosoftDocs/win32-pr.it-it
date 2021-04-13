---
description: Individuazione delle partizioni durante l'attivazione
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Individuazione delle partizioni durante l'attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561163"
---
# <a name="locating-partitions-during-activation"></a>Individuazione delle partizioni durante l'attivazione

Individuare la partizione corretta in cui attivare un componente dipende da quanto segue:

-   La chiamata di funzione e i parametri usati nel programma chiamante per attivare il componente
-   Indica se il componente attivato è locale o remoto
-   Uso interno della cache della partizione

## <a name="the-calling-program"></a>Programma chiamante

COM+ seleziona la partizione per l'attivazione dei componenti in base alla modalità di attivazione del componente da parte del programma chiamante.

Sono disponibili tre diverse azioni che possono essere eseguite da COM+ quando si seleziona una partizione per l'attivazione dei componenti. L'azione eseguita dipende dalla modalità con cui il programma chiamante crea un'istanza dell'oggetto, ovvero se la chiamata di funzione include un moniker della partizione, costituito da un ID di partizione e un CLSID, oppure include solo un CLSID.

Nella tabella seguente vengono illustrate le varie azioni che COM+ può intraprendere, in ordine di precedenza, per individuare una partizione.



| Chiamata di funzione                                                  | Parametro                                                      | Azione COM+                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) o **GetObject**<br/> | Moniker partizione (include ID partizione e CLSID)<br/> | Usa l'ID di partizione specificato nel moniker della partizione.<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Usa l'ID di partizione della partizione predefinita dell'identità utente o l'ID di partizione aggiunto al contesto durante un'attivazione del componente precedente nello stesso processo.<br/> |



 

Nelle sezioni seguenti vengono descritte le azioni COM+ elencate nella tabella precedente.

## <a name="use-of-partition-monikers"></a>Uso dei moniker della partizione

Una partizione può essere selezionata in modo esplicito all'interno di una chiamata di funzione usando un *moniker della partizione*. Un moniker di partizione viene usato all'interno del codice per specificare in modo esplicito la partizione del componente attivato. Se per individuare la partizione viene utilizzato un moniker della partizione, l'attivazione viene eseguita da tale partizione. Ovvero, l'ID partizione incluso nel moniker ha la precedenza sulla partizione predefinita dell'utente o su un ID di partizione esistente nel contesto del chiamante.

Nel codice C++, la sintassi per l'uso di un moniker di partizione è la seguente:


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



Nell'esempio seguente viene illustrato un frammento di codice C++, in cui un moniker di partizione viene usato come argomento per la funzione [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



Nel codice Visual Basic la sintassi per un moniker di partizione è la seguente:


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



Nell'esempio seguente viene illustrato un frammento di codice di Visual Basic, in cui un moniker della partizione viene usato come argomento della funzione **GetObject** :


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Utilizzo del mapping predefinito

Quando la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) viene utilizzata per attivare un componente, utilizzando il CLSID del componente, com+ utilizza il mapping dell'identità utente predefinito, ovvero il set di partizioni a cui l'utente è mappato all'interno Active Directory. Tuttavia, se l'utente non è mappato a un set di partizioni all'interno Active Directory, viene selezionata la partizione globale.

## <a name="use-of-partition-ids-and-object-context"></a>Uso degli ID di partizione e del contesto dell'oggetto

Una delle cinque proprietà assegnate a una nuova partizione è l'ID della partizione. Quando il programma client chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza di un oggetto, l'ID partizione viene aggiunto al contesto. L'uso dell'ID partizione dal contesto per individuare la partizione è importante perché garantisce che dopo l'avvio di una catena di attivazioni l'ID di partizione rimanga invariato, a meno che non venga modificato in modo esplicito tramite un moniker della partizione.

Per ulteriori informazioni sull'individuazione delle partizioni durante l'attivazione, vedere [componenti e partizioni in coda com+](com--queued-components-and-partitions.md).

## <a name="local-and-remote-activation"></a>Attivazione locale e remota

-   Se il componente chiamato è presente in un altro computer, viene effettuato il marshalling delle proprietà della partizione (incluso l'ID partizione) nell'altro computer e il componente viene attivato dalla partizione sottoposta a marshalling. Se non è stato eseguito il marshalling di un ID di partizione, COM+ utilizza il set di partizioni predefinito mappato all'identità utente all'interno Active Directory.

## <a name="the-partition-cache"></a>Cache della partizione

In un ambiente di dominio, COM+ utilizza i mapping in Active Directory per individuare la partizione corretta per l'attivazione dei componenti. Tuttavia, le ricerche frequenti in Active Directory possono causare un traffico di rete eccessivo. Per ridurre al minimo il traffico di rete risultante da ricerche frequenti di mapping di set da utente a partizione in Active Directory, COM+ usa una *cache di partizione*.

La cache di partizione contiene i mapping eseguiti in Active Directory tra identità utente o unità organizzative e i relativi set di partizioni. Questa cache di partizione si trova nel server applicazioni in cui risiedono le applicazioni COM+.

Quando COM+ deve determinare la partizione predefinita di un utente o convalidare i diritti di accesso di un utente per una partizione, controlla la cache della partizione in locale per cercare il mapping dell'utente, invece di controllare Active Directory in remoto.

Se la ricerca nella cache della partizione ha esito negativo, COM+ controlla Active Directory. Se la ricerca ha esito positivo in Active Directory, COM+ archivia tale mapping nella cache della partizione. La volta successiva che viene eseguita una ricerca per il mapping da utente a partizione, COM+ lo troverà nella cache della partizione.

Nella figura seguente viene illustrato il processo utilizzato da COM+ per individuare una partizione per l'attivazione dei componenti.

![Diagramma che mostra un albero per la risoluzione dei problemi per il processo utilizzato da COM+ per individuare una partizione per l'attivazione dei componenti.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

Le dimensioni della cache e l'ora di scadenza per le voci della cache vengono impostate tramite le chiavi del registro di sistema. Per informazioni sulla configurazione di queste chiavi del registro di sistema, vedere [creazione e configurazione di partizioni com+](creating-and-configuring-com--partitions.md).

> [!Note]  
> Se un computer server è disconnesso dalla rete e il mapping tra utente e partizione viene modificato mentre il server è disconnesso, la cache della partizione potrebbe contenere un mapping da utente a partizione obsoleto. Questo potrebbe causare un errore di attivazione se il mapping da utente a partizione è il meccanismo usato per attivare un componente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione di un componente per l'attivazione](locating-a-component-for-activation.md)
</dt> </dl>

 

