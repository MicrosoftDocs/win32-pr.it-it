---
description: In questo argomento viene illustrata la funzionalità Set Program Access and Computer Defaults (SPAD) disponibile in Pannello di controllo.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978749171366e3091738ac22c78e04cd92123a75d2288f7c83200ee8532d232c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861465"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)

In questo argomento viene illustrata la funzionalità Set **Program Access and Computer Defaults (SPAD) disponibile** in Pannello di controllo. SPAD si trova sotto [l'elemento programmi](default-programs.md) Pannello di controllo in Windows Vista e versioni successive di Windows. In Windows XP, si trova nell'elemento Installazione applicazioni e intitolata Imposta accesso ai programmi **e Impostazioni predefinite.** 

> [!IMPORTANT]
> Questo argomento non si applica a Windows 10. Il funzionamento delle associazioni di file predefinite è stato modificato in Windows 10. Per altre informazioni, vedere la sezione Modifiche **alla gestione** Windows 10 app predefinite in questo [post.](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

-   [Uso dello strumento Imposta accesso ai programmi e Impostazioni predefinite computer](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Panoramica dell'impostazione dell'accesso ai programmi e delle impostazioni predefinite del computer](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Valore del Registro di sistema LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Applicazione di filtri all'elenco Installazione applicazioni](#filtering-the-add-or-remove-programs-list)
-   [Risorse aggiuntive](#filtering-the-add-or-remove-programs-list)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Uso dello strumento Imposta accesso ai programmi e Impostazioni predefinite computer

> [!Note]  
> Al Windows 8, SPAD configura le impostazioni predefinite per ogni utente per l'utente corrente. Prima di Windows 8, SPAD impostava le impostazioni predefinite per computer. Quando un'impostazione predefinita per utente non è ancora stata configurata dall'utente, il sistema chiederà di impostare un valore predefinito per utente anziché eseguire il rollback in un'impostazione predefinita per computer. È possibile che le impostazioni predefinite per computer non siano mai state viste dagli utenti in Windows Vista e Windows 7 se in precedenza erano state impostate impostazioni predefinite per utente, perché le impostazioni predefinite per utente sostituiscono le impostazioni predefinite per computer in tali sistemi operativi.

 

In Windows XP, **Impostare** l'accesso ai programmi e le impostazioni predefinite è uno strumento disponibile **Pannello di controllo'elemento** Installazione applicazioni. In Windows Vista e versioni successive, si trova [nell'elemento programmi](default-programs.md) Pannello di controllo. Per [i programmi](reg-middleware-apps.md) registrati, esegue le funzioni seguenti:

-   Consente la scelta di programmi predefiniti per ogni tipo di client (fino Windows 7).
-   Consente il controllo della visualizzazione delle icone, dei tasti di scelta rapida e delle voci di menu del programma.
-   Fornisce un set di scelte predefinite per il programma. (Windows solo XP Service Pack 1 (SP1)

Questo strumento viene usato per i cinque tipi di client seguenti.

-   Browser
-   E-mail
-   Programma di scambio istantaneo
-   Lettore multimediale
-   Macchina virtuale per Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Panoramica dell'impostazione dell'accesso ai programmi e delle impostazioni predefinite del computer

La Windows 8 **imposta l'accesso al programma** e le impostazioni predefinite del computer è illustrata nello screenshot seguente.

![Screenshot della visualizzazione delle voci impostata per l'accesso al programma e le impostazioni predefinite del computer](images/spad-initial.png)

All'utente vengono presentate tre possibili opzioni di configurazione, con l'opzione che consente agli OEM di presentare una quarta opzione intitolata "Produttore computer".

-   [Microsoft Windows](#microsoft-windows)
-   [Non Microsoft](#non-microsoft)
-   [Impostazione personalizzata](#custom)
-   [Produttore del computer](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

La **configurazione Windows** microsoft è costituita da un set di programmi predefiniti forniti con Windows, come illustrato nello screenshot seguente.

![Screenshot dell'impostazione dell'accesso al programma e delle opzioni Microsoft predefinite](images/mspage.png)

La selezione **della Windows** microsoft consente anche la visualizzazione delle icone, dei collegamenti o delle voci di menu per ogni programma registrato per uno dei cinque tipi di client. Tali icone, collegamenti e voci di menu sono disponibili per l'utente nel menu **Start** o schermata Start, sul desktop e in tutte le altre posizioni in cui sono state aggiunte.

### <a name="non-microsoft"></a>Non Microsoft

La **configurazione non Microsoft,** illustrata nello screenshot seguente, viene usata per le applicazioni registrate nel sistema dell'utente non prodotte da Microsoft. Queste applicazioni possono essere preinstallate nel sistema dell'utente oppure possono essere applicazioni non Microsoft installate dall'utente.

> [!Note]  
> Le applicazioni devono registrarsi per essere visualizzate in questa pagina. Per istruzioni sulla registrazione di un'applicazione, vedere [Registrazione di programmi con tipi di client.](reg-middleware-apps.md)

 

![screenshot dell'impostazione dell'accesso al programma e delle opzioni non Microsoft predefinite](images/nonmspage.png)

Se si **seleziona l'opzione Non Microsoft,** viene rimosso anche l'accesso alle icone, ai collegamenti e alle voci di menu dei programmi Microsoft elencati nella configurazione di [Microsoft Windows](#microsoft-windows) per tutti i tipi di client che li hanno. Queste icone, collegamenti e voci di menu Microsoft vengono rimosse dal menu **Start,** dal desktop e da altre posizioni in cui sono state aggiunte.

### <a name="custom"></a>Personalizzato

La **configurazione** personalizzata, illustrata nello screenshot seguente, consente agli utenti di personalizzare i propri sistemi con qualsiasi combinazione di programmi Microsoft e non Microsoft registrati come possibilità predefinite per i cinque tipi di client. Questa è l'unica delle quattro opzioni disponibili in Windows 2000 Service Pack 3 (SP3).

![Screenshot dell'impostazione dell'accesso al programma e delle opzioni personalizzate predefinite](images/custompage.png)

Tutte le opzioni presentate nelle [configurazioni microsoft Windows](#microsoft-windows) e [non](#non-microsoft) Microsoft  sono disponibili per l'utente nella sezione Personalizzata, nonché per tutte le applicazioni Microsoft installate che non fanno parte di Windows. Il **pulsante di opzione Usa il Web browser corrente** è preselezionato, come illustrato nello screenshot precedente. Non è possibile determinare il browser predefinito corrente dall'interfaccia utente. Richiamare collegamenti Web o file in Windows è l'unico modo per individuare il browser predefinito corrente.

Quando un utente  seleziona la casella di controllo Abilita l'accesso a questo programma per un programma, le icone, i collegamenti e le voci di menu del programma vengono visualizzate nel menu Start o nel schermata Start, sul desktop o in qualsiasi altra posizione in cui sono stati installati. La cancellazione di questa opzione dovrebbe rimuovere le icone, i collegamenti e le voci di menu, ma il comportamento di queste opzioni dipende interamente dal fornitore dell'applicazione. Windows non controlla come viene abilitato o rimosso l'accesso in tutta l'interfaccia utente. È anche importante comprendere che le applicazioni non devono registrarsi per Impostare l'accesso ai programmi e le impostazioni **predefinite del computer.**

### <a name="computer-manufacturer"></a>Produttore del computer

Nella finestra SPAD di alcuni sistemi può essere visualizzata una quarta categoria intitolata "Produttore computer". I produttori di computer possono scegliere di preconfigurare i computer con un set personalizzato di impostazioni predefinite, scegliendo tra le stesse opzioni disponibili nella [configurazione](#custom) personalizzata. A scopo illustrativo, viene registrato un set fittizio di applicazioni denominato LitWare per l'uso con tutti i tipi di client. Un utente può tornare alla configurazione predefinita del produttore  del computer in qualsiasi momento scegliendo l'opzione Produttore computer, come illustrato nella schermata Windows XP seguente.

> [!Note]  
> Questa configurazione non viene visualizzata in tutti i sistemi. Per informazioni dettagliate, vedere OEM Preinstallation Kit (OPK).

 

![Screenshot dell'impostazione dell'accesso al programma e delle opzioni predefinite del produttore del computer](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Valore del Registro di sistema LastUserInitiatedDefaultChange

Il valore LastUserInitiatedDefaultChange è stato aggiunto al Registro di sistema per aiutare le applicazioni a riconoscere e rispettare le scelte predefinite dell'utente. Il valore contiene i dati REG BINARY sotto forma di una struttura FILETIME che contiene la data e l'ora \_ (in Coordinated Universal Time [](/windows/win32/api/minwinbase/ns-minwinbase-filetime) (UTC)) dell'ultima modifica di una scelta predefinita da parte dell'utente tramite lo strumento Imposta accesso al programma e impostazioni predefinite computer.  Questo valore si trova nella sottochiave seguente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

Lo scenario seguente usa questo valore per un'applicazione che monitora le associazioni di file.

1.  Un'applicazione registra internamente l'ora dell'ultima impostazione come programma predefinito per il tipo di client (in fase di installazione o in un secondo momento).
2.  L'applicazione rileva che il programma predefinito per il relativo tipo di client è stato modificato in un programma diverso da se stesso o dall'applicazione che rappresenta (nel caso di programmi helper in background). Non supportato in Windows 8.
3.  L'applicazione legge il valore di LastUserInitiatedDefaultChange (il timestamp dell'ultima modifica predefinita avviata dall'utente) e lo confronta con il valore del timestamp archiviato per la propria scelta come predefinito.
4.  Se LastUserInitiatedDefaultChange è successivo al valore archiviato dell'applicazione, l'applicazione non deve eseguire alcuna azione perché la modifica è stata richiesta in modo esplicito dall'utente tramite lo strumento Imposta accesso al programma e impostazioni **predefinite.**
5.  L'applicazione non monitora più l'associazione di file fino a quando non viene nuovamente scelta come predefinita. Non supportato in Windows 8.

Aderendo a tale schema, i desideri dell'utente vengono rispettati e viene mantenuta la proprietà finale dei sistemi.

## <a name="filtering-the-add-or-remove-programs-list"></a>Applicazione di filtri all'elenco Installazione applicazioni

> [!Note]  
> Questa sezione si applica Windows XP Service Pack 2 (SP2) e versioni successive e Windows Server 2003 e versioni successive.

 

In Windows XP e Windows Server 2003, l'elenco di applicazioni  visualizzato nella scheda  Cambia o rimuovi programmi in Installazione applicazioni può essere filtrato dall'utente per escludere le voci per gli aggiornamenti delle applicazioni. In queste versioni di Windows questa operazione viene eseguita tramite una **casella di** controllo Mostra aggiornamenti nella parte superiore della finestra. **L'opzione Mostra** aggiornamenti non è selezionata per impostazione predefinita, quindi gli aggiornamenti non vengono *visualizzati* a meno che l'utente non scegli di mostrarli. Le modifiche apportate allo stato della casella di controllo vengono mantenute **alla chiusura di** Installazione applicazioni. Se un utente sceglie di visualizzare gli aggiornamenti, continua a essere visualizzato fino a quando l'utente non deseleziona la casella di controllo.

> [!Note]  
> Il Windows XP SP2 è un'eccezione al filtro. Viene sempre visualizzato indipendentemente dallo stato della casella di controllo.

 

In Windows Vista e versioni successive, gli aggiornamenti delle applicazioni vengono visualizzati in una pagina separata in Pannello di controllo dedicati solo agli aggiornamenti. Questa pagina viene visualizzata quando l'utente fa clic sul **collegamento Dell'attività Visualizza aggiornamenti** installati. Non è disponibile alcuna opzione selezionabile dall'utente per visualizzare gli aggiornamenti nella stessa pagina dei programmi installati. Nonostante la modifica dell'interfaccia utente, il meccanismo per la registrazione come aggiornamento a un programma installato rimane invariato rispetto alle versioni precedenti di Windows.

Le applicazioni Microsoft e non Microsoft che usano Windows Installer non devono eseguire altre attività perché gli aggiornamenti siano riconosciuti come aggiornamenti. Le applicazioni non Microsoft che non usano Windows Installer devono dichiarare determinati valori nel Registro di sistema come parte dell'installazione per essere riconosciute come aggiornamento di un programma esistente.

Nell'esempio seguente vengono illustrati i valori del Registro di sistema da dichiarare per un'installazione da riconoscere come aggiornamento di un programma esistente.

1.  L'applicazione padre deve aggiungere le informazioni di disinstallazione in una sottochiave nella sottochiave **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall.** Per altre [informazioni sull'uso](/previous-versions/ms997548(v=msdn.10)) della sottochiave Uninstall, vedere **l'argomento** Installazione.
2.  Ogni aggiornamento all'applicazione padre deve inoltre aggiungere le informazioni come sottochiave della **sottochiave Uninstall.** Deve usare una particolare convenzione di denominazione di propria scelta, nel tentativo di evitare potenziali conflitti con altri programmi. Le convenzioni seguenti sono riservate come nomi di sottochiave da Microsoft per l'uso con Windows aggiornamenti.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguito da sei cifre, ad esempio "KB123456"
    -   "Q" seguito da sei cifre, ad esempio "Q123456"
    -   Sei cifre, ad esempio "123456"
3.  Oltre alle informazioni di disinstallazione standard aggiunte per l'applicazione padre, le sottochiavi per ogni aggiornamento devono includere anche due delle tre voci seguenti. I valori sono di tipo REG \_ SZ.
    -   **ParentKeyName**. Questo valore è obbligatorio. Si tratta del nome della sottochiave dell'elemento padre dichiarata nel passaggio 1. In questo modo l'aggiornamento viene associato al programma.
    -   **ParentDisplayName**. Questo valore è obbligatorio. Se nessuna sottochiave corrisponde a quella denominata in ParentKeyName, questo valore viene utilizzato come programma padre segnaposto da visualizzare in Installazione **applicazioni**.
    -   **InstallDate**. Questo valore è facoltativo. Deve usare il modulo `yyyymmdd` per specificare la data. Questa data viene usata per **le informazioni installate** in visualizzate accanto alla voce dell'aggiornamento nell'interfaccia utente. Se non è presente **alcuna voce InstallDate** o se è presente ma non è assegnato alcun valore, si verifica quanto segue:
        -   Versioni del sistema operativo diverse Windows Vista e Windows 7: non **viene visualizzata alcuna** informazione installata in .
        -   Windows Vista e versioni successive: viene usata una data predefinita. Si tratta della data dell'ultima modifica per una delle voci nella sottochiave dell'aggiornamento. Questo è in genere il giorno in cui l'aggiornamento è stato aggiunto al Registro di sistema. Tuttavia, poiché si tratta di una data dell'ultima modifica, qualsiasi modifica successiva apportata alle voci della sottochiave determina la modifica del valore InstallDate alla data di tale modifica.

L'esempio seguente illustra le voci del Registro di sistema pertinenti per un aggiornamento dell'applicazione LitWare LitWare LitWare.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

Le applicazioni non Microsoft che non forniscono le informazioni appropriate del Registro di sistema, ad esempio gli aggiornamenti prodotti prima che questa opzione fosse disponibile, continuano a essere visualizzate normalmente nell'elenco dei programmi installati e non vengono filtrate.

Il filtro degli aggiornamenti nelle versioni del sistema operativo diverse da Windows Vista e Windows 7 è in genere un'impostazione controllata dall'utente e deve essere rispettata come tale dalle applicazioni. In un ambiente aziendale, tuttavia, gli amministratori possono controllare se agli utenti viene data la possibilità di filtrare gli aggiornamenti tramite il valore del Registro di sistema DontGroupPatches, come illustrato nell'esempio seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

Questo valore è di tipo REG \_ DWORD e viene interpretato come segue.



| Valore DontGroupPatches             | Significato                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | La **casella di controllo** Mostra aggiornamenti viene visualizzata all'utente. Il filtro dipende dal fatto che l'utente abbia selezionato o meno questa casella.                                                                                         |
| 1                                  | La **casella di controllo Mostra** aggiornamenti viene rimossa dall'interfaccia utente. Gli aggiornamenti non vengono filtrati dall'elenco. Questo valore ripristina essenzialmente il comportamento Windows XP SP1, prima dell'introduzione **della funzionalità** Mostra aggiornamenti. |
| Voce DontGroupPatches non presente | Equivale a impostare il valore su 0.                                                                                                                                                                       |



 

DontGroupPatches non ha effetto in Windows Vista e Windows 7, in cui l'interfaccia utente non contiene caselle di controllo e gli aggiornamenti registrati vengono sempre filtrati.

> [!Note]  
> I criteri vengono impostati solo dagli amministratori. Le applicazioni non devono modificare questo valore. Per altre informazioni su come impostare un'Criteri di gruppo basata sul Registro di sistema, vedere Criteri di gruppo [o](/previous-versions/windows/desktop/Policy/group-policy-start-page) Windows [Server Criteri di gruppo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Registrazione di programmi con tipi di client](reg-middleware-apps.md)
-   [Installazione](/previous-versions/ms997548(v=msdn.10))
-   [Configurazione di Installazione applicazioni con il programma Windows installazione](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione delle applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> </dl>

 

 
