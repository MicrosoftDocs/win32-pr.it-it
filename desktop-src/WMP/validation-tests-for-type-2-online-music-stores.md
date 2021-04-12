---
title: Test di convalida per i negozi online di tipo 2 di onboarding
description: Questo argomento descrive i test che verranno eseguiti da Microsoft per convalidare l'archivio online di tipo 2. Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata. È necessario che l'archivio online passi i test da pubblicare.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396086"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Test di convalida per i negozi online di tipo 2 di onboarding

Questo argomento descrive i test che verranno eseguiti da Microsoft per convalidare l'archivio online di tipo 2. Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata. È necessario che l'archivio online passi i test da pubblicare.

> [!Note]  
> Se l'archivio è di tipo 1 anziché di tipo 2, è possibile usare questo argomento come linea guida per comprendere l'ambito del test di certificazione trattato per gli archivi di tipo 1. Per il set completo di test per i negozi di tipo 1, contattare [supporto tecnico Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

In questo argomento sono contenute le sezioni seguenti.

-   [Elenco di controllo test](#test-checklist)
    -   [Preparazione superamento test](#test-pass-preparation)
-   [Ambiente di test](#test-environment)
-   [Installazione e configurazione](#configuration-and-setup)
    -   [Configurazione di un computer di test](#setting-up-a-test-machine)
    -   [Configurazione di un archivio](#setting-up-a-store)
    -   [Creazione di un account](#creating-an-account)
    -   [Impostazione della memorizzazione delle credenziali nella cache](#setting-up-credential-caching)
-   [Acquisizione contenuto](#content-acquisition)
    -   [Flusso di contenuti](#streaming-content)
    -   [Recupero del contenuto](#obtaining-content)
    -   [Burning del contenuto](#burning-content)
    -   [Trasferimento di contenuto](#transferring-content)
-   [Funzionalità di archiviazione](#store-features)
    -   [Gestione di un account](#managing-an-account)
    -   [Gestione del centro informazioni](#managing-the-info-center)
-   [Interazione archivio](#store-interaction)
    -   [Cedendo all'archivio attivo](#yielding-to-the-active-store)
    -   [Impedire all'archivio testato di assumere l'archivio attivo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Accesso a un archivio in modalità High-Contrast](#accessing-a-store-in-high-contrast-mode)
    -   [Protezione di un archivio](#securing-a-store)

## <a name="test-checklist"></a>Elenco di controllo test

Usare l'elenco di controllo nella tabella seguente per convalidare il negozio online di tipo 2 che si vuole portare a bordo.



Test

Windows XP

Windows Vista

Windows 7

Risultato (superato/non superato/non applicabile)

32

64

32

64

32

64

1. Verificare che il software sia installato.

2. Verificare la disinstallazione del software.

3. Verificare che il software non venga eseguito nell'area di notifica.

4. Verificare che la scheda Store funzioni.

5. Verificare che l'archivio disponga di un'opzione per creare un nuovo account.

6. Verificare che l'account creato possa effettuare l'accesso.

7. Verificare che l'archivio disponga di un'opzione per salvare le informazioni utente.

8. Verificare che la memorizzazione nella cache delle credenziali sia presente e funzionante.

9. Verificare che all'utente vengano richieste le credenziali se non sono memorizzate nella cache.

10. Verificare che tutti i tipi di flusso di contenuto disponibili.

11. Verificare che il contenuto riproduca in Microsoft Windows Media Player.

12. Verificare che il prezzo calcolato sia corretto.

13. Verificare che il contenuto acquistato venga scaricato nella libreria.

14. Verificare che i metadati vengano scaricati per l'acquisto.

15. Verificare che i diritti di utilizzo del supporto siano corretti per l'acquisto.

16. Verificare che il contenuto acquistato possa essere riprodotto.

17. Verificare che facendo clic sul pulsante **Acquista** **o acquista sia** possibile passare allo Store.

18. Verificare che il contenuto acquistato sia stato scaricato.

19. Verificare che il contenuto acquistato possa essere bruciato.

20. Verificare che il numero di masterizzazioni venga decrementato.

21. Verificare che il contenuto possa essere trasferito a un altro computer.

22. Verificare che il contenuto venga trasferito a un dispositivo.

23. Verificare che il numero di sincronizzazioni venga decrementato.

24. Verificare che la cronologia degli acquisti tenga traccia degli acquisti precedenti.

25. Verificare che sia possibile ripristinare un acquisto precedente.

26. Verificare la funzionalità di un archivio per gestire più computer.

27. Verificare che il centro informazioni sia disattivato per impostazione predefinita.

28. Verificare che il centro informazioni includa informazioni multimediali nell'area Now-Playing.

29. Verificare che i collegamenti accedano all'archivio.

30. Verificare che l'archivio testato venga restituito nell'archivio attivo.

31. Verificare che l'archivio testato non occupi l'archivio corrente.

32. Verificare che l'archivio sia accessibile in modalità a contrasto elevato.

33. Verificare che l'archivio sia protetto.



 

### <a name="test-pass-preparation"></a>Preparazione superamento test

Prima di eseguire un test superato, è necessario assicurarsi che l'archivio e gli account di test siano pronti per il test. Prima dell'avvio del passaggio, è necessario determinare le informazioni seguenti. Se è possibile determinare le informazioni per alcuni giorni prima del superamento del test, il passaggio viene eseguito in modo più efficiente.

-   Determinare le seguenti informazioni sugli account di test forniti dall'archivio:
    -   Account e password funzionano per consentire a un utente di eseguire l'accesso
    -   Gli account sono finanziati correttamente e adeguatamente per ogni tipo di modalità aziendale offerta dallo Store
    -   Gli account sono validi per tutte le impostazioni locali da testare oppure sono presenti account per ogni impostazione locale se gli account non possono superare le impostazioni locali
-   Determinare le impostazioni locali da testare.
-   Determinare le lingue da testare.
-   Determinare le seguenti informazioni sull'ambiente di testing:

    -   Archivi Live compatibili con Windows XP, Windows Vista e Windows 7
    -   Archivio non Live da testare
    -   Verificare che l'archivio non Live da testare sia visibile in tutte le versioni del sistema operativo e in tutte le versioni della piattaforma Windows Media Player.

-   Determinare le informazioni seguenti sull'archivio da testare:

    -   Nome archivio
    -   Grafica e etichetta del logo della scheda Store prevista
    -   Lo Store è attivo per tutte le versioni del sistema operativo?
    -   Si tratta di una nuova versione dell'archivio sottoposta a test?
    -   L'archivio è sottoposto a test di tipo 1 o di tipo 2?
    -   Il tipo di archivio è stato modificato?

-   Determinare in quali versioni e piattaforme del sistema operativo si prevede di testare l'archivio.
-   Determinare che il programma di installazione e il plug-in funzionano su tutte le versioni e le piattaforme del sistema operativo da testare.
-   Determinare se è necessario un documento di navigazione.
-   Determinare le informazioni seguenti sui supporti offerti dal negozio:

    -   Formati
    -   È necessario un software proprietario?
    -   È necessario testare tutti i tipi di supporto o solo un subset di tipi di supporti?

-   Determinare le seguenti informazioni sui diritti di utilizzo del supporto:

    -   I supporti di archiviazione hanno la protezione del contenuto?
    -   In tal caso, determinare il tipo di protezione del contenuto del supporto.
    -   In tal caso, determinare il comportamento protetto previsto.
    -   I diritti di utilizzo dei supporti includono la condivisione da computer a computer?
    -   Diritti di sincronizzazione
    -   Diritti di masterizzazione
    -   Diritti di riproduzione
    -   Date di scadenza, se presenti

-   Determinare se sono presenti supporti sufficienti (un catalogo sufficientemente grande) per fornire un campione significativo.
-   Determinare quale passaggio della fase è: RC 0, conformità e così via.
-   Determinare se il superamento del test è un tipo specifico: regressione, fumo e così via.

## <a name="test-environment"></a>Ambiente di test

È necessario eseguire il test delle configurazioni seguenti:

-   Microsoft Windows Media Player 11 nei sistemi operativi Windows XP con Service Pack 3 (SP3) a 32 bit e a 64 bit
-   Windows Media Player 11 nei sistemi operativi Windows Vista a 32 bit e a 64 bit (Windows Media Player a 32 bit)
-   Microsoft Windows Media Player 12 nei sistemi operativi Windows a 7 32 bit e a 64 bit (Windows Media Player a 32 bit)

Sebbene sia necessario eseguire test su tutte le versioni e le piattaforme del sistema operativo elencate, le versioni a 32 bit di Windows Vista e Windows 7 sono le versioni del sistema operativo prioritarie. È necessario testare l'installazione di qualsiasi software su tutte le piattaforme.

Le schermate in questo argomento usano un archivio fittizio, Proseware, per illustrare l'uso dell'interfaccia utente.

## <a name="configuration-and-setup"></a>Installazione e configurazione

Le sezioni seguenti descrivono come configurare e configurare i test di convalida per il caricamento in un archivio online di tipo 2.

### <a name="setting-up-a-test-machine"></a>Configurazione di un computer di test

Per configurare un computer di test, seguire questa procedura:

1.  Puntare il computer di test ai server di test del contenuto aggiungendo una chiave del registro di sistema specifica dell'archivio.
2.  Impostare i valori nella finestra di dialogo **Opzioni internazionali e della lingua** sulla lingua e le impostazioni locali appropriate. Per impostare la lingua, selezionare la scheda **formati** , quindi selezionare la lingua nella casella combinata **formato corrente** . Per impostare l'area, selezionare la scheda **località** , quindi selezionare l'area nella casella combinata **percorso corrente** . Inoltre, per gli archivi che richiedono l'installazione di un plug-in o di un software personalizzato specifico dell'archivio, potrebbe essere necessario modificare le impostazioni locali del sistema in base alla lingua delle impostazioni locali del negozio per facilitare l'installazione. Il programma di installazione software deve supportare sia caratteri a byte singolo che doppi e deve essere eseguito in qualsiasi impostazione locale. È necessario eseguire il test nelle impostazioni locali native. Per impostare le impostazioni locali native, aprire la finestra di dialogo **regione e lingua** , selezionare la scheda **amministrativa** , quindi fare clic sul pulsante **Modifica impostazioni locali del sistema** , come illustrato nella schermata seguente. Quando si fa clic su questo pulsante viene visualizzata la finestra **di dialogo Impostazioni area e lingua** . Nella casella combinata **impostazioni locali del sistema corrente** della finestra di dialogo vengono modificate le impostazioni locali del sistema.

    Le schermate seguenti mostrano le schede in cui è possibile impostare l'area e la lingua:

    ![screenshot della finestra di dialogo Opzioni internazionali e della lingua](images/reg-lang-opt.png)

    ![screenshot che Mostra come modificare le impostazioni locali correnti del sistema](images/reg-lang-settings.png)

3.  Disattivare la visualizzazione del centro informazioni di un negozio impostando Windows Media Player per riprodurre una visualizzazione. La differenza principale tra le piattaforme è che in Windows Media Player 11, si inizia facendo clic su **Now Playing**, mentre in Windows Media Player 12 si inizia facendo clic con il pulsante destro del mouse sulla finestra principale.

    Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione in Windows Media Player 11:

    ![screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 11](images/wmp11-visual.png)

    Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione in Windows Media Player 12:

    ![screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configurazione di un archivio

Eseguire prima di tutto i passaggi seguenti per configurare un archivio e quindi eseguire i passaggi che seguono i passaggi iniziali per verificare l'installazione del negozio:

1.  Avviare Windows Media Player e attendere alcuni secondi per acquisire il file di AllServices.xml più recente.
2.  Per Windows XP e Windows Vista, per selezionare uno Store online, fare prima clic sulla scheda che divide tra la visualizzazione della guida multimediale e la visualizzazione negozi online. Quindi, dal menu fare clic su **Sfoglia tutti gli archivi online** e selezionare l'archivio facendo clic sull'icona nell'elenco di archivi. Per Windows 7, fare clic sul pulsante nel riquadro di spostamento della libreria che divide tra il pulsante della **Guida multimediale** e il pulsante **online stores** . Quindi, dal menu fare clic su **Sfoglia tutti gli archivi online** e selezionare l'archivio facendo clic sull'icona nell'elenco di archivi.

    Lo screenshot seguente mostra come selezionare uno Store online in Windows Media Player 11:

    ![screenshot che illustra come selezionare uno Store online in Windows Media Player 11](images/wmp11-set-store.png)

    Lo screenshot seguente mostra come selezionare uno Store online in Windows Media Player 12:

    ![screenshot che illustra come selezionare uno Store online in Windows Media Player 12](images/wmp12-set-store.png)

3.  Seguire le istruzioni dello Store per installare eventuali software aggiuntivi necessari per usare lo Store.

**Per verificare l'installazione dell'archivio**

1.  Verificare che il software venga installato.

    Verificare che il plug-in OCX o qualsiasi altro software dallo Store venga scaricato e installato senza errori.

2.  Verificare la disinstallazione del software.

    Verificare che nel pannello di controllo, nell'elemento **programmi e funzionalità** , il software installato dall'archivio venga visualizzato nell'elenco **Disinstalla o modifica programma** e verificare che sia possibile disinstallarlo da questo elenco senza errori.

3.  Verificare che il software non venga eseguito nella barra di sistema.

    Verificare che nessuno dei software dello Store aggiunga icone all'area di notifica del programma (sulla barra delle applicazioni a sinistra del clock) prima del consenso del cliente per scaricare il software dello Store.

    L'esperienza di archiviazione di base non richiede l'installazione di software aggiuntivo. Dovrebbe essere disponibile un'esperienza di supporto di base, ad esempio flussi multimediali. Alcuni negozi installano software aggiuntivo, ad esempio Download Manager, per un'esperienza di supporto Premier. questi archivi possono avere icone nella barra di sistema se le icone rappresentano applicazioni separate da Windows Media Player.

4.  Verificare che la scheda Store funzioni.

    Verificare che la scheda archivia cambi per indicare l'archivio selezionato.

    Per Windows XP e Windows Vista con Windows Media Player 11, verificare che il nome e l'icona del negozio siano visibili sullo sfondo di Windows Media Player 11 scuro.

    Per Windows 7 con Windows Media Player 12, verificare che il nome e l'icona dell'archivio siano visibili nel riquadro di spostamento della libreria, nel menu di scelta rapida del selettore del servizio.

    Verificare che l'archivio sia elencato nella parte superiore dell'elenco dei selettori del negozio nel menu.

    > [!Note]  
    > Non verrà aggiunta l'opzione **di menu Aggiungi servizio corrente** se l'archivio di tipo 2 è l'archivio in primo piano (impostazione predefinita) per l'area.

     

    Lo screenshot seguente mostra il menu visualizzato quando si fa clic sulla scheda nell'angolo superiore destro di Windows Media Player 11:

    ![screenshot che mostra la scheda Store in Windows Media Player 11](images/wmp11-verify-store.png)

    Lo screenshot seguente mostra il menu visualizzato quando si fa clic sul pulsante di menu combinato nell'angolo inferiore sinistro di Windows Media Player 12:

    ![screenshot che mostra la scheda Store in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Creazione di un account

**Per verificare la configurazione dell'account**

1.  Verificare che l'archivio disponga di un'opzione per creare un nuovo account e quindi seguire le istruzioni per la creazione di un nuovo account.

    Lo screenshot seguente evidenzia un pulsante **Crea nuovo account** come potrebbe essere visualizzato in Windows Media Player 11:

    ![screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 11](images/wmp11-verify-account.png)

    Lo screenshot seguente evidenzia un pulsante **Crea nuovo account** come potrebbe essere visualizzato in Windows Media Player 12:

    ![screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 12](images/wmp12-verify-account.png)

2.  Verificare che sia possibile accedere all'account creato.

### <a name="setting-up-credential-caching"></a>Impostazione della memorizzazione delle credenziali nella cache

Eseguire prima di tutto i passaggi seguenti per configurare la memorizzazione delle credenziali nella cache, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare la configurazione della memorizzazione nella cache delle credenziali:

1.  Nella pagina di accesso immettere le credenziali e selezionare l'opzione per salvare le informazioni utente.
2.  Verificare che nella pagina di accesso sia presente una casella di controllo che consente all'utente di memorizzare nella cache le credenziali.
3.  La memorizzazione nella cache delle credenziali facoltativa è un punto di sicurezza importante. Il caching automatico delle credenziali può esporre informazioni personali degli utenti che effettuano l'accesso a un computer condiviso o pubblico. È consigliabile proteggere le informazioni dei clienti offrendo una casella di controllo che consente di eseguire il rendering facoltativo della memorizzazione nella cache.

**Per verificare la memorizzazione delle credenziali nella cache**

1.  Verificare che nell'archivio sia presente una casella di controllo per l'opzione **Salva le informazioni utente** .

    1.  Chiudere Media Player di Windows.
    2.  Riaprire Media Player di Windows e provare a scaricare contenuto.

2.  Verificare che la memorizzazione nella cache delle credenziali sia presente e funzionante.

    1.  Disconnettersi dallo Store.
    2.  Chiudere Media Player di Windows.
    3.  Riaprire Media Player di Windows e provare a scaricare contenuto.

3.  Verificare che all'utente vengano richieste le credenziali se non sono memorizzate nella cache.

    Dopo la disconnessione e il tentativo di usare lo Store, al cliente verranno richieste le credenziali.

## <a name="content-acquisition"></a>Acquisizione contenuto

In questa sezione vengono descritti i vari modi per acquisire contenuto e come verificare che il contenuto sia stato acquisito.

### <a name="streaming-content"></a>Flusso di contenuti

Trasmettere tutti i tipi di contenuto disponibili dall'archivio. Ad esempio, flusso di contenuto Radio, video, audio e anteprime.

**Per verificare il contenuto di streaming**

1.  Verificare che tutti i tipi di flusso di contenuto disponibili.

2.  Verificare che il contenuto riproduca in Windows Media Player e non in un altro lettore o controllo.

### <a name="obtaining-content"></a>Recupero del contenuto

Eseguire prima di tutto i passaggi seguenti per acquistare il contenuto, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare l'acquisto e verificare che il contenuto sia stato scaricato:

1.  Avviare Windows Media Player.
2.  Accedere all'account di test.
3.  Passare al contenuto da acquistare.
4.  Seguire la procedura specifica dell'archivio per acquistare il contenuto.

**Per verificare il contenuto acquistato e scaricato**

1.  Verificare che il prezzo calcolato sia corretto.

    Verificare che il prezzo sia corretto, in particolare quando si acquistano più parti di contenuto contemporaneamente e si verifica che le informazioni di saldo del conto siano aggiornate correttamente dopo l'acquisto. Alcuni contenuti possono essere acquistati come singole tracce e solo alcuni come album. Verificare che il prezzo dell'album non sia maggiore della somma delle singole tracce.

2.  Verificare che il contenuto acquistato venga scaricato nella libreria.

    Al termine del download, passare al contenuto scaricato nella libreria Media Player di Windows. Il contenuto scaricato si trova nella libreria dell'utente corrente.

    -   Per Windows XP e Windows Vista con Windows Media Player 11, il contenuto scaricato viene visualizzato nel riquadro di spostamento della libreria, in pivot **libreria** , quindi in **canzoni**.
    -   Per Windows 7 con Windows Media Player 12, il contenuto scaricato nella libreria di Windows Media Player viene visualizzato nel riquadro di spostamento Media Player Windows in **musica**.

3.  Verificare che vengano scaricati i metadati per l'acquisto.

    Verificare che le colonne seguenti siano visualizzate nella libreria Media Player di Windows (aggiungere in caso contrario):

    -   Artista album
    -   Titolo
    -   Titolo album
    -   Provider di contenuti
    -   Genre

    È necessario popolare le colonne precedenti. Il contenuto deve avere album art. Tuttavia, non è necessario che l'Art album superi i test di convalida.

4.  Verificare che i diritti di utilizzo del supporto siano corretti per l'acquisto.

    Per ogni traccia scaricata, fare clic con il pulsante destro del mouse sulla traccia e selezionare **Proprietà**, quindi selezionare la scheda **diritti di utilizzo del supporto** .

    L'archivio può scegliere di proteggere il contenuto con i diritti di utilizzo dei supporti oppure può scegliere di non proteggere il contenuto. La scheda **diritti di utilizzo del supporto** riflette tale stato elencando le restrizioni oppure indicando che il contenuto non è protetto. L'archivio deve comunicare il piano più recente per i diritti di utilizzo dei supporti. È necessario verificare i risultati effettivi rispetto a questo comportamento previsto.

    Le licenze per i diritti multimediali devono essere pre-recapitate. Il cliente non deve necessariamente riprodurre il contenuto o eseguire altre procedure per ottenere la licenza. È necessario confrontare i diritti di utilizzo di supporti specifici per le comunicazioni tra il negozio e il cliente in base alle esigenze. I diritti devono essere trasferibili ad almeno altri due computer. I clienti devono poter masterizzare e sincronizzare i propri supporti.

    Lo screenshot seguente illustra i diritti di utilizzo del supporto di un file protetto:

    ![screenshot che mostra i diritti di utilizzo dei supporti per un file protetto](images/media-rights-protected.png)

    Se il contenuto non è protetto, la scheda **Rights Usage media** indicherà questo fatto.

    Lo screenshot seguente illustra i diritti di utilizzo del supporto di un file non protetto:

    ![screenshot che mostra i diritti di utilizzo dei supporti per un file non protetto](images/media-rights-not-protected.png)

5.  Verificare che il contenuto acquistato venga riprodotto.

    Verificare che il contenuto scaricato venga riprodotto in Windows Media Player.

    Riprodurre qualsiasi contenuto acquistato dallo Store e che risiede nella libreria locale oppure trasmettere un'anteprima.

    Per acquistare contenuto in Windows XP e Windows Vista con Windows Media Player 11, seguire questa procedura:

    1.  Fare clic sulla scheda **Now Playing** .
    2.  Nel riquadro dell'elenco posizionare il puntatore del mouse sul passaggio del mouse su album art per visualizzare il collegamento **Acquista** .
    3.  Fare clic su **Acquista**.

    Lo screenshot seguente mostra il percorso del collegamento **buy** in Windows Media Player 11:

    ![screenshot che illustra come acquistare contenuto in Windows Media Player 11](images/wmp11-verify-buy-play.png)

    Per acquistare contenuto in Windows 7 con Windows Media Player 12, attenersi alla procedura seguente:

    1.  In modalità libreria fare clic sulla scheda **Riproduci** .
    2.  Nella playlist, in album Art, fare clic su **Shop**

    Lo screenshot seguente mostra come acquistare contenuto in Windows Media Player 12:

    ![screenshot che illustra come acquistare contenuto in Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  Verificare **che fare clic** su **Acquista** o acquista opzioni per lo Store.

    Il Media Player di Windows dovrebbe passare allo Store nella visualizzazione libreria e caricare l'esperienza di acquisto dello Store.

    È quindi necessario continuare a acquistare la traccia.

7.  Verificare che dopo aver fatto clic su **acquista o acquista** , il contenuto viene scaricato.

    Verificare che i diritti di utilizzo del supporto siano appropriati per il contenuto acquistato e i relativi metadati e verificare che la traccia riproduca. In generale, questo metodo di acquisto deve avere gli stessi risultati di altri metodi.

### <a name="burning-content"></a>Burning del contenuto

Eseguire prima di tutto i passaggi seguenti per masterizzare il contenuto acquistato (copiare il contenuto acquistato in un CD o DVD scrivibile), quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto bruci:

> [!Note]  
> Prima di masterizzare una traccia acquistata, annotare il numero di Burn, in modo da poter verificare in seguito se il conteggio diminuisce dopo aver bruciato la traccia.

 

1.  Fare clic sulla scheda **Burn**
2.  Trascinare le tracce acquistate nell' **elenco di masterizzazioni**.
3.  Fare clic sul pulsante **Avvia Burn** .

Lo screenshot seguente mostra l' **elenco di masterizzazioni** sul lato destro dello schermo e il pulsante **Avvia Burn** sotto l' **elenco di masterizzazione** in Windows Media Player 11:

![screenshot che illustra come masterizzare contenuto in Windows Media Player 11](images/wmp11-verify-burn.png)

Lo screenshot seguente mostra come viene visualizzato l'elenco di masterizzazione in Windows Media Player 12 dopo aver trascinato una traccia nell'elenco di masterizzazione e viene visualizzato il pulsante **Avvia Burn** nella parte superiore della scheda **Burn** :

![screenshot che illustra come masterizzare contenuto in Windows Media Player 12](images/wmp12-verify-burn.png)

**Per verificare che il contenuto acquistato possa essere bruciato**

1.  Verificare che il contenuto acquistato venga bruciato giocando il CD o il DVD dopo il completamento della masterizzazione.

2.  Verificare che il numero di masterizzazioni venga decrementato.

    Passare alla raccolta e aprire i diritti di utilizzo del supporto per una traccia acquistata che è stata bruciata.

    Se il numero di volte in cui è possibile masterizzare una traccia è limitato, verificare che questo numero venga diminuito dopo che la traccia è stata bruciata.

### <a name="transferring-content"></a>Trasferimento di contenuto

Trasferire il contenuto a un altro computer.

**Per verificare che il contenuto acquistato possa essere trasferito a un altro computer**

-   Se l'archivio consente il trasferimento di contenuto a un altro computer, trasferire il contenuto ad almeno due computer.

Eseguire prima di tutto i passaggi seguenti per sincronizzare un dispositivo e trasferire il contenuto acquistato al dispositivo, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto venga trasferito:

> [!Note]  
> Prima di trasferire una traccia acquistata, annotare il numero di sincronizzazioni, in modo da poter verificare in seguito se il conteggio diminuisce dopo il trasferimento della traccia.

 

1.  Connettere un dispositivo con un clock protetto. Alcuni esempi includono i dispositivi che usano Windows Media DRM per i dispositivi portatili, ad esempio un centro multimediale portatile come iRiver H10, Creative Zen e così via.
2.  In Windows Media Player fare clic sulla scheda **Sincronizza** .
3.  Trascinare il contenuto dalla libreria all'area **elenco sincronizzazione** nella scheda **Sincronizza** .
4.  Fare clic sul pulsante **Avvia sincronizzazione** .

Lo screenshot seguente mostra la traccia 1 nell'area **elenco sincronizzazione** e Mostra il pulsante **Avvia sincronizzazione** in Windows Media Player 11:

![screenshot che Mostra come trasferire il contenuto in Windows Media Player 11](images/wmp11-verify-transfer.png)

Lo screenshot seguente mostra la traccia 1 nell'area **elenco sincronizzazione** e Mostra il pulsante **Avvia sincronizzazione** in Windows Media Player 12:

![screenshot che Mostra come trasferire il contenuto in Windows Media Player 12](images/wmp12-verify-transfer.png)

**Per verificare che il contenuto acquistato possa essere trasferito a un altro dispositivo**

1.  Verificare che il contenuto acquistato venga trasferito al dispositivo giocando al contenuto del dispositivo. Anche il contenuto trasferito deve avere metadati appropriati.

2.  Verificare che il numero di sincronizzazioni venga decrementato.

    Passare alla raccolta e aprire i diritti di utilizzo del supporto per una traccia trasferita.

    Se il numero di volte in cui è possibile sincronizzare una traccia è limitato, verificare che questo numero diminuisca quando viene trasferita la traccia.

## <a name="store-features"></a>Funzionalità di archiviazione

Le sezioni seguenti descrivono come testare le varie funzionalità di un negozio online caricato.

### <a name="managing-an-account"></a>Gestione di un account

Accedere con un account che ha effettuato alcuni acquisti e aprire la cronologia degli acquisti.

**Per verificare la cronologia degli acquisti**

-   Verificare che la cronologia degli acquisti tenga traccia degli acquisti precedenti.

Se il tipo di account o archivio supporta questa funzionalità, provare a ripristinare un acquisto eliminato.

**Per verificare che gli acquisti precedenti possano essere riacquisiti**

-   Verificare che sia possibile ripristinare un acquisto precedente.

Se l'archivio supporta l'utilizzo di più computer con l'account, verificare le funzionalità fornite da questa funzionalità.

**Per verificare la gestione di più computer con un singolo account**

-   Verificare la funzionalità dell'archivio per gestire più computer.

### <a name="managing-a-store-specific-account"></a>Gestione di un account Store-Specific

L'archivio potrebbe non avere tipi di account, restrizioni o contenuti tipici. Ad esempio, un archivio che affitta il video di streaming potrebbe richiedere un'interfaccia utente per visualizzare i noleggi attivi e l'interfaccia utente deve essere testata.

> [!Note]  
> Sebbene Microsoft non sia in grado di certificare le funzionalità degli account specifici dell'archivio, per garantire una migliore esperienza con i clienti, è consigliabile testare tale funzionalità.

 

### <a name="managing-the-info-center"></a>Gestione del centro informazioni

Eseguire prima di tutto i passaggi seguenti per preparare il test dello stato predefinito, quindi eseguire il passaggio successivo che segue i passaggi iniziali per verificare che il centro informazioni sia disattivato per impostazione predefinita:

1.  Riprodurre contenuto dall'archivio.
2.  Passa alla modalità di riproduzione. In Windows XP o Windows Vista con Windows Media Player 11, fare clic sulla scheda **Now Playing** . In Windows 7 con Windows Media Player 12 fare clic sul pulsante **passa a ora di riproduzione** nell'angolo in basso a destra.

**Per verificare che il centro informazioni sia disattivato per impostazione predefinita**

-   Verificare che il centro informazioni sia disattivato per impostazione predefinita.

Se l'archivio offre una visualizzazione del centro informazioni, Riproduci contenuto dallo Store e durante la riproduzione del contenuto passa alla modalità di riproduzione e attiva il centro informazioni.

In Windows XP o Windows Vista con Windows Media Player 11, fare clic con il pulsante destro del mouse sulla finestra Now-playing, quindi scegliere **visualizzazione centro informazioni** dal menu di scelta rapida.

Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 11:

![screenshot che illustra come accedere al centro informazioni di un negozio in Windows Media Player 11](images/wmp11-info-center.png)

In Windows 7 con Windows Media Player 12, fare clic con il pulsante destro del mouse sulla finestra Now-playing, scegliere **visualizzazioni** dal menu di scelta rapida e quindi fare clic su **visualizzazione centro informazioni**.

Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 12:

![screenshot che illustra come accedere al centro informazioni di un negozio in Windows Media Player 12](images/wmp12-info-center.png)

**Per verificare che il centro informazioni funzioni**

-   Verificare che il centro informazioni mostri informazioni sui supporti nell'area di riproduzione. Lo screenshot seguente mostra un esempio di tali informazioni sui supporti:

    ![screenshot che mostra la funzionalità del centro informazioni di un negozio](images/media-information.png)

Se nella pagina vengono visualizzati collegamenti di acquisto o altri collegamenti, fare clic sui collegamenti.

**Per verificare i collegamenti nella visualizzazione del centro informazioni**

-   Verificare che i collegamenti visualizzino l'archivio.

    Il Media Player di Windows dovrebbe passare all'archivio nella propria libreria.

## <a name="store-interaction"></a>Interazione archivio

Le sezioni seguenti descrivono come testare l'interazione tra gli altri archivi e l'archivio che si sta testando.

### <a name="yielding-to-the-active-store"></a>Cedendo all'archivio attivo

Passa a un archivio diverso da quello testato.

**Per verificare il cedimento all'archivio attivo**

-   Verificare che l'archivio testato venga restituito nell'archivio attivo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedire all'archivio testato di assumere l'archivio attivo

-   Con un altro archivio selezionato, chiudere Windows Media Player e riavviare il computer.
-   Avviare Windows Media Player.

**Per verificare che l'archivio testato non riprenda**

-   Verificare che venga visualizzato l'archivio attivo più di recente e che l'archivio testato non venga visualizzato.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Accesso a un archivio in modalità High-Contrast

Per prima cosa abilitare la modalità a contrasto elevato premendo MAIUSC a sinistra + ALT di sinistra + STAMP, quindi eseguire i passaggi seguenti per verificare l'accessibilità a contrasto elevato:

**Per verificare che l'archivio sia accessibile in modalità a contrasto elevato**

1.  Verificare che l'interfaccia utente di accesso sia intatta e funzionante.
2.  Verificare che tutte le finestre e le finestre di dialogo vengano visualizzate correttamente.
3.  Acquistare supporti. Verificare che i pulsanti per l'acquisto e il download, i manager di download, le informazioni sui prezzi e così via siano visibili.
4.  Verificare che sia possibile trasmettere, masterizzare e sincronizzare.
5.  Cercare elementi di testo e interfaccia utente ritagliati, testo non leggibile e altri difetti visibili.

### <a name="securing-a-store"></a>Protezione di un archivio

Per verificare la sicurezza dell'account, attenersi alla procedura seguente:

**Per verificare la sicurezza dell'account**

1.  Immettere le informazioni relative all'account con formato non valido nella pagina e nella finestra di dialogo di accesso e verificare che l'archivio la rifiuti.
2.  Accedere, visualizzare la pagina dell'account e disconnettersi.
3.  Fare clic sul pulsante indietro in Windows Media Player e verificare di non visualizzare le informazioni sull'account utente precedente.

 

 




