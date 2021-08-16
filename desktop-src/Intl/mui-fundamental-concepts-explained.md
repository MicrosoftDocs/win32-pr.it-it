---
description: Spiegati i concetti fondamentali di MUI
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Spiegati i concetti fondamentali di MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390891"
---
# <a name="mui-fundamental-concepts-explained"></a>Spiegati i concetti fondamentali di MUI

-   [Prerequisito per MUI](#prerequisite-for-mui)
-   [Separazione del codice sorgente dalle risorse specifiche del linguaggio](#separation-of-source-code-from-language-specific-resources)
    -   [Primi giorni: il codice e le risorse convivere](#the-early-days-code-and-resources-live-together)
    -   [Separazione logica del codice e delle risorse localizzabili](#logically-separating-code-and-localizable-resources)
    -   [Separazione fisica di codice e risorse](#physically-separating-code-and-resources)
-   [Caricamento dinamico di risorse specifiche del linguaggio](#dynamically-loading-language-specific-resources)
-   [Compilazione di applicazioni MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Prerequisito per MUI

Il prerequisito di base per la compilazione di un'applicazione conforme a MUI per Windows Vista e oltre è la progettazione dell'applicazione in base alle linee guida Windows [sulla globalizzazione.](https://msdn.microsoft.com/goglobal/bb688110.aspx)

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separazione del codice sorgente dalle risorse specifiche del linguaggio

Una delle sedi fondamentali della tecnologia MUI è la separazione del codice sorgente dell'applicazione dalle risorse specifiche del linguaggio, per consentire scenari multilingue nelle applicazioni in modo più efficiente. La separazione di codice e risorse è stata ottenuta tramite meccanismi diversi e in diversi gradi nel tempo, come descritto nelle sezioni seguenti. Ogni metodo offre vari livelli di flessibilità per la compilazione, la distribuzione e la manutenzione dell'applicazione.

La soluzione consigliata per le applicazioni conformi a MUI è l'ultimo metodo descritto qui, in questo caso la separazione fisica del codice sorgente e delle risorse dell'applicazione, con le risorse stesse ulteriormente suddivise in un file per ogni linguaggio supportato per la massima flessibilità nella compilazione, nella distribuzione e nella manutenzione.

### <a name="the-early-days-code-and-resources-live-together"></a>Primi giorni: il codice e le risorse convivere

Inizialmente, le applicazioni localizzate sono state create modificando il codice sorgente e modificando le risorse (in genere stringhe) nel codice stesso e ricompilando le applicazioni. Ciò significava che per produrre una versione localizzata era necessario copiare il codice sorgente originale, tradurre gli elementi di testo (risorse) all'interno del codice sorgente e ricompilare il codice. L'immagine seguente mostra il codice dell'applicazione con testo che deve essere localizzato.

![Diagramma concettuale che illustra un'applicazione che contiene unità di risorse di testo incorporate](images/mui-fundamental-concepts-explained-fig3.gif)

Sebbene questo approccio consenta la creazione di applicazioni localizzate, presenta anche svantaggi significativi:

-   Richiede più versioni del codice sorgente, almeno una per il linguaggio di origine e una per ognuna delle lingue di destinazione. Ciò crea problemi significativi durante la sincronizzazione delle diverse versioni in lingua dell'applicazione. In particolare, quando un difetto deve essere corretto nel codice, il difetto deve essere corretto in ogni copia del codice sorgente (uno per ogni lingua).
-   È anche estremamente rischioso perché i localizzatori, che non sono sviluppatori, devono apportare modifiche al codice sorgente, creando così un notevole rischio in termini di integrità del codice.

La combinazione di questi svantaggi rende questa proposta estremamente inefficiente ed è necessario un modello migliore.

### <a name="logically-separating-code-and-localizable-resources"></a>Separazione logica del codice e delle risorse localizzabili

Un miglioramento significativo rispetto al modello precedente è la separazione logica del codice e delle risorse localizzabili per un'applicazione. In questo modo il codice viene isolato dalle risorse e viene garantito che il codice rimanga invariato quando le risorse vengono modificate dalla localizzazione. Dal punto di vista dell'implementazione, le stringhe e altri elementi dell'interfaccia utente vengono archiviati in file di risorse, relativamente facili da tradurre e separati logicamente dalle sezioni di codice.

Idealmente, l'aggiunta del supporto per una determinata lingua può essere semplice come la traduzione delle risorse localizzabili in questa nuova lingua e l'uso di queste risorse tradotte per creare una nuova versione localizzata dell'applicazione, senza richiedere alcuna modifica del codice. L'immagine seguente illustra come separare logicamente il codice e le risorse localizzabili all'interno di un'applicazione.

![Diagramma concettuale che mostra un'applicazione che contiene risorse localizzabili separate dal codice](images/mui-fundamental-concepts-explained-fig4.gif)

Questo modello semplifica la creazione di versioni localizzate di un'applicazione ed è un miglioramento significativo rispetto al modello precedente. Questo modello, implementato tramite l'uso di strumenti di gestione delle risorse, ha avuto molto successo nel corso degli anni ed è ancora comunemente usato da molte applicazioni. Tuttavia, ha svantaggi significativi:

-   Anche se separati logicamente, il codice e le risorse localizzate vengono ancora uniti fisicamente in un unico file eseguibile. In particolare, la gestibilità è ancora problematica perché lo stesso difetto del codice (identico in tutte le versioni del linguaggio) richiede una patch per ogni linguaggio. Pertanto, se l'applicazione viene rilasciata in 20 lingue, è necessario emissione di una patch del servizio 20 volte (una per ogni lingua), anche se il codice viene corretto una sola volta.
-   La distribuzione e l'uso di applicazioni multilingue non sono supportati in modo adeguato da questo modello. Questo può essere un problema significativo negli scenari OEM e aziendali. Ad esempio, se un computer deve essere condiviso tra due utenti che usano lingue diverse, le applicazioni dovranno essere installate due volte con questo modello e quindi sarà necessario abilitato un meccanismo per alternare le due installazioni. Ciò presuppone che non siano presenti dipendenze aggiuntive che impediscono anche l'implementazione di questo scenario. L'immagine seguente mostra un esempio di un singolo difetto del codice che richiede due patch.

![Diagramma concettuale che mostra due applicazioni localizzate con lo stesso difetto del codice](images/mui-fundamental-concepts-explained-fig5.gif)

È chiaro che anche se questo modello funziona bene in alcuni scenari, le limitazioni per le applicazioni multilingue e le relative distribuzioni possono essere molto problematiche.

Una variante di questo modello che attenua alcuni problemi relativi alle applicazioni multilingue è il modello in cui le risorse localizzabili contengono un set di risorse di lingue diverse. Questo modello ha una codebase comune e diverse risorse per linguaggi diversi nella stessa applicazione. Ad esempio, un'applicazione può essere spedita con inglese, tedesco, francese, spagnolo, olandese e italiano nello stesso pacchetto. L'immagine seguente mostra un'applicazione che contiene più risorse di linguaggio.

![Diagramma concettuale che illustra un'applicazione con codice separato da due risorse specifiche delle impostazioni locali](images/mui-fundamental-concepts-explained-fig6.gif)

Questo modello semplifica la gestione dell'applicazione quando è necessario correzione di un difetto del codice, un miglioramento, ma non migliora rispetto ai modelli precedenti quando si tratta di supportare linguaggi aggiuntivi. In questo caso, è ancora necessario rilasciare una nuova versione dell'applicazione e tale versione è potenzialmente complicata dalla necessità di garantire che tutte le risorse del linguaggio siano sincronizzate all'interno della stessa distribuzione.

### <a name="physically-separating-code-and-resources"></a>Separazione fisica di codice e risorse

Il passaggio successivo dell'evoluzione consiste nel separare fisicamente il codice e le risorse. In questo modello le risorse vengono astratte dal codice e separate fisicamente in file di implementazione diversi. In particolare, ciò significa che il codice può diventare realmente indipendente dal linguaggio; Lo stesso codice fisico viene effettivamente fornito per tutte le versioni localizzate di un'applicazione. L'immagine seguente illustra che il codice e le risorse localizzabili devono essere fisicamente separati.

![Diagramma concettuale che mostra un'applicazione separata dalle relative risorse localizzabili](images/mui-fundamental-concepts-explained-fig7.gif)

Questo approccio presenta diversi vantaggi rispetto a quello precedente:

-   La distribuzione di soluzioni multilingue è notevolmente semplificata. L'aggiunta del supporto per una determinata lingua richiede solo la spedizione e l'installazione di un nuovo set di risorse per la lingua specifica. Ciò è particolarmente importante quando le risorse del linguaggio non sono tutte disponibili simultaneamente. Con questo modello è possibile distribuire un'applicazione in un set di linguaggi di base e aumentare il numero di lingue supportate nel tempo senza dover modificare o ridistribuire il codice effettivo. Questo vantaggio viene ulteriormente esteso da un meccanismo di fallback che consente la localizzazione parziale delle applicazioni e dei componenti di sistema in una determinata lingua, assicurando che le risorse che non si trovano in questa lingua preferita "eseenzino" a un'altra lingua comprensibile anche agli utenti. In generale, questo modello consente di ridurre il notevole carico di lavoro che le aziende globali devono affrontare nella distribuzione di applicazioni in più lingue, perché consente la distribuzione di singole immagini in modo molto più efficace.
-   La gestibilità è stata migliorata. Un difetto del codice deve essere corretto e distribuito una sola volta, perché il codice è completamente indipendente dalla localizzazione. Con questo modello, l'emissione di una correzione per un difetto del codice, a condizione che la modifica non sia correlata all'interfaccia utente, è molto più semplice e conveniente rispetto a qualsiasi modello precedente.

## <a name="dynamically-loading-language-specific-resources"></a>Caricamento dinamico di risorse specifiche del linguaggio

I concetti fondamentali [](#physically-separating-code-and-resources)di MUI relativi alla separazione fisica del codice sorgente dalle risorse specifiche del linguaggio e alla creazione di un file binario di base indipendente dal linguaggio per un'applicazione, configurano essenzialmente un'architettura che consente di implementare il caricamento dinamico delle risorse specifiche della lingua in base alle impostazioni della lingua dell'utente e del sistema.

Il codice sorgente dell'applicazione in bundle nel file binario di base indipendente dalla lingua può usare le API MUI nella piattaforma Windows per astrarre la selezione della lingua dell'interfaccia utente di visualizzazione appropriata per un determinato contesto. MUI supporta questa operazione:

-   Creazione di un elenco con priorità delle lingue dell'interfaccia utente visualizzate in base alle impostazioni a livello di sistema, utente e applicazione, a livello di utente e a livello di sistema.
-   Implementazione di un meccanismo di fallback che sceglie un candidato appropriato da questo elenco di lingue in ordine di priorità, in base alla disponibilità delle risorse localizzate.

I vantaggi del caricamento dinamico delle risorse dell'interfaccia utente con fallback con priorità sono:

-   Consente la localizzazione parziale delle applicazioni e dei componenti di sistema in una determinata lingua, perché le risorse che non si trovano in questa lingua preferita eseranno automaticamente il fall back alla lingua successiva nell'elenco con priorità.
-   Consente scenari come il passaggio dinamico da un linguaggio a un altro.
-   Consente di creare immagini di distribuzione singola a livello regionale o mondiale che coprono un set di lingue per OEM e aziende.

## <a name="building-mui-applications"></a>Compilazione di applicazioni MUI

Le sezioni precedenti illustrano le opzioni per la separazione del codice sorgente dalle risorse specifiche della lingua e il vantaggio di poter usare le API della piattaforma core Windows per caricare dinamicamente le risorse localizzate. Anche se si tratta di linee guida, è necessario notare che non esiste un modo prescrittivo specifico per sviluppare un'applicazione MUI per la Windows piattaforma.

Gli sviluppatori di applicazioni hanno la possibilità di scegliere il modo in cui gestiscono le varie impostazioni della lingua dell'interfaccia utente, le opzioni di creazione delle risorse e i metodi di caricamento delle risorse. Gli sviluppatori possono valutare le linee guida fornite in questo documento e scegliere una combinazione adatta ai propri requisiti e all'ambiente di sviluppo.

La tabella seguente riepiloga le diverse opzioni di progettazione disponibili per gli sviluppatori di applicazioni che desiderano creare un'applicazione MUI per la Windows piattaforma.



<table>
<thead>
<tr class="header">
<th>Impostazioni della lingua dell'interfaccia utente</th>
<th>Creazione di risorse</th>
<th>Caricamento delle risorse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Seguire le impostazioni della lingua dell'interfaccia utente nel sistema operativo${REMOVE}$<br />
</td>
<td>Singola lingua in un file binario di risorse suddivise (TECNOLOGIA DELLE RISORSE MUI)<br/> -oppure-<br/> Più lingue in un file binario di risorse non suddiviso<br/></td>
<td>L'applicazione chiama le funzioni standard di caricamento delle risorse. Le risorse vengono restituite nelle lingue corrispondenti alle impostazioni del sistema operativo.<br/></td>
</tr>
<tr class="even">
<td>Meccanismo delle risorse specifico dell'applicazione<br/></td>
<td>L'applicazione chiama l'API MUI per recuperare dal sistema operativo le lingue dell'interfaccia utente preferite dai thread o le lingue dell'interfaccia utente preferite dal processo e usare queste impostazioni per caricare le proprie risorse.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Impostazioni della lingua dell'interfaccia utente specifiche dell'applicazione${REMOVE}$<br />
</td>
<td>Singola lingua in un file binario di risorse suddivise<br/> -oppure-<br/> Più lingue in un file binario di risorse non suddiviso<br/></td>
<td>L'applicazione chiama l'API MUI per impostare le lingue dell'interfaccia utente specifiche dell'applicazione o le lingue dell'interfaccia utente preferite dal processo e quindi chiama le funzioni standard di caricamento delle risorse. Le risorse vengono restituite nelle lingue impostate dall'applicazione o dalle lingue di sistema.<br/> -oppure-<br/> L'applicazione ricerca le risorse in un linguaggio specifico e gestisce la propria estrazione delle risorse dai dati binari recuperati.<br/></td>
</tr>
<tr class="even">
<td>Meccanismo delle risorse specifico dell'applicazione<br/></td>
<td>L'applicazione gestisce il caricamento delle risorse.<br/></td>

</tr>
</tbody>
</table>



 

 

 




