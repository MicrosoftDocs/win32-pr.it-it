---
title: Controllo dell'account utente (nozioni di base sulla progettazione)
description: Un'esperienza di controllo dell'account utente ben progettata consente di evitare modifiche indesiderate a livello di sistema in modo prevedibile e richiede un impegno minimo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0330ee3ffbf608296bcb89abe3e02ef6969500356d0cca4f45db9d24d8ff73f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935948"
---
# <a name="user-account-control"></a>Controllo dell'account utente

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un'esperienza di controllo dell'account utente ben progettata consente di evitare modifiche indesiderate a livello di sistema in modo prevedibile e richiede un impegno minimo.

Con il controllo dell'account utente completamente abilitato, gli amministratori interattivi vengono in genere eseguiti con privilegi minimi, ma possono elevare autonomamente i privilegi per eseguire attività amministrative fornendo il consenso esplicito con l'interfaccia utente di consenso. Tali attività amministrative includono l'installazione di software e driver, la modifica delle impostazioni a livello di sistema, la visualizzazione o la modifica di altri account utente e l'esecuzione di strumenti di amministrazione.

Nel loro stato con privilegi minimi, gli amministratori sono definiti amministratori protetti. Nello stato con privilegi elevati, vengono definiti amministratori con privilegi elevati. Al contrario, gli utenti Standard non possono elevare i privilegi da soli, ma possono chiedere a un amministratore di elevarli usando l'interfaccia utente delle credenziali. L'account Predefinito Administrator non richiede l'elevazione dei privilegi.

![Screenshot del messaggio di sicurezza "Consenti programma" ](images/winenv-uac-image1.png)

L'interfaccia utente di consenso, usata per elevare gli amministratori protetti in modo che abbia privilegi amministrativi.

![Screenshot del messaggio che richiede la password ](images/winenv-uac-image2.png)

L'interfaccia utente delle credenziali, usata per elevare i privilegi degli utenti standard.

Controllo dell'account utente offre i vantaggi seguenti:

-   Riduce il numero di programmi eseguiti con privilegi elevati, consentendo di impedire agli utenti di modificare accidentalmente le impostazioni di sistema e di impedire al "malware" di ottenere l'accesso a livello di sistema. Quando l'elevazione dei privilegi viene negata, il malware può influire solo sui dati dell'utente corrente. Senza elevazione dei privilegi, il malware non può apportare modifiche a livello di sistema o influire su altri utenti.
-   Per [gli ambienti gestiti,](glossary.md)le esperienze di controllo dell'account utente ben progettate consentono agli utenti di essere più produttivi quando vengono eseguiti come utenti Standard rimuovendo le restrizioni non necessarie.
-   Offre agli utenti Standard la possibilità di chiedere agli amministratori di concedere loro l'autorizzazione per eseguire attività amministrative all'interno della sessione corrente.
-   Per gli ambienti domestici, consente un migliore controllo dei genitori sulle modifiche a livello di sistema, incluso il software installato.

**Sviluppatori:** Per informazioni sull'implementazione, vedere [Riprogettare l'interfaccia utente per la compatibilità con controllo dell'account utente.](/previous-versions/bb756990(v=msdn.10))

In Windows Vista, gli amministratori protetti possono scegliere di ricevere una notifica su tutte le modifiche del sistema o nessuna. L'impostazione predefinita di Controllo dell'account utente consente di notificare tutte le modifiche, indipendentemente dall'origine. Quando si riceve una notifica, il desktop verrà visualizzato in grigio ed è necessario approvare o rifiutare la richiesta nella finestra di dialogo Controllo dell'account utente prima di poter eseguire qualsiasi altra operazione nel computer. L'attenuazione del desktop viene definita [desktop](glossary.md) sicuro perché altri programmi non possono essere eseguiti mentre è in grigio.

Windows 7 introduce due impostazioni intermedie di Controllo dell'account utente per gli amministratori protetti, oltre alle due di Windows Vista. Il primo è notificare agli utenti solo quando un programma sta apportando la modifica, in modo che gli amministratori siano automaticamente elevati quando apportano una modifica. Questa è l'impostazione predefinita di Controllo dell'account utente Windows 7 e usa anche il desktop sicuro.

La seconda impostazione intermedia Windows 7 è la stessa della prima, ad eccezione del fatto che non usa il desktop sicuro.

![Screenshot di quattro impostazioni di controllo dell'account utente in Windows 7 ](images/winenv-uac-image3.png)

Windows 7 introduce due impostazioni intermedie di Controllo dell'account utente.

**Nota:** Le linee guida relative alla [scrittura di codice per supportare il controllo dell'account utente](/previous-versions/aa905330(v=msdn.10)) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Obiettivi**

Un'esperienza di controllo dell'account utente ben progettata ha gli obiettivi seguenti:

-   **Eliminare l'elevazione dei privilegi non necessaria.** Gli utenti devono elevare i privilegi solo per eseguire attività che richiedono privilegi amministrativi. Tutte le altre attività devono essere progettate per eliminare la necessità di elevazione dei privilegi. Spesso il software legacy richiede privilegi di amministratore inutilmente scrivendo nelle sezioni del Registro di sistema HKLM o HKCR o nelle cartelle Programmi Windows sistema.
-   **Essere prevedibili.** Gli utenti standard devono sapere quali attività devono essere eseguite da un amministratore o non possono essere eseguite in ambienti gestiti. Gli amministratori devono sapere quali attività richiedono l'elevazione dei privilegi. Se non possono prevedere con precisione la necessità di elevazione dei privilegi, è più probabile che consenzino le attività amministrative quando non dovrebbero.
-   **Richiedere il minimo sforzo.** Le attività che richiedono privilegi amministrativi devono essere progettate per richiedere una singola elevazione dei privilegi. Le attività che richiedono più elevazioni diventano rapidamente noiose.
-   **Ripristinare i privilegi minimi.** Al termine di un'attività che richiede privilegi amministrativi, il programma deve ripristinare lo stato con privilegi minimi.

**Flusso di attività di elevazione dei privilegi**

Quando un'attività richiede l'elevazione dei privilegi, è necessario eseguire i passaggi seguenti:

1.  **Punto di ingresso.** Le attività che richiedono l'elevazione dei privilegi immediata quando controllo dell'account utente è completamente abilitato hanno punti di ingresso contrassegnati con lo shield di Controllo dell'account utente. In questo caso, gli utenti devono aspettarsi di visualizzare un'interfaccia utente di elevazione dei privilegi immediatamente dopo aver fatto clic su tali comandi e devono essere molto cauti quando vedono l'interfaccia utente di elevazione dei privilegi da attività che non hanno uno schermo.

    ![Screenshot delle icone degli schermi di controllo dell'account utente e delle relative etichette ](images/winenv-uac-image4.png)

    In questo esempio, gli elementi del Pannello di controllo controllo degli account utente e controllo genitori richiedono l'elevazione dei privilegi.

    Quando controllo dell'account utente è parzialmente abilitato o disattivato completamente, viene comunque visualizzato lo shield di Controllo dell'account utente per indicare che l'attività comporta modifiche a livello di sistema e pertanto richiede l'elevazione dei privilegi, anche se l'utente potrebbe non visualizzare l'interfaccia utente di elevazione dei privilegi. La visualizzazione sempre dello shield di Controllo dell'account utente per le attività che richiedono l'elevazione dei privilegi mantiene l'interfaccia utente semplice e prevedibile.

2.  **Elevazione.** Per gli amministratori protetti, l'attività richiede il consenso usando l'interfaccia utente di consenso. Per gli utenti standard, l'attività richiede le credenziali di amministratore usando l'interfaccia utente delle credenziali.

    ![Screenshot di due tipi di elevazione dei privilegi ](images/winenv-uac-image5.png)

    Questi esempi illustrano l'interfaccia utente delle credenziali e l'interfaccia utente di consenso.

3.  **Separare il processo con privilegi elevati.** Internamente, viene creato un nuovo processo con privilegi elevati per eseguire l'attività.
4.  **Ripristinare i privilegi minimi.** Se necessario, ripristinare i privilegi minimi per completare i passaggi che non richiedono l'elevazione dei privilegi.

Si noti che le attività non "ricordano" gli stati elevati. Ad esempio, se l'utente si sposta avanti e indietro su un punto di ingresso di elevazione dei privilegi in una procedura guidata, l'utente deve elevare i privilegi ogni volta.

## <a name="usage-patterns"></a>Modelli di utilizzo

Controllo dell'account utente ha diversi modelli di utilizzo (in ordine di preferenza):

1.  **Lavorare per gli utenti Standard.** Progettare la funzionalità per tutti gli utenti limitando l'ambito all'utente corrente. Limitando le impostazioni all'utente corrente (anziché a livello di sistema), si elimina completamente la necessità di un'interfaccia utente di elevazione dei privilegi e si consente agli utenti di completare l'attività.

    **Non corretto:**

    ![Screenshot del messaggio: Non si dispone dei privilegi ](images/winenv-uac-image6.png)

    In questo esempio gli Windows XP dovevano avere privilegi amministrativi per visualizzare o modificare il fuso orario corrente.

    **Corretto:**

    ![Screenshot della finestra di dialogo di data e ora ](images/winenv-uac-image7.png)

    In questo esempio la funzionalità di fuso orario è stata riprogettata in Windows 7 e Windows Vista per tutti gli utenti.

2.  **Disporre di elementi dell'interfaccia utente separati per utenti e amministratori Standard.** Separare chiaramente le attività dell'utente Standard dalle attività amministrative. Concedere a tutti gli utenti l'accesso a informazioni utili di sola lettura. Identificare chiaramente le attività amministrative con lo shield di Controllo dell'account utente.

    ![immagine dello shield di controllo dell'account utente che mostra l'elevazione necessaria ](images/winenv-uac-image8.png)

    In questo esempio l'elemento del Pannello di controllo Sistema mostra il proprio stato a tutti gli utenti, ma la modifica delle impostazioni a livello di sistema richiede l'elevazione dei privilegi.

3.  **Consentire agli utenti standard di tentare l'attività e di elevare i privilegi in caso di errore.** Se gli utenti standard possono visualizzare le informazioni e sono in grado di apportare alcune modifiche senza elevazione dei privilegi, consentire loro di accedere all'interfaccia utente e di elevarli solo se l'attività ha esito negativo. Questo approccio è adatto quando gli utenti Standard hanno accesso limitato, ad esempio con le proprietà dei propri file in Windows Explorer. È adatto anche per le impostazioni nelle Pannello di controllo dell'hub ibrido.

    ![Screenshot del messaggio di accesso negato ](images/winenv-uac-image9.png)

    In questo esempio l'utente ha tentato di modificare le proprietà del file di programma, ma non ha avuto privilegi sufficienti. L'utente può elevare i privilegi e riprovare.

4.  **Lavorare solo per gli amministratori.** Usare questo approccio solo per le funzionalità e i programmi dell'amministratore. Se una funzionalità è destinata solo agli amministratori (e non ha percorsi di navigazione o informazioni utili di sola lettura per gli utenti standard), è possibile richiedere le credenziali di amministratore nel punto di ingresso prima di visualizzare qualsiasi interfaccia utente. Usare questo approccio per procedure guidate e flussi di [pagina](glossary.md) lunghi quando tutti i percorsi richiedono privilegi amministrativi.

    Se l'intero programma è solo per gli amministratori, contrassegnarlo per richiedere le credenziali di amministratore per l'avvio. Windows le icone del programma con la sovrapposizione dello shield di Controllo dell'account utente.

    ![Screenshot del logo di Windows e della sovrimpressione uac shield ](images/winenv-uac-image10.png)

    In questo esempio il programma richiede privilegi amministrativi per l'avvio.

## <a name="guidelines"></a>Indicazioni

### <a name="uac-shield-icon"></a>Icona di schermatura di Controllo dell'account utente

-   **Visualizzare i controlli con lo shield di Controllo dell'account** utente per indicare che l'attività richiede l'elevazione dei privilegi immediata quando controllo dell'account utente è completamente abilitato, anche se controllo dell'account utente non è attualmente completamente abilitato. Se tutti i percorsi di una procedura guidata e di un [flusso di pagina](glossary.md) richiedono l'elevazione dei privilegi, visualizzare lo shield di Controllo dell'account utente nel punto di ingresso dell'attività. L'uso corretto dello shield di Controllo dell'account utente consente agli utenti di prevedere quando è necessaria l'elevazione dei privilegi.
-   **Se il programma supporta più versioni di Windows, visualizzare lo shield di Controllo dell'account utente se almeno una versione richiede l'elevazione dei privilegi.** Poiché Windows XP non richiede mai l'elevazione dei privilegi, provare a rimuovere gli schermi di Controllo dell'account utente per Windows XP se è possibile eseguire questa operazione in modo coerente e senza danneggiare le prestazioni.
-   **Non visualizzare lo shield di Controllo dell'account utente per le attività che non richiedono l'elevazione dei privilegi nella maggior parte dei contesti.** Poiché questo approccio a volte è fuorviante, l'approccio preferito consiste nell'usare un comando contestuale correttamente schermato.

    ![Screenshot dei file di foto in Esplora risorse ](images/winenv-uac-image11.png)

    Poiché il comando Nuova cartella richiede l'elevazione dei privilegi solo se usato nelle cartelle di sistema, viene visualizzato senza uno shield di Controllo dell'account utente.

-   Lo shield di Controllo dell'account utente può essere visualizzato nei controlli seguenti:

    **Pulsanti di comando:**

    ![Screenshot del pulsante di comando con l'icona uac shield ](images/winenv-uac-image12.png)

    Pulsante di comando che richiede l'elevazione dei privilegi immediata.

    **Collegamenti di comando:**

    ![Screenshot del collegamento di comando con l'icona uac shield ](images/winenv-uac-image13.png)

    Collegamento di comando che richiede l'elevazione dei privilegi immediata.

    **Link:**

    ![Screenshot del collegamento cambia account con uac shield ](images/winenv-uac-image14.png)

    Collegamento che richiede l'elevazione immediata dei privilegi.

    **Menu:**

    ![Screenshot del menu con uac shield ](images/winenv-uac-image15.png)

    Menu a discesa che richiede l'elevazione dei privilegi immediata.

-   Poiché le attività non ricordano gli stati con privilegi elevati, non modificare lo shield di Controllo **dell'account utente per riflettere lo stato.**
-   **Visualizzare lo shield di Controllo dell'account utente anche se Controllo dell'account utente è stato disattivato o se l'utente usa l'account amministratore predefinito.** La visualizzazione coerente dello shield di Controllo dell'account utente è più facile da programmare e fornisce agli utenti informazioni sulla natura dell'attività.

### <a name="elevation"></a>Altitudine

-   **Quando possibile, progettare attività che devono essere eseguite dagli utenti Standard senza elevazione dei privilegi.** Concedere a tutti gli utenti l'accesso a informazioni utili di sola lettura.
-   **Elevare i privilegi in base alle attività, non in base all'impostazione.** Non combinare le impostazioni utente standard con le impostazioni amministrative in una singola pagina o finestra di dialogo. Ad esempio, se gli utenti Standard possono modificare alcune ma non tutte le impostazioni, suddividere tali impostazioni in una superficie dell'interfaccia utente separata.

    **Non corretto:**

    ![Screenshot della finestra di dialogo delle impostazioni di data e ora ](images/winenv-uac-image16.png)

    In questo esempio le impostazioni utente standard vengono erroneamente miste alle impostazioni amministrative.

    **Corretto:**

    ![Screenshot della stessa finestra di dialogo senza schermate uac ](images/winenv-uac-image17.png)

    In questo esempio le impostazioni per la modifica di data e ora si trova in una finestra di dialogo separata, disponibile solo per gli amministratori. Le impostazioni del fuso orario sono disponibili per gli utenti standard e non sono miste alle impostazioni amministrative.

-   **Non considerare la necessità di elevare i privilegi quando si determina se un controllo deve essere visualizzato o disabilitato.** Motivo:
    -   Negli ambienti non gestiti, si supponga che gli utenti Standard potrebbero elevare i privilegi chiedendo a un amministratore. La disabilitazione dei controlli che richiedono l'elevazione dei privilegi impedirebbe agli utenti di elevare i privilegi degli amministratori.
    -   Negli ambienti gestiti presupporre che gli utenti Standard non possano elevare i privilegi. La rimozione dei controlli che richiedono l'elevazione dei privilegi impedirebbe agli utenti di sapere quando interrompere la ricerca.
-   **Per eliminare l'elevazione dei privilegi non necessaria:**
    -   **Se un'attività potrebbe richiedere l'elevazione dei privilegi, elevare i privilegi il più tardi possibile.** Se un'attività richiede una [conferma,](mess-confirm.md)visualizzare l'interfaccia utente di elevazione dei privilegi solo dopo che l'utente ha confermato. Se un'attività richiede sempre l'elevazione dei privilegi, elevare i privilegi al punto di ingresso.
    -   **Dopo l'elevazione dei privilegi, rimanere elevati fino a quando i privilegi elevati non sono più necessari.** Gli utenti non devono elevare più volte i privilegi per eseguire una singola attività.
    -   **Se gli utenti devono elevare i privilegi per apportare una modifica ma scegliere di non apportare alcuna modifica, lasciare abilitati i pulsanti di commit positivi, ma gestire il commit come annullamento.** In questo modo gli utenti non devono elevare i privilegi solo per chiudere una finestra.
    -   **Non corretto:**
    -   ![Screenshot della finestra con un solo pulsante attivo ](images/winenv-uac-image18.png)
    -   In questo esempio il pulsante Salva modifiche è disabilitato per evitare un'elevazione dei privilegi non necessaria, ma viene abilitato quando gli utenti modificano la selezione. Tuttavia, il pulsante commit disabilitato fa sembrare che gli utenti non hanno una scelta.
-   **Non visualizzare un messaggio di errore quando le attività hanno esito negativo perché gli utenti hanno scelto di non elevare i privilegi.** Si supponga che gli utenti scelsino intenzionalmente di non procedere, in modo che non considerino questa situazione come un errore.

    **Non corretto:**

    ![Screenshot del messaggio: Fabrikam restore can't run (Impossibile eseguire il ripristino di fabrikam) ](images/winenv-uac-image19.png)

    In questo esempio, Fabrikam Restore restituisce erroneamente un messaggio di errore quando l'utente decide di non elevare i privilegi.

-   **Non visualizzare avvisi per spiegare che gli utenti potrebbero dover elevare i propri privilegi per eseguire attività.** Consentire agli utenti di scoprire questo fatto in modo proprio.
-   **Visualizzare l'interfaccia utente di schermatura ed elevazione dei privilegi di Controllo dell'account utente in base alla tabella seguente:**

    | Oggetto | Circostanza | Dove inserire lo shield di Controllo dell'account utente | Quando elevare i privilegi |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | Programma<br/>    | L'intero programma è solo per gli amministratori.<br/>                                                                                                            | ![Screenshot del logo di Windows e della sovrimpressione uac shield ](images/winenv-uac-image10.png)<br/> Sovrapposizione dello shield di Controllo dell'account utente sull'icona del programma.<br/>                                                                       | Visualizzare l'interfaccia utente di elevazione dei privilegi all'avvio.<br/>                                                           |
    | Comando<br/>    | L'intero comando è solo per gli amministratori.<br/>                                                                                                            | ![Screenshot del collegamento per la modifica dell'account e dello shield di controllo dell'account utente ](images/winenv-uac-image14.png)<br/> Schermatura di Controllo dell'account utente sul pulsante di comando o sul collegamento.<br/>                                                                      | Visualizza l'interfaccia utente di elevazione dei privilegi quando si fa clic sul pulsante di comando o sul collegamento, ma dopo eventuali conferme.<br/> |
    | Comando<br/>    | Il comando visualizza informazioni utili di sola lettura appropriate per tutti gli utenti, ma le modifiche richiedono privilegi amministrativi.<br/>                               | ![Screenshot del collegamento di modifica delle impostazioni e dello shield di controllo dell'account utente ](images/winenv-uac-image8.png)<br/> Schermatura di Controllo dell'account utente sul pulsante di comando o sul collegamento per apportare modifiche.<br/>                                                      | Visualizza l'interfaccia utente di elevazione dei privilegi quando si fa clic sul pulsante di comando, ma dopo eventuali conferme.<br/>         |
    | Comando<br/>    | Gli utenti standard possono visualizzare le informazioni ed eventualmente apportare alcune modifiche senza elevazione dei privilegi. consentire agli utenti standard di tentare e di elevare i privilegi in caso di errore.<br/> | ![Screenshot dell'errore con l'icona di controllo dell'account utente sul pulsante riprova ](images/winenv-uac-image9.png)<br/> Non visualizzare lo shield di Controllo dell'account utente per il comando, ma mostrarlo per il punto di ingresso di elevazione dei privilegi se il comando non riesce.<br/> | Visualizzare l'interfaccia utente di elevazione dei privilegi quando l'utente riprova a eseguire il comando.<br/>                                       |
    | Passaggio attività<br/>  | Tutti i passaggi successivi richiedono l'elevazione dei privilegi.<br/>                                                                                                               | ![Screenshot del pulsante di comando successivo con uac shield ](images/winenv-uac-image20.png)<br/> Schermata di Controllo dell'account utente sul pulsante Avanti (o equivalente).<br/>                                                                | Visualizza l'interfaccia utente di elevazione dei privilegi quando si fa clic sul pulsante Avanti o altro commit.<br/>                         |
    | Passaggio attività<br/>  | Alcuni rami richiedono l'elevazione dei privilegi.<br/>                                                                                                                      | ![Screenshot del collegamento di comando con uac shield ](images/winenv-uac-image21.png)<br/> Protezione del controllo dell'account utente nei collegamenti di comando che richiedono l'elevazione dei privilegi.<br/>                                                              | Visualizzare l'interfaccia utente di elevazione dei privilegi quando si fa clic sui collegamenti di comando con lo schermo del controllo dell'account utente.<br/>                      |

    

     

### <a name="elevation-ui"></a>Interfaccia utente di elevazione dei privilegi

-   **Se l'utente fornisce un account non valido (nome o password) o che non dispone di privilegi di amministratore, è sufficiente visualizzare di nuovo l'interfaccia utente delle credenziali.** Non visualizzare un messaggio di errore.
-   **Se l'utente annulla l'interfaccia utente delle credenziali, restituire l'utente all'interfaccia utente originale.** Non visualizzare un messaggio di errore.
-   Se Controllo account utente è stato disattivato e un utente Standard tenta di eseguire un'attività che richiede l'elevazione dei privilegi, fornire un messaggio di errore che indica che questa attività richiede privilegi di amministratore. Per eseguire questa attività, è necessario accedere con un account amministratore."

![Screenshot dell'attività che richiede il messaggio di privilegi ](images/winenv-uac-image22.png)

In questo esempio Il controllo dell'account utente è stato disattivato, quindi un messaggio di errore spiega che l'utente deve usare un account amministratore.

### <a name="wizards"></a>Procedure guidate

-   **Non elevare più volte.** Una volta che una procedura guidata è stata elevata, deve rimanere con privilegi elevati.
-   Se l'attività viene eseguita all'interno della procedura guidata, inserire uno schermo del controllo dell'account utente sul pulsante "Avanti" della pagina Commit (a cui deve essere data [un'etichetta più specifica).](win-wizards.md) Quando l'utente esegue il commit:
    -   Se la pagina successiva è una pagina Stato, passare a tale pagina e visualizzare modale l'interfaccia utente di elevazione dei privilegi. Al termine dell'elevazione dei privilegi, eseguire l'attività.
    -   Se la pagina successiva è una pagina di completamento, passare a tale pagina (ma sostituire temporaneamente il contenuto con "Waiting for permission...") e visualizzare modalmente l'interfaccia utente di elevazione dei privilegi. Al termine dell'elevazione dei privilegi, eseguire l'attività e quindi visualizzare il contenuto della pagina Completamento.
    -   Se l'utente annulla l'interfaccia utente di elevazione dei privilegi, tornare alla pagina Commit. Questa operazione consente all'utente di riprovare.
-   Se l'attività viene eseguita al termine della procedura guidata, inserire uno schermo del controllo dell'account utente sul pulsante "Fine" della pagina Commit (a cui deve essere data [un'etichetta più specifica).](win-wizards.md) Quando l'utente esegue il commit:
    -   Rimanere nella pagina Commit e visualizzare in modo modale l'interfaccia utente di elevazione dei privilegi. Al termine dell'elevazione, chiudere la procedura guidata.
    -   Se l'utente annulla l'interfaccia utente di elevazione dei privilegi, tornare alla pagina Commit. Questa operazione consente all'utente di riprovare.
-   Per procedure guidate lunghe destinate solo agli amministratori, è possibile richiedere le credenziali di amministratore nel punto di ingresso prima di visualizzare qualsiasi interfaccia utente.

## <a name="text"></a>Testo

-   **Non usare i puntini di sospensione solo perché un comando richiede l'elevazione dei privilegi.** La necessità di elevare è indicata con lo schermo del controllo dell'account utente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a Controllo account utente:

-   Fare riferimento alla funzionalità come Controllo dell'account utente (per prima cosa) o Controllo dell'account utente (alla menzione successiva), non come Account utente con privilegi minimi o LUA.
-   Fare riferimento a utenti non amministratori come utenti Standard.
-   Fare riferimento agli amministratori di computer predefiniti come amministratori predefiniti.

Nella documentazione dell'utente:

-   Fare riferimento all'atto di concedere il consenso per eseguire un'attività amministrativa come concedere l'autorizzazione.

Nella programmazione e in altre informazioni tecniche:

-   Fare riferimento all'atto di fornire il consenso per eseguire un'attività amministrativa come elevazione dei privilegi.
-   Nel contesto del controllo dell'account utente, fare riferimento agli amministratori come amministratori protetti quando non con privilegi elevati e amministratori con privilegi elevati dopo l'elevazione dei privilegi.
-   Fare riferimento alla finestra di dialogo usata per immettere le password come interfaccia utente delle credenziali. Fare riferimento alla finestra di dialogo usata per fornire il consenso come interfaccia utente di consenso. Fare riferimento a entrambi in genere come Elevazione dell'interfaccia utente.

