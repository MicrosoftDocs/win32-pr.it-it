---
title: Distribuzione di Direct3D 11 per sviluppatori di giochi
description: Questo articolo descrive come distribuire i componenti di Direct3D 11 in un sistema, se necessario.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223988"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Distribuzione di Direct3D 11 per sviluppatori di giochi

Questo articolo descrive come distribuire i componenti di Direct3D 11 in un sistema, se necessario.

-   [Overview](#overview)
-   [Direct3D 11,3](#direct3d-113)
-   [Direct3D 11,2](#direct3d-112)
-   [Direct3D 11,1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Integrazione nei programmi di installazione](#integrating-into-installation-programs)
    -   [Integrazione in InstallShield](#integrating-into-installshield)
    -   [Integrazione in un pacchetto MSI](#integrating-into-an-msi-package)
-   [Suggerimenti per il debug](#debugging-tips)
-   [Impostazioni aziendali](#corporate-settings)
-   [Articoli correlati](#related-articles)

## <a name="overview"></a>Panoramica

L'API Direct3D 11 estende l'API Direct3D 10,1 esistente con supporto per il rendering multithreading e la creazione di risorse, compute shader, schema a mosaico hardware, compressione della trama BC6H/BC7 e HLSL Shader Model 5,0 con collegamento dinamico dello shader. Oltre al componente Direct3D 11, nel runtime di DirectX 11 sono inclusi numerosi componenti grafici aggiuntivi: Direct3D 11, DXGI 1,1, livelli di funzionalità 10level9, WARP10 software rendering device, Direct2D, DirectWrite e una versione aggiornata di Direct3D 10,1 con supporto per 10level9 e WARP10. Per informazioni su questi e altri componenti grafici di Windows, vedere [API grafiche in Windows](graphics-apis-in-windows-vista.md).

Tutti questi nuovi componenti grafici sono incorporati nei sistemi operativi Windows 7 e Windows Server 2008 R2. L'API Direct3D 11 e i componenti correlati possono anche essere installati in Windows Vista tramite un aggiornamento del sistema da Windows Update; vedere l'articolo della Knowledge base [KB 971644](https://support.microsoft.com/kb/971644). Questo aggiornamento richiede Windows Vista e Service Pack 2. Gli utenti finali con aggiornamenti automatici abilitati avranno probabilmente già installato i componenti di Direct3D 11, così come tutti gli utenti di Windows 7.

L'esempio D3D11InstallHelper è progettato per semplificare il rilevamento dell'API Direct3D 11, installare automaticamente l'aggiornamento del sistema, se applicabile a un computer dell'utente finale, e fornire messaggi appropriati all'utente finale nella procedura manuale se è necessario un Service Pack più recente.

> [!Note]  
> Il compilatore HLSL (D3DCompile \* . dll) e la libreria di utilità D3DX per Direct3D 11 (D3DX11 \* . dll) non sono incorporati in alcuna versione del sistema operativo Windows, ma possono essere distribuiti come parte del programma di installazione di un'applicazione utilizzando la tecnologia DirectSetup esistente. per ulteriori informazioni sull'utilizzo di DirectSetup, vedere [installazione di DirectX per sviluppatori di giochi](/windows/desktop/DxTechArts/directx-setup-for-game-developers). "Effects 11" è disponibile come libreria di supporto per le origini condivise a [effetti per l'aggiornamento di Direct3D 11](https://github.com/Microsoft/FX11)ed è possibile includerla direttamente in un'app, molto simile alla libreria di utilità DXUT. Non dispone quindi di requisiti aggiuntivi per la ridistribuzione in fase di esecuzione.

## <a name="direct3d-113"></a>Direct3D 11,3

Windows 10 viene fornito con l'API Direct3D 11,3 incorporata. Vedere le [funzionalità di direct3d 11,3](/windows/desktop/direct3d11/direct3d-11-3-features) per un elenco delle nuove funzionalità nell'API Direct3D 11,3.

## <a name="direct3d-112"></a>Direct3D 11,2

Windows 8.1 e Windows Server 2012 R2 vengono forniti con l'API Direct3D 11,2 incorporata. Vedere le [funzionalità di direct3d 11,2](/windows/desktop/direct3d11/direct3d-11-2-features) per un elenco delle nuove funzionalità nell'API Direct3D 11,2.

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 e Windows Server 2012 vengono forniti con l' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) incorporata. Il supporto parziale per l'API Direct3D 11,1 è disponibile in Windows 7 o Windows Server 2008 R2 con l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838) installato. Per ulteriori informazioni sull'aggiornamento della piattaforma per Windows 7, vedere [aggiornamento della piattaforma per Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll ospita le funzionalità di base per il rilevamento dei componenti di Direct3D 11 ed esegue l'aggiornamento del sistema tramite il servizio di Windows Update, se applicabile. Nella DLL non vengono visualizzati direttamente messaggi o finestre di dialogo.

La DLL è costituita dai punti di ingresso seguenti:

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Questa funzione esegue i controlli necessari e restituisce lo stato di Direct3D 11 nel computer. Questa funzione non richiede diritti di amministratore.

-   Lo stato D3D11IH \_ \_ installato indica che Direct3D 11 è già installato nel computer ed è pronto per l'utilizzo.
-   \_Lo stato D3D11IH \_ non \_ supportato indica che questa versione di Windows non supporta Direct3D 11 o tecnologie correlate.
-   Lo stato D3D11IH \_ \_ richiede \_ la versione più recente di \_ SP indica che l'utente deve installare il Service Pack più recente di Windows Vista.
-   Infine, lo stato di D3D11IH \_ \_ richiede \_ Update indica che nel sistema non è installato Direct3D 11, ma che l'aggiornamento del sistema è applicabile a questa versione di Windows.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Questa funzione usa l'API Windows Update per eseguire l'aggiornamento del sistema per l'installazione di Direct3D 11 in questo sistema, se applicabile. Si noti che questa funzione richiede la connettività di rete a Windows Update per avere esito positivo, oltre ai diritti amministrativi. Accetta una funzione di callback dello stato di avanzamento facoltativa e un puntatore al contesto dell'utente e restituisce un codice di risultato finale al termine dell'operazione.

-   Il risultato \_ dell' \_ esito positivo del D3D11IH indica che l'aggiornamento del sistema è stato applicato ed è pronto per l'uso, mentre il \_ riavvio D3D11IH risultati \_ riusciti \_ indica che l'aggiornamento del sistema richiede che il computer venga riavviato prima del completamento. Si noti che questa funzione non pianifica un riavvio del sistema.
-   \_Il risultato di D3D11IH \_ non \_ è supportato indica che l'aggiornamento del sistema non si applica a questa versione di Windows. Questo risultato non deve verificarsi se questa funzione viene chiamata solo dopo che il recupero \_ dello stato di D3D11IH \_ richiede \_ lo stato di aggiornamento da CheckDirect3D11Status.
-   Il risultato dell'aggiornamento dei risultati di D3D11IH \_ \_ \_ non \_ è stato trovato indica che il pacchetto di aggiornamento del sistema non è stato trovato nei server Windows Update.
-   Se il download o l'installazione del Windows Update non riesce, il \_ download dell'aggiornamento dei risultati \_ di D3D11IH \_ \_ non è riuscito o l'installazione dell'aggiornamento dei risultati di D3D11IH non è \_ \_ \_ \_ riuscita.
-   Se viene restituito un errore di connettività di rete dall'API di Windows Update, viene restituito il risultato dell' \_ errore del servizio D3D11IH \_ , che \_ \_ indica che il problema potrebbe essere intermittente o correlato alla configurazione di rete o alle impostazioni del firewall. Il tentativo di eseguire nuovamente la funzione Update potrebbe avere esito positivo.

</dd> </dl>

Per altre informazioni sull'API Windows Update, vedere [api Windows Update Agent](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe richiede l'esecuzione di D3D11InstallHelper.dll.

D3D11Install.exe è uno strumento per l'uso di D3D11InstallHelper.dll come programma di installazione autonomo completo con i messaggi dell'interfaccia utente e dell'utente finale, oltre a fungere da esempio per l'uso corretto della DLL. Il processo viene chiuso con 0 se Direct3D 11 è già installato, se l'aggiornamento del sistema viene applicato correttamente senza richiedere un riavvio del sistema, se è necessaria un'installazione del Service Pack o se Direct3D 11 non è supportato da questo computer. Viene restituito 1 se l'aggiornamento del sistema viene applicato correttamente e richiede il completamento di un riavvio del sistema. Viene restituito un valore 2 per altre condizioni di errore. Si noti che questo file eseguibile richiede i diritti di amministratore per l'esecuzione e dispone di un manifesto che richiede l'elevazione quando viene eseguito in Windows Vista o Windows 7 con UAC abilitato. D3D11Install.exe può essere usato come strumento autonomo per la distribuzione dell'aggiornamento di Direct3D 11 oppure può essere usato direttamente dai programmi di installazione.

Supporta le opzioni della riga di comando seguenti:

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/quiet 
</dt> <dd>

Non Visualizza messaggi, prompt, finestre di dialogo di stato o messaggi di errore.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/passive 
</dt> <dd>

Non vengono visualizzati messaggi, richieste o messaggi di errore, ma verrà visualizzata la finestra di dialogo stato.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Mostra solo le richieste minime.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Evita la richiesta di conferma dell'installazione dell'aggiornamento, se necessario e applicabile, per un'installazione standard e minima.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid Decimal 
</dt> <dd>

Impone il codice dell'identificatore di lingua da usare per la visualizzazione di messaggi dell'utente finale e risorse della finestra di dialogo. Il valore predefinito è 1024, che usa l'impostazione della lingua predefinita del sistema.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Impone l'utilizzo di Windows Update anziché l'impostazione predefinita di sistema, che può essere Windows Server Update Services (WSUS) in esecuzione in un server gestito o in un'altra configurazione non standard.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Integrazione nei programmi di installazione

Per garantire la conformità con il supporto di installazione semplice, [requisito tecnico 3,1 per i giochi per Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006), è necessario prestare attenzione affinché eventuali richieste dell'utente finale vengano presentate all'inizio del processo di installazione e per assicurarsi che non siano presenti più richieste di elevazione dei privilegi relative a UAC. Per raggiungere questo obiettivo sono disponibili tre opzioni di base:

1.  Il metodo più semplice consiste nell'eseguire il D3D11Install.exe con l'opzione della riga di comando **/minimal**. Questa operazione deve essere eseguita all'inizio del programma di installazione Q&A e l'installazione deve usare il valore restituito 1 per indicare che è necessario pianificare un riavvio al termine dell'installazione. L'esecuzione del programma richiede diritti amministrativi.
2.  Usare direttamente D3D11InstallHelper.dll per rilevare la necessità dell'aggiornamento, fornendo tutti i messaggi degli utenti finali necessari per lo stato D3D11IH di stato \_ \_ necessario \_ più recente \_ SP, in cui la risoluzione richiede operazioni manuali dell'utente. Il risultato dello stato dello \_ stato D3D11IH \_ non \_ supportato potrebbe essere usato per controllare l'installazione di asset correlati a Direct3D 11 o come condizione di errore per le applicazioni Direct3D 11, ma non è necessariamente un messaggio utile dell'utente finale. Per lo stato D3D11IH \_ è \_ necessario \_ aggiornare, il programma di installazione può utilizzare direttamente il punto di ingresso della dll DoUpdateForDirect3D11 per eseguire l'aggiornamento e gestire i vari messaggi dell'utente finale risultante. È possibile trovare esempi di messaggi standard esaminando la finestra di dialogo D3D11Install.exe e le risorse della tabella di stringhe. Il punto di ingresso dell'aggiornamento richiede i diritti di amministratore.
3.  Un approccio ibrido consiste nel controllare lo stato con D3D11InstallHelper.dll e, nel caso del codice di stato D3D11IH, è \_ \_ necessario \_ aggiornare lo \_ stato SP o D3D11IH più recente \_ . è possibile eseguire \_ \_ D3D11Install.exe con le opzioni **/minimal** e **/y** per visualizzare la finestra di dialogo o per eseguire l'aggiornamento, in base alle esigenze. Questi passaggi devono essere eseguiti all'inizio del processo di installazione, in genere immediatamente dopo Q&A e l'esecuzione del file eseguibile richiede diritti amministrativi.

### <a name="integrating-into-installshield"></a>Integrazione in InstallShield

La gestione della distribuzione di Direct3D 11 da InstallScript di InstallShield viene eseguita facilmente usando l'esempio D3D11InstallHelper. I passaggi necessari per l'integrazione con InstallShield usando InstallScript sono i seguenti (usando il metodo 3, descritto nella sezione precedente):

1.  Aprire un progetto InstallScript nell'editor InstallShield.
2.  Aggiungere D3D11InstallHelper.dll e D3D11Install.exe al progetto nei **file di supporto**.

    **Per aggiungere i file al progetto InstallShield**

    1.  Nella scheda **progettazione installazione** fare clic su **file di supporto/affissioni** in **comportamento e logica** nel riquadro di spostamento a sinistra.
    2.  Fare clic su **indipendente dalla lingua**, quindi fare clic con il pulsante destro del mouse nella finestra **file** e scegliere **Inserisci file**. Sfogliare per aggiungere D3D11InstallHelper.dll e D3D11Install.exe. Il percorso predefinito per questi file è: esempi radice \\ SDK \\ C++ \\ varie \\ bin \\ x86

3.  In InstallScript Explorer fare clic sul file InstallScript (in genere Setup. rul) che chiamerà la DLL o l'eseguibile, situato in **comportamento e logica** nel riquadro di spostamento a sinistra.
4.  Incollare il InstallScript seguente nel file vicino alla parte superiore:

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  Incollare il InstallScript seguente nel file nella funzione **OnFirstUIBefore** , immediatamente prima del risultato 0:

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>Integrazione in un pacchetto MSI

Di seguito è riportata una descrizione di alto livello dei passaggi necessari per integrare la distribuzione di Direct3D 11 usando le azioni personalizzate MSI (usando il metodo 3, descritto in precedenza in questo argomento):

1.  Aggiungere una proprietà alla tabella delle proprietà MSI denominata **RelativePathToD3D11IH** contenente il percorso relativo a D3D11Install.exe e D3D11InstallHelper.dll durante l'installazione. si tratta in genere dell'immagine multimediale. Imposta anche lo stato D3D11IH della proprietà MSI sullo \_ stato restituito da CheckDirect3D11Status (una proprietà di stringa uguale al simbolo di enumerazione o "Error").
2.  Dopo l'azione CostFinalize secondo, chiamare la funzione D3D11InstallHelper.dll **SetD3D11InstallMSIProperties** come azione personalizzata immediata per impostare le proprietà MSI appropriate per le altre azioni personalizzate.
3.  Al momento dell'installazione, attivare un'azione personalizzata posticipata dopo l'azione InstallFiles che chiama la funzione D3D11InstallHelper.dll **DoD3D11InstallUsingMSI**. L'azione personalizzata deve impostare il flag msidbCustomActionTypeNoImpersonate per l'esecuzione in un contesto con privilegi elevati.
4.  Dopo l'azione InstallFinalize, chiamare la funzione D3D11InstallHelper.dll **FinishD3D11InstallUsingMSI** come azione personalizzata immediata per gestire il codice risultato della richiesta di riavvio, se necessario.

Questa procedura è descritta in dettaglio nelle istruzioni seguenti, che descrivono un processo che può essere eseguito usando un editor MSI, ad esempio l' [editor ORCA](/windows/desktop/Msi/orca-exe). Alcuni editor MSI hanno procedure guidate che semplificano alcuni di questi passaggi di configurazione.

**Per configurare un pacchetto MSI per l'integrazione con D3D11InstallHelper.dll**

1.  Aprire il pacchetto MSI in Orca.
2.  Aggiungere la riga illustrata nella tabella seguente alla tabella binaria nel pacchetto MSI.

    | Nome    | Data                                         |
    |---------|----------------------------------------------|
    | D3D11IH | Percorso del file della DLL \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Questo file verrà incorporato nel pacchetto MSI, quindi è necessario eseguire questo passaggio ogni volta che si ricompila D3D11InstallHelper.dll.

     

3.  Aggiungere le righe mostrate nella tabella seguente alla tabella CustomAction del pacchetto MSI. 

    | Azione              | Tipo                                                                                                                                                                   | Source (Sorgente)  | Destinazione                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  Aggiungere i valori visualizzati per Action, Condition e Sequence nella tabella seguente alla tabella InstallExecuteSequence del pacchetto MSI. 

    | Azione              | Condizione     | Sequenza | Note                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | Il numero di sequenza inserisce l'azione subito dopo CostFinalize secondo.                                                                                                 |
    | Direct3D11DoInstall | NON installato | 4004     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione per tutti gli utenti. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo il rollback. |
    | Direct3D11Finish    |               | 6615     | Il numero di sequenza inserisce l'azione subito dopo InstallFinalize.                                                                                              |

    

     

5.  Aggiungere la riga illustrata nella tabella seguente alla tabella delle **Proprietà** nel pacchetto MSI. 

    | Proprietà              | Valore                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | percorso relativo del file che contiene D3D11Install.exe e D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Il percorso specificato dal percorso è relativo alla posizione specificata dal percorso di installazione, ad esempio "Redist \\ ".

     

6.  Salvare il pacchetto MSI. Per informazioni più dettagliate sui pacchetti MSI e Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Suggerimenti per il debug

Sia D3D11InstallHelper.dll che D3D11Install.exe possono essere compilati con la configurazione di debug in Visual Studio e queste versioni stampano i messaggi nel meccanismo di output di debug standard di Windows.

## <a name="corporate-settings"></a>Impostazioni aziendali

L'esempio D3D11InstallHelper è progettato per la distribuzione standard tramite Windows Update, che è lo scenario più comune per l'installazione di un gioco da parte dei consumer. Tuttavia, molti sviluppatori di giochi, che lavorano per gli editori e negli studi di sviluppo, eseguono questa operazione nelle impostazioni aziendali che dispongono di un server gestito localmente che fornisce aggiornamenti software tramite la tecnologia Windows Server Update Services (WSUS). In questo tipo di ambiente, l'amministratore IT locale ha il controllo di approvazione degli aggiornamenti resi disponibili per i computer all'interno della rete aziendale e la versione consumer standard dell'aggiornamento KB 971644 non è disponibile.

Sono disponibili tre soluzioni di base per la distribuzione di DirectX 11 in impostazioni aziendali/aziendali:

-   In alcune configurazioni è possibile controllare direttamente Windows Update anziché utilizzare il server WSUS gestito localmente. Per questo motivo, D3D11InstallHelper supporta l'opzione della riga di comando **/Wu** . Tuttavia, non tutte le reti aziendali consentono le connessioni ai server Microsoft pubblici.
-   L'amministratore IT locale può approvare KB 971512, un aggiornamento supportato dall'organizzazione distribuito da WSUS, che include l'API Direct3D 11. Questa è l'unica opzione che consente a un utente standard di ottenere l'aggiornamento di Direct3D 11 in un ambiente completamente bloccato.
-   In alternativa, è possibile installare manualmente [KB 971512](https://support.microsoft.com/kb/971512/) .

È molto raro che il computer di un giocatore possa ottenere gli aggiornamenti solo da un server WSUS gestito localmente ed è solo per gli sviluppatori di organizzazioni di grandi dimensioni che probabilmente si trovano in tali ambienti.

## <a name="related-articles"></a>Articoli correlati

[Windows Firewall per sviluppatori di giochi](/windows/desktop/DxTechArts/games-and-firewalls)

[Esplora giochi di Windows per sviluppatori di giochi](/windows/desktop/DxTechArts/windows-game-explorer-integration)