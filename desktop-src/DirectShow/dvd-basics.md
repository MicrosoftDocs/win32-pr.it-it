---
description: Nozioni di base su DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Nozioni di base su DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a61299c4c0d3e83235a741c262efae685aa74ffa525aa08f9cf9a2e58b957e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102941"
---
# <a name="dvd-basics"></a>Nozioni di base su DVD

Le funzionalità che rendono il DVD accattivante per i consumer, ovvero diramazione facile, più lingue, controllo genitori, supporto per il mondo dello stile di vita e più angolazioni, rendono anche il lavoro dello sviluppatore un po' più complesso. Un lettore DVD non deve solo riprodurre flussi audio, video e immagini secondarie, ma anche tenere traccia delle opzioni di navigazione attualmente disponibili nel disco e gestire correttamente molti tipi di comandi utente. Lo strumento di navigazione DVD protegge da gran parte di questa complessità consentendo al tempo stesso di creare un'applicazione DVD completamente funzionale. Non è necessario fare riferimento alla specifica DVD per usare l'API DVD Navigator in modo efficace, ma è necessario conoscere i concetti di base di navigazione dei DVD.

**Dati del controllo di navigazione**

I dati audio e video in un disco DVD-Video vengono interfoliati a intervalli regolari con vari tipi di dati di controllo di navigazione. Questi dati possono essere un'istruzione che indica al lettore di eseguire un'operazione, ad esempio lo spostamento in una posizione specifica sul disco, oppure un marcatore informativo che informa il lettore, ad esempio, che il contenuto che segue ha un livello di gestione dei genitori superiore al contenuto precedente o che l'operazione di salto del capitolo è disabilitata. Il giocatore inoltra queste informazioni a un'applicazione ed è responsabilità dell'applicazione agire su di essa. Questi marcatori di navigazione fanno parte di ciò che assegna al DVD un livello più elevato di interattività utente rispetto ai CD video. Un'applicazione lettore DVD deve gestire gli eventi che hanno origine con il disco, nonché gli eventi che hanno origine con l'utente.

**Dati audio, video e immagini secondarie**

Un DVD-Video contiene tre tipi principali di flussi: video, audio e immagine secondaria.

-   Il flusso video può contenere fino a nove "angoli", che possono essere pensati come sottostream. Gli autori di DVD possono includere più angolazioni ovunque vogliano offrire al visualizzatore una scelta di angolazioni della fotocamera da cui visualizzare la stessa scena. Può essere attivo un solo angolo alla volta. Il flusso video contiene anche i dati della riga 21 dei sottotitoli codificati, se presenti.
-   Possono essere presenti fino a otto flussi audio separati, o tracce, che forniscono fino a otto colonne sonore multicanale e consentono ai dischi DVD per dvd di utilizzare l'audio multicanale.
-   Un DVD può contenere fino a 32 *flussi di immagini* secondarie. Sono costituite da bitmap a 16 colori compresse con un canale alfa, sovrapposte al video. In genere, i flussi di immagini secondarie contengono sottotitoli e pulsanti di menu, anche se possono contenere anche altri elementi grafici. Un flusso di immagini secondarie può avere una lingua specificata. Alcuni contenuti delle immagini secondarie vengono sempre visualizzati e alcuni contenuti delle immagini secondarie vengono visualizzati solo se l'utente lo abilita.

Si noti che i sottotitoli in un flusso di immagini secondarie non sono uguali ai sottotitoli codificati della riga 21. I sottotitoli codificati, destinati agli utenti con problemi di udito, vengono incorporati nel segnale video. Sono costituiti interamente da stringhe di caratteri. Le didascalie delle immagini secondarie, d'altra parte, sono bitmap grafiche. In un dispositivo consumer, i sottotitoli codificati vengono visualizzati dal set televisivo, mentre il flusso dell'immagine secondaria viene sottoposto a rendering dal lettore DVD. Un DVD può contenere entrambi i tipi di sottotitoli.

**Titoli e capitoli**

Il contenuto video in un DVD è suddiviso in *titoli* *e menu.* I titoli sono ulteriormente suddivisi in unità che la specifica DVD *chiama parti* di titoli (PTT). Più spesso, si tratta di *scene* o *capitoli.* La documentazione DirectShow usa il termine capitolo. Il visualizzatore può passare a titoli o capitoli specifici all'interno di titoli.

L'autore di un DVD decide come dividere il contenuto in titoli e capitoli. Quando un DVD contiene un film lungometraggio, l'intero film viene spesso inserito in un solo titolo, suddiviso in capitoli per le singole scene. Le funzionalità aggiuntive del DVD, ad esempio trailer o scene eliminate, vengono inserite in titoli separati. Tuttavia, queste divisioni sono arbitrarie e molti DVD sono organizzati in modo diverso.

In un disco possono essere presenti fino a 99 titoli e gli autori di dischi possono dividere il titolo in un massimo di 999 capitoli logici. Nella maggior parte dei film su DVD, il contenuto dei film è formattato come una serie di capitoli che vengono riprodotti automaticamente uno dopo l'altro. Su tali dischi, il marcatore di fine capitolo contiene un'istruzione di diramazione che indica al lettore di continuare a riprodurre il capitolo successivo nella sequenza. Questi titoli sono denominati *One Sequential PGC Titles*. (PGC è l'acronimo di Program Chain, un altro nome per un gruppo di capitoli che appartengono insieme. Questo termine non viene usato nella documentazione di DVD Navigator. Nei dischi con altri tipi di contenuto, ad esempio dischi per il baseball, un marcatore di fine capitolo potrebbe indicare al lettore di visualizzare un menu o potrebbe semplicemente indicare al lettore di arrestarsi.

Gli sviluppatori di applicazioni DVD usano i numeri di titolo e capitolo per passare a punti specifici su un disco. Per un accesso più fine, è possibile usare un numero time code titolo. I codici di tempo possono essere usati solo con un titolo PGC sequenziale, poiché altri tipi non contengono time code mappe.

**Menu**

La specifica DVD definisce sei tipi di menu:

-   **Titolo.** Il menu del titolo è il primo menu da visualizzare. In genere contiene pulsanti per la selezione dei titoli. Il menu del titolo è denominato anche *menu di gestione video.* In un DVD è presente un solo menu titolo.
-   **Radice.** Un menu radice è il menu di primo livello per un titolo. Ogni titolo può avere un menu radice. I quattro menu successivi sono sottomenu del menu radice. Un menu radice è anche detto *menu del set di titoli video.* Il menu radice include in genere pulsanti che consentono di passare a uno dei titoli nel set di titoli. Inoltre, può avere sottomenu che consentono all'utente di scegliere le opzioni per il flusso audio, l'angolo della fotocamera, il flusso di immagini secondarie o il capitolo. Tuttavia, questi sottomenu non vengono usati nella maggior parte dei DVD.
-   **Immagine secondaria.** Il menu dell'immagine secondaria seleziona il flusso dell'immagine secondaria.
-   **Audio.** Il menu audio seleziona il flusso audio. In genere, questo menu consente al visualizzatore di selezionare una traccia della lingua.
-   **Angolo.** Il menu dell'angolo seleziona l'angolo della fotocamera.
-   **Capitolo.** Il menu del capitolo, detto anche menu PTT, seleziona i capitoli all'interno di un titolo.

La maggior parte dei menu ha pulsanti, che possono *essere selezionati* e *attivati.* La selezione di un pulsante modifica l'aspetto del pulsante. L'attivazione di un pulsante attiva un comando DVD, ad esempio la visualizzazione di un altro menu o l'avvio della riproduzione.

**Livelli di gestione dei genitori**

Tutto o parte di un disco DVD può essere codificato con un livello di gestione genitori (PML) numerato da uno a otto. Otto è il livello più restrittivo (solo adulti) e uno è il meno restrittivo (tutte le età). L'idea è impedire ai bambini di guardare contenuti per adulti senza il consenso dei genitori, consentendo allo stesso tempo agli adulti di guardare contenuti sicuri per i bambini. Nel Stati Uniti e in Canada, i livelli vengono mappati al sistema di valutazione dell'area MPAA (G, PG, PG-13, NC-17), ma questo non è il caso in altri paesi o aree geografiche.

Poiché i capitoli possono esistere logicamente all'interno di un blocco parentale, possono essere presenti due versioni dello stesso capitolo in un titolo, ognuna con un PML diverso e in un blocco di genitori diverso. Ad esempio, un figlio che accede e riproduce il disco dovrebbe visualizzare una versione del capitolo 3 e un adulto che accede visualizza una versione diversa, presupponendo che l'applicazione supporti i file PML.

Un titolo o un capitolo può anche contenere file PML temporanei, il cui contenuto è valutato più alto del PML per il titolo o il capitolo nel suo complesso. Ciò significa che un titolo può avere più di un livello di genitori. I pml temporanei vengono in genere creati come blocchi angolari, in modo che una scena in un film possa avere due versioni, una classificata per i più piccoli e una per gli adulti.

È responsabilità dell'applicazione del giocatore applicare i livelli di genitori.

**Domini**

Il termine *dominio si* riferisce allo stato interno di un lettore DVD. non è un elemento creato sul disco. I domini sono importanti perché alcuni comandi DVD sono validi solo in determinati domini. DirectShow consente di eseguire query sul dominio corrente e di ricevere una notifica quando il dominio cambia. Sono definiti i domini seguenti:

-   **Prima di tutto Play.** In questo dominio, il lettore DVD ha appena iniziato a riprodurre il DVD. Dopo aver immesso il dominio First Play, il lettore passa a un altro dominio, ovvero un dominio di menu o il dominio del titolo, a seconda del disco.
-   **Menu Gestione video.** Il lettore visualizza il menu Gestione video, detto anche menu del titolo.
-   **Menu VTS.** Il lettore visualizza un menu associato a un set di titoli video, ovvero il menu radice o un sottomenu (audio, immagine secondaria, angolo o capitolo).
-   **Titolo.** Il lettore sta riproducendo il video in un titolo.
-   **Fermare.** Il lettore non visualizza nulla. In senso stretto, la specifica DVD non definisce questo stato come dominio, ma può essere considerato come un dominio.

Il dominio può essere pensato come una variabile di stato monitorata da un lettore DVD per tenere traccia del tipo di contenuto che il lettore sta attualmente leggendo dal disco. I lettori DVD usano i domini per evitare di emettere comandi non importanti nell'unità DVD.

**Controlli delle operazioni utente**

I controlli delle operazioni utente sono marcatori su un disco che gli autori di DVD possono inserire in qualsiasi punto per limitare le opzioni di navigazione dell'utente. La maggior parte dei dischi segue le restrizioni UOP standard. Ad esempio, la maggior parte dei dischi non consente al visualizzatore di inoltrare rapidamente o visualizzare un menu nel dominio First Play. In linea di principio, ogni disco può inserire qualsiasi comando UOP in qualsiasi punto del disco, anche se il comando sarebbe altrimenti valido all'interno del dominio corrente. Ad esempio, un disco può essere creato per impedire l'inoltro rapido in un determinato titolo o per impedire la visualizzazione di un determinato menu dopo che l'utente ha immesso il dominio del titolo. Dvd Navigator è conforme a tutti questi comandi dal disco e non consentirà a un'applicazione di eseguire l'override dei controlli UOP del disco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



