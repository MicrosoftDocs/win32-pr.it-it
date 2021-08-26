---
title: Icone standard
description: Le icone standard sono le icone di errore, avviso, informazioni e punto interrogativo che fanno parte di Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74f5b70fb218606eb5f87cbad247c1c75a100f9c5e0f675bb6c075e559fd1a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936383"
---
# <a name="standard-icons"></a>Icone standard

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le icone standard sono le icone di errore, avviso, informazioni e punto interrogativo che fanno parte di Windows.

![Screenshot di quattro icone standard ](images/vis-std-icons-image1.png)

Icone di errore, avviso, informazioni e punto interrogativo standard.

Le icone standard hanno questi significati:

-   **Icona di errore.** L'interfaccia utente presenta un errore o un problema che si è verificato.
-   **Icona di avviso.** L'interfaccia utente presenta una condizione che potrebbe causare un problema in futuro.
-   **Icona Informazioni.** L'interfaccia utente presenta informazioni utili.
-   **Icona punto interrogativo.** L'interfaccia utente indica un punto di ingresso della Guida.

Le icone standard sono importanti perché sono incorporate in molte API (Application Programming Interface) di Windows, [](ctrl-balloons.md)ad esempio finestre di dialogo [attività,](win-dialog-box.md)finestre di [messaggio,](glossary.md)fumetto e [notifiche.](mess-notif.md) Vengono comunemente usati anche nei [messaggi sul](glossary.md) posto e nelle barre [di stato](ctrl-status-bars.md).

**Nota:** Le linee guida [relative alle icone](vis-icons.md) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Esistono diversi fattori nella scelta dell'icona standard appropriata che spiega in parte perché vengono usate così spesso in modo errato. Gli errori più comuni sono:

-   Uso di un'icona di avviso per errori secondari. Gli avvisi non sono errori "attenuati".
-   Uso di un'icona standard quando è meglio non usare alcuna icona. Non tutti i messaggi hanno bisogno di un'icona.
-   Allarmare gli utenti fornendo avvisi per problemi minori o presentando domande di routine come avvisi. In questo modo, i programmi appaiono increscio e sminerano da problemi realmente significativi.

Nella parte restante di questa sezione viene illustrato come pensare alle icone standard per evitare questi errori comuni.

### <a name="message-type-vs-severity"></a>Tipo di messaggio e gravità

Scegliere le icone standard in base al tipo di messaggio, non alla gravità del problema sottostante. I tipi di messaggio sono:

-   **Errore.** Si è verificato un errore o un problema.
-   **Avviso.** Condizione che potrebbe causare un problema in futuro.
-   **Informazioni.** Informazioni utili.

Di conseguenza, un messaggio di errore potrebbe richiedere un'icona di errore, ma mai un'icona di avviso. Non usare le icone di avviso per attenuare gli errori secondari. Pertanto, nonostante la differenza di gravità, "Dimensione del carattere non corretta" è un errore, mentre "Continuare con questa operazione darà fuoco alla casa" è un avviso.

### <a name="determining-the-appropriate-message-type"></a>Determinazione del tipo di messaggio appropriato

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato in base alla configurazione Windows Internet Explorer corrente:

-   **Errore.** "Questa pagina non può caricare un controllo ActiveX non firmato." (Formulato come un problema esistente.
-   **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per caricare i controlli ActiveX non firmati." o "Consenti a questa pagina di installare un controllo ActiveX non firmato? Questa operazione da origini non attendibili può danneggiare il computer." Entrambe formulate come condizioni che possono causare problemi futuri.
-   **Informazioni.** "Sono stati configurati Windows Internet Explorer per bloccare i controlli ActiveX non firmati." (Formulato come una dichiarazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono conoscere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, viene visualizzato come errore. se l'utente può procedere, si tratta di un avviso. Creare [l'istruzione principale](text-ui.md) o altro testo corrispondente in base a tale stato attivo e quindi scegliere un'icona (standard o diversa) che corrisponde al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

### <a name="severity"></a>Gravità

Anche se la gravità non è una considerazione quando si sceglie tra le icone di errore, avviso e informazioni, la gravità è un fattore per determinare se un'icona standard deve essere **usata.**

Le icone funzionano meglio se usate per comunicare visivamente. Si noti che per motivi di accessibilità, questa comunicazione visiva deve essere sempre ridondante con un'altra forma, ad esempio testo o suono. Gli utenti devono essere in grado di indicare a colpo d'occhio la natura delle informazioni e le conseguenze della risposta, quindi è necessario distinguere gli errori critici e gli avvisi dalle controparti ordinarie. Gli errori e gli avvisi critici hanno queste caratteristiche:

-   Comportano una potenziale perdita di uno o più degli elementi seguenti:
    -   Un asset prezioso, ad esempio perdita di dati o perdita finanziaria.
    -   Accesso o integrità del sistema.
    -   Privacy o controllo sulle informazioni riservate.
    -   Tempo dell'utente (una quantità significativa, ad esempio 30 secondi o più).
-   Hanno conseguenze impreviste o impreviste.
-   Richiedono ora una gestione corretta, perché gli errori non possono essere risolti facilmente e possono anche essere irreversibili.

Per distinguere gli errori e gli avvisi non critici da quelli critici, i messaggi non critici vengono in genere visualizzati senza un'icona. Questa operazione richiama l'attenzione dei messaggi critici, rende visivamente distinti i messaggi critici e non critici ed è coerente con il tono [Windows.](text-style-tone.md)

Non tutti i messaggi hanno bisogno di un'icona. Le icone non sono un modo per decorare i messaggi.

Di seguito è riportato un buon esempio di avviso critico perché soddisfa le caratteristiche definite in precedenza.

![Screenshot di un avviso per eseguire il backup dei dati ](images/vis-std-icons-image2.png)

In questo esempio, un avviso critico avvisa gli utenti di una potenziale perdita irreversibile di dati.

Tuttavia, l'esempio successivo non è critico perché è probabile che sia intenzionale e che i risultati siano facilmente annullabili.

**Non corretto:**

![Screenshot di un uso fuorviante di un'icona di avviso ](images/vis-std-icons-image3.png)

In questo esempio, questa [conferma](mess-confirm.md) non è fondamentale perché è probabile che sia intenzionale e facilmente annullata.

In un'interfaccia utente tipica la maggior parte degli errori è correlata agli errori di input dell'utente. La maggior parte degli errori di input dell'utente non è fondamentale perché sono facilmente corretti e gli utenti devono correggerli prima di continuare. Inoltre, attirare troppo attenzione agli errori minori dell'utente è contrario al Windows tono. Di conseguenza, gli errori di input utente minori vengono in genere visualizzati senza un'icona di errore. Per rafforzare la natura non critica, si tratta di problemi di input dell'utente.

![Screenshot che informa gli utenti dell'input corretto ](images/vis-std-icons-image4.png)

In questo esempio, questo piccolo problema di input dell'utente non è critico, quindi non è necessaria un'icona quando viene visualizzata in una finestra di dialogo.

### <a name="avoid-overwarning"></a>Evitare l'overwarning

Si è invasa in Windows programmi. Il tipico Windows ha icone di avviso apparentemente ovunque, che avvisano su elementi che hanno poco significato. In alcuni programmi quasi tutte le domande vengono presentate come avviso. L'overwarning fa in modo che l'uso di un programma sia un'attività rischiosa e sminuziona i problemi realmente significativi.

Il semplice potenziale di perdita di dati da solo non è sufficiente per chiamare un'icona di avviso. Inoltre, tutti i risultati indesiderati devono essere imprevisti o imprevisti e non essere facilmente corretti. In caso contrario, è possibile che qualsiasi domanda con risposta errata possa comportare una perdita di dati di qualche tipo e meritare un'icona di avviso.

Per concentrare le icone di avviso su problemi realmente critici:

-   Assicurarsi che il problema garantisca una maggiore attenzione da parte dell'utente. [Le conferme e](mess-confirm.md) le domande di routine non devono avere icone di avviso.
-   È probabile che gli utenti si comportino in modo diverso in seguito all'icona di avviso? È probabile che gli utenti considerino la decisione con maggiore attenzione?

**Non corretto:**

![screenshot dell'icona di avviso usata inutilmente ](images/vis-std-icons-image5.png)

In questo esempio è probabile che gli utenti rispondano a questa domanda in modo diverso a causa dell'icona di avviso?

-   C'è un'azione significativa da fare o da prendere? Gli avvisi senza azioni fanno solo in modo che gli utenti si senta paranoico.

**Non corretto:**

![Screenshot dell'icona di avviso usata con il promemoria ](images/vis-std-icons-image6.png)

Perché questa notifica è un avviso? Cosa dovrebbero fare gli utenti (oltre alla preoccupazione)?

### <a name="context"></a>Context

Il contesto è anche una considerazione per l'uso delle icone standard perché il contesto stesso comunica le informazioni. In particolare:

-   Anche se le finestre di dialogo( incluse le finestre di dialogo attività e le finestre di messaggio) e le notifiche non necessitano di icone per gli errori non critici, gli errori sul posto necessitano sempre di icone di errore. In caso contrario, tale feedback non modale sarebbe troppo facile da tralasciare.
-   Gli avvisi sul posto necessitano sempre di icone di avviso per distinguerle dal testo normale.
-   Le finestre di dialogo, le notifiche e i balloon non necessitano di icone di informazioni perché presentano chiaramente le informazioni. Al contrario, i banner necessitano di informazioni di 16x16 pixel o altre icone perché tale feedback non modale sarebbe troppo facile da tralasciare.

Poiché il contesto è un fattore significativo nell'utilizzo delle icone, le linee guida standard per le icone in questo articolo vengono fornite in termini di contesto.

### <a name="evaluating-standard-icon-appropriateness"></a>Valutazione dell'appropriatezza dell'icona standard

Quando si valuta il testo dell'interfaccia utente, leggere anche le icone standard. Leggere le icone di errore come "errore!", le icone di avviso come "avviso, prestare molta attenzione qui!" e le icone delle informazioni come "attenzione!". Continuare quindi a leggere il contesto rimanente, ad esempio l'istruzione principale, l'area del contenuto e i pulsanti di commit. Assicurarsi che il significato e il tono di ogni icona standard corrispondano al significato e al tono del contesto. In caso contrario, è stato rilevato un problema.

**Se si fa una sola cosa...**

Assicurarsi che il significato e il tono di ogni icona standard corrispondano al significato e al tono del contesto. Se non corrispondono, modificare o rimuovere l'icona.

## <a name="guidelines"></a>Indicazioni

**Nota:** Per le linee guida seguenti, "sul posto" significa in qualsiasi normale area della finestra, ad esempio all'interno dell'area del contenuto di una procedura guidata, una finestra delle proprietà o una pagina di elementi del Pannello di controllo.

### <a name="general"></a>Generale

-   Scegliere le icone standard in base al tipo di messaggio, non alla gravità del problema sottostante:
    -   **Errore.** Errore o problema che si è verificato.
    -   **Avviso.** Condizione che potrebbe causare un problema in futuro.
    -   **Informazioni.** Informazioni utili.
-   Se un problema si verifica in diversi tipi di messaggio, concentrarsi sull'aspetto più importante su cui gli utenti devono intervenire.
-   Le icone devono sempre corrispondere all'istruzione principale o a un altro testo corrispondente.

**Corretto:**

![Screenshot dell'icona di errore usata con il testo dell'errore ](images/vis-std-icons-image7.png)

**Non corretto:**

![Screenshot dell'icona di avviso usata con il testo dell'errore ](images/vis-std-icons-image8.png)

Nell'esempio non corretto, l'icona di avviso standard non corrisponde all'istruzione principale (che restituisce un errore).

### <a name="icon-size"></a>Dimensioni icona

-   **Scegliere le dimensioni dell'icona standard in base al contesto:**
  



    | Context                         | Utilizzo                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>  | Usare 32x32 pixel per le icone dell'area del contenuto; 16x16 pixel per le icone dell'area delle note a piè di pagina.<br/> |
    | Sul posto<br/>      | Usare 32x32 pixel per le pagine di errore; Icone da 16x16 pixel per tutti gli altri.<br/>           |
    | Notifiche<br/> | Usare icone da 16x16 pixel.<br/>                                                       |
    | Palloncini<br/>      | Usare icone da 16x16 pixel.<br/>                                                       |
    | Banner<br/>       | Usare icone da 16x16 pixel.<br/>                                                       |



 

### <a name="error-icons"></a>Icone di errore

-   **Usare le icone di errore solo quando si è verificato un errore o un problema:**



    | Context                           | Utilizzo                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>    | Usare solo per gli errori critici. Non usare icone standard per gli errori non critici. <br/> ![Screenshot che mostra l'icona di errore usata con il messaggio di errore ](images/vis-std-icons-image9.png)<br/>                                              |
    | Errori sul posto<br/> | Usare per tutti gli errori. <br/> ![Screenshot dell'icona di errore usata con un messaggio di errore.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notifiche<br/>   | Usare solo per gli errori critici. (per [gli errori di azione).](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx) <br/> ![Screenshot che mostra un'icona di errore usata con un messaggio di errore di notifica.](images/vis-std-icons-image11.png)<br/> |
    | Palloncini<br/>        | Non usare. I balloon non devono essere usati per gli errori critici e non necessitano di icone di errore per gli errori non critici.<br/>                                                                                                               |
    | Banner<br/>         | Non usare. I banner non devono essere usati per gli errori.<br/>                                                                                                                                                                                  |



 

-   In genere, le icone di errore non sono necessarie per i problemi di input utente non critici. Tuttavia, le icone sono necessarie per gli errori sul posto, perché in caso contrario tale feedback contestuale sarebbe troppo facile da tralasciare.
-   **Per le finestre di dialogo attività, non usare icone di nota a piè di pagina di errore.** Le icone di errore devono essere visualizzate solo nell'area del contenuto.

### <a name="warning-icons"></a>Icone di avviso

-   **Usare le icone di avviso solo quando una condizione potrebbe causare un problema in futuro:**



    | Context                             |  Utilizzo                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>      | Usare per tutti gli avvisi. <br/> ![Screenshot dell'avviso di modifica dell'estensione del nome file ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Avvisi sul posto<br/> | Usare per identificare il testo come avviso. <br/> ![Screenshot dell'avviso di spazio libero insufficiente ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notifiche<br/>     | Usare per tutti gli avvisi. (per [gli eventi di sistema non critici).](glossary.md) <br/> ![Screenshot della notifica di avviso di batteria in esaurimento ](images/vis-std-icons-image14.png)<br/> |
    | Palloncini<br/>          | Usare per [condizioni speciali](ctrl-balloons.md). <br/> ![Screenshot dell'avviso del fumetto relativo al blocco delle maiuscole ](images/vis-std-icons-image15.png)<br/>                           |
    | Banner<br/>           | Usare per attirare l'attenzione sul banner. <br/> ![Screenshot del banner con avviso di tpm mancante ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **Non usare le icone di avviso per "attenuare" gli errori non critici.** Gli errori non sono avvisi, ma applicano invece le linee guida relative all'icona di errore.
-   **Per le finestre di dialogo delle domande, usare le icone di avviso solo per le domande con conseguenze significative.** Non usare icone di avviso per le domande di routine.

**Corretto:**

![Avviso dello screenshot per non arrestare il ripristino del sistema ](images/vis-std-icons-image17.png)

**Non corretto:**

![Screenshot di avviso relativo alla chiusura dei promemoria ](images/vis-std-icons-image18.png)

Nell'esempio non corretto, un'icona di avviso viene usata in modo non corretto per una domanda di routine.

-   **Per le finestre di dialogo delle attività, è possibile usare un'icona a piè di pagina di avviso per avvisare gli utenti delle conseguenze rischiose.** Usare tuttavia un'icona di avviso nell'area del contenuto o nell'area delle note a piè di pagina, ma non entrambe.

![Screenshot di avviso di un file potenzialmente non sicuro ](images/vis-std-icons-image19.png)

In questo esempio viene usato uno schermo di sicurezza giallo in una nota a piè di pagina.

### <a name="information-icons"></a>Icone delle informazioni

-   **Usare le icone delle informazioni solo quando il contesto ovviamente non presenta informazioni:**



    | Context                         | Utilizzo                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Finestre di dialogo<br/>  | Non usare.<br/>                                                                                                                             |
    | Sul posto<br/>      | Non usare. In alternativa, usare testo statico normale o un banner.<br/>                                                                           |
    | Notifiche<br/> | Non usare.<br/>                                                                                                                             |
    | Palloncini<br/>      | Non usare.<br/>                                                                                                                             |
    | Banner<br/>       | usare per attirare l'attenzione sul banner. <br/> ![Screenshot del banner con informazioni sulle impostazioni ](images/vis-std-icons-image20.png)<br/> |



 

-   Le icone delle informazioni non sono necessarie nelle finestre di dialogo, nelle notifiche e nei fumetto perché il contesto comunica sufficientemente che forniscono informazioni agli utenti.
-   **Per le finestre di dialogo delle attività, non usare le icone delle note a piè di pagina delle informazioni.** Le note a piè di pagina sono sufficientemente visibili ed è chiaro che si tratta di informazioni.

### <a name="question-mark-icons"></a>Icone punto interrogativo

-   **Usare l'icona del punto interrogativo solo per i punti di ingresso della Guida.** Per altre informazioni, vedere le linee guida [per il punto di ingresso della](winenv-help.md) Guida.
-   **Non usare l'icona del punto interrogativo per porre domande.** Anche in questo caso, usare l'icona del punto interrogativo solo per i punti di ingresso della Guida. Non è necessario porre domande usando l'icona del punto interrogativo. È comunque sufficiente presentare un'istruzione principale come domanda.
-   **Non sostituire regolarmente le icone del punto interrogativo con le icone di avviso.** Sostituire un'icona punto interrogativo con un'icona di avviso solo se la domanda ha conseguenze significative. In caso contrario, non usare alcuna icona.

 

