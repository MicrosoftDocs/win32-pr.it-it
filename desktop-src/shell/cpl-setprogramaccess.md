---
description: In questo argomento viene illustrata la funzionalità set Program Access and computer Defaults (SPAD) disponibile nel pannello di controllo.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225928"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)

In questo argomento viene illustrata la funzionalità **set Program Access and computer Defaults (SPAD)** disponibile nel pannello di controllo. SPAD si trova sotto l'elemento del pannello di controllo [programmi predefiniti](default-programs.md) in Windows Vista e nelle versioni successive di Windows. In Windows XP si trova nell'elemento **Installazione applicazioni** e intitolato **Imposta accesso programma e impostazioni predefinite**.

> [!IMPORTANT]
> Questo argomento non è applicabile a Windows 10. Il modo in cui le associazioni di file predefinite cambiano in Windows 10. Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Utilizzo dello strumento imposta accesso al programma e impostazioni predefinite computer](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Panoramica dell'impostazione dell'accesso al programma e delle impostazioni predefinite del computer](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Valore del registro di sistema LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Applicazione di filtri all'elenco Installazione applicazioni](#filtering-the-add-or-remove-programs-list)
-   [Risorse aggiuntive](#filtering-the-add-or-remove-programs-list)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Utilizzo dello strumento imposta accesso al programma e impostazioni predefinite computer

> [!Note]  
> A partire da Windows 8, SPAD configura le impostazioni predefinite in base al singolo utente per l'utente corrente. Prima di Windows 8, SPAD imposta le impostazioni predefinite per computer. Quando un valore predefinito per utente non è stato ancora configurato dall'utente, il sistema chiederà di impostare un valore predefinito per singolo utente anziché eseguire il fallback per impostazione predefinita per computer. È possibile che le impostazioni predefinite per computer non siano mai state visualizzate dagli utenti di Windows Vista e Windows 7 se in precedenza erano impostate impostazioni predefinite per singolo utente, perché i valori predefiniti per singolo utente sostituiscono i valori predefiniti per computer in tali sistemi operativi.

 

In Windows XP, **impostare accesso al programma e impostazioni predefinite** è uno strumento trovato come opzione nell'elemento **Installazione applicazioni** del pannello di controllo. In Windows Vista e versioni successive si trova nell'elemento del pannello di controllo [programmi predefiniti](default-programs.md) . Per i programmi [registrati](reg-middleware-apps.md) , vengono eseguite le funzioni seguenti:

-   Consente la scelta dei programmi predefiniti per ogni tipo di client (solo fino a Windows 7).
-   Consente di controllare la visualizzazione delle icone, dei collegamenti e delle voci di menu del programma.
-   Fornisce un set di opzioni predefinite del programma preimpostato. (Solo Windows XP Service Pack 1 (SP1))

Questo strumento viene usato per i cinque tipi di client seguenti.

-   Browser
-   E-mail
-   Programma messaging istantaneo
-   Lettore multimediale
-   Macchina virtuale per Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Panoramica dell'impostazione dell'accesso al programma e delle impostazioni predefinite del computer

La pagina Windows 8 **set Program Access and computer defaults** viene visualizzata nella schermata seguente.

![screenshot della visualizzazione voce imposta accesso al programma e impostazioni predefinite computer](images/spad-initial.png)

All'utente vengono presentate tre opzioni di configurazione, con l'opzione per consentire agli OEM di presentare una quarta opzione denominata "produttore computer".

-   [Microsoft Windows](#microsoft-windows)
-   [Non Microsoft](#non-microsoft)
-   [Impostazione personalizzata](#custom)
-   [Produttore del computer](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

La configurazione di **Microsoft Windows** è costituita da un set di programmi predefiniti fornito con Windows, come illustrato nella schermata seguente.

![screenshot delle opzioni di impostazione dell'accesso al programma e delle impostazioni predefinite Microsoft](images/mspage.png)

Selezionando la configurazione di **Microsoft Windows** , è possibile visualizzare anche le icone, i collegamenti o le voci di menu per ogni programma registrato per uno dei cinque tipi di client. Le icone, i collegamenti e le voci di menu sono disponibili per l'utente nel menu **Start** o nella schermata Start, sul desktop e in tutti gli altri percorsi in cui sono stati aggiunti.

### <a name="non-microsoft"></a>Non Microsoft

La configurazione **non Microsoft** , illustrata nella schermata seguente, viene usata per le applicazioni registrate nel sistema dell'utente che non sono prodotti da Microsoft. Queste applicazioni possono essere preinstallate nel sistema dell'utente oppure possono essere applicazioni non Microsoft installate dall'utente.

> [!Note]  
> Le applicazioni devono essere registrate per essere visualizzate in questa pagina. Per istruzioni sulla registrazione di un'applicazione, vedere la pagina relativa alla [registrazione di programmi con i tipi di client](reg-middleware-apps.md).

 

![screenshot delle opzioni Imposta accesso al programma e impostazioni predefinite non Microsoft](images/nonmspage.png)

Se si seleziona l'opzione **non Microsoft** , viene rimosso anche l'accesso alle icone, ai collegamenti e alle voci di menu dei programmi Microsoft elencati nella configurazione di [Microsoft Windows](#microsoft-windows) per tutti i tipi di client che li dispongono. Le icone, i collegamenti e le voci di menu di Microsoft vengono rimossi dal menu **Start** , dal desktop e da altre posizioni in cui sono stati aggiunti.

### <a name="custom"></a>Personalizzato

La configurazione **personalizzata** , mostrata nella schermata seguente, consente agli utenti di personalizzare i propri sistemi con qualsiasi combinazione di programmi Microsoft e non Microsoft registrati come possibilità predefinite per i cinque tipi di client. Questa è l'unica tra le quattro opzioni disponibili in Windows 2000 Service Pack 3 (SP3).

![screenshot delle opzioni personalizzate di impostazione dell'accesso al programma e delle impostazioni predefinite](images/custompage.png)

Tutte le opzioni presentate nelle configurazioni [Microsoft Windows](#microsoft-windows) e [non Microsoft](#non-microsoft) sono disponibili per l'utente nella sezione **personalizzata** , oltre che in altre applicazioni Microsoft installate che non fanno parte di Windows. Il pulsante di opzione **Usa il Web browser corrente** è preselezionato, come illustrato nello screenshot precedente. Non è possibile determinare il browser predefinito corrente dall'interfaccia utente. Richiamando i collegamenti Web o i file in Windows è l'unico modo per individuare il browser predefinito corrente.

Quando un utente seleziona la casella di controllo **Abilita l'accesso al programma** per un programma, le icone, i collegamenti e le voci di menu del programma vengono visualizzati nel menu Start o nella schermata Start, sul desktop o in qualsiasi altra posizione in cui sono stati installati. Se si deseleziona questa opzione, le icone, i collegamenti e le voci di menu verranno rimossi. Tuttavia, il comportamento di queste opzioni è interamente per il fornitore dell'applicazione. Windows non controlla il modo in cui l'accesso viene abilitato o rimosso nell'interfaccia utente. È inoltre importante comprendere che le applicazioni non devono eseguire la registrazione per **impostare l'accesso al programma e le impostazioni predefinite del computer**.

### <a name="computer-manufacturer"></a>Produttore del computer

Una quarta categoria denominata "produttore computer" può essere visualizzata nella finestra SPAD in alcuni sistemi. I produttori di computer possono scegliere di preconfigurare i computer con un set personalizzato di impostazioni predefinite, scegliendo tra le stesse selezioni disponibili nella configurazione [personalizzata](#custom) . (A scopo illustrativo, un set fittizio di applicazioni denominato LitWare viene registrato per l'uso con tutti i tipi di client). Un utente può tornare alla configurazione predefinita del produttore del computer in qualsiasi momento scegliendo l'opzione **produttore computer** , come illustrato nella schermata seguente di Windows XP.

> [!Note]  
> Questa configurazione non viene visualizzata in tutti i sistemi. Per informazioni dettagliate, fare riferimento alla OEM Preinstallation Kit (OPK).

 

![screenshot delle opzioni Imposta accesso al programma e impostazioni predefinite del produttore del computer](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Valore del registro di sistema LastUserInitiatedDefaultChange

Il valore LastUserInitiatedDefaultChange è stato aggiunto al registro di sistema per aiutare le applicazioni a riconoscere e rispettare le scelte predefinite dell'utente. Il valore contiene \_ dati binari reg sotto forma di struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene la data e l'ora (in formato UTC (Coordinated Universal Time) dell'ultima volta in cui l'utente ha modificato una scelta predefinita tramite lo strumento **Imposta accesso al programma e impostazioni predefinite computer** . Questo valore si trova nella sottochiave seguente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

Lo scenario seguente utilizza questo valore per un'applicazione che monitora le associazioni di file.

1.  Un'applicazione registra internamente l'ora dell'ultimo set come programma predefinito per il tipo di client (in fase di installazione o in un secondo momento).
2.  L'applicazione rileva che il programma predefinito per il tipo di client è stato modificato in un programma diverso da se stesso o dall'applicazione che rappresenta (nel caso di programmi helper in background). Non supportato in Windows 8.
3.  L'applicazione legge il valore di LastUserInitiatedDefaultChange (il timestamp dell'Ultima modifica predefinita avviata dall'utente) e lo confronta con il valore timestamp archiviato per la propria scelta come predefinito.
4.  Se LastUserInitiatedDefaultChange è successivo al valore archiviato dell'applicazione, non deve essere eseguita alcuna azione da parte dell'applicazione perché la modifica è stata richiesta in modo esplicito dall'utente tramite lo strumento **Imposta accesso programma e impostazioni predefinite** .
5.  L'applicazione non esegue più il monitoraggio dell'associazione di file fino a quando non viene scelto di nuovo come impostazione predefinita. Non supportato in Windows 8.

Aderendo a tale schema, le richieste dell'utente vengono rispettate e la relativa proprietà finale dei sistemi viene mantenuta.

## <a name="filtering-the-add-or-remove-programs-list"></a>Applicazione di filtri all'elenco Installazione applicazioni

> [!Note]  
> Questa sezione si applica a Windows XP Service Pack 2 (SP2) e versioni successive e Windows Server 2003 e versioni successive.

 

In Windows XP e Windows Server 2003, l'elenco delle applicazioni visualizzate nella scheda **Cambia o Rimuovi programmi** in **installazione** applicazioni può essere filtrato dall'utente per escludere le voci per gli aggiornamenti dell'applicazione. In queste versioni di Windows, questa operazione viene eseguita tramite una casella di controllo **Mostra aggiornamenti** nella parte superiore della finestra. Per impostazione predefinita, l'opzione **Mostra aggiornamenti** non è selezionata, quindi gli aggiornamenti non vengono visualizzati, a meno che l'utente *non* scelga di visualizzarli. Le modifiche apportate allo stato della casella di controllo vengono mantenute quando si chiude **Installazione applicazioni** . Se un utente sceglie di visualizzare gli aggiornamenti, continuerà a essere visualizzato fino a quando l'utente non cancella la casella di controllo.

> [!Note]  
> L'aggiornamento di Windows XP SP2 è un'eccezione al filtro. Viene sempre visualizzata indipendentemente dallo stato della casella di controllo.

 

In Windows Vista e versioni successive, gli aggiornamenti dell'applicazione vengono visualizzati in una pagina separata nel pannello di controllo dedicata solo agli aggiornamenti. Questa pagina viene visualizzata quando l'utente fa clic sul collegamento **Visualizza aggiornamenti installati** . Non è disponibile alcuna opzione selezionabile dall'utente per visualizzare gli aggiornamenti nella stessa pagina dei programmi installati. Nonostante la modifica dell'interfaccia utente, il meccanismo per la registrazione come aggiornamento a un programma installato rimane invariato rispetto alle versioni precedenti di Windows.

Le applicazioni Microsoft e non Microsoft che usano il Windows Installer non devono eseguire altre operazioni perché gli aggiornamenti vengano riconosciuti come aggiornamenti. Le applicazioni non Microsoft che non utilizzano Windows Installer devono dichiarare determinati valori nel registro di sistema come parte dell'installazione per essere riconosciuti come aggiornamento a un programma esistente.

Nell'esempio seguente vengono illustrati i valori del registro di sistema da dichiarare affinché un'installazione venga riconosciuta come aggiornamento a un programma esistente.

1.  L'applicazione padre deve aggiungere le informazioni di disinstallazione in una sottochiave nella sottochiave **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall** . Per ulteriori informazioni sull'utilizzo della sottochiave **Uninstall** , vedere l'argomento relativo all' [installazione](/previous-versions/ms997548(v=msdn.10)) .
2.  Ogni aggiornamento a tale applicazione padre deve anche aggiungere le informazioni come sottochiave della sottochiave di **disinstallazione** . Deve usare una convenzione di denominazione specifica, tentando di evitare potenziali conflitti con altri programmi. Le convenzioni seguenti sono riservate come nomi di sottochiavi da Microsoft per l'uso con gli aggiornamenti di Windows.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguito da sei cifre, ad esempio "KB123456"
    -   "Q" seguito da sei cifre, ad esempio "Q123456"
    -   Sei cifre, ad esempio "123456"
3.  Oltre alle informazioni di disinstallazione standard aggiunte per l'applicazione padre, le sottochiavi per ogni aggiornamento devono includere anche due delle tre voci seguenti. I relativi valori sono di tipo REG \_ SZ.
    -   **ParentKeyName**. Questo valore è obbligatorio. Si tratta del nome della sottochiave dell'elemento padre dichiarata nel passaggio 1. L'aggiornamento viene associato al programma.
    -   **ParentDisplayName**. Questo valore è obbligatorio. Se nessuna sottochiave corrisponde a quella denominata in ParentKeyName, questo valore viene usato come programma padre segnaposto da visualizzare in **Installazione applicazioni**.
    -   **InstallDate**. Questo valore è facoltativo. Deve usare il modulo `yyyymmdd` per specificare la data. Questa data viene utilizzata per le informazioni **installate** in visualizzate accanto alla voce dell'aggiornamento nell'interfaccia utente. Se non è presente alcuna voce **InstallDate** o se è presente, ma non è stato assegnato alcun valore, si verifica quanto segue:
        -   Versioni del sistema operativo diverse da Windows Vista e Windows 7: non vengono visualizzate le informazioni **installate** .
        -   Windows Vista e versioni successive: viene utilizzata una data predefinita. Si tratta della data dell'Ultima modifica per qualsiasi voce sotto la sottochiave dell'aggiornamento. Questo è in genere il giorno in cui l'aggiornamento è stato aggiunto al registro di sistema. Tuttavia, poiché si tratta di una data dell'Ultima modifica, qualsiasi modifica successiva a una delle voci della sottochiave fa sì che il valore InstallDate venga modificato in una data di tale modifica.

Nell'esempio seguente vengono illustrate le voci del registro di sistema pertinenti per un aggiornamento all'applicazione LitWare Deluxe.

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

Le applicazioni non Microsoft che non forniscono le informazioni del registro di sistema appropriate, ad esempio gli aggiornamenti prodotti prima che questa opzione fosse disponibile, continueranno a essere visualizzate normalmente nell'elenco dei programmi installati e non verranno esclusi.

Il filtro degli aggiornamenti nelle versioni del sistema operativo diverse da Windows Vista e Windows 7 è in genere un'impostazione controllata dall'utente e deve essere rispettato dalle applicazioni. Tuttavia, in un ambiente aziendale gli amministratori possono controllare se gli utenti hanno la possibilità di filtrare gli aggiornamenti tramite il valore del registro di sistema DontGroupPatches, come illustrato nell'esempio seguente.

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

Questo valore è di tipo REG \_ DWORD ed è interpretato nel modo seguente.



| Valore DontGroupPatches             | Significato                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | La casella di controllo **Mostra aggiornamenti** viene visualizzata all'utente. Il filtro varia a seconda che l'utente abbia o meno selezionato questa casella.                                                                                         |
| 1                                  | La casella di controllo **Mostra aggiornamenti** viene rimossa dall'interfaccia utente. Gli aggiornamenti non vengono filtrati dall'elenco. Questo valore essenzialmente ripristina il comportamento di Windows XP SP1, prima dell'introduzione della funzionalità **Mostra aggiornamenti** . |
| Voce DontGroupPatches non presente | Equivale a impostare il valore su 0.                                                                                                                                                                       |



 

DontGroupPatches non ha alcun effetto in Windows Vista e Windows 7, dove l'interfaccia utente non contiene alcuna casella di controllo e gli aggiornamenti registrati sono sempre filtrati.

> [!Note]  
> I criteri vengono impostati solo dagli amministratori. Le applicazioni non devono modificare questo valore. Per ulteriori informazioni su come impostare un Criteri di gruppo basato sul Registro di sistema, vedere [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page) o [Windows Server criteri di gruppo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Registrazione di programmi con tipi di client](reg-middleware-apps.md)
-   [Installazione](/previous-versions/ms997548(v=msdn.10))
-   [Configurazione di installazione applicazioni con Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione di file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> </dl>

 

 
