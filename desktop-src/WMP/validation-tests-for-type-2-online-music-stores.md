---
title: Test di convalida per i negozi online di tipo 2 di on boarding
description: Questo argomento descrive i test che Microsoft eseguirà per convalidare lo store online di tipo 2. Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata. Lo store online deve superare correttamente questi test per la pubblicazione.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2cb1b4d44b1bd3c6289311c6b276de7c75ed1bcd955431796a36d272811942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901306"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Test di convalida per i negozi online di tipo 2 di on boarding

Questo argomento descrive i test che Microsoft eseguirà per convalidare lo store online di tipo 2. Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata. Lo store online deve superare correttamente questi test per la pubblicazione.

> [!Note]  
> Se il negozio è di tipo 1 anziché di tipo 2, è possibile usare questo argomento come linea guida per comprendere l'ambito dei test di certificazione trattati per gli store di tipo 1. Per il set completo di test per gli archivi di tipo 1, [contattare Supporto tecnico Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

In questo argomento sono contenute le sezioni seguenti.

-   [Elenco di controllo per i test](#test-checklist)
    -   [Preparazione test superato](#test-pass-preparation)
-   [Ambiente di test](#test-environment)
-   [Installazione e configurazione](#configuration-and-setup)
    -   [Configurazione di un computer di test](#setting-up-a-test-machine)
    -   [Configurazione di uno Store](#setting-up-a-store)
    -   [Creazione di un account](#creating-an-account)
    -   [Configurazione delle credenziali Caching](#setting-up-credential-caching)
-   [Acquisizione del contenuto](#content-acquisition)
    -   [Streaming di contenuti](#streaming-content)
    -   [Recupero di contenuto](#obtaining-content)
    -   [Contenuto inevaso](#burning-content)
    -   [Trasferimento di contenuto](#transferring-content)
-   [Funzionalità dello Store](#store-features)
    -   [Gestione di un account](#managing-an-account)
    -   [Gestione del Centro informazioni](#managing-the-info-center)
-   [Interazione con l'archivio](#store-interaction)
    -   [Cede all'archivio attivo](#yielding-to-the-active-store)
    -   [Impedire all'archivio testato di assumere la proprietà dell'archivio attivo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Accesso a uno Store in High-Contrast predefinita](#accessing-a-store-in-high-contrast-mode)
    -   [Protezione di uno Store](#securing-a-store)

## <a name="test-checklist"></a>Elenco di controllo per i test

Usare l'elenco di controllo nella tabella seguente per convalidare lo store online di tipo 2 da portare a bordo.



Test

Windows XP

Windows Vista

Windows 7

Risultato (pass/fail/non applicabile)

32

64

32

64

32

64

1. Verificare che il software sia installato.

2. Verificare che il software sia disinstallato.

3. Verificare che il software non sia in esecuzione nell'area di notifica.

4. Verificare che la scheda Store funzioni.

5. Verificare che lo Store abbia un'opzione per creare un nuovo account.

6. Verificare che l'account creato possa accedere.

7. Verificare che l'archivio abbia un'opzione per salvare le informazioni utente.

8. Verificare che la memorizzazione delle credenziali nella cache sia presente e funzionante.

9. Verificare che all'utente siano richieste le credenziali se non sono memorizzate nella cache.

10. Verificare che tutti i tipi di flusso di contenuto disponibili.

11. Verificare che il contenuto sia riprodotto in Microsoft Windows Media Player.

12. Verificare che un prezzo calcolato sia corretto.

13. Verificare che il contenuto acquistato sia stato scaricato nella raccolta.

14. Verificare che i metadati siano stati scaricati per l'acquisto.

15. Verificare che i diritti di utilizzo dei supporti siano corretti per l'acquisto.

16. Verificare che il contenuto acquistato possa essere riprodotto.

17. Verificare che facendo clic **sul pulsante Acquista** o **Acquista** si passa al Negozio.

18. Verificare che il contenuto acquistato sia stato scaricato.

19. Verificare che i contenuti acquistati possano essere acquistati.

20. Verificare che il numero di ustioni sia decrementato.

21. Verificare che il contenuto possa essere trasferito a un altro computer.

22. Verificare che il contenuto si trasferisca a un dispositivo.

23. Verificare che il numero di sincronizzazione sia decrementato.

24. Verificare che la cronologia degli acquisti tiene traccia degli acquisti precedenti.

25. Verificare che sia possibile ripristinare un acquisto precedente.

26. Verificare la funzionalità di un negozio per gestire più computer.

27. Verificare che l'Info Center sia disattivato per impostazione predefinita.

28. Verificare che l'Info Center abbia informazioni multimediali nell'area di riproduzione.

29. Verificare che i collegamenti si snavigare nell'archivio.

30. Verificare che l'archivio testato ceda all'archivio attivo.

31. Verificare che l'archivio testato non apporti la proprietà dell'archivio corrente.

32. Verificare che l'archivio sia accessibile in modalità a contrasto elevato.

33. Verificare che l'archivio sia sicuro.



 

### <a name="test-pass-preparation"></a>Preparazione test superato

Prima di eseguire un test superato, è necessario assicurarsi che l'archivio e gli account di test siano pronti per il test. Prima di iniziare il passaggio, è necessario determinare le informazioni seguenti. Se è possibile determinare le informazioni alcuni giorni prima del test superato, il test verrà eseguito in modo più efficiente.

-   Determinare le informazioni seguenti sugli account di test forniti dall'archivio:
    -   Account e password funzionano per consentire a un utente di accedere
    -   Gli account sono correttamente e adeguatamente gestiti per ogni tipo di modalità aziendale offerta dallo Store
    -   Gli account sono validi per tutte le impostazioni locali da testare oppure esistono account per ogni impostazione locale se gli account non possono attraversare le impostazioni locali
-   Determinare le impostazioni locali da testare.
-   Determinare le lingue da testare.
-   Determinare le informazioni seguenti sull'ambiente di test:

    -   Live Store che funzionano con Windows XP, Windows Vista e Windows 7
    -   Archivio non live da testare
    -   Verificare che l'archivio non live da testare sia visibile in tutte le versioni del sistema operativo e in tutte le versioni Windows Media Player piattaforma.

-   Determinare le informazioni seguenti sull'archivio da testare:

    -   Nome archivio
    -   Prevista etichetta e grafica del logo della scheda dello store
    -   Lo Store è disponibile per tutte le versioni del sistema operativo?
    -   Si tratta di una nuova versione dell'archivio testato?
    -   L'archivio sotto test è un archivio di tipo 1 o di tipo 2?
    -   Il tipo di archivio è stato modificato?

-   Determinare in quali versioni e piattaforme del sistema operativo si prevede di testare l'archivio.
-   Determinare che il programma di installazione e il plug-in funzionino in tutte le versioni e le piattaforme del sistema operativo da testare.
-   Determinare se è necessario un documento di navigazione.
-   Determinare le informazioni seguenti sui supporti offerte dall'archivio:

    -   Formati
    -   È necessario un software proprietario?
    -   È necessario testare tutti i tipi di supporti o solo un subset di tipi di supporti?

-   Determinare le informazioni seguenti sui diritti di utilizzo dei supporti:

    -   I supporti dello Store hanno la protezione del contenuto?
    -   In tal caso, determinare il tipo di protezione del contenuto del supporto.
    -   In tal caso, determinare il comportamento protetto previsto.
    -   I diritti di utilizzo dei supporti includono la condivisione da computer a computer?
    -   Diritti di sincronizzazione
    -   Diritti di masterizzazione
    -   Diritti di riproduzione
    -   Date di scadenza, se presenti

-   Determinare se si dispone di supporti sufficienti (un catalogo sufficientemente grande) per fornire un esempio significativo.
-   Determinare il passaggio di fase: RC 0, conformità e così via.
-   Determinare se il test superato è un determinato tipo: regressione, fumata e così via.

## <a name="test-environment"></a>Ambiente di test

È necessario eseguire test sulle configurazioni seguenti:

-   Microsoft Windows Media Player 11 in Windows XP con sistemi operativi a 3 e 64 bit Service Pack 3 (SP3)
-   Windows Media Player 11 nei sistemi operativi Windows Vista a 32 e 64 bit (Windows Media Player) a 32 bit
-   Microsoft Windows Media Player 12 nei Windows a 7 sistemi operativi a 32 e 64 bit (Windows Media Player) a 32 bit

Anche se è necessario eseguire test su tutte le versioni e le piattaforme del sistema operativo elencate, le versioni a 32 bit di Windows Vista e Windows 7 sono le versioni del sistema operativo di destinazione prioritarie. È necessario testare l'installazione di qualsiasi software in tutte le piattaforme.

Le schermate in questo argomento usano un archivio fittizio, Proseware, per illustrare l'utilizzo dell'interfaccia utente.

## <a name="configuration-and-setup"></a>Installazione e configurazione

Le sezioni seguenti descrivono come configurare e configurare i test di convalida per l'on-board di un negozio online di tipo 2.

### <a name="setting-up-a-test-machine"></a>Configurazione di un computer di test

Per configurare un computer di test, seguire questa procedura:

1.  Puntare il computer di test ai server di test del contenuto aggiungendo una chiave del Registro di sistema specifica dell'archivio.
2.  Impostare i valori nella **finestra di dialogo Opzioni internazionali** e della lingua sulle impostazioni della lingua e delle impostazioni locali appropriate. Per impostare la lingua, selezionare la **scheda Formati** e quindi selezionare la lingua dalla **casella combinata Formato** corrente. Per impostare l'area, selezionare la **scheda** Località e quindi selezionare l'area dalla **casella combinata Posizione** corrente. Inoltre, per gli archivi che richiedono l'installazione di un plug-in o software personalizzato specifico dell'archivio, potrebbe essere necessario modificare le impostazioni locali del sistema nella lingua delle impostazioni locali dello store per facilitare l'installazione. Il programma di installazione software deve supportare sia caratteri a byte singolo che doppio e deve essere eseguito in qualsiasi impostazione locale. È necessario eseguire il test nelle impostazioni locali native. Per impostare le impostazioni  locali native, aprire la  finestra di dialogo Area e lingua, selezionare la scheda Amministrazione e quindi fare clic sul pulsante Cambia impostazioni locali **di** sistema, come illustrato nello screenshot seguente. Facendo clic su questo pulsante viene **visualizzata la finestra di dialogo Area Impostazioni** lingua. La **casella combinata Impostazioni locali del sistema** correnti in tale finestra di dialogo modifica le impostazioni locali del sistema.

    Le schermate seguenti mostrano le schede in cui è possibile impostare l'area e la lingua:

    ![Screenshot della finestra di dialogo Opzioni internazionali e della lingua](images/reg-lang-opt.png)

    ![Screenshot che illustra come modificare le impostazioni locali correnti del sistema](images/reg-lang-settings.png)

3.  Disattivare la visualizzazione del Centro informazioni di un negozio impostando Windows Media Player per riprodurre una visualizzazione. La differenza principale tra le piattaforme è che in Windows Media Player 11 si inizia facendo clic su Ora in riproduzione **,** mentre in Windows Media Player 12 si inizia facendo clic con il pulsante destro del mouse sulla finestra principale.

    Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione Windows Media Player 11:

    ![Screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 11](images/wmp11-visual.png)

    Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione Windows Media Player 12:

    ![Screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configurazione di uno Store

Prima di tutto, eseguire la procedura seguente per configurare un negozio e quindi seguire i passaggi iniziali per verificare la configurazione del negozio:

1.  Avviare Windows Media Player e attendere alcuni secondi per acquisire il file di AllServices.xml più recente.
2.  Per Windows XP e Windows Vista, per selezionare un negozio online, fare prima clic sulla scheda suddivisa tra la visualizzazione Guida multimediale e la visualizzazione Negozi online. Scegliere quindi Sfoglia tutti **i Negozi online** dal menu e selezionare il negozio facendo clic sulla relativa icona nell'elenco dei negozi. Per Windows 7, fare clic sul pulsante nel riquadro di spostamento della libreria suddiviso tra il pulsante **Media Guide** (Guida multimediale) e il pulsante Online **Stores (Negozi** online). Scegliere quindi Sfoglia tutti **i negozi online** dal menu e selezionare il negozio facendo clic sulla relativa icona nell'elenco dei negozi.

    La schermata seguente mostra come selezionare un negozio online in Windows Media Player 11:

    ![Screenshot che illustra come selezionare un negozio online in Windows Media Player 11](images/wmp11-set-store.png)

    Lo screenshot seguente illustra come selezionare un Negozio online in Windows Media Player 12:

    ![Screenshot che illustra come selezionare un negozio online in Windows Media Player 12](images/wmp12-set-store.png)

3.  Seguire le istruzioni dello Store per installare qualsiasi software aggiuntivo necessario per l'uso dello store.

**Per verificare la configurazione dell'archivio**

1.  Verificare che il software sia installato.

    Verificare che il plug-in OCX o qualsiasi altro software dallo Store scarica e installi senza errori.

2.  Verificare che il software sia disinstallato.

    Verificare che in Pannello di controllo, nell'elemento Programmi e funzionalità, il software installato  dallo store venga visualizzato nell'elenco Disinstalla o modifica programma e verificare che sia possibile disinstallarlo da questo elenco senza errori. 

3.  Verificare che il software non sia in esecuzione nell'area di notifica.

    Verificare che nessuno del software dello Store a cui sono aggiunte icone nell'area di notifica del programma (sulla barra delle applicazioni a sinistra dell'orologio) prima del consenso del cliente per scaricare il software del negozio.

    L'esperienza di base dell'archivio non deve richiedere l'installazione di software aggiuntivo. Deve essere disponibile un'esperienza multimediale di base, ad esempio i supporti di streaming. Alcuni archivi installano software aggiuntivo, ad esempio download manager per un'esperienza multimediale premier; questi archivi possono avere icone nella barra delle applicazioni se rappresentano applicazioni separate da Windows Media Player.

4.  Verificare che la scheda store funzioni.

    Verificare che la scheda store cambi per indicare l'archivio selezionato.

    Per Windows XP e Windows Vista con Windows Media Player 11, verificare che il nome e l'icona del negozio siano visibili sullo sfondo scuro Windows Media Player 11.

    Per Windows 7 con Windows Media Player 12, verificare che il nome e l'icona del negozio siano visibili nel riquadro di spostamento della libreria, nel menu di scelta rapida del selettore di servizio.

    Verificare che il negozio sia elencato nella parte superiore dell'elenco del selettore del negozio nel menu.

    > [!Note]  
    > Non sarà disponibile **l'opzione** di menu Aggiungi servizio corrente a se l'archivio di tipo 2 è l'archivio in primo piano (predefinito) per l'area.

     

    Lo screenshot seguente mostra il menu visualizzato quando si fa clic sulla scheda nell'angolo superiore destro Windows Media Player 11:

    ![Screenshot che mostra la scheda Store in Windows Media Player 11](images/wmp11-verify-store.png)

    Lo screenshot seguente mostra il menu visualizzato quando si fa clic sul pulsante di divisione nell'angolo inferiore sinistro Windows Media Player 12:

    ![Screenshot che mostra la scheda Store in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Creazione di un account

**Per verificare la configurazione dell'account**

1.  Verificare che lo Store abbia un'opzione per creare un nuovo account e quindi seguire le istruzioni dello Store per creare un nuovo account.

    Lo screenshot seguente evidenzia un pulsante Crea **nuovo account** come potrebbe essere visualizzato in Windows Media Player 11:

    ![Screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 11](images/wmp11-verify-account.png)

    Lo screenshot seguente evidenzia un pulsante Crea nuovo **account** come potrebbe essere visualizzato in Windows Media Player 12:

    ![Screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 12](images/wmp12-verify-account.png)

2.  Verificare che sia possibile accedere all'account creato.

### <a name="setting-up-credential-caching"></a>Configurazione delle credenziali Caching

Eseguire prima di tutto la procedura seguente per configurare la memorizzazione nella cache delle credenziali e quindi seguire i passaggi iniziali per verificare la configurazione della memorizzazione nella cache delle credenziali:

1.  Nella pagina di accesso immettere le credenziali e selezionare l'opzione per salvare le informazioni utente.
2.  Verificare che nella pagina di accesso sia presente una casella di controllo che consente all'utente di memorizzare le credenziali nella cache.
3.  La memorizzazione nella cache delle credenziali facoltativa è un importante punto di sicurezza. La memorizzazione automatica delle credenziali nella cache può esporre le informazioni personali degli utenti che a un computer condiviso o pubblico a loro accesso. È consigliabile proteggere le informazioni dei clienti offrendo una casella di controllo che rende facoltativa la memorizzazione nella cache.

**Per verificare la memorizzazione nella cache delle credenziali**

1.  Verificare che l'archivio abbia una casella di controllo per **l'opzione Salva informazioni utente.**

    1.  Chiudere Windows Media Player.
    2.  Riaprire Windows Media Player e provare a scaricare alcuni contenuti.

2.  Verificare che la memorizzazione delle credenziali nella cache sia presente e funzionante.

    1.  Disconnettersi dall'archivio.
    2.  Chiudere Windows Media Player.
    3.  Riaprire Windows Media Player e provare a scaricare alcuni contenuti.

3.  Verificare che all'utente siano richieste le credenziali se non sono memorizzate nella cache.

    Dopo la disconnessione e il tentativo di usare l'archivio, al cliente devono essere richieste le credenziali.

## <a name="content-acquisition"></a>Acquisizione del contenuto

Questa sezione descrive i vari modi per acquisire il contenuto e come verificare che il contenuto sia stato acquisito.

### <a name="streaming-content"></a>Streaming di contenuti

Trasmettere tutti i tipi di contenuto disponibili dallo Store. Ad esempio, trasmettere contenuti radio, video, audio e anteprime.

**Per verificare il contenuto in streaming**

1.  Verificare che tutti i tipi di flusso di contenuto disponibili.

2.  Verificare che il contenuto sia riprodotto in Windows Media Player e non in un altro lettore o controllo.

### <a name="obtaining-content"></a>Recupero di contenuto

Eseguire prima di tutto i passaggi seguenti per acquistare il contenuto e quindi eseguire i passaggi che seguono i passaggi iniziali per verificare l'acquisto e verificare che il contenuto sia stato scaricato:

1.  Avviare Windows Media Player.
2.  Accedere all'account di test.
3.  Passare al contenuto da acquistare.
4.  Seguire la procedura specifica dello Store per acquistare contenuto.

**Per verificare il contenuto acquistato e scaricato**

1.  Verificare che il prezzo calcolato sia corretto.

    Verificare che il prezzo sia corretto, soprattutto quando si acquistano più contenuti contemporaneamente, e verificare che le informazioni sul saldo dell'account vengano aggiornate correttamente dopo l'acquisto. Alcuni contenuti possono essere acquistati come singoli tracce e altri solo come album. Verificare che il prezzo dell'album non sia superiore alla somma delle singole tracce.

2.  Verificare che il contenuto acquistato sia scaricato nella raccolta.

    Al termine del download, passare al contenuto scaricato nella Windows Media Player raccolta. Il contenuto scaricato si trova nella libreria dell'utente corrente.

    -   Per Windows XP e Windows Vista con Windows Media Player 11, il contenuto scaricato viene  visualizzato nel riquadro di spostamento della raccolta, in Pivot libreria e quindi in **Musica.**
    -   Per Windows 7 con Windows Media Player 12, il contenuto scaricato nella raccolta Windows Media Player viene visualizzato nel riquadro di spostamento Windows Media Player sotto **Musica**.

3.  Verificare che i metadati siano scaricati per l'acquisto.

    Assicurarsi che le colonne seguenti siano visualizzate nella libreria Windows Media Player (aggiungerle in caso di errore):

    -   Album Artist
    -   Titolo
    -   Titolo album
    -   Provider di contenuti
    -   Genre

    Le colonne precedenti devono essere popolate. Il contenuto deve avere la grafica degli album. Tuttavia, la grafica album non è necessaria per superare i test di convalida.

4.  Verificare che i diritti di utilizzo dei supporti siano corretti per l'acquisto.

    Per ogni traccia scaricata, fare clic con il pulsante destro del mouse sulla traccia e scegliere Proprietà **e** quindi selezionare la scheda Diritti **di utilizzo** dei supporti.

    Lo Store può scegliere di proteggere il contenuto con diritti di utilizzo dei file multimediali o di non proteggere il contenuto. La **scheda Diritti di utilizzo** dei supporti riflette tale stato elencando le restrizioni o indicando che il contenuto non è protetto. L'archivio deve comunicare il piano più attuale per i diritti di utilizzo dei supporti. È necessario verificare i risultati effettivi rispetto a questo comportamento previsto.

    Le licenze con diritti multimediali devono essere pre-recapitate. Al cliente non deve essere richiesto di riprodurre il contenuto o eseguire un altro processo per ottenere la licenza. È necessario confrontare i diritti di utilizzo dei supporti specifici con ciò che lo Store ha comunicato al cliente in base alle esigenze. I diritti devono essere trasferibili ad almeno altri due computer. I clienti devono essere in grado di masterizzare e sincronizzare i propri supporti.

    Lo screenshot seguente mostra i diritti di utilizzo dei file multimediali di un file protetto:

    ![Screenshot che mostra i diritti di utilizzo dei file multimediali per un file protetto](images/media-rights-protected.png)

    Se il contenuto non è protetto, la **scheda Diritti di utilizzo** dei supporti indica questo fatto.

    Lo screenshot seguente mostra i diritti di utilizzo dei file multimediali di un file non protetto:

    ![Screenshot che mostra i diritti di utilizzo dei file multimediali per un file non protetto](images/media-rights-not-protected.png)

5.  Verificare che il contenuto acquistato sia riprodotto.

    Verificare che il contenuto scaricato sia riprodotto Windows Media Player.

    Riprodurre i contenuti acquistati dallo Store e che risiedono nella libreria locale oppure trasmettere in streaming un'anteprima.

    Seguire questa procedura per acquistare contenuto in Windows XP e Windows Vista con Windows Media Player 11:

    1.  Fare clic **sulla scheda Now Playing (Riproduzione** in esecuzione).
    2.  Nel riquadro dell'elenco posizionare il puntatore del mouse per passare il puntatore del mouse sull'album art per visualizzare il **collegamento** Acquista.
    3.  Fare clic **su Acquista**.

    Lo screenshot seguente mostra la posizione del **collegamento Acquista** in Windows Media Player 11:

    ![Screenshot che illustra come acquistare contenuto in Windows Media Player 11](images/wmp11-verify-buy-play.png)

    Seguire questa procedura per acquistare contenuto in Windows 7 con Windows Media Player 12:

    1.  In modalità libreria fare clic sulla **scheda** Riproduci.
    2.  Nella playlist, sotto l'immagine dell'album, fare clic su **Shop**

    Lo screenshot seguente illustra come acquistare contenuto in Windows Media Player 12:

    ![Screenshot che illustra come acquistare contenuto in Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  Verificare che facendo clic **su Acquista** o **Acquista si** passa al Negozio.

    Il Windows Media Player deve passare all'archivio nella visualizzazione libreria e caricare l'esperienza di acquisto dello store.

    È quindi necessario continuare ad acquistare la traccia.

7.  Verificare che dopo aver fatto **clic su Acquista** o **Acquista**, il contenuto verrà scaricato.

    Verificare che i diritti di utilizzo del contenuto multimediale siano appropriati per il contenuto acquistato e i relativi metadati e verificare che la traccia sia riprodotta. In generale, questo metodo di acquisto deve avere gli stessi risultati degli altri metodi.

### <a name="burning-content"></a>Contenuto inevaso

Eseguire prima di tutto la procedura seguente per masterizzare il contenuto acquistato (copiare il contenuto acquistato in un CD o DVD scrivibile) e quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto masterizza:

> [!Note]  
> Prima di masterizzare una traccia acquistata, annotare il numero di ustioni, in modo da poter verificare in un secondo momento se il conteggio decrementa dopo aver masterizzato la traccia.

 

1.  Fare clic sulla **scheda Masterizza**
2.  Trascinare le tracce acquistate **in Burn List**.
3.  Fare clic **sul pulsante Avvia masterizzazione.**

Lo screenshot seguente mostra **burn list** sul lato destro dello schermo e il pulsante **Start Burn** (Avvia masterizzazione) sotto **l'elenco burn** Windows Media Player 11:

![Screenshot che mostra come masterizzare il contenuto in Windows Media Player 11](images/wmp11-verify-burn.png)

Lo screenshot seguente mostra come viene visualizzato l'elenco di masterizzazione in Windows Media Player 12 dopo aver trascinato una traccia nell'elenco burn e viene visualizzato il pulsante **Avvia** masterizzazione nella parte superiore della scheda **Masterizzazione:**

![Screenshot che mostra come masterizzare il contenuto in Windows Media Player 12](images/wmp12-verify-burn.png)

**Per verificare che i contenuti acquistati possano essere acquistati**

1.  Verificare che il contenuto acquistato masterizza riproducendo il CD o IL DVD al termine della riproduzione.

2.  Verificare che il numero di ustioni sia decrementato.

    Passare alla libreria e aprire i diritti di utilizzo dei file multimediali per una traccia acquistata che era stata acquistata.

    Se il numero di volte in cui una traccia può essere sgomento è limitato, verificare che questo numero diminuisca dopo che la traccia è stata rilevata.

### <a name="transferring-content"></a>Trasferimento di contenuto

Trasferire il contenuto in un altro computer.

**Per verificare che il contenuto acquistato possa essere trasferito a un altro computer**

-   Se lo Store consente il trasferimento del contenuto a un altro computer, trasferire il contenuto ad almeno due computer.

Eseguire prima di tutto la procedura seguente per eseguire la sincronizzazione con un dispositivo e trasferire il contenuto acquistato in tale dispositivo, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto sia stato trasferito:

> [!Note]  
> Prima di trasferire una traccia acquistata, annotare il numero di sincronizzazioni in modo da poter verificare in un secondo momento se il conteggio decrementa dopo il trasferimento.

 

1.  Connessione un dispositivo con un orologio sicuro. Ad esempio, i dispositivi che usano Windows Media DRM per i dispositivi portatili, ad esempio un Media Center portatile come iRiver H10, Creative Zen e così via.
2.  Nella Windows Media Player fare clic sulla **scheda Sincronizza.**
3.  Trascinare il contenuto dalla raccolta all'area **Elenco di** sincronizzazione della **scheda Sincronizza.**
4.  Fare clic sul **pulsante Avvia sincronizzazione.**

Lo screenshot seguente mostra Track 1 nell'area **Sync list** (Elenco di sincronizzazione) e il pulsante **Start Sync** (Avvia sincronizzazione) Windows Media Player 11:

![Screenshot che mostra come trasferire il contenuto in Windows Media Player 11](images/wmp11-verify-transfer.png)

Lo screenshot seguente mostra Track 1 nell'area **Dell'elenco Sync** (Sincronizza) e il pulsante **Start Sync** (Avvia sincronizzazione) Windows Media Player 12:

![Screenshot che mostra come trasferire il contenuto in Windows Media Player 12](images/wmp12-verify-transfer.png)

**Per verificare che il contenuto acquistato possa essere trasferito a un altro dispositivo**

1.  Verificare che il contenuto acquistato sia trasferito al dispositivo riproducendo il contenuto nel dispositivo. Anche il contenuto trasferito deve avere metadati appropriati.

2.  Verificare che il numero di sincronizzazione sia decrementato.

    Passare alla libreria e aprire i diritti di utilizzo dei file multimediali per una traccia trasferita.

    Se il numero di volte in cui una traccia può essere sincronizzata è limitato, verificare che questo numero diminuisca quando la traccia viene trasferita.

## <a name="store-features"></a>Funzionalità dello Store

Le sezioni seguenti descrivono come testare le varie funzionalità di un negozio online di cui è stato fatto l'on boarded.

### <a name="managing-an-account"></a>Gestione di un account

Accedere con un account che ha effettuato alcuni acquisti e aprire la cronologia degli acquisti.

**Per verificare la cronologia degli acquisti**

-   Verificare che la cronologia degli acquisti tiene traccia degli acquisti precedenti.

Se il tipo di archivio o di account supporta questa funzionalità, provare a ripristinare un acquisto eliminato.

**Per verificare che sia possibile riacquisire gli acquisti precedenti**

-   Verificare che sia possibile ripristinare un acquisto precedente.

Se lo Store supporta l'uso di più computer con l'account, verificare le funzionalità fornite da questa funzionalità.

**Per verificare la gestione di più computer con un singolo account**

-   Verificare la funzionalità dello Store per gestire più computer.

### <a name="managing-a-store-specific-account"></a>Gestione di un Store-Specific account

Lo Store potrebbe non avere tipi di account, restrizioni o contenuti tipici. Ad esempio, un negozio che noleggia video in streaming avrebbe bisogno di un'interfaccia utente per visualizzare i noleggi attivi e tale interfaccia utente dovrà essere testata.

> [!Note]  
> Anche se Microsoft non è in grado di certificare la funzionalità dell'account specifico del negozio, per garantire un'esperienza ottimale per i clienti, è consigliabile testare tale funzionalità.

 

### <a name="managing-the-info-center"></a>Gestione del Centro informazioni

Eseguire prima di tutto i passaggi seguenti per preparare il test dello stato predefinito e quindi eseguire il passaggio successivo che segue i passaggi iniziali per verificare che l'Info Center sia disattivato per impostazione predefinita:

1.  Riprodurre contenuto dallo Store.
2.  Passare alla modalità Di riproduzione in esecuzione. In Windows XP o Windows Vista con Windows Media Player 11 fare clic sulla **scheda Ora in** riproduzione. In Windows 7 con Windows Media Player 12 fare clic  sul pulsante Passa a Riproduzione in esecuzione nell'angolo in basso a destra.

**Per verificare che l'Info Center sia disattivato per impostazione predefinita**

-   Verificare che l'Info Center sia disattivato per impostazione predefinita.

Se lo Store offre una visualizzazione Info Center, riprodurre contenuto dallo Store e, durante la riproduzione del contenuto, passare alla modalità Di riproduzione e attivare Info Center.

In Windows XP o Windows Vista con Windows Media Player 11 fare clic con il pulsante destro del mouse sulla finestra attualmente in riproduzione e quindi scegliere Visualizzazione Info Center dal menu di **scelta rapida.**

Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 11:

![Screenshot che mostra come accedere all'info center di uno store in Windows Media Player 11](images/wmp11-info-center.png)

In Windows 7 con Windows Media Player 12 fare clic con il pulsante destro del mouse sulla finestra in riproduzione, scegliere Visualizzazioni dal menu di scelta rapida e quindi fare clic su **Visualizzazione Info Center.**

Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 12:

![Screenshot che mostra come accedere all'info center di uno store in Windows Media Player 12](images/wmp12-info-center.png)

**Per verificare che l'Info Center sia funzionante**

-   Verificare che nell'Info Center siano visualizzate informazioni multimediali nell'area di riproduzione. Lo screenshot seguente mostra un esempio di tali informazioni multimediali:

    ![Screenshot che mostra la funzionalità del centro informazioni di uno store](images/media-information.png)

Se nella pagina vengono visualizzati collegamenti di acquisto o altri collegamenti, fare clic sui collegamenti.

**Per verificare i collegamenti nella visualizzazione Info Center**

-   Verificare che i collegamenti mostrino l'archivio.

    Il Windows Media Player deve passare all'archivio nella relativa libreria.

## <a name="store-interaction"></a>Interazione con l'archivio

Le sezioni seguenti descrivono come testare l'interazione tra gli altri negozi e l'archivio che si sta testando.

### <a name="yielding-to-the-active-store"></a>Cede all'archivio attivo

Passare a un archivio diverso da quello testato.

**Per verificare la ceding all'archivio attivo**

-   Verificare che l'archivio testato ceda all'archivio attivo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedire all'archivio testato di assumere la proprietà dell'archivio attivo

-   Con un altro archivio selezionato, chiudere Windows Media Player e riavviare il computer.
-   Avviare Windows Media Player.

**Per verificare che l'archivio testato non prenda il controllo**

-   Verificare che venga visualizzato l'archivio attivo più recente e che l'archivio testato non sia visualizzato.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Accesso a uno Store in High-Contrast predefinita

Abilitare prima la modalità a contrasto elevato premendo MAIUSC DI SINISTRA+ALT+STAMP e quindi eseguire la procedura seguente per verificare l'accessibilità a contrasto elevato:

**Per verificare che l'archivio sia accessibile in modalità a contrasto elevato**

1.  Verificare che l'interfaccia utente di accesso sia intatta e funzionale.
2.  Verificare che tutte le finestre e le finestre di dialogo siano visualizzate correttamente.
3.  Acquistare supporti. Verificare che i pulsanti di acquisto e download, i responsabili del download, le informazioni sui prezzi e così via siano visibili.
4.  Verificare che sia possibile trasmettere, masterizzare e sincronizzare.
5.  Cercare testo ritagliato ed elementi dell'interfaccia utente, testo non leggibile e altri difetti visibili.

### <a name="securing-a-store"></a>Protezione di uno Store

Per verificare la sicurezza dell'account, seguire questa procedura:

**Per verificare la sicurezza dell'account**

1.  Immettere le informazioni sull'account in formato non valido nella pagina e nella finestra di dialogo di accesso e verificare che l'archivio le rifiuti.
2.  Accedere, visualizzare la pagina dell'account e disconnettersi.
3.  Fare clic sul pulsante Indietro Windows Media Player e verificare che le informazioni sull'account utente precedente non siano visualizzate.

 

 




