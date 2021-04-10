---
title: Icone standard
description: Le icone standard sono le icone di errore, avviso, informazioni e punto interrogativo che fanno parte di Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 69085f4c527db8431b5e33f0dba4668d43d1c669
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351056"
---
# <a name="standard-icons"></a>Icone standard

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le icone standard sono le icone di errore, avviso, informazioni e punto interrogativo che fanno parte di Windows.

![Screenshot di quattro icone standard ](images/vis-std-icons-image1.png)

Icone di errore, avviso, informazioni e punto interrogativo standard.

Le icone standard hanno i significati seguenti:

-   **Icona di errore.** L'interfaccia utente (UI) presenta un errore o un problema che si è verificato.
-   **Icona di avviso.** L'interfaccia utente presenta una condizione che potrebbe causare un problema in futuro.
-   **Icona informazioni.** L'interfaccia utente presenta informazioni utili.
-   **Icona del punto interrogativo.** L'interfaccia utente indica un punto di ingresso della guida.

Le icone standard sono importanti perché sono compilate in molte API (Application Programming Interface) di Windows, ad esempio le finestre di [dialogo delle attività](win-dialog-box.md), le [finestre di messaggio](glossary.md), i [palloncini](ctrl-balloons.md)e le [notifiche](mess-notif.md). Sono comunemente usati anche nei [messaggi sul posto e nelle barre di](glossary.md) [stato](ctrl-status-bars.md).

**Nota:** Le linee guida correlate alle [Icone](vis-icons.md) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Ci sono diversi fattori nella scelta dell'icona standard appropriata, che in parte spiega perché vengono usati spesso in modo non corretto. Gli errori più comuni sono:

-   Uso di un'icona di avviso per errori secondari. Gli avvisi non sono errori "attenuati".
-   Usare un'icona standard quando è preferibile non usare alcuna icona. Non tutti i messaggi richiedono un'icona.
-   Avvisare gli utenti fornendo avvisi per problemi di lieve entità o presentare domande di routine come avvisi. In questo modo i programmi risultano soggetti a rischi e derivano da problemi realmente significativi.

Nella parte restante di questa sezione viene illustrato come pensare alle icone standard per evitare questi errori comuni.

### <a name="message-type-vs-severity"></a>Tipo di messaggio e gravità

Scegliere icone standard in base al tipo di messaggio, non alla gravità del problema sottostante. I tipi di messaggio sono:

-   **Errore.** Errore o problema che si è verificato.
-   **Avviso.** Condizione che potrebbe causare un problema in futuro.
-   **Informazioni.** Informazioni utili.

Di conseguenza, un messaggio di errore potrebbe richiedere un'icona di errore ma non un'icona di avviso. Non usare icone di avviso per attenuare gli errori secondari. Quindi, nonostante la differenza di gravità, "dimensioni del carattere non corrette" è un errore, mentre la "continuazione con questa operazione consentirà di impostare la casa in caso di incendio" è un avviso.

### <a name="determining-the-appropriate-message-type"></a>Determinazione del tipo di messaggio appropriato

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato basato sulla configurazione corrente di Windows Internet Explorer:

-   **Errore.** "Questa pagina non può caricare un controllo ActiveX senza segno". (Frase come problema esistente).
-   **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per il caricamento di controlli ActiveX non firmati". oppure "Consenti a questa pagina di installare un controllo ActiveX senza segno? Questa operazione da origini non attendibili potrebbe danneggiare il computer ". (Entrambe espresse come condizioni che possono causare problemi futuri).
-   **Informazioni.** "È stato configurato Windows Internet Explorer per bloccare i controlli ActiveX non firmati." (Enunciato come dichiarazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono sapere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, viene visualizzato come errore; Se l'utente può continuare, si tratta di un avviso. Creare l' [istruzione principale](text-ui.md) o un altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona (standard o altro) che corrisponda al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

### <a name="severity"></a>Gravità

Mentre la gravità non è una considerazione quando si sceglie tra le icone di errore, di avviso e di informazioni, la **gravità è un fattore determinante se deve essere usata un'icona standard.**

Le icone funzionano meglio quando vengono usate per comunicare visivamente. Si noti che per motivi di accessibilità questa comunicazione visiva deve sempre essere ridondante con un altro modulo, ad esempio testo o audio. Gli utenti dovrebbero essere in grado di indicare a colpo d'occhio la natura delle informazioni e le conseguenze della loro risposta, quindi è necessario distinguere gli errori critici e gli avvisi dalle controparti ordinarie. Gli errori e gli avvisi critici presentano queste caratteristiche:

-   Che comportano una perdita potenziale di uno o più degli elementi seguenti:
    -   Una risorsa preziosa, ad esempio la perdita di dati o la perdita finanziaria.
    -   Accesso al sistema o integrità.
    -   Privacy o controllo sulle informazioni riservate.
    -   Tempo utente (un importo significativo, ad esempio 30 secondi o più).
-   Hanno conseguenze impreviste o impreviste.
-   Richiedono una corretta gestione adesso, perché gli errori non possono essere risolti facilmente e possono anche essere irreversibili.

Per distinguere gli errori e gli avvisi non critici da quelli critici, i messaggi non critici vengono in genere visualizzati senza un'icona. Questa operazione richiama l'attenzione sui messaggi critici, rende visivamente distinti i messaggi critici e non critici ed è coerente con il [tono di Windows](text-style-tone.md).

Non tutti i messaggi richiedono un'icona. Le icone non rappresentano un modo per decorare i messaggi.

Di seguito è riportato un valido esempio di avviso critico perché soddisfa le caratteristiche definite in precedenza.

![Screenshot di un avviso per eseguire il backup dei dati ](images/vis-std-icons-image2.png)

In questo esempio, un avviso critico avvisa gli utenti di potenziali perdite di dati irreversibili.

Tuttavia, l'esempio successivo non è critico perché è probabile che sia intenzionale e che i risultati vengano annullati facilmente.

**Non corretto:**

![Screenshot di un uso fuorviante di un'icona di avviso ](images/vis-std-icons-image3.png)

In questo esempio, questa [conferma](mess-confirm.md) non è cruciale perché è probabile che sia intenzionale e annullata facilmente.

In una tipica interfaccia utente la maggior parte degli errori si riferisce agli errori di input dell'utente. La maggior parte degli errori di input dell'utente non è fondamentale perché sono facilmente corretti e gli utenti devono correggerli prima di continuare. Inoltre, il prelievo di troppe attenzioni sugli errori degli utenti secondari è contrario al tono di Windows. Di conseguenza, gli errori di input degli utenti secondari vengono in genere visualizzati senza un'icona di errore. Per rafforzare la natura non critica, si fa riferimento a questi problemi come input dell'utente.

![screenshot che informa gli utenti dell'input corretto ](images/vis-std-icons-image4.png)

In questo esempio, questo problema di input dell'utente secondario non è critico, pertanto non è necessaria un'icona quando viene visualizzato in una finestra di dialogo.

### <a name="avoid-overwarning"></a>Evitare l'overwarning

I programmi di Windows sono overwarn. Il normale programma Windows presenta icone di avviso apparentemente ovunque, avvisi relativi a elementi con scarso significato. In alcuni programmi, quasi tutte le domande vengono presentate come un avviso. L'overwarning fa in modo che l'uso di un programma risulti un'attività pericolosa e si riducono da problemi realmente significativi.

Il mero potenziale per la perdita di dati da solo non è sufficiente per chiamare un'icona di avviso. Inoltre, eventuali risultati indesiderati devono essere imprevisti o imprevisti e non facilmente corretti. In caso contrario, è possibile che venga interpretata la perdita di dati di un certo tipo e che si meriti un'icona di avviso.

Per concentrare le icone di avviso sui problemi realmente critici:

-   Verificare che il problema giustifichi l'attenzione dell'utente. Le [conferme](mess-confirm.md) e le domande di routine non devono avere icone di avviso.
-   È probabile che gli utenti si comportino in modo diverso in seguito all'icona di avviso? È probabile che gli utenti considerino la decisione con maggiore attenzione?

**Non corretto:**

![screenshot dell'icona di avviso usata inutilmente ](images/vis-std-icons-image5.png)

In questo esempio, è probabile che gli utenti rispondano a questa domanda in modo diverso a causa dell'icona di avviso?

-   Sono previste azioni significative da eseguire o da prendere in decisione? Gli avvisi senza azioni fanno solo sentire paranoici.

**Non corretto:**

![screenshot dell'icona di avviso usata con promemoria ](images/vis-std-icons-image6.png)

Perché si tratta di una notifica di avviso? Che cosa dovrebbero fare gli utenti (oltre a preoccuparsi)?

### <a name="context"></a>Context

Il contesto è anche una considerazione nell'uso delle icone standard, perché il contesto stesso comunica le informazioni. In particolare:

-   Nelle finestre di dialogo (incluse le finestre di dialogo e le finestre di messaggio) e le notifiche non sono necessarie icone per errori non critici, gli errori sul posto richiedono sempre icone di errore. In caso contrario, il feedback non modale sarà troppo facile da ignorare.
-   Gli avvisi sul posto richiedono sempre icone di avviso per distinguerli dal testo normale.
-   Per le finestre di dialogo, le notifiche e gli aerostati non sono necessarie le icone delle informazioni perché presentano chiaramente informazioni. Al contrario, i banner necessitano di informazioni 16x16 pixel o altre icone, perché questo feedback non modale sarebbe troppo semplice da ignorare.

Poiché il contesto è un fattore significativo nell'utilizzo delle icone, le linee guida per le icone standard in questo articolo sono fornite in termini di contesto.

### <a name="evaluating-standard-icon-appropriateness"></a>Valutazione dell'idoneità dell'icona standard

Quando si valuta il testo dell'interfaccia utente, è possibile leggere anche tutte le icone standard. Leggere le icone di errore come "Error!", icone di avviso come "avviso, prestare attenzione qui!" e le icone delle informazioni come "attenzione!". Continuare quindi a leggere il contesto rimanente, ad esempio l'istruzione principale, l'area del contenuto e i pulsanti di commit. Verificare che il significato e il tono di ogni icona standard corrispondano al significato e al tono del relativo contesto. In caso contrario, si è riscontrato un problema.

**Se si esegue una sola operazione...**

Verificare che il significato e il tono di ogni icona standard corrispondano al significato e al tono del relativo contesto. Se non corrispondono, modificare o rimuovere l'icona.

## <a name="guidelines"></a>Indicazioni

**Nota:** Per le linee guida seguenti, "sul posto" significa su qualsiasi superficie normale della finestra, ad esempio all'interno dell'area del contenuto di una procedura guidata, della finestra delle proprietà o della pagina dell'elemento del pannello di controllo.

### <a name="general"></a>Generale

-   Scegliere icone standard in base al tipo di messaggio, non alla gravità del problema sottostante:
    -   **Errore.** Errore o problema che si è verificato.
    -   **Avviso.** Condizione che potrebbe causare un problema in futuro.
    -   **Informazioni.** Informazioni utili.
-   Se un problema si concentra sui diversi tipi di messaggi, concentrarsi sull'aspetto più importante su cui gli utenti devono agire.
-   Le icone devono sempre corrispondere all'istruzione principale o ad altro testo corrispondente.

**Corretto:**

![screenshot dell'icona di errore utilizzata con il testo dell'errore ](images/vis-std-icons-image7.png)

**Non corretto:**

![screenshot dell'icona di avviso utilizzata con il testo dell'errore ](images/vis-std-icons-image8.png)

Nell'esempio errato, l'icona di avviso standard non corrisponde all'istruzione principale (che restituisce un errore).

### <a name="icon-size"></a>Dimensioni icona

-   **Scegliere le dimensioni dell'icona standard in base al contesto:**
  



    | Context                         | Utilizzo                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>  | Usare il pixel 32x32 per le icone dell'area di contenuto; pixel 16x16 per le icone dell'area a piè di nota.<br/> |
    | Sul posto<br/>      | Usare il pixel 32x32 per le pagine di errore; Icone pixel 16x16 per tutti gli altri.<br/>           |
    | Notifiche<br/> | Usare le icone 16x16 pixel.<br/>                                                       |
    | Palloncini<br/>      | Usare le icone 16x16 pixel.<br/>                                                       |
    | Banner<br/>       | Usare le icone 16x16 pixel.<br/>                                                       |



 

### <a name="error-icons"></a>Icone di errore

-   **Usare icone di errore solo quando si è verificato un errore o un problema:**



    | Context                           | Utilizzo                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>    | Utilizzare solo per errori critici. Non usare icone standard per errori non critici. <br/> ![Screenshot che mostra l'icona di errore utilizzata con il messaggio di errore ](images/vis-std-icons-image9.png)<br/>                                              |
    | Errori sul posto<br/> | Usare per tutti gli errori. <br/> ![screenshot dell'icona di errore utilizzata con un messaggio di errore.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notifiche<br/>   | Utilizzare solo per errori critici. per gli [errori di azione](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx). <br/> ![Screenshot che mostra un'icona di errore utilizzata con un messaggio di errore di notifica.](images/vis-std-icons-image11.png)<br/> |
    | Palloncini<br/>        | Non usare. Gli aerostati non devono essere usati per errori critici e non richiedono icone di errore per errori non critici.<br/>                                                                                                               |
    | Banner<br/>         | Non usare. I banner non devono essere usati per gli errori.<br/>                                                                                                                                                                                  |



 

-   In genere, le icone di errore non sono necessarie per problemi di input utente non critici. Tuttavia, le icone sono necessarie per gli errori sul posto, perché altrimenti tali commenti contestuali sarebbero troppo semplici da ignorare.
-   **Per le finestre di dialogo attività, non usare icone note di errore.** Le icone di errore devono essere presentate solo nell'area del contenuto.

### <a name="warning-icons"></a>Icone di avviso

-   **Usare le icone di avviso solo quando una condizione potrebbe causare un problema in futuro:**



    | Context                             |  Utilizzo                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>      | Utilizzare per tutti gli avvisi. <br/> ![avviso di screenshot della modifica dell'estensione del nome di file ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Avvisi sul posto<br/> | Utilizzare per identificare il testo come un avviso. <br/> ![screenshot dell'avviso di spazio disponibile insufficiente ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notifiche<br/>     | Utilizzare per tutti gli avvisi. (per [gli eventi di sistema non critici](glossary.md)). <br/> ![screenshot della notifica di avviso a batteria insufficiente ](images/vis-std-icons-image14.png)<br/> |
    | Palloncini<br/>          | Usare per [le condizioni speciali](ctrl-balloons.md). <br/> ![cattura di schermata dell'avviso del blocco maiuscolo ](images/vis-std-icons-image15.png)<br/>                           |
    | Banner<br/>           | Usare per attirare l'attenzione sul banner. <br/> ![screenshot del banner con avviso di TPM mancante ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **Non usare icone di avviso per "ammorbidire" gli errori non critici.** Gli errori non sono avvisi applicano le linee guida dell'icona di errore.
-   **Per le finestre di dialogo delle domande, usare le icone di avviso solo per le domande con conseguenze significative.** Non usare icone di avviso per domande di routine.

**Corretto:**

![avviso per non arrestare il ripristino del sistema ](images/vis-std-icons-image17.png)

**Non corretto:**

![cattura di schermata di avviso sulla chiusura dei promemoria ](images/vis-std-icons-image18.png)

Nell'esempio errato, un'icona di avviso viene utilizzata erroneamente per una domanda di routine.

-   **Per le finestre di dialogo delle attività, è possibile usare un'icona a piè di pagina di avviso per avvertire gli utenti delle conseguenze rischiose.** Tuttavia, usare un'icona di avviso nell'area del contenuto o nell'area della nota, ma non in entrambi.

![avviso di screenshot di un file potenzialmente non sicuro ](images/vis-std-icons-image19.png)

In questo esempio viene usato un scudo di sicurezza giallo in una nota a piè di pagina.

### <a name="information-icons"></a>Icone informazioni

-   **Usare le icone delle informazioni solo quando il contesto non presenta ovviamente le informazioni:**



    | Context                         | Utilizzo                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>  | Non usare.<br/>                                                                                                                             |
    | Sul posto<br/>      | Non usare. Usare invece un testo statico normale o un banner.<br/>                                                                           |
    | Notifiche<br/> | Non usare.<br/>                                                                                                                             |
    | Palloncini<br/>      | Non usare.<br/>                                                                                                                             |
    | Banner<br/>       | usare per attirare l'attenzione sul banner. <br/> ![screenshot del banner con le informazioni sulle impostazioni ](images/vis-std-icons-image20.png)<br/> |



 

-   Le icone delle informazioni non sono necessarie nelle finestre di dialogo, nelle notifiche e nei palloni perché il contesto comunica sufficientemente che forniscono agli utenti informazioni.
-   **Per le finestre di dialogo attività, non usare le icone a piè di pagina delle informazioni.** Le note a piè di pagina sono sufficientemente visibili e vanno senza dire che si tratta di informazioni.

### <a name="question-mark-icons"></a>Icone punto interrogativo

-   **Utilizzare l'icona del punto interrogativo solo per i punti di ingresso della guida.** Per ulteriori informazioni, vedere le linee guida del [punto di ingresso della Guida](winenv-help.md) .
-   **Non usare l'icona del punto interrogativo per porre domande.** Anche in questo caso, usare l'icona del punto interrogativo solo per i punti di ingresso della guida. Non è necessario porre domande usando l'icona del punto interrogativo, tuttavia è sufficiente presentare un'istruzione principale come domanda.
-   **Non sostituire periodicamente le icone dei punti interrogativi con le icone di avviso.** Sostituire un'icona con un punto interrogativo con un'icona di avviso solo se la domanda ha conseguenze significative. In caso contrario, usare nessuna icona.

 

