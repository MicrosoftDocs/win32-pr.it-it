---
title: Esplora giochi di Windows per sviluppatori di giochi
description: Questo articolo illustra il processo di registrazione di un gioco con Esplora giochi e controlli padre in Windows Vista e Windows 7 usando il nuovo schema GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f59b90a23f407be3990a6a4e24b92d39e66852
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300106"
---
# <a name="windows-games-explorer-for-game-developers"></a>Esplora giochi di Windows per sviluppatori di giochi

Windows Vista migliora l'esperienza utente dei giochi in Windows, includendo Esplora giochi. Game Explorer viene esposto nel menu Start di Windows Vista come cartella dei giochi e fornisce una posizione centralizzata per l'accesso ai giochi.

A partire dalla versione di marzo 2009 di DirectX SDK, viene usato un nuovo schema del file di definizione del gioco (GDF) per supportare le funzionalità di Windows 7, del provider di giochi e del feed RSS e di IGameExplorer2. IGameExplorer2 è una nuova interfaccia di Windows 7 che semplifica il processo di integrazione di un gioco con Game Explorer.

Questo articolo illustra il processo di registrazione di un gioco con Esplora giochi e controlli padre in Windows Vista e Windows 7 usando il nuovo schema GDF.

Contenuto:

-   [Prerequisiti](#prerequisites)
-   [Integrazione con un programma di installazione](#integrating-with-an-installer)
-   [Processo di integrazione](#integration-process)
-   [Attività di Esplora giochi](#games-explorer-tasks)
-   [Integrazione in InstallScript](#integrating-into-installscript)
-   [Integrazione in un pacchetto MSI](#integrating-into-an-msi-package)
-   [Suggerimenti per il debug](#debugging-tips)
    -   [Eseguire il test con il codice di esempio](#test-with-sample-code)
    -   [Verificare che il gioco sia stato rimosso correttamente](#make-sure-that-your-game-was-removed-properly)
    -   [Assicurarsi di firmare con Authenticode](#be-sure-to-sign-using-authenticode)
    -   [Assicurarsi che i controlli parentali siano disponibili](#be-sure-that-parental-controls-are-available)
    -   [Verificare che le attività siano del tipo corretto](#verify-that-tasks-are-of-the-correct-type)
    -   [Verificare i dati nel file binario di GDF](#verify-the-data-in-gdf-binary)
-   [Summary](#summary)

## <a name="prerequisites"></a>Prerequisiti

Prima di poter integrare un gioco in Game Explorer, è necessario creare un file di definizione del gioco (GDF). Un oggetto GDF è un file XML che contiene i metadati che descrivono il gioco. Nella versione di marzo 2009 di DirectX SDK è stata aggiunta una sezione per il provider di giochi, il feed RSS e l'attività di gioco allo schema GDF. Per usare le istruzioni riportate in questo articolo, è necessario usare questo nuovo formato GDF per creare il file GDF.

Microsoft fornisce uno strumento per la creazione di GDFs in DirectX SDK, editor di file di definizione del gioco, per semplificare il processo di creazione. Questo strumento consente inoltre di creare versioni localizzate di un GDF.

Dopo la creazione e la localizzazione di un GDF, il file deve essere incapsulato all'interno di una sezione delle risorse di un file binario (un eseguibile o DLL), oltre all'anteprima e all'icona del gioco. Il GDF contiene tutti i metadati associati al gioco, inclusa la classificazione del gioco. I controlli padre di Windows usano la classificazione del gioco per consentire ai genitori di controllare l'accesso al gioco. Il file binario che contiene l'oggetto GDF deve essere firmato digitalmente con un certificato Authenticode valido; in caso contrario, Esplora giochi e il sistema di controllo padre ignoreranno la classificazione del gioco, perché le informazioni relative alla classificazione non possono essere considerate attendibili senza certificazione. Per altri dettagli sulla firma del codice con Authenticode, vedere [firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Integrazione con un programma di installazione

Per semplificare l'integrazione di Game Explorer, l'esempio GameUXInstallHelper fornisce un'API comune che può essere chiamata su Windows XP, Windows Vista e Windows 7. È progettato per funzionare con gli script per InstallShield e il sistema di installazione Wise, nonché per le azioni personalizzate MSI e gli strumenti di installazione personalizzati. Il rilevamento del sistema operativo viene gestito all'interno di questa DLL di esempio, pertanto il chiamante non deve preoccuparsi se il client esegue Windows XP, Windows Vista o Windows 7.

Le funzioni esportate da questa DLL sono le seguenti:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registra un gioco con Game Explorer, dato un percorso del file binario di GDF, il percorso completo della cartella in cui è installato il gioco e l'ambito di installazione.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registra un gioco con Game Explorer; Versione ANSI di **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Rimuove un gioco dalla registrazione con Game Explorer, dato un percorso al file binario di GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Rimuove un gioco dalla registrazione con Game Explorer; Versione ANSI di **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configura le proprietà CustomActionData per le azioni di un'installazione personalizzata MSI posticipata. L'utilizzo di questa funzione è descritto in dettaglio più avanti in questo articolo.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Aggiunge un gioco a Game Explorer; da usare durante un'installazione di un'azione personalizzata MSI.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Rimuovere un gioco da Game Explorer; da usare durante un'installazione di un'azione personalizzata MSI.

</dd> </dl>

Queste funzioni sono descritte ulteriormente nell'intestazione GameUXInstallHelper. h.

## <a name="integration-process"></a>Processo di integrazione

Quando il file GDF e i file correlati sono stati aggiunti a una risorsa binaria, è possibile integrare il gioco con Game Explorer. Con **GameUXInstallHelper** il processo di integrazione viene semplificato. Per registrare il gioco con Game Explorer, chiamare **GameExplorerInstall** con il percorso del file binario di GDF, il percorso completo della cartella in cui è installato il gioco e l'ambito di installazione. Per rimuovere la registrazione del gioco, chiamare **GameExplorerUninstall** con un percorso del file binario di GDF.

Si noti che il processo di rimozione rimuove solo un'installazione univoca. Se un gioco è stato installato più volte, è necessario ripetere questo processo per ogni installazione univoca.

## <a name="games-explorer-tasks"></a>Attività di Esplora giochi

Le attività di Esplora giochi verranno visualizzate nel menu di scelta rapida di un elemento in Game Explorer. Le attività sono divise in attività di riproduzione e attività di supporto. Le attività di riproduzione avviano un gioco in una modalità specifica, mentre le attività di supporto servono qualsiasi altro scopo, incluso il collegamento a siti Web.

In Windows Vista, le attività sono semplicemente collegamenti che si trovano in cartelle specifiche. Le attività di riproduzione e le attività di supporto vengono archiviate in cartelle con i nomi corrispondenti PlayTasks e SupportTasks. GameUXInstallHelper può leggere le informazioni sulle attività del gioco dal file binario di GDF e creare automaticamente tutti i tasti di scelta rapida.

In Windows 7, i collegamenti alle attività non sono necessari, perché Game Explorer Ottiene tutte le informazioni sulle attività direttamente dal file binario di GDF.

## <a name="integrating-into-installscript"></a>Integrazione in InstallScript

La chiamata di API di Esplora giochi dalla InstallScript di InstallShield è semplificata usando l'esempio GameUXInstallHelper. I passaggi necessari per l'integrazione con InstallShield sono i seguenti:

1.  Aprire un progetto InstallScript nell'editor InstallShield.
2.  Aggiungere GameUXInstallHelper.dll al progetto da installare nella directory di destinazione.

    **Per aggiungere GameUXInstallHelper.dll a un progetto InstallScript:**

    1.  Nella scheda **progettazione installazione** fare clic su **dati applicazione** nel riquadro di spostamento a sinistra.
    2.  Fare clic su **file e cartelle** e selezionare le **cartelle del computer di origine** per individuare GameUXInstallerHelper.dll nei **file del computer di origine**.

        Il percorso predefinito per GameUXInstallerHelper.dll è i campioni radice di DirectX SDK \\ \\ C++ \\ misc \\ bin \\ x86.

    3.  In **cartelle del computer di destinazione** fare clic su **cartella di destinazione dell'applicazione**.
    4.  Trascinare GameUXInstallerHelper.dll dai **file del computer di origine** ai **file del computer di destinazione**.

3.  In InstallScript Explorer fare clic sul file InstallScript (in genere Setup. rul) che chiama la funzione DLL.
4.  Incollare il InstallScript seguente nel file:

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>Integrazione in un pacchetto MSI

Di seguito è riportata una descrizione di alto livello dei passaggi necessari per chiamare le API di Esplora giochi usando le azioni personalizzate MSI:

1.  Aggiungere una proprietà alla tabella delle proprietà MSI denominata "RelativePathToGDF" contenente il percorso relativo del file binario di GDF.
2.  Dopo l'azione CostFinalize secondo, chiamare la funzione GameUXInstallHelper DLL **SetMSIGameExplorerProperties** in un'azione personalizzata immediata per impostare le proprietà MSI appropriate per le altre azioni personalizzate.
3.  Al momento dell'installazione, attivare un'azione personalizzata posticipata dopo l'azione InstallFiles che chiama la funzione DLL GameUXInstallHelper **AddToGameExplorerUsingMSI**. Se l'installazione è per tutti gli utenti, l'azione personalizzata deve impostare il flag msidbCustomActionTypeNoImpersonate; in caso contrario, non deve impostare questo flag. Sono pertanto definite due azioni personalizzate quasi identiche: GameUXAddAsAdmin e GameUXAddAsCurUser.
4.  Al momento della rimozione dell'installazione, attivare un'azione personalizzata posticipata prima dell'azione RemoveFiles che chiama la funzione DLL GameUXInstallHelper **RemoveFromGameExplorerUsingMSI**. Se l'installazione è stata eseguita per tutti gli utenti, l'azione personalizzata deve impostare il flag msidbCustomActionTypeNoImpersonate; in caso contrario, non deve impostare questo flag. Sono pertanto definite due azioni personalizzate quasi identiche: GameUXRemoveAsAdmin e GameUXRemoveAsCurUser.
5.  Definire le azioni personalizzate di rollback per gestire il caso in cui l'utente annulla l'installazione o la rimozione dopo che è già stata eseguita una delle azioni personalizzate. Ciò comporta altre 4 azioni personalizzate: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin e GameUXRollBackRemoveAsCurUser.

Questa procedura è descritta in dettaglio nelle istruzioni seguenti, che descrivono un processo che può essere eseguito usando un editor MSI, ad esempio l'editor ORCA disponibile in Platform SDK. Alcuni editor MSI hanno procedure guidate che semplificano alcuni di questi passaggi di configurazione.

**Per configurare un pacchetto MSI per l'integrazione con Game Explorer**

1.  Aprire il pacchetto MSI in Orca.
2.  Aggiungere la riga illustrata nella tabella seguente alla tabella **binaria** nel pacchetto MSI. 

    | Nome   | Data                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | percorso del file della DLL \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Questo file verrà incorporato nel pacchetto MSI, pertanto è necessario eseguire questo passaggio ogni volta che si ricompila GameUXInstallHelper.dll.

     

3.  Aggiungere le righe mostrate nella tabella seguente alla tabella **CustomAction** del pacchetto MSI.

    | Azione                        | Tipo                                                                                                                                                                                                   | Source (Sorgente) | Destinazione                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  Aggiungere i valori visualizzati per Action, Condition e Sequence nella tabella seguente alla tabella **InstallExecuteSequence** del pacchetto MSI.

    | Azione                        | Condizione                      | Sequenza | Note                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | Il numero di sequenza inserisce l'azione subito dopo CostFinalize secondo.                                                                                                                                   |
    | GameUXAddAsAdmin              | NON installato e ALLUSERS     | 4003     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione per tutti gli utenti. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo il rollback.                                 |
    | GameUXAddAsCurUser            | NON installato e non ALLUSERS | 4004     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione solo per l'utente corrente. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo il rollback.                     |
    | GameUXRollBackAddAsAdmin      | NON installato e ALLUSERS     | 4001     | Questa azione personalizzata verrà eseguita solo quando viene annullata una nuova installazione per tutti gli utenti. Il numero di sequenza inserisce l'azione dopo InstallFiles e prima dell'azione personalizzata Aggiungi.             |
    | GameUXRollBackAddAsCurUser    | NON installato e non ALLUSERS | 4002     | Questa azione personalizzata verrà eseguita solo quando viene annullata una nuova installazione per l'utente corrente. Il numero di sequenza inserisce l'azione dopo InstallFiles e prima dell'azione personalizzata Aggiungi. |
    | GameUXRemoveAsAdmin           | REMOVE ~ = "ALL" E ALLUSERS     | 3452     | Questa azione personalizzata verrà eseguita solo durante la rimozione di tutti gli utenti. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                                     |
    | GameUXRemoveAsCurUser         | REMOVE ~ = "ALL" E NON ALLUSERS | 3453     | Questa azione personalizzata verrà eseguita solo durante la rimozione dell'utente corrente. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                              |
    | GameUXRollBackRemoveAsAdmin   | REMOVE ~ = "ALL" E ALLUSERS     | 3450     | Questa azione personalizzata verrà eseguita solo quando viene annullata la rimozione per tutti gli utenti. Il numero di sequenza posiziona l'azione immediatamente prima di RemoveFiles e prima dell'azione personalizzata Rimuovi.              |
    | GameUXRollBackRemoveAsCurUser | REMOVE ~ = "ALL" E NON ALLUSERS | 3451     | Questa azione personalizzata verrà eseguita solo quando viene annullata la rimozione per l'utente corrente. Il numero di sequenza posiziona l'azione immediatamente prima di RemoveFiles e prima dell'azione personalizzata Rimuovi.       |

    

     

5.  Aggiungere la riga illustrata nella tabella seguente alla tabella delle proprietà nel pacchetto MSI.

    | Proprietà          | Valore                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | nome del percorso file relativo \\ del file binario che contiene l'oggetto GDF |

    

     

    > [!Note]  
    > Il percorso specificato dal percorso è relativo alla posizione specificata dal percorso di installazione. Ad esempio, bin \\GDF.dll.

     

6.  Salvare il pacchetto MSI.

Per informazioni più dettagliate sui pacchetti MSI e Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Suggerimenti per il debug

Di seguito sono riportati alcuni suggerimenti per facilitare il debug dei problemi quando si chiamano le API di Esplora giochi:

### <a name="test-with-sample-code"></a>Eseguire il test con il codice di esempio

La compilazione della soluzione di esempio GameUXInstallHelper creerà un GameUXInstallHelper.dll e una GDFInstall.exe. Il GDFInstall.exe è un'applicazione di esempio che usa GameUXInstallHelper.dll. In esecuzione GDFInstall.exe verrà chiesto se si vuole installare o rimuovere un file binario di GDF da Game Explorer. È possibile testare il file binario di GDF passandolo come prima riga di comando ARG per GDFInstall.exe.

Se non si dispone di un file binario di GDF o l'installazione non riesce, provare a usare l'esempio GDF in DirectX SDK. L'esempio GDFExampleBinary è disponibile in DirectX SDK ed è solo una DLL che contiene solo un file GDF. Il progetto GDFMaker è incluso anche nell'origine. È possibile compilarlo e testarlo utilizzando GDFInstall.exe. È anche possibile confrontare il relativo codice XML con il proprio per individuare esattamente il punto in cui si verifica il problema.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Verificare che il gioco sia stato rimosso correttamente

Se il gioco è già installato in Games Explorer, le successive chiamate a **IGameExplorer:: AddGame** restituiranno E \_ non riusciranno quindi assicurarsi che il gioco non venga installato prima del test. Questo vale anche se si installa il GDF solo per l'utente corrente e quindi si prova a installare il GDF per tutti gli utenti. È necessario prima rimuovere il gioco dagli utenti correnti prima che **IGameExplorer:: AddGame** abbia esito positivo.

Se si esegue **GDFInstall.exe enum**, l'applicazione di esempio entrerà in una modalità diversa che enumera tutti i giochi di Esplora giochi installati e richiede di rimuoverli. È anche possibile cercare nel registro di \_ sistema HKEY LOCAL \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ GameUX per verificare che il gioco non sia installato per un altro utente nel sistema. Tuttavia, non modificare queste impostazioni del registro di sistema per altri scopi, poiché non è garantito che rimangano compatibili nelle versioni future del sistema operativo.

### <a name="be-sure-to-sign-using-authenticode"></a>Assicurarsi di firmare con Authenticode

Se è stata specificata una classificazione, ma non viene visualizzato in Games Explorer, assicurarsi di aver usato Authenticode per firmare il file eseguibile o DLL che contiene la classificazione. Esplora giochi ignora le informazioni sulle classificazioni nei file non firmati. Per ulteriori informazioni su Authenticode, vedere [firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Assicurarsi che i controlli parentali siano disponibili

Assicurarsi di eseguire il test dei controlli padre in un'edizione di Windows Vista che fornisce controlli padre: Home Basic, Home Premium o Ultimate. Windows Vista Business e Windows Vista Enterprise non forniscono controlli padre. Tuttavia, se si esegue il test in Windows Vista Ultimate e il computer di test è aggiunto a un dominio, è necessario modificare un'impostazione di criteri di gruppo rendere visibili i controlli padre. Per eseguire questa operazione, vedere [Introduzione con Game Explorer](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Verificare che le attività siano del tipo corretto

Se sono state specificate attività di supporto che non vengono visualizzate in Game Explorer, verificare che siano tutti collegamenti Web. Qualsiasi altra attività di collegamento deve essere creata come attività di riproduzione. Le attività sono descritte in precedenza in questo articolo nelle [attività di Esplora giochi](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Verificare i dati nel file binario di GDF

GDFTrace.exe è uno strumento disponibile in DirectX SDK. È possibile eseguire GDFTrace.exe nel file binario di GDF e tutti i metadati GDF contenuti nel file binario vengono restituiti per ogni lingua supportata per la convalida rapida. Vengono inoltre visualizzati gli avvisi relativi a informazioni mancanti o obsolete.

## <a name="summary"></a>Riepilogo

Esplora giochi in Windows Vista offre un modo semplice e personalizzabile per presentare il gioco agli utenti di Windows Vista, ma richiede anche di registrare il gioco con il sistema durante il processo di installazione. L'esempio GameUXInstallHelper semplifica notevolmente questo processo per gli sviluppatori.

 

 