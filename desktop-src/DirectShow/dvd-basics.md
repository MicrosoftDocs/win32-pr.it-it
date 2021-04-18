---
description: Nozioni fondamentali sui DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Nozioni fondamentali sui DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d0b2af8bc16fa0890c0103a063e750364cece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304112"
---
# <a name="dvd-basics"></a>Nozioni fondamentali sui DVD

Le funzionalità che rendono i DVD attraenti per i consumer, ovvero la diramazione trasparente, più lingue, il controllo parentale, il supporto per karaoke e diversi angoli, rendono il lavoro dello sviluppatore un po' più complesso. Un lettore DVD non deve riprodurre solo i flussi audio, video e immagine non solo, ma deve anche tenere traccia delle opzioni di navigazione che il disco è attualmente in grado di consentire e gestire correttamente molti tipi di comandi utente. Il navigatore DVD protegge dalla maggior parte di questa complessità e consente di creare un'applicazione DVD completamente funzionante. Non è necessario fare riferimento alla specifica DVD per utilizzare in modo efficace l'API Navigator DVD, ma è necessario conoscerne i concetti di base.

**Dati di controllo di navigazione**

I dati audio e video in un disco di DVD-Video sono interfogliati a intervalli regolari con vari tipi di dati di controllo di navigazione. Questi dati possono essere un'istruzione che indica al lettore di eseguire un'operazione, ad esempio spostare in una determinata posizione sul disco, oppure un marcatore solo informativo che informa il lettore che il contenuto che segue ha un livello di gestione padre superiore rispetto al contenuto precedente oppure che l'operazione di Skip del capitolo è disabilitata. Il giocatore inoltra queste informazioni a un'applicazione ed è responsabilità dell'applicazione agire su di essa. Questi marcatori di spostamento fanno parte di un DVD con un livello di interattività utente superiore rispetto ai CD video. Un'applicazione DVD-Player deve gestire gli eventi che hanno origine con il disco, nonché gli eventi che hanno origine con l'utente.

**Dati audio, video e subimmagine**

Un disco DVD-Video contiene tre tipi principali di flussi: video, audio e immagine.

-   Il flusso video può contenere fino a nove "angoli", che possono essere considerati come sottoflussi. Gli autori di DVD possono includere diversi angoli laddove vogliono offrire al visualizzatore una scelta degli angoli della fotocamera da cui visualizzare la stessa scena. Può essere attivo un solo angolo alla volta. Il flusso video contiene anche i dati della didascalia chiusa della riga 21, se esistenti.
-   Ci possono essere fino a otto flussi audio distinti, o tracce, fornendo fino a otto Soundtrack multicanale e consentendo ai dischi Karaoke DVD di usare l'audio multicanale.
-   Un DVD può contenere un massimo di 32 flussi di *Immagini* . Sono costituite da bitmap a 16 colori compresse con un canale alfa, sovrapposto al video. In genere, i flussi delle sottoimmagini contengono sottotitoli e pulsanti di menu, sebbene possano contenere anche altri elementi grafici. Un flusso di sottoimmagine può avere una lingua specificata. Il contenuto di un'immagine è sempre visualizzato e il contenuto di tale immagine viene visualizzato solo se l'utente lo Abilita.

Si noti che le didascalie in un flusso di un'immagine non sono uguali a quelle dei sottotitoli riga 21. Le didascalie chiuse, destinate a utenti con problemi di udito, sono incorporate nel segnale video. Sono costituiti interamente da stringhe di caratteri. Le didascalie dell'immagine, d'altra parte, sono bitmap grafiche. In un dispositivo consumer, i sottotitoli vengono visualizzati dal televisore, mentre il flusso di sottoimmagine viene sottoposto a rendering dal lettore DVD. Un DVD può contenere entrambi i tipi di didascalia.

**Titoli e capitoli**

Il contenuto video in un DVD è suddiviso in *titoli* e *menu*. I titoli sono ulteriormente divisi in unità che la specifica DVD chiama *parti di titoli* (PTTs). Più spesso, questi sono detti *scene* o *capitoli*. La documentazione di DirectShow usa il termine capitolo. Il visualizzatore può passare a titoli o capitoli specifici all'interno di titoli.

L'autore di un DVD decide come dividere il contenuto in titoli e capitoli. Quando un DVD contiene un film di lunghezza della funzionalità, l'intero film viene spesso inserito in un titolo, diviso in capitoli per le singole scene. Le funzionalità aggiuntive del DVD, ad esempio trailer o scene eliminate, vengono inserite in titoli distinti. Tuttavia, queste divisioni sono arbitrarie e molti DVD sono organizzati in modo diverso.

Potrebbero essere presenti fino a 99 titoli in un disco e gli autori di dischi possono dividere il titolo in un massimo di 999 capitoli logici. Nella maggior parte dei film di funzionalità su DVD, il contenuto cinematografico viene formattato come una serie di capitoli che vengono riprodotti automaticamente uno dopo l'altro. Su tali dischi, il marcatore di fine del capitolo contiene un'istruzione di diramazione che indica al lettore di continuare a riprodurre il capitolo successivo della sequenza. Questi titoli sono detti *solo titoli PGC sequenziali*. (PGC corrisponde alla catena di programmi, un altro nome per un gruppo di capitoli che appartengono insieme. Questo termine non viene utilizzato nella documentazione relativa al navigatore DVD. Nei dischi con altri tipi di contenuto, ad esempio i dischi Karaoke, un marcatore di fine capitolo potrebbe indicare al lettore di visualizzare un menu oppure indicare semplicemente al lettore di arrestarsi.

Gli sviluppatori di applicazioni DVD utilizzano i numeri di titolo e capitolo per passare a punti specifici su un disco. Per un accesso più preciso, è possibile usare un numero di titolo e un codice orario. I codici temporali possono essere utilizzati solo con titoli PGC sequenziali, poiché altri tipi non contengono mappe del codice temporale.

**Menu**

La specifica DVD definisce sei tipi di menu:

-   **Titolo.** Il menu titolo è il primo menu da visualizzare. In genere contiene pulsanti per la selezione di titoli. Il menu titolo viene anche chiamato *menu di gestione video*. È disponibile un solo menu titolo in un DVD.
-   **Radice.** Un menu radice è il menu di primo livello di un titolo. Ogni titolo può avere un menu radice. I quattro menu successivi sono sottomenu dal menu radice. Un menu radice viene anche chiamato *menu set del titolo del video*. Il menu radice include in genere pulsanti che consentono di spostarsi tra i titoli del set di titoli. Inoltre, può includere sottomenu che consentono all'utente di scegliere le opzioni per il flusso audio, l'angolo della fotocamera, il flusso di immagini o il capitolo. Tuttavia, questi sottomenu non vengono utilizzati nella maggior parte dei DVD.
-   **Sottoimmagine.** Il menu della sottoimmagine seleziona il flusso dell'immagine.
-   **Audio.** Il menu audio consente di selezionare il flusso audio. In genere, questo menu consente al visualizzatore di selezionare una traccia della lingua.
-   **Angolo.** Il menu angolo seleziona l'angolo della fotocamera.
-   **Capitolo.** Il menu del capitolo, denominato anche menu PTT, seleziona i capitoli all'interno di un titolo.

Per la maggior parte dei menu sono disponibili pulsanti che possono essere *selezionati* e *attivati*. Se si seleziona un pulsante, viene modificato l'aspetto del pulsante. L'attivazione di un pulsante attiva un comando DVD, ad esempio la visualizzazione di un altro menu o l'avvio della riproduzione.

**Livelli di gestione padre**

Tutto o parte di un disco DVD può essere codificato con un livello di gestione padre (PML) numerato da uno a otto. Otto è il livello più restrittivo (solo adulti) e uno è il meno restrittivo (tutte le età). L'idea è impedire agli elementi figlio di guardare i contenuti per adulti senza il consenso del genitore, consentendo allo stesso tempo agli adulti di guardare contenuti figlio. In Stati Uniti e in Canada i livelli vengono mappati al sistema di classificazione della MPAA (G, PG, PG-13, NC-17), ma ciò non avviene in altri paesi o aree geografiche.

Poiché i capitoli possono esistere logicamente all'interno di un blocco padre, è possibile che in un titolo siano presenti due versioni dello stesso capitolo, ognuna delle quali ha assegnato un valore PML diverso e in un blocco padre diverso. Ad esempio, un bambino che esegue l'accesso e riproduce il disco visualizzerà una versione del capitolo 3 e un adulto che esegue l'accesso visualizzerà una versione diversa, presupponendo che l'applicazione supporti PMLs.

Un titolo o un capitolo può anche contenere PMLs temporanei, il cui contenuto è classificato su un valore superiore a PML per il titolo o il capitolo nel suo complesso. Questo significa che un titolo può avere più di un livello padre. I PMLs temporanei vengono in genere creati come blocchi angolari, in modo che una scena in un film possa avere due versioni, una per i visualizzatori più giovani e una per gli adulti.

È responsabilità dell'applicazione del lettore applicare i livelli padre.

**Domini**

Il termine *dominio* si riferisce allo stato interno di un lettore DVD; non è un elemento creato sul disco. I domini sono importanti perché alcuni comandi DVD sono validi solo in alcuni domini. DirectShow consente di eseguire una query sul dominio corrente e di ricevere una notifica quando viene modificato il dominio. Sono definiti i seguenti domini:

-   **Prima riproduzione.** In questo dominio, il lettore DVD ha appena iniziato a riprodurre il DVD. Dopo aver inserito il primo dominio di riproduzione, il lettore passa a un altro dominio, ovvero un dominio di menu o il dominio del titolo, a seconda del disco.
-   **Menu di gestione video.** Il lettore Visualizza il menu di video Manager, detto anche menu titolo.
-   **Menu VTS.** Il lettore Visualizza un menu associato a un set di titoli video, ovvero il menu radice o un sottomenu (audio, immagine secondaria, angolo o capitolo).
-   **Titolo.** Il lettore sta riproducendo video in un titolo.
-   **Arrestare.** Il lettore non visualizza alcun elemento. (In modo esplicito, la specifica DVD non chiama questo stato come dominio, ma può essere considerato come uno).

Il dominio può essere considerato come una variabile di stato monitorata da un lettore DVD, per tenere traccia del tipo di contenuto che il lettore sta attualmente leggendo dal disco. i lettori DVD utilizzano i domini per evitare di emettere comandi significativi nell'unità DVD.

**Controlli dell'operazione dell'utente**

I controlli dell'operazione utente (UOPs) sono indicatori in un disco che gli autori di DVD possono inserire ovunque per limitare le opzioni di navigazione di un utente. La maggior parte dei dischi segue le restrizioni UOP standard. Ad esempio, la maggior parte dei dischi non consente al visualizzatore di eseguire in modo rapido o visualizzare un menu mentre si è in primo dominio di riproduzione. In linea di principio, ogni disco può inserire qualsiasi comando UOP in qualsiasi punto del disco, anche se il comando sarebbe altrimenti valido all'interno del dominio corrente. Ad esempio, è possibile creare un disco per non consentire l'invio rapido in un determinato titolo o per impedire che un particolare menu venga visualizzato dopo che l'utente immette il dominio del titolo. Il navigatore DVD è conforme a tutti questi comandi dal disco e non consente a un'applicazione di eseguire l'override dei controlli UOP del disco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



