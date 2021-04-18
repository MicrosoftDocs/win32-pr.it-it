---
description: ICE62 esegue verifiche complete sulla tabella IsolatedComponent per i dati che possono causare un comportamento imprevisto.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314791"
---
# <a name="ice62"></a>ICE62

ICE62 esegue verifiche complete sulla [tabella IsolatedComponent](isolatedcomponent-table.md) per i dati che possono causare un comportamento imprevisto.

La mancata correzione di un errore segnalato da ICE62 può comportare un errore del sistema di componenti isolati in un'ampia gamma di modi. Se, ad esempio, il bit SharedDllRefCount non è impostato per un componente condiviso, la registrazione per il componente potrebbe essere rimossa quando un'altra applicazione usa tale ComponentId e viene disinstallata.

## <a name="result"></a>Risultato

ICE62 Invia un avviso o un errore quando trova i dati nella tabella IsolatedComponent che possono produrre un comportamento imprevisto.

## <a name="example"></a>Esempio

ICE62 segnala gli errori e gli avvisi seguenti per gli esempi mostrati.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 è elencato come componente dell'applicazione per l'isolamento di Component1. Tuttavia, Component2 dispone di un percorso della chiave del registro di sistema e non fornisce un percorso eseguibile valido da utilizzare per isolare il componente.

Per correggere l'errore, usare un componente diverso come applicazione per il componente isolato Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 è elencato come componente condiviso isolato, ma non ha il bit SharedDllRefCount impostato. Questo potrebbe comportare la durata del componente non corretto. Se un'altra applicazione utilizza questo componente (isolato o meno) e viene disinstallato, la registrazione per il componente viene rimossa, ma la copia isolata di questa applicazione rimane. Ciò causa problemi di ripristino e disinstallazione.

Per correggere l'errore, impostare il bit SharedDllRefCount per il componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 e Component2 vengono installati da diverse funzionalità. Component1 viene installato da Feature1 e Component2 viene installato da Funzionalità2. Feature1 non è un elemento padre di funzionalità2, di conseguenza è possibile che l'applicazione sia installata, ma non il componente isolato, per suddividere l'isolamento.

Per correggere l'errore, aggiungere una voce alla tabella FeatureComponents che collega Component1 alla stessa funzione di (o a una funzionalità padre di) la funzionalità che installa Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 presenta una condizione nella tabella dei componenti. Se questa condizione viene modificata da TRUE a FALSE durante il ciclo di vita di un'installazione di in un computer, il componente isolato potrebbe essere orfano senza informazioni di registrazione.

Per correggere il problema, rimuovere la condizione oppure creare la condizione in modo che non possa mai passare da TRUE a FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 è isolato sia per Component2 che per Component3 e i due componenti vengono inoltre installati nella stessa directory. Le applicazioni condividono un componente isolato, ma se un'applicazione viene rimossa, viene rimosso anche il componente condiviso, causando la perdita del componente isolato da parte di altre applicazioni.

Per correggere il problema, installare le applicazioni in directory diverse o controllare se alcune applicazioni richiedono effettivamente un componente isolato.

[Tabella IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ condiviso | \_Applicazione componente |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Tabella componenti](component-table.md)



| Componente  | ComponentId | Directory\_ | Attributi | Condizione   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MYCONDITION | File1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | File3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Funzionalità2  | Component2  |
| Feature1  | Component3  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  | \_Elemento padre della funzionalità |
|----------|-----------------|
| Feature1 |                 |
| Funzionalità2 |                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



