---
description: ICE62 esegue controlli estesi sulla tabella IsolatedComponent per i dati che possono causare un comportamento imprevisto.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528241"
---
# <a name="ice62"></a>ICE62

ICE62 esegue controlli estesi sulla tabella [IsolatedComponent per](isolatedcomponent-table.md) i dati che possono causare un comportamento imprevisto.

La mancata correzione di un errore segnalato da ICE62 può causare un errore del sistema di componenti isolati in diversi modi. Ad esempio, se il bit SharedDllRefCount non è impostato per un componente condiviso, la registrazione per il componente potrebbe essere rimossa quando un'altra applicazione usa tale ComponentId e viene disinstallata.

## <a name="result"></a>Risultato

ICE62 invia un avviso o un errore quando rileva dati nella tabella IsolatedComponent che possono produrre un comportamento imprevisto.

## <a name="example"></a>Esempio

ICE62 segnala gli errori e gli avvisi seguenti per gli esempi illustrati.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 è elencato come componente dell'applicazione per l'isolamento di component1. Tuttavia, Component2 ha un percorso della chiave del Registro di sistema e non fornisce un percorso eseguibile valido da usare per isolare il componente.

Per correggere l'errore, usare un componente diverso come applicazione per il componente isolato Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 è elencato come componente condiviso isolato, ma non ha il bit SharedDllRefCount impostato. Ciò potrebbe comportare che la durata del componente non sia corretta. Se un'altra applicazione usa questo componente (isolato o meno) e viene disinstallata, la registrazione per il componente viene rimossa, ma la copia isolata dell'applicazione rimane. Ciò causa problemi di ripristino e disinstallazione.

Per correggere l'errore, impostare il bit SharedDllRefCount per il componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 e Component2 vengono installati da funzionalità diverse. Component1 viene installato da Feature1 e Component2 viene installato da Feature2. Feature1 non è un elemento padre di Feature2, pertanto è possibile che l'applicazione sia installata ma non il componente isolato, interrompendo l'isolamento.

Per correggere l'errore, aggiungere una voce alla tabella FeatureComponents collegando Component1 alla stessa funzionalità (o a una funzionalità padre di) della funzionalità che installa Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 ha una condizione nella tabella Component. Se questa condizione cambia da TRUE a FALSE durante la durata di un'installazione in un computer, il componente isolato potrebbe essere orfano senza informazioni di registrazione.

Per correggere l'avviso, rimuovere la condizione o creare la condizione in modo che non possa mai cambiare da TRUE a FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 è isolato sia per Component2 che per Component3 e anche i due componenti vengono installati nella stessa directory. Le applicazioni condividono un componente isolato, ma se un'applicazione viene rimossa, il componente condiviso viene rimosso e le altre applicazioni perdono il componente isolato.

Per correggere questo avviso, installare le applicazioni in directory diverse o verificare se alcune applicazioni richiedono effettivamente un componente isolato.

[Tabella IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ condiviso | Applicazione \_ componente |
|-------------------|------------------------|
| Componente1        | Componente2             |
| Componente1        | Componente3             |



 

[Tabella dei componenti](component-table.md)



| Componente  | Componentid | Directory\_ | Attributi | Condition   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Componente1 |             | Dir1        | 0          | MYCONDITION | File1     |
| Componente2 |             | Targetdir   | 4          |             | Registro di sistema 2 |
| Componente3 |             | Targetdir   | 0          |             | File3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Funzionalità1  | Componente1  |
| Funzionalità2  | Componente2  |
| Funzionalità1  | Componente3  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  | Elemento padre \_ della funzionalità |
|----------|-----------------|
| Funzionalità1 |                 |
| Funzionalità2 |                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



