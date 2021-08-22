---
title: Windows Games Explorer per sviluppatori di giochi
description: Questo articolo illustra il processo di registrazione di un gioco con Games Explorer e controllo genitori in Windows Vista e Windows 7 usando il nuovo schema GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6420b4783cfad7afd82483d45448ccb219342b4a7b88aa54e36c2de15ca0f778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070421"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows Games Explorer per sviluppatori di giochi

Windows Vista migliora l'esperienza utente dei giochi in Windows includendo Games Explorer. Games Explorer viene esposto nel menu Start di Windows Vista come cartella Giochi e offre una posizione centrale per l'accesso ai giochi.

A partire dalla versione di marzo 2009 di DirectX SDK, viene usato un nuovo schema GDF (Game Definition File) per supportare le funzionalità di Windows 7, Game Provider e feed RSS e IGameExplorer2. IGameExplorer2 è una nuova interfaccia Windows 7 che semplifica il processo di integrazione di un gioco con Games Explorer.

Questo articolo illustra il processo di registrazione di un gioco con Games Explorer e controllo genitori in Windows Vista e Windows 7 usando il nuovo schema GDF.

Contenuto:

-   [Prerequisiti](#prerequisites)
-   [Integrazione con un programma di installazione](#integrating-with-an-installer)
-   [Processo di integrazione](#integration-process)
-   [Games Explorer attività](#games-explorer-tasks)
-   [Integrazione in InstallScript](#integrating-into-installscript)
-   [Integrazione in un pacchetto MSI](#integrating-into-an-msi-package)
-   [Debug Suggerimenti](#debugging-tips)
    -   [Eseguire test con codice di esempio](#test-with-sample-code)
    -   [Assicurarsi che il gioco sia stato rimosso correttamente](#make-sure-that-your-game-was-removed-properly)
    -   [Assicurarsi di firmare con Authenticode](#be-sure-to-sign-using-authenticode)
    -   [Assicurarsi che il controllo genitori sia disponibile](#be-sure-that-parental-controls-are-available)
    -   [Verificare che le attività siano del tipo corretto](#verify-that-tasks-are-of-the-correct-type)
    -   [Verificare i dati nel file binario GDF](#verify-the-data-in-gdf-binary)
-   [Summary](#summary)

## <a name="prerequisites"></a>Prerequisiti

Prima di poter integrare un gioco in Games Explorer, è necessario creare un file di definizione del gioco (GDF). Una funzione definita dall'utente è un file XML che contiene metadati che descrivono il gioco. Nella versione di marzo 2009 di DirectX SDK è stata aggiunta una sezione per il provider di giochi, il feed RSS e l'attività di gioco allo schema GDF. Per usare le istruzioni contenute in questo articolo, è necessario usare questo nuovo formato GDF per creare il file GDF.

Microsoft offre uno strumento per la creazione di GDF in DirectX SDK, Game Definition File Editor, per semplificare questo processo di creazione. Questo strumento consente anche di creare versioni localizzate di una funzione definita dall'utente.

Una volta creato e localizzato, una funzione GDF deve essere incapsulata all'interno di una sezione di risorse di un file binario (eseguibile o DLL), insieme all'anteprima e all'icona del gioco. La funzione definita dall'utente contiene tutti i metadati associati al gioco, inclusa la classificazione del gioco. Windows Controllo genitori usa la classificazione del gioco per consentire ai genitori di controllare l'accesso al gioco. Il file binario che contiene la funzione definita dall'utente deve essere firmato digitalmente con un certificato Authenticode valido. in caso contrario, Games Explorer e il sistema di controllo genitori ignorano la classificazione del gioco, perché le informazioni sulla classificazione non possono essere attendibili senza certificazione. Per altre informazioni sulla firma del codice con Authenticode, vedere [Firma Authenticode per sviluppatori di giochi.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

## <a name="integrating-with-an-installer"></a>Integrazione con un programma di installazione

Per semplificare Games Explorer integrazione, l'esempio GameUXInstallHelper fornisce un'API comune che può essere chiamata in Windows XP, Windows Vista e Windows 7. È progettato per l'uso con script per InstallShield e Wise Installation System, nonché azioni personalizzate msi e strumenti di installazione personalizzati. Il rilevamento del sistema operativo viene gestito all'interno di questa DLL di esempio, pertanto il chiamante non deve preoccuparsi se il client esegue Windows XP, Windows Vista o Windows 7.

Le funzioni esportate da questa DLL sono le seguenti:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registra un gioco con Games Explorer, dato un percorso al file binario GDF, un percorso completo della cartella in cui è installato il gioco e l'ambito di installazione.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registra un gioco con Games Explorer; Versione ANSI di **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Rimuove un gioco dalla registrazione con Games Explorer, dato un percorso al file binario GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Rimuove un gioco dalla registrazione con Games Explorer; Versione ANSI di **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configura le proprietà CustomActionData per le azioni di un'installazione personalizzata posticipata dell'msi. L'utilizzo di questa funzione è descritto in dettaglio più avanti in questo articolo.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Aggiunge un gioco a Games Explorer; da usare durante l'installazione di un'azione personalizzata msi.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Rimuovere un gioco da Games Explorer; da usare durante l'installazione di un'azione personalizzata msi.

</dd> </dl>

Queste funzioni sono illustrate ulteriormente nell'intestazione GameUXInstallHelper.h.

## <a name="integration-process"></a>Processo di integrazione

Dopo aver aggiunto la funzione GDF e i file correlati a una risorsa binaria, è possibile integrare il gioco con Games Explorer. **L'uso di GameUXInstallHelper** semplifica il processo di integrazione. Per registrare il gioco con Games Explorer, chiamare **GameExplorerInstall** con un percorso al file binario GDF, un percorso completo della cartella in cui è installato il gioco e l'ambito di installazione. Per rimuovere la registrazione del gioco, chiamare **GameExplorerUninstall** con un percorso al file binario GDF.

Si noti che il processo di rimozione rimuove solo un'installazione univoca. Se un gioco è stato installato più volte, questo processo deve essere ripetuto per ogni installazione univoca.

## <a name="games-explorer-tasks"></a>Games Explorer attività

Games Explorer attività verranno visualizzate nel menu di scelta rapida di una voce in Games Explorer. Le attività sono suddivise in attività di riproduzione e attività di supporto. Le attività di riproduzione avviano un gioco in una particolare modalità, mentre le attività di supporto servono a qualsiasi altro scopo, incluso il collegamento a siti Web.

In Windows Vista, le attività sono semplicemente collegamenti che si trovano in cartelle specifiche. Le attività di riproduzione e le attività di supporto vengono archiviate in cartelle con i nomi Corrispondenti PlayTasks e SupportTasks. GameUXInstallHelper può leggere le informazioni sulle attività del gioco dal file binario GDF e creare automaticamente tutti i collegamenti.

In Windows 7, i collegamenti alle attività non sono necessari, perché Games Explorer ottiene tutte le informazioni sull'attività direttamente dal file binario GDF.

## <a name="integrating-into-installscript"></a>Integrazione in InstallScript

Chiamare Games Explorer API da InstallScript di InstallShield è semplice usando l'esempio GameUXInstallHelper. I passaggi necessari per l'integrazione con InstallShield sono i seguenti:

1.  Aprire un progetto InstallScript nell'editor InstallShield.
2.  Aggiungere GameUXInstallHelper.dll al progetto da installare nella directory di destinazione.

    **Per aggiungere GameUXInstallHelper.dll a un progetto InstallScript:**

    1.  Nella scheda **Progettazione installazione** fare clic su **Dati applicazione** nel riquadro di spostamento a sinistra.
    2.  Fare **clic su File e** cartelle e passare alle cartelle del **computer** di origine per individuare GameUXInstallerHelper.dll nei file del computer **di origine.**

        Il percorso predefinito per GameUXInstallerHelper.dll è DirectX SDK root \\ Samples \\ C++ \\ Misc \\ Bin \\ x86.

    3.  In **Cartelle del computer di destinazione fare** clic su Cartella di destinazione **applicazione**.
    4.  Trascinare GameUXInstallerHelper.dll **file del computer di origine** nei file del computer di **destinazione**.

3.  In Esplora InstallScript fare clic sul file InstallScript (in genere setup.rul) che chiama la funzione DLL.
4.  Incollare il codice InstallScript seguente nel file:

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

Di seguito è riportata una descrizione di alto livello dei passaggi necessari per chiamare le API Games Explorer tramite azioni personalizzate msi:

1.  Aggiungere una proprietà alla tabella delle proprietà MSI denominata "RelativePathToGDF" contenente il percorso relativo del file binario GDF.
2.  Dopo l'azione CostFinalize, chiamare la funzione DLL GameUXInstallHelper **SetMSIGameExplorerProperties** in un'azione personalizzata immediata per impostare le proprietà msi appropriate per le altre azioni personalizzate.
3.  Al momento dell'installazione, attivare un'azione personalizzata posticipata dopo l'azione InstallFiles che chiama la funzione DLL GameUXInstallHelper **AddToGameExplorerUsingMSI**. Se l'installazione è per tutti gli utenti, l'azione personalizzata deve impostare il flag msidbCustomActionTypeNoImpersonate; In caso contrario, non deve impostare questo flag. Di conseguenza, vengono definite due azioni personalizzate quasi identiche: GameUXAddAsAdmin e GameUXAddAsCurUser.
4.  Dopo la rimozione dell'installazione, attivare un'azione personalizzata posticipata prima dell'azione RemoveFiles che chiama la funzione DLL GameUXInstallHelper **RemoveFromGameExplorerUsingMSI**. Se l'installazione è stata eseguita per tutti gli utenti, l'azione personalizzata deve impostare il flag msidbCustomActionTypeNoImpersonate; In caso contrario, non deve impostare questo flag. Di conseguenza, vengono definite due azioni personalizzate quasi identiche: GameUXRemoveAsAdmin e GameUXRemoveAsCurUser.
5.  Definire azioni personalizzate di rollback per gestire il caso in cui l'utente annulla l'installazione o la rimozione dopo che è già stata verificata una di queste azioni personalizzate. Ciò comporta altre 4 azioni personalizzate: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin e GameUXRollBackRemoveAsCurUser.

Questa procedura viene descritta in dettaglio nelle istruzioni seguenti, che descrivono un processo che può essere eseguito usando un editor msi, ad esempio l'editor Orca disponibile in Platform SDK. Alcuni editor msi hanno procedure guidate che semplificano alcuni di questi passaggi di configurazione.

**Per configurare un pacchetto MSI per l'integrazione con Games Explorer**

1.  Aprire il pacchetto MSI in Orca.
2.  Aggiungere la riga illustrata nella tabella seguente alla **tabella Binary** nel pacchetto MSI. 

    | Nome   | Dati                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | percorso del file dll \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Questo file verrà incorporato nel pacchetto MSI, quindi è necessario eseguire questo passaggio ogni volta che si ricompila GameUXInstallHelper.dll.

     

3.  Aggiungere le righe illustrate nella tabella seguente alla **tabella CustomAction** nel pacchetto MSI.

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

    

     

4.  Aggiungere i valori visualizzati per Azione, Condizione e Sequenza nella tabella seguente alla **tabella InstallExecuteSequence** nel pacchetto MSI.

    | Azione                        | Condition                      | Sequenza | Note                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | Il numero di sequenza inserisce l'azione subito dopo CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NON installato E ALLUSERS     | 4003     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione per tutti gli utenti. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo i rollback.                                 |
    | GameUXAddAsCurUser            | NON installato E NON ALLUSERS | 4004     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione solo per l'utente corrente. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo i rollback.                     |
    | GameUXRollBackAddAsAdmin      | NON installato E ALLUSERS     | 4001     | Questa azione personalizzata verrà eseguita solo quando viene annullata una nuova installazione per tutti gli utenti. Il numero di sequenza inserisce l'azione dopo InstallFiles e prima dell'azione Aggiungi personalizzata.             |
    | GameUXRollBackAddAsCurUser    | NON installato E NON ALLUSERS | 4002     | Questa azione personalizzata verrà eseguita solo quando viene annullata una nuova installazione solo per l'utente corrente. Il numero di sequenza inserisce l'azione dopo InstallFiles e prima dell'azione Aggiungi personalizzata. |
    | GameUXRemoveAsAdmin           | REMOVE~="ALL" E ALLUSERS     | 3452     | Questa azione personalizzata verrà eseguita solo durante la rimozione per tutti gli utenti. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                                     |
    | GameUXRemoveAsCurUser         | REMOVE~="ALL" E NON ALLUSERS | 3453     | Questa azione personalizzata verrà eseguita solo durante la rimozione per l'utente corrente. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                              |
    | GameUXRollBackRemoveAsAdmin   | REMOVE~="ALL" E ALLUSERS     | 3450     | Questa azione personalizzata verrà eseguita solo quando la rimozione per tutti gli utenti viene annullata. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e prima dell'azione personalizzata Remove.              |
    | GameUXRollBackRemoveAsCurUser | REMOVE~="ALL" E NON ALLUSERS | 3451     | Questa azione personalizzata verrà eseguita solo quando la rimozione per l'utente corrente viene annullata. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e prima dell'azione personalizzata Remove.       |

    

     

5.  Aggiungere la riga illustrata nella tabella seguente alla tabella Property nel pacchetto MSI.

    | Proprietà          | Valore                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | nome del percorso \\ file relativo del file binario che contiene la funzione definita dall'utente |

    

     

    > [!Note]  
    > Il percorso specificato dal percorso è relativo al percorso specificato dal percorso di installazione. Ad esempio, bin \\GDF.dll.

     

6.  Salvare il pacchetto MSI.

Per informazioni più dettagliate sui pacchetti MSI e sul programma Windows, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Debug Suggerimenti

Di seguito sono riportati alcuni suggerimenti che consentono di eseguire il debug dei problemi durante la chiamata Games Explorer API:

### <a name="test-with-sample-code"></a>Eseguire test con codice di esempio

La compilazione della soluzione di esempio GameUXInstallHelper creerà un GameUXInstallHelper.dll e un GDFInstall.exe. Il GDFInstall.exe è un'applicazione di esempio che usa GameUXInstallHelper.dll. Eseguendo GDFInstall.exe verrà richiesto se si vuole installare o rimuovere un file binario GDF da Game Explorer. È possibile testare il file binario GDF passandolo come prima riga di comando arg GDFInstall.exe.

Se non si dispone di un file binario GDF o se l'installazione non riesce, provare a usare la funzione GDF di esempio in DirectX SDK. L'esempio GDFExampleBinary si trova in DirectX SDK ed è solo una DLL che contiene solo un file GDF. Nell'origine è incluso anche il progetto GDFMaker. È possibile compilarlo e testarlo usando GDFInstall.exe. È anche possibile confrontare il relativo codice XML con il proprio per individuare esattamente dove si trova il problema.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Assicurarsi che il gioco sia stato rimosso correttamente

Se il gioco è già installato in Games Explorer, le chiamate successive a **IGameExplorer::AddGame** restituiranno E FAIL, quindi assicurati che il gioco non sia installato prima del \_ test. Questo vale anche se si installa la funzione GDF solo per l'utente corrente e quindi si tenta di installare la funzione GDF per tutti gli utenti. Devi prima rimuovere il gioco dagli utenti correnti prima che **IGameExplorer::AddGame** riesca.

Se si esegue **GDFInstall.exe enum**, l'applicazione di esempio entra in una modalità diversa che enumerà tutti i giochi Games Explorer installati e chiederà di rimuoverli. È anche possibile esplorare e cercare il Registro di sistema in HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion GameUX \\ per assicurarsi che il gioco non sia installato per un altro utente nel sistema. Tuttavia, non modificare queste impostazioni del Registro di sistema per altri scopi, perché non è garantito che rimangano compatibili nelle versioni future del sistema operativo.

### <a name="be-sure-to-sign-using-authenticode"></a>Assicurarsi di eseguire l'accesso con Authenticode

Se è stata specificata una classificazione, ma non viene visualizzato in Games Explorer, assicurarsi di aver usato Authenticode per firmare il file eseguibile o dll che contiene la classificazione. Games Explorer ignora le informazioni sulle classificazioni nei file non firmati. Per altre informazioni su Authenticode, vedere [Firma Authenticode per sviluppatori di giochi.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

### <a name="be-sure-that-parental-controls-are-available"></a>Assicurarsi che i controlli genitori siano disponibili

Assicurarsi di testare il controllo genitori in un'edizione di Windows Vista che fornisce controlli genitori: Home Basic, Home Premium o Ultimate. Windows Vista Business e Windows Vista Enterprise non forniscono il controllo genitori, tuttavia se si esegue il test in Windows Vista Ultimate e il computer di test è aggiunto a un dominio, è necessario modificare un'impostazione di Criteri di gruppo per rendere visibili i controlli genitori. A tale scopo, vedere [Attività iniziali con Games Explorer](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Verificare che le attività siano del tipo corretto

Se sono state specificate attività di supporto che non vengono visualizzate Games Explorer, verificare che siano tutti collegamenti Web. Qualsiasi altra attività di collegamento deve essere creata come attività di riproduzione. Le attività sono trattate in precedenza in [questo articolo in Games Explorer attività](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Verificare i dati nel file binario GDF

GDFTrace.exe è uno strumento disponibile in DirectX SDK. È possibile eseguire GDFTrace.exe nel file binario GDF e verranno restituiti tutti i metadati GDF contenuti nel file binario per ogni linguaggio supportato per una convalida rapida. Visualizza anche eventuali avvisi relativi a informazioni mancanti o obsolete.

## <a name="summary"></a>Riepilogo

Games Explorer in Windows Vista offre un modo semplice e personalizzabile per presentare il gioco agli utenti di Windows Vista, ma richiede anche la registrazione del gioco con il sistema durante il processo di installazione. L'esempio GameUXInstallHelper semplifica notevolmente questo processo per gli sviluppatori.

 

 