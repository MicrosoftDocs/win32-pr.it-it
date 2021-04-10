---
description: Concetti fondamentali di MUI descritti
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Concetti fondamentali di MUI descritti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dbeedb246944bef6c23c739eafddff86423b35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966932"
---
# <a name="mui-fundamental-concepts-explained"></a>Concetti fondamentali di MUI descritti

-   [Prerequisito per MUI](#prerequisite-for-mui)
-   [Separazione del codice sorgente da risorse specifiche del linguaggio](#separation-of-source-code-from-language-specific-resources)
    -   [Primi giorni: codice e risorse risiedono insieme](#the-early-days-code-and-resources-live-together)
    -   [Separazione logica del codice e delle risorse localizzabili](#logically-separating-code-and-localizable-resources)
    -   [Separazione fisica di codice e risorse](#physically-separating-code-and-resources)
-   [Caricamento dinamico di risorse specifiche della lingua](#dynamically-loading-language-specific-resources)
-   [Compilazione di applicazioni MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Prerequisito per MUI

Il prerequisito di base per la creazione di un'applicazione compatibile con MUI per Windows Vista e oltre consiste nel progettare l'applicazione in base alle [linee guida per la globalizzazione](https://msdn.microsoft.com/goglobal/bb688110.aspx)di Windows.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separazione del codice sorgente da risorse specifiche del linguaggio

Uno degli elementi fondamentali della tecnologia MUI è la separazione del codice sorgente dell'applicazione da risorse specifiche della lingua, per consentire più efficacemente scenari multilingue nelle applicazioni. La separazione del codice e delle risorse è stata realizzata tramite meccanismi diversi e a gradi diversi nel tempo, come descritto nelle sezioni seguenti. Ogni metodo ha fornito diversi gradi di flessibilità per la compilazione, la distribuzione e la manutenzione dell'applicazione.

La soluzione consigliata per le applicazioni compatibili con MUI è l'ultimo metodo illustrato in questo articolo, ovvero la separazione fisica del codice sorgente e delle risorse dell'applicazione, con le risorse stesse ulteriormente suddivise in un file per ogni lingua supportata per la massima flessibilità di compilazione, distribuzione e manutenzione.

### <a name="the-early-days-code-and-resources-live-together"></a>Primi giorni: codice e risorse risiedono insieme

Inizialmente, le applicazioni localizzate sono state create modificando il codice sorgente e modificando le risorse (in genere stringhe) nel codice stesso e ricompilando le applicazioni. Ciò significava che per produrre una versione localizzata, era necessario copiare il codice sorgente originale, tradurre gli elementi di testo (risorse) all'interno del codice sorgente e ricompilare il codice. Nell'immagine seguente viene illustrato il codice dell'applicazione con testo che deve essere localizzato.

![diagramma concettuale che mostra un'applicazione contenente unità di risorse di testo incorporate](images/mui-fundamental-concepts-explained-fig3.gif)

Sebbene questo approccio consenta la creazione di applicazioni localizzate, presenta anche svantaggi significativi:

-   Richiede più versioni del codice sorgente, almeno una per la lingua di origine e una per ogni lingua di destinazione. Questa operazione consente di creare problemi significativi durante la sincronizzazione delle diverse versioni di lingua dell'applicazione. In particolare, quando è necessario correggere un difetto nel codice, è necessario correggere il difetto in ogni copia del codice sorgente (uno per lingua).
-   È inoltre estremamente soggetto a errori poiché richiede localizzatori, che non sono sviluppatori, per apportare modifiche nel codice sorgente, creando così un notevole rischio in termini di integrità del codice.

La combinazione di questi svantaggi rende questa proposta estremamente inefficiente ed è necessario un modello migliore.

### <a name="logically-separating-code-and-localizable-resources"></a>Separazione logica del codice e delle risorse localizzabili

Un miglioramento significativo rispetto al modello precedente è la separazione logica del codice e delle risorse localizzabili per un'applicazione. In questo modo si isola il codice dalle risorse e si garantisce che il codice rimanga invariato quando le risorse vengono modificate dalla localizzazione. Dal punto di vista dell'implementazione, le stringhe e altri elementi dell'interfaccia utente vengono archiviati nei file di risorse, che sono relativamente facili da tradurre e sono separati logicamente dalle sezioni di codice.

Idealmente, l'aggiunta del supporto per qualsiasi lingua può essere semplice quanto la conversione delle risorse localizzabili in questo nuovo linguaggio e l'utilizzo di queste risorse tradotte per creare una nuova versione localizzata dell'applicazione, senza richiedere alcuna modifica del codice. Nell'immagine seguente viene illustrato il modo in cui il codice e le risorse localizzabili devono essere separate logicamente all'interno di un'applicazione.

![diagramma concettuale che mostra un'applicazione che contiene risorse localizzabili separate dal codice](images/mui-fundamental-concepts-explained-fig4.gif)

Questo modello consente una creazione più semplice di versioni localizzate di un'applicazione e rappresenta un miglioramento significativo rispetto al modello precedente. Questo modello, implementato tramite l'utilizzo degli strumenti di gestione delle risorse, ha avuto un successo nel corso degli anni e viene ancora comunemente utilizzato da molte applicazioni. Tuttavia, presenta svantaggi significativi:

-   Sebbene siano separate logicamente, il codice e le risorse localizzate vengono ancora Uniti fisicamente in un file eseguibile. In particolare, la manutenzione è ancora problematica, in quanto lo stesso difetto del codice (identico in tutte le versioni del linguaggio) richiede una patch per ogni lingua. Se, pertanto, un'applicazione viene distribuita in 20 lingue, è necessario emettere una patch del servizio 20 volte (una per ogni lingua), anche se il codice viene corretto una sola volta.
-   La distribuzione e l'uso di applicazioni multilingue non sono supportate in modo adeguato da questo modello. Questo può costituire un problema significativo negli scenari OEM e aziendali. Se, ad esempio, un computer deve essere condiviso tra due utenti che utilizzano linguaggi diversi, sarà necessario installare le applicazioni due volte con questo modello, quindi è necessario abilitare un meccanismo per alternare le due installazioni. Si presuppone che non siano presenti dipendenze aggiuntive che impediscono l'implementazione di questo scenario. Nell'immagine seguente viene illustrato un esempio di un singolo difetto del codice che richiede due patch.

![diagramma concettuale che mostra due applicazioni localizzate con lo stesso difetto del codice](images/mui-fundamental-concepts-explained-fig5.gif)

È chiaro che anche se questo modello funziona bene in alcuni scenari, le limitazioni per le applicazioni multilingue e le relative distribuzioni possono essere molto problematiche.

Una variante di questo modello che attenua alcuni problemi di applicazioni multilingue è il modello in cui le risorse localizzabili contengono un set di risorse di lingua diverse. Questo modello dispone di una codebase comune e di diverse risorse per lingue diverse nella stessa applicazione. Ad esempio, un'applicazione può essere fornita con inglese, tedesco, francese, spagnolo, olandese e italiano nello stesso pacchetto. Nell'immagine seguente viene illustrata un'applicazione che contiene più risorse di lingua.

![diagramma concettuale che mostra un'applicazione con codice separato da due risorse specifiche delle impostazioni locali](images/mui-fundamental-concepts-explained-fig6.gif)

Questo modello rende più semplice il servizio dell'applicazione quando è necessario correggere un difetto del codice, ovvero un miglioramento, ma non migliora rispetto ai modelli precedenti quando si tratta di supportare lingue aggiuntive. In questo caso, è ancora necessario rilasciare una nuova versione dell'applicazione (e tale versione è potenzialmente complessa dalla necessità di garantire che tutte le risorse della lingua siano sincronizzate all'interno della stessa distribuzione).

### <a name="physically-separating-code-and-resources"></a>Separazione fisica di codice e risorse

Il successivo passaggio evoluzionario consiste nel separare fisicamente il codice e le risorse. In questo modello, le risorse vengono astratte dal codice e separate fisicamente in diversi file di implementazione. In particolare, ciò significa che il codice può diventare realmente indipendente dal linguaggio; lo stesso codice fisico viene effettivamente spedito per tutte le versioni localizzate di un'applicazione. Nell'immagine seguente viene illustrato che il codice e le risorse localizzabili devono essere separate fisicamente.

![diagramma concettuale che mostra un'applicazione separata dalle risorse localizzabili](images/mui-fundamental-concepts-explained-fig7.gif)

Questo approccio presenta diversi vantaggi rispetto agli approcci precedenti:

-   La distribuzione di soluzioni multilingue è molto semplificata. L'aggiunta del supporto per qualsiasi lingua specifica richiede solo la distribuzione e l'installazione di un nuovo set di risorse della lingua per questa lingua. Questa operazione è particolarmente importante quando le risorse di lingua non sono tutte disponibili simultaneamente. Con questo modello, è possibile distribuire un'applicazione in un set di linguaggi di base e aumentare il numero di lingue supportate nel tempo senza dover modificare o ridistribuire il codice effettivo. Questo vantaggio è ulteriormente esteso da un meccanismo di fallback che consente la localizzazione parziale delle applicazioni e dei componenti di sistema in un determinato linguaggio garantendo che le risorse che non sono presenti in questo linguaggio preferenziale "rientrino" in un'altra lingua che gli utenti comprendono. In generale, questo modello contribuisce a ridurre il carico considerevole che le aziende globali devono affrontare per la distribuzione di applicazioni in più lingue, perché consente la distribuzione di singole immagini in modo molto più efficace.
-   È stato migliorato il servizio. Un difetto del codice deve essere risolto e distribuito solo una volta, poiché il codice è completamente indipendente dalla localizzazione. Con questo modello, l'emissione di una correzione per un difetto del codice, purché la modifica non sia correlata all'interfaccia utente, è molto più semplice ed economicamente conveniente rispetto ai modelli precedenti.

## <a name="dynamically-loading-language-specific-resources"></a>Caricamento dinamico di risorse specifiche della lingua

I concetti fondamentali di MUI relativi alla [separazione fisica del codice sorgente da risorse specifiche della lingua](#physically-separating-code-and-resources)e alla creazione di un file binario di base indipendente dalla lingua per un'applicazione, configurano essenzialmente un'architettura che contribuisce all'implementazione del caricamento dinamico di risorse specifiche della lingua in base alle impostazioni della lingua dell'utente e del sistema.

Il codice sorgente dell'applicazione incluso nel file binario Core indipendente dalla lingua può utilizzare le API MUI nella piattaforma Windows per astrarre la selezione della lingua dell'interfaccia utente di visualizzazione appropriata per un determinato contesto. MUI supporta:

-   Creazione di un elenco con priorità di lingue dell'interfaccia utente per la visualizzazione in base alle impostazioni a livello di sistema, utente e a livello di applicazione, a livello di utente e di sistema.
-   Implementazione di un meccanismo di fallback che sceglie un candidato appropriato da questo elenco di lingue con priorità, in base alla disponibilità delle risorse localizzate.

I vantaggi del caricamento dinamico delle risorse dell'interfaccia utente con fallback con priorità sono:

-   Consente la localizzazione parziale delle applicazioni e dei componenti di sistema in una determinata lingua, perché le risorse che non sono presenti in questa lingua preferita verranno automaticamente riportate alla lingua successiva nell'elenco con priorità.
-   Consente scenari come il cambio dinamico da un linguaggio a un altro.
-   Consente la creazione di immagini di distribuzione singola a livello di area o di tutto il mondo che coprono un set di lingue per OEM e aziende.

## <a name="building-mui-applications"></a>Compilazione di applicazioni MUI

Nelle sezioni precedenti sono state descritte le opzioni per la separazione del codice sorgente da risorse specifiche della lingua e il vantaggio risultante nella possibilità di utilizzare le API della piattaforma Windows Core per caricare dinamicamente le risorse localizzate. Anche se si tratta di linee guida, è opportuno sottolineare che non esiste un modo prescrittivo specifico per sviluppare un'applicazione MUI per la piattaforma Windows.

Gli sviluppatori di applicazioni hanno la possibilità di scegliere la modalità di gestione delle diverse impostazioni della lingua dell'interfaccia utente, le opzioni di creazione delle risorse e i metodi di caricamento delle risorse. Gli sviluppatori possono valutare le linee guida fornite in questo documento e scegliere una combinazione che soddisfi i requisiti e l'ambiente di sviluppo.

Nella tabella seguente sono riepilogate le diverse opzioni di progettazione disponibili per gli sviluppatori di applicazioni che vogliono creare un'applicazione MUI per la piattaforma Windows.



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
<td rowspan="2">Seguire le impostazioni della lingua dell'interfaccia utente nel sistema operativo $ {REMOVE} $<br />
</td>
<td>Linguaggio singolo in un file binario della risorsa divisa (tecnologia delle risorse MUI)<br/> -oppure-<br/> Più lingue in un file binario di risorse non suddivise<br/></td>
<td>L'applicazione chiama funzioni di caricamento delle risorse standard. Le risorse vengono restituite nelle lingue corrispondenti alle impostazioni del sistema operativo.<br/></td>
</tr>
<tr class="even">
<td>Meccanismo delle risorse specifico dell'applicazione<br/></td>
<td>L'applicazione chiama l'API MUI per recuperare le lingue dell'interfaccia utente preferite dal thread o i linguaggi dell'interfaccia utente preferiti dal sistema operativo e usare queste impostazioni per caricare le proprie risorse.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Impostazioni della lingua dell'interfaccia utente specifiche dell'applicazione $ {REMOVE} $<br />
</td>
<td>Linguaggio singolo in un file binario di una risorsa divisa<br/> -oppure-<br/> Più lingue in un file binario di risorse non suddivise<br/></td>
<td>L'applicazione chiama l'API MUI per impostare le lingue dell'interfaccia utente specifiche dell'applicazione o le lingue dell'interfaccia utente preferite del processo e quindi chiama le funzioni standard di caricamento delle risorse. Le risorse vengono restituite nelle lingue impostate dalle lingue dell'applicazione o del sistema.<br/> -oppure-<br/> L'applicazione esegue il probe delle risorse in una lingua specifica e gestisce la propria estrazione delle risorse dai dati binari recuperati.<br/></td>
</tr>
<tr class="even">
<td>Meccanismo delle risorse specifico dell'applicazione<br/></td>
<td>L'applicazione gestisce il caricamento delle risorse.<br/></td>

</tr>
</tbody>
</table>



 

 

 




