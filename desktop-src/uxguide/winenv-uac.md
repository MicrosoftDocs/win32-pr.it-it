---
title: Controllo dell'account utente (nozioni di base sulla progettazione)
description: Un'esperienza di controllo dell'account utente ben progettata consente di impedire modifiche indesiderate a livello di sistema in modo prevedibile e richiede il minimo sforzo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b346e5cb581ac83ad2ebffabe73c5fbed636d814
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566383"
---
# <a name="user-account-control"></a>Controllo dell'account utente

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Un'esperienza di controllo dell'account utente ben progettata consente di impedire modifiche indesiderate a livello di sistema in modo prevedibile e richiede il minimo sforzo.

Con il controllo dell'account utente (UAC) completamente abilitato, gli amministratori interattivi normalmente vengono eseguiti con privilegi minimi, ma possono autoelevare per eseguire attività amministrative concedendo il consenso esplicito all'interfaccia utente del consenso. Tali attività amministrative includono l'installazione di software e driver, la modifica delle impostazioni a livello di sistema, la visualizzazione o la modifica di altri account utente e l'esecuzione di strumenti di amministrazione.

Nello stato con privilegi minimi, gli amministratori vengono definiti amministratori protetti. Nello stato con privilegi elevati vengono definiti amministratori con privilegi elevati. Al contrario, gli utenti standard non possono elevare autonomamente, ma possono chiedere a un amministratore di elevarle usando l'interfaccia utente delle credenziali. L'account amministratore predefinito non richiede l'elevazione dei privilegi.

![screenshot del messaggio di sicurezza ' Consenti programma ' ](images/winenv-uac-image1.png)

Interfaccia utente di consenso, utilizzata per elevare gli amministratori protetti con privilegi amministrativi.

![screenshot del messaggio che richiede la password ](images/winenv-uac-image2.png)

Interfaccia utente delle credenziali, utilizzata per elevare gli utenti standard.

Il controllo dell'account utente offre i vantaggi seguenti:

-   Riduce il numero di programmi eseguiti con privilegi elevati, consentendo pertanto di impedire agli utenti di modificare accidentalmente le impostazioni di sistema e di impedire che "malware" ottenga l'accesso a livello di sistema. Quando l'elevazione viene negata, il malware può influire solo sui dati dell'utente corrente. Senza elevazione, il malware non può apportare modifiche a livello di sistema o influire su altri utenti.
-   Per gli [ambienti gestiti](glossary.md), le esperienze di controllo dell'account utente ben progettate consentono agli utenti di essere più produttivi quando vengono eseguite come utenti standard rimuovendo restrizioni superflue.
-   Fornisce agli utenti standard la possibilità di chiedere agli amministratori di concedere loro l'autorizzazione per eseguire attività amministrative all'interno della sessione corrente.
-   Per gli ambienti domestici, consente un migliore controllo parentale sulle modifiche a livello di sistema, incluso il software installato.

**Sviluppatori:** Per informazioni sull'implementazione, vedere [riprogettare l'interfaccia utente per la compatibilità del controllo dell'account utente](/previous-versions/bb756990(v=msdn.10)).

In Windows Vista, gli amministratori protetti possono scegliere di ricevere notifiche relative a tutte le modifiche apportate al sistema o nessuna. L'impostazione predefinita del controllo dell'account utente prevede la notifica di tutte le modifiche, indipendentemente dall'origine. Quando si riceve una notifica, il desktop viene disattivato ed è necessario approvare o rifiutare la richiesta nella finestra di dialogo controllo dell'account utente prima di poter eseguire qualsiasi altra operazione nel computer. L'attenuazione del desktop viene definita [desktop protetto](glossary.md) perché non è possibile eseguire altri programmi mentre è in grigio.

Windows 7 introduce due impostazioni UAC intermedie per gli amministratori protetti, oltre alle due di Windows Vista. Il primo consiste nel notificare agli utenti solo quando un programma sta apportando la modifica, in modo che gli amministratori vengano automaticamente elevati quando apportano una modifica. Questa è l'impostazione predefinita del controllo dell'account utente in Windows 7 e usa anche il desktop sicuro.

La seconda impostazione intermedia in Windows 7 è identica alla prima, ad eccezione del fatto che non usa il desktop sicuro.

![Screenshot di quattro impostazioni di controllo dell'account utente in Windows 7 ](images/winenv-uac-image3.png)

Windows 7 introduce due impostazioni di controllo dell'account utente intermedie.

**Nota:** Le linee guida relative alla scrittura [di codice per supportare il controllo dell'account utente](/previous-versions/aa905330(v=msdn.10)) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Obiettivi**

Un'esperienza di controllo dell'account utente ben progettata ha gli obiettivi seguenti:

-   **Eliminare l'elevazione non necessaria.** Gli utenti devono essere in grado di elevare solo per eseguire attività che richiedono privilegi amministrativi. Tutte le altre attività devono essere progettate per eliminare la necessità di elevazione dei privilegi. Spesso il software legacy richiede privilegi di amministratore inutilmente scrivendo nelle sezioni del registro di sistema HKLM o HKCR o nei file di programma o nelle cartelle di sistema di Windows.
-   **Essere prevedibile.** Gli utenti standard devono stabilire quali attività richiedono che un amministratore esegua o non possa essere eseguita in ambienti gestiti. Gli amministratori devono essere a conoscenza delle attività che richiedono l'elevazione. Se non è possibile prevedere accuratamente la necessità di elevazione dei privilegi, è più probabile che forniscano il consenso per le attività amministrative.
-   **Richiede il minimo sforzo.** Le attività che richiedono privilegi amministrativi devono essere progettate in modo da richiedere un'elevazione singola. Le attività che richiedono più elevazioni diventano rapidamente noiose.
-   **Ripristinare i privilegi minimi.** Quando un'attività che richiede privilegi amministrativi è completa, il programma deve ripristinare lo stato dei privilegi minimi.

**Flusso attività di elevazione**

Quando un'attività richiede l'elevazione dei privilegi, prevede i passaggi seguenti:

1.  **Punto di ingresso.** Le attività che richiedono l'elevazione immediata quando UAC è completamente abilitata hanno punti di ingresso contrassegnati con lo scudo UAC. In questo caso, gli utenti dovrebbero aspettarsi di visualizzare un'interfaccia utente di elevazione dei privilegi immediatamente dopo aver fatto clic su tali comandi e dovrebbero essere molto cauti quando visualizzano l'interfaccia utente di elevazione delle attività che non hanno uno scudo.

    ![screenshot delle icone dello scudo del controllo dell'account utente e delle relative etichette ](images/winenv-uac-image4.png)

    In questo esempio gli elementi del pannello di controllo Parental Control e User Accounts richiedono l'elevazione.

    Quando il controllo dell'account utente è parzialmente abilitato o spento completamente, lo scudo del controllo dell'account utente viene comunque visualizzato per indicare che l'attività implica modifiche a livello di sistema e pertanto richiede l'elevazione dei privilegi, anche se l'utente potrebbe non visualizzare l'interfaccia utente di elevazione La visualizzazione sempre dello scudo UAC per le attività che richiedono l'elevazione dei privilegi mantiene l'interfaccia utente semplice e prevedibile.

2.  **Elevazione.** Per gli amministratori protetti, l'attività richiede il consenso usando l'interfaccia utente del consenso. Per gli utenti standard, l'attività richiede le credenziali di amministratore tramite l'interfaccia utente delle credenziali.

    ![Screenshot di due tipi di elevazione ](images/winenv-uac-image5.png)

    Questi esempi illustrano l'interfaccia utente delle credenziali e l'interfaccia utente di consenso.

3.  **Processo con privilegi elevati separato.** Internamente, viene creato un nuovo processo con privilegi elevati per eseguire l'attività.
4.  **Ripristinare il privilegio minimo.** Se necessario, ripristinare i privilegi minimi per completare tutti i passaggi che non richiedono l'elevazione dei privilegi.

Si noti che le attività non ricordano gli Stati con privilegi elevati. Se, ad esempio, l'utente si sposta avanti e indietro su un punto di ingresso di elevazione in una procedura guidata, l'utente deve elevare ogni volta.

## <a name="usage-patterns"></a>Modelli di utilizzo

Il controllo dell'account utente dispone di diversi modelli di utilizzo (in ordine di preferenza):

1.  **Lavorare per gli utenti standard.** Progettare la funzionalità per tutti gli utenti limitando l'ambito all'utente corrente. Limitando le impostazioni all'utente corrente (anziché a livello di sistema), si elimina la necessità di un'interfaccia utente di elevazione del tutto e si consente agli utenti di completare l'attività.

    **Non corretto:**

    ![screenshot del messaggio: non si dispone dei privilegi ](images/winenv-uac-image6.png)

    In questo esempio, gli utenti di Windows XP dovevano disporre dei privilegi amministrativi per visualizzare o modificare il fuso orario corrente.

    **Corretto:**

    ![screenshot della finestra di dialogo Data e ora ](images/winenv-uac-image7.png)

    In questo esempio, la funzionalità del fuso orario è stata riprogettata in Windows 7 e Windows Vista per funzionare per tutti gli utenti.

2.  **Disporre di elementi dell'interfaccia utente distinti per utenti e amministratori standard.** Separare chiaramente le attività utente standard dalle attività amministrative. Concedere a tutti gli utenti l'accesso a informazioni di sola lettura utili. Identificare chiaramente le attività amministrative con lo scudo UAC.

    ![rappresentazione grafica dello scudo UAC con elevazione obbligatoria ](images/winenv-uac-image8.png)

    In questo esempio, l'elemento del pannello di controllo del sistema Mostra il proprio stato a tutti gli utenti, ma la modifica delle impostazioni a livello di sistema richiede l'elevazione dei privilegi.

3.  **Consente agli utenti standard di provare l'attività e di elevare in caso di errore.** Se gli utenti standard possono visualizzare le informazioni e sono in grado di apportare alcune modifiche senza elevazione dei privilegi, consentono loro di accedere all'interfaccia utente e di elevarle solo se l'attività ha esito negativo. Questo approccio è adatto quando gli utenti standard hanno accesso limitato, ad esempio con le proprietà dei propri file in Esplora risorse. È adatto anche per le impostazioni nel pannello di controllo pagine dell'Hub ibrido.

    ![screenshot dell'accesso negato messaggio ](images/winenv-uac-image9.png)

    In questo esempio, l'utente ha tentato di modificare le proprietà del file di programma ma non ha privilegi sufficienti. L'utente può elevare e riprovare.

4.  **Lavorare solo per gli amministratori.** Utilizzare questo approccio solo per le funzionalità e i programmi di amministratore. Se una funzionalità è destinata solo agli amministratori (e non dispone di percorsi di navigazione o di informazioni di sola lettura utili per gli utenti standard), è possibile richiedere le credenziali di amministratore nel punto di ingresso prima di visualizzare qualsiasi interfaccia utente. Utilizzare questo approccio per le procedure guidate lunghe e i [flussi di pagina](glossary.md) quando tutti i percorsi richiedono privilegi amministrativi.

    Se l'intero programma è solo per gli amministratori, contrassegnarlo per richiedere le credenziali di amministratore per poter essere avviato. Windows visualizza tali icone di programma con la sovrimpressione dello scudo del controllo dell'account utente.

    ![screenshot del logo di Windows e della sovrimpressione dello scudo del controllo dell'account utente ](images/winenv-uac-image10.png)

    In questo esempio, il programma richiede privilegi amministrativi per l'avvio.

## <a name="guidelines"></a>Indicazioni

### <a name="uac-shield-icon"></a>Icona dello scudo UAC

-   **Visualizzare i controlli con lo scudo UAC per indicare che l'attività richiede un'elevazione immediata quando UAC è completamente abilitata,** anche se UAC non è attualmente completamente abilitata. Se per tutti i percorsi di una procedura guidata e di un [flusso di pagina](glossary.md) è richiesta l'elevazione dei privilegi, visualizzare lo scudo UAC al punto di ingresso dell'attività L'uso appropriato dello scudo UAC consente agli utenti di prevedere quando è richiesta l'elevazione dei privilegi.
-   **Se il programma supporta più versioni di Windows, visualizzare lo scudo UAC se almeno una versione richiede l'elevazione dei privilegi.** Poiché Windows XP non richiede mai l'elevazione dei privilegi, provare a rimuovere gli schermi UAC per Windows XP, se è possibile eseguire questa operazione in modo coerente e senza danneggiare le prestazioni.
-   **Non visualizzare lo scudo UAC per le attività che non richiedono l'elevazione dei privilegi nella maggior parte dei contesti.** Poiché questo approccio è talvolta fuorviante, l'approccio migliore consiste nell'usare invece un comando contestuale correttamente schermato.

    ![screenshot dei file di foto in Esplora risorse ](images/winenv-uac-image11.png)

    Poiché il comando nuova cartella richiede l'elevazione dei privilegi solo quando viene usato nelle cartelle di sistema, viene visualizzato senza uno scudo del controllo dell'account utente.

-   È possibile visualizzare lo scudo UAC sui seguenti controlli:

    **Pulsanti di comando:**

    ![screenshot del pulsante di comando con icona dello scudo UAC ](images/winenv-uac-image12.png)

    Pulsante di comando che richiede l'elevazione immediata.

    **Collegamenti comando:**

    ![screenshot del collegamento del comando con l'icona dello scudo UAC ](images/winenv-uac-image13.png)

    Collegamento di comando che richiede l'elevazione immediata.

    **Collegamenti**

    ![screenshot del collegamento dell'account di modifica con controllo dell'account utente ](images/winenv-uac-image14.png)

    Collegamento che richiede l'elevazione immediata.

    **Menu**

    ![screenshot del menu con scudo UAC ](images/winenv-uac-image15.png)

    Menu A discesa che richiede l'elevazione immediata.

-   Poiché le attività non ricordano gli Stati con privilegi elevati, **non modificare la scherma dell'UAC per riflettere lo stato.**
-   **Visualizzare lo scudo UAC anche se il controllo dell'account utente è stato disattivato o se l'utente utilizza l'account predefinito Administrator.** La visualizzazione coerente dello scudo UAC è più semplice da programmare e fornisce agli utenti informazioni sulla natura dell'attività.

### <a name="elevation"></a>Altitudine

-   **Quando possibile, le attività di progettazione devono essere eseguite dagli utenti standard senza elevazione dei privilegi.** Concedere a tutti gli utenti l'accesso a informazioni di sola lettura utili.
-   **Elevare per ogni singola attività, non per ogni impostazione.** Non combinare le impostazioni utente standard con impostazioni amministrative in una singola pagina o finestra di dialogo. Se, ad esempio, gli utenti standard possono modificare alcune impostazioni ma non tutte, suddividerle come superficie dell'interfaccia utente separata.

    **Non corretto:**

    ![screenshot della finestra di dialogo Impostazioni data e ora ](images/winenv-uac-image16.png)

    In questo esempio le impostazioni utente standard non vengono combinate correttamente con le impostazioni amministrative.

    **Corretto:**

    ![screenshot della stessa finestra di dialogo senza schermate UAC ](images/winenv-uac-image17.png)

    In questo esempio le impostazioni per modificare la data e l'ora si trovano in una finestra di dialogo separata, disponibile solo per gli amministratori. Le impostazioni del fuso orario sono disponibili per gli utenti standard e non sono combinate con le impostazioni amministrative.

-   **Non considerare la necessità di elevare quando si determina se un controllo deve essere visualizzato o disabilitato.** Motivo:
    -   Negli ambienti non gestiti, si supponga che gli utenti standard potessero elevare chiedendo a un amministratore. La disabilitazione dei controlli che richiedono l'elevazione dei privilegi impedirebbe agli utenti di elevare gli amministratori.
    -   Negli ambienti gestiti, si supponga che gli utenti standard non possano elevare. La rimozione di controlli che richiedono l'elevazione dei privilegi impedirebbe agli utenti di sapere quando smettere di cercare.
-   **Per eliminare l'elevazione non necessaria:**
    -   **Se un'attività potrebbe richiedere l'elevazione dei privilegi, elevare il più tardi possibile.** Se un'attività richiede una [conferma](mess-confirm.md), visualizzare l'interfaccia utente di elevazione dei privilegi solo dopo che l'utente ha confermato. Se un'attività richiede sempre l'elevazione dei privilegi, elevare al punto di ingresso.
    -   **Una volta elevato, rimane elevato fino a quando non sono più necessari privilegi elevati.** Per eseguire una singola attività, gli utenti non dovrebbero dover elevare più volte.
    -   **Se gli utenti devono elevare per apportare una modifica ma scelgono di non apportare alcuna modifica, lasciare i pulsanti di commit positivi abilitati, ma gestire il commit come annullamento.** Questa operazione Elimina gli utenti che devono elevare solo la chiusura di una finestra.
    -   **Non corretto:**
    -   ![screenshot della finestra con un solo pulsante attivo ](images/winenv-uac-image18.png)
    -   In questo esempio il pulsante Salva modifiche è disabilitato per evitare un'elevazione superflua, ma viene abilitato quando gli utenti modificano la selezione. Tuttavia, il pulsante di commit disabilitato lo rende simile agli utenti che non hanno una scelta.
-   **Non visualizzare un messaggio di errore quando le attività hanno esito negativo perché gli utenti hanno scelto di non elevare.** Si supponga che gli utenti abbiano intenzionalmente scelto di non procedere, quindi non considereranno questa situazione come un errore.

    **Non corretto:**

    ![screenshot del messaggio: Impossibile eseguire il ripristino Fabrikam ](images/winenv-uac-image19.png)

    In questo esempio, Fabrikam Restore restituisce erroneamente un messaggio di errore quando l'utente decide di non elevare.

-   **Non visualizzare avvisi per spiegare che gli utenti potrebbero dover elevare i propri privilegi per l'esecuzione di attività.** Consentire agli utenti di individuare questo fatto in modo autonomo.
-   **Visualizzare l'interfaccia utente di schermatura e di elevazione del controllo dell'account utente basata sulla tabella seguente:**

    |                       |                                                                                                                                                                  |                                                                                                                                                                                                                       |                                                                                                      |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Object**      | **Circostanza**                                                                                                                                                | **Posizione in cui inserire lo scudo UAC**                                                                                                                                                                               | **Quando elevare**                                                                            |
    | Programma<br/>    | L'intero programma è solo per gli amministratori.<br/>                                                                                                            | ![screenshot del logo di Windows e della sovrimpressione dello scudo del controllo dell'account utente ](images/winenv-uac-image10.png)<br/> Sovrapposizione schermate UAC sull'icona del programma.<br/>                                                                       | Visualizza l'interfaccia utente di elevazione all'avvio.<br/>                                                           |
    | Comando<br/>    | L'intero comando è solo per gli amministratori.<br/>                                                                                                            | ![screenshot del collegamento dell'account di modifica e dello scudo UAC ](images/winenv-uac-image14.png)<br/> Schermata UAC sul pulsante di comando o sul collegamento.<br/>                                                                      | Visualizza l'interfaccia utente di elevazione quando si fa clic sul pulsante di comando o sul collegamento, ma dopo le conferme.<br/> |
    | Comando<br/>    | Il comando Visualizza informazioni utili di sola lettura appropriate per tutti gli utenti, ma le modifiche richiedono privilegi amministrativi.<br/>                               | ![screenshot del collegamento alle impostazioni di modifica e dello scudo UAC ](images/winenv-uac-image8.png)<br/> Schermate UAC sul pulsante di comando o sul collegamento per apportare modifiche.<br/>                                                      | Visualizza l'interfaccia utente di elevazione quando si fa clic sul pulsante di comando, ma dopo le conferme.<br/>         |
    | Comando<br/>    | Gli utenti standard possono visualizzare le informazioni ed eventualmente apportare alcune modifiche senza elevazione dei privilegi. consente agli utenti standard di provare e di elevare in caso di errore.<br/> | ![screenshot dell'errore con l'icona UAC sul pulsante Riprova ](images/winenv-uac-image9.png)<br/> Non visualizzare lo scudo del controllo dell'account utente per il comando, ma visualizzarlo per il punto di ingresso dell'elevazione se il comando ha esito negativo.<br/> | Visualizza l'interfaccia utente di elevazione quando l'utente ripete il comando.<br/>                                       |
    | Passaggio attività<br/>  | Per tutti i passaggi successivi è richiesta l'elevazione.<br/>                                                                                                               | ![screenshot del pulsante di comando successivo con lo scudo UAC ](images/winenv-uac-image20.png)<br/> Scherma UAC sul pulsante Avanti (o equivalente).<br/>                                                                | Visualizza l'interfaccia utente di elevazione quando si fa clic su Avanti o su altro pulsante di commit.<br/>                         |
    | Passaggio attività<br/>  | Per alcuni rami è richiesta l'elevazione.<br/>                                                                                                                      | ![screenshot del collegamento del comando con controllo dell'account utente ](images/winenv-uac-image21.png)<br/> Controllo UAC sui collegamenti ai comandi che richiedono l'elevazione dei privilegi.<br/>                                                              | Visualizza l'interfaccia utente di elevazione quando si fa clic sui collegamenti ai comandi con controllo dell'account utente.<br/>                      |

    

     

### <a name="elevation-ui"></a>Interfaccia utente di elevazione

-   **Se l'utente fornisce un account che non è valido (nome o password) o non dispone dei privilegi di amministratore, è sufficiente visualizzare nuovamente l'interfaccia utente delle credenziali.** Non visualizzare un messaggio di errore.
-   **Se l'utente annulla l'interfaccia utente delle credenziali, riportare l'utente all'interfaccia utente originale.** Non visualizzare un messaggio di errore.
-   Se il controllo dell'account utente è stato disattivato e un utente standard tenta di eseguire un'attività che richiede l'elevazione dei privilegi, fornire un messaggio di errore che indica che l'attività richiede privilegi di amministratore. Per eseguire questa attività, è necessario accedere con un account amministratore. "

![screenshot dell'attività che richiede il messaggio dei privilegi ](images/winenv-uac-image22.png)

In questo esempio, il controllo dell'account utente è stato disattivato, quindi un messaggio di errore indica che l'utente deve utilizzare un account amministratore.

### <a name="wizards"></a>Procedure guidate

-   **Non elevare più volte.** Una volta elevata, una procedura guidata deve rimanere elevata.
-   Se l'attività viene eseguita all'interno della procedura guidata, inserire una schermata del controllo dell'account utente nel pulsante "Avanti" della pagina di commit (a cui deve essere assegnata un' [etichetta più specifica](win-wizards.md)). Quando l'utente esegue il commit:
    -   Se la pagina successiva è una pagina di stato, passare alla pagina e visualizzare in modo modale l'interfaccia utente di elevazione. Al termine dell'elevazione, eseguire l'attività.
    -   Se la pagina successiva è una pagina di completamento, passare alla pagina (ma sostituirla temporaneamente con "Waiting for...") e visualizzare in modo modale l'interfaccia utente di elevazione. Al termine dell'elevazione, eseguire l'attività, quindi visualizzare il contenuto della pagina di completamento.
    -   Se l'utente annulla l'interfaccia utente di elevazione dei privilegi, tornare alla pagina commit. Questa operazione consente all'utente di riprovare.
-   Se l'attività viene eseguita al termine della procedura guidata, inserire uno scudo del controllo dell'account utente nel pulsante "fine" della pagina di commit (a cui deve essere assegnata un' [etichetta più specifica](win-wizards.md)). Quando l'utente esegue il commit:
    -   Rimanere nella pagina commit e visualizzare in modalità modale l'interfaccia utente di elevazione dei privilegi. Una volta completata l'elevazione dei privilegi, chiudere la procedura guidata.
    -   Se l'utente annulla l'interfaccia utente di elevazione dei privilegi, tornare alla pagina commit. Questa operazione consente all'utente di riprovare.
-   Per le procedure guidate lunghe previste solo per gli amministratori, è possibile richiedere le credenziali di amministratore nel punto di ingresso prima di visualizzare qualsiasi interfaccia utente.

## <a name="text"></a>Testo

-   **Non usare i puntini di sospensione solo perché un comando richiede l'elevazione dei privilegi.** La necessità di elevare è indicata con lo scudo del controllo dell'account utente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento al controllo dell'account utente:

-   Vedere la funzionalità come controllo dell'account utente (alla prima menzione) o UAC (nella menzione successiva), account utente con privilegi minimi o LUA.
-   Vedere utenti non amministratori come utenti standard.
-   Fare riferimento agli amministratori di computer predefiniti come amministratori predefiniti.

Nella documentazione dell'utente:

-   Fare riferimento all'azione di concessione del consenso per eseguire un'attività amministrativa come concessione dell'autorizzazione.

In programmazione e altri documenti tecnici:

-   Fare riferimento all'azione di concessione del consenso per eseguire un'attività amministrativa come elevazione dei privilegi.
-   Nel contesto di controllo dell'account utente, fare riferimento agli amministratori come amministratori protetti quando non sono elevati e amministratori con privilegi elevati dopo l'elevazione.
-   Fare riferimento alla finestra di dialogo utilizzata per immettere le password come interfaccia utente delle credenziali. Fare riferimento alla finestra di dialogo usata per concedere il consenso come interfaccia utente del consenso. Fare riferimento a entrambi in genere come interfaccia utente di elevazione.

