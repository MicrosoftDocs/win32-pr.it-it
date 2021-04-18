---
title: Windows Firewall per sviluppatori di giochi
description: In questo articolo vengono descritte le Windows Firewall, il motivo per cui esiste, il risultato dell'operazione e il relativo funzionamento. In particolare, viene descritto come configurare il gioco per funzionare correttamente con il firewall.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88656fb3f622a847c15544646c333b807f3a0fb2
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530565"
---
# <a name="windows-firewall-for-game-developers"></a>Windows Firewall per sviluppatori di giochi

In questo articolo vengono descritte le Windows Firewall, il motivo per cui esiste, il risultato dell'operazione e il relativo funzionamento. In particolare, viene descritto come configurare il gioco per funzionare correttamente con il firewall.

Contenuto:

-   [Che cos'è un firewall?](#what-is-a-firewall)
-   [Come è possibile stabilire se il gioco è interessato?](#how-can-i-tell-if-my-game-is-affected)
-   [Il firewall prima di Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Windows XP SP2 firewall è migliore](#windows-xp-sp2-firewall-is-better)
-   [Utilizzo del Windows Firewall](#working-with-the-windows-firewall)
-   [Integrazione con InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integrazione in Wise for Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integrazione in Windows Installer](#integrating-into-windows-installer)
-   [Indicazioni](#recommendations)

## <a name="what-is-a-firewall"></a>Che cos'è un firewall?

Il firewall fornisce una barriera contro le intrusioni basate sulla rete. Blocca il traffico in ingresso non richiesto e rende il sistema principalmente invisibile su Internet rifiutando le richieste di Internet Control Message Protocol (ICMP). Ciò significa che ping e tracert non funzioneranno. Il firewall cerca inoltre e rifiuta i pacchetti non validi.

Questo ostacolo impedisce gli attacchi opportunistici. Gli attacchi si diffondono grazie alla ricerca di molti sistemi con la stessa vulnerabilità. Il firewall può contrastare molti attacchi inserendo un segno di "non disturbare" per le funzionalità attualmente in uso; l'attacco viene ignorato e non colpisce Home. Il vantaggio fondamentale del Windows Firewall è che le funzionalità e le applicazioni che non sono in uso non possono essere vie di attacco.

L'utente configura il sistema in modo da identificare le applicazioni e le funzionalità necessarie e devono essere aperte alla rete. Questo errore si verifica quando viene installata un'applicazione o quando si tenta di aprirla alla rete.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Come è possibile stabilire se il gioco è interessato?

Con l'arrivo di Windows XP SP2, il Windows Firewall è stato ampiamente distribuito. Tutti i giochi di Windows multiplayer sono interessati a un certo livello. Sebbene i client si trovino in genere in forma corretta, i server, gli host e i peer in peer-to-peer necessitano del firewall configurato per continuare a funzionare. In particolare, il traffico in ingresso non richiesto viene eliminato. Il firewall intercetta i pacchetti di filtro del traffico di rete in base al contenuto dei pacchetti e alle attività di rete recenti. Il firewall utilizza il contenuto e l'attività per decidere di inviare o eliminare un pacchetto. Una volta configurato correttamente il firewall, un gioco sarà in grado di accettare il traffico non richiesto in ingresso come prima.

Chi ha traffico indesiderato in ingresso?

-   Client/server: tutti i partecipanti si connettono a un server centrale. Il server centrale è quello con traffico non richiesto in entrata. I client che si connettono al server richiedono il traffico di ritorno, che è previsto e che può passare attraverso il firewall se vengono seguite le regole per i client. Il server centrale deve essere configurato in modo da accettare il traffico non richiesto per consentire al traffico client di passare attraverso il firewall.
-   Massively multiplayer (MMP): tutti i partecipanti sono connessi a una data center. Ciò equivale a una relazione client/server complessa, poiché il data center ha il traffico non richiesto in ingresso. I partecipanti sono client e, in generale, non devono accettare traffico non richiesto.
-   Peer-to-peer, in cui tutti i partecipanti sono connessi tra loro direttamente: tutti i partecipanti devono essere pronti ad accettare il traffico non richiesto da qualsiasi nuovo giocatore che partecipa al gruppo. In un certo senso, ognuno dei partecipanti deve fungere da host, quindi è necessario che tutti siano configurati come se fossero host.

I client sono in genere in forma corretta. Le connessioni Transmission Control Protocol/Internet Protocol (TCP/IP) in uscita funzioneranno correttamente, così come i messaggi UDP (User Datagram Protocol) e le risposte tempestive a tali messaggi, il firewall mantiene la porta aperta per 90 secondi dopo ogni messaggio in uscita in attesa di una risposta.

## <a name="the-firewall-before-windows-xp-sp2"></a>Il firewall prima di Windows XP SP2

Il firewall connessione Internet (ICF) in Windows XP e Windows Server 2003 è un filtro di pacchetti con stato e gestisce sia il protocollo Internet, la versione 4 (IPv4) sia il protocollo Internet versione 6 (IPv6). Tuttavia, non è attiva per impostazione predefinita e non supporta stack di rete di terze parti, di cui è presente un numero significativo nel mondo, ad esempio provider Internet di grandi dimensioni, incluse le società telefoniche nazionali.

Per chi non si trova in Windows XP SP2, è consigliabile attivare l'ICF. Vedere le istruzioni "usare un firewall Internet" https://www.microsoft.com/security/protect come primo passaggio per la protezione del PC. Il firewall connessione Internet (ICF) fornisce il mapping delle porte per eseguire l'override del filtro pacchetti. In sostanza, si specifica la porta da aprire e rimane aperta fino a quando non viene chiusa. Se l'utente viene riavviato prima della chiusura, rimarrà aperto fino a quando non viene chiuso in modo specifico. Il controllo del firewall e la gestione dei mapping delle porte vengono eseguiti tramite [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) e [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Il Windows Firewall per Windows XP SP2 è una soluzione più completa che supporta stack di rete di terze parti e gestisce le porte in modo più intelligente: le porte vengono mantenute aperte solo se l'applicazione che li richiede è ancora attiva.

## <a name="windows-xp-sp2-firewall-is-better"></a>Windows XP SP2 firewall è migliore

Windows XP SP2 inserisce le scelte di sicurezza e le impostazioni in primo piano. L'obiettivo è la protezione per impostazione predefinita e consente all'utente di prendere decisioni informate sulle applicazioni consentite per l'esecuzione nel computer.

La nuova Windows Firewall è disponibile in Windows XP SP2 e Windows Server 2003 Service Pack 1 (SP1). Analogamente a ICF, si tratta di un firewall software che supporta sia IPv4 che IPv6, ma a differenza di ICF il Windows Firewall:

-   Dispone della protezione in fase di avvio del sistema, eliminando una piccola finestra di vulnerabilità durante l'avvio.
-   Supporta stack di rete di terze parti.
-   Dispone di una modalità "on senza eccezioni" che blocca tutti i pacchetti in ingresso non richiesti. Si tratta di un'ottima soluzione quando si usa una rete pubblica, ad esempio in un aeroporto o in un bar.

Nella modalità "on senza eccezioni" tutti i buchi statici vengono chiusi. Le chiamate API per aprire un foro statico sono consentite ma posticipate; ovvero, non vengono applicati finché il firewall torna al normale funzionamento. Verranno ignorate anche tutte le richieste di ascolto per le applicazioni. Le connessioni in uscita riusciranno comunque.

Per le nuove applicazioni, aggiungere l'applicazione all'elenco "eccezioni" durante l'installazione. È possibile aggiungere l'applicazione usando l'interfaccia [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , specificando il percorso completo. Verranno illustrati i dettagli nell'esempio.

Come si può notare, è possibile chiedersi se si tratta di un rischio per la sicurezza che le applicazioni possano aggiungere e rimuovere applicazioni dall'elenco di eccezioni per qualsiasi intervento da parte dell'utente o se si ritiene che il rischio più grande sia che le applicazioni possano disabilitare completamente il firewall. Per eseguire queste operazioni, l'applicazione deve disporre di privilegi di amministratore. Se si dispone di codice dannoso in esecuzione in modalità amministratore nel sistema, il gioco è già scaduto e il pirata informatico ha già vinto. La capacità del pirata informatico di disabilitare il firewall meriterebbe molto più di una nota.

Le applicazioni legacy, incluse le applicazioni installate prima dell'aggiornamento a Windows XP SP2, vengono gestite con il popup dell'elenco di eccezioni (vedere la figura 1). Questa finestra di dialogo Mostra quando un'applicazione tenta di aprire una porta per il traffico in ingresso, quando si chiama bind () con una porta diversa da zero per UDP oppure si accetta () per il protocollo TCP/IP. È necessario essere un amministratore per "sbloccare" le applicazioni, mentre "Richiedi in seguito" impedisce questo periodo di tempo, ma chiede di nuovo la volta successiva.

Si tratta di una finestra di dialogo modale del sistema non bloccante. Quando si esegue un'applicazione Microsoft Direct3D a schermo intero, la finestra di dialogo viene visualizzata sotto. l'utente può quindi gestirlo quando l'applicazione chiude la modalità a schermo intero o ALT-TAB sul desktop. Tuttavia, non è sempre ovvio per l'utente che questa finestra di dialogo è stata visualizzata quando il gioco è in esecuzione a schermo intero, quindi è importante evitare che questa finestra di dialogo venga visualizzata usando l'interfaccia [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , come illustrato di seguito.

**Figura 1. Finestra di dialogo popup elenco eccezioni**

![finestra di dialogo popup elenco eccezioni](images/firewalls1.jpg)

Si noterà che il popup conosce il nome e l'autore dell'applicazione. Non c'è niente di magico. viene effettuato il pull dalle informazioni sulla versione dell'eseguibile. Queste informazioni sono uno strumento di amministrazione del sistema importante; viene anche usato per il lavoro di compatibilità delle applicazioni in corso. Alcune applicazioni trascurano il mantenimento delle informazioni sulla versione aggiornate.

Gli utenti possono anche aggiungere le proprie applicazioni tramite l'interfaccia utente (vedere la figura 2).

**Figura 2. Configurazione del firewall**

![configurazione del firewall](images/firewalls2.jpg)

**Figura 3. Aggiunta di un programma all'elenco di eccezioni del firewall**

![Aggiunta di un programma all'elenco di eccezioni del firewall](images/firewalls3.jpg)

Lo scenario migliore consiste nel rendere automatiche le aggiunte e le rimozioni dall'elenco di eccezioni. Il momento migliore per eseguire queste operazioni di aggiunta e rimozione è durante il processo di installazione e disinstallazione. Per aggiungere o rimuovere dall'elenco di eccezioni del firewall sono necessari i privilegi di amministratore, pertanto assicurarsi di tenere conto di questo.

## <a name="working-with-the-windows-firewall"></a>Utilizzo del Windows Firewall

Anche in questo caso, la maggior parte dei giochi devono essere aggiunti all'elenco di eccezioni del firewall solo se possono fungere da server o se implementano un protocollo di comunicazione peer-to-peer. Il FirewallInstallHelper.dll è una DLL di esempio che può essere chiamata da un programma di installazione. L'origine è disponibile se si vuole integrare l'origine direttamente nella propria applicazione. L'esempio è disponibile qui:



|             |                                                                              |
|-------------|------------------------------------------------------------------------------|
| Origine:     | (Radice SDK) \\ Esempi \\ C++ \\ \\ FirewallInstallHelper varie                        |
| Eseguibile: | (Radice SDK) \\ Esempi \\ \\ \\ \\ <arch> \\FirewallInstallHelper.dll bin varie C++ |



 

Le funzioni esportate da questa DLL sono le seguenti:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Questa funzione aggiunge un'applicazione all'elenco di eccezioni. Accetta un percorso completo dell'eseguibile e un nome descrittivo che verrà visualizzato nell'elenco di eccezioni del firewall. Questa funzione richiede privilegi di amministratore.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Versione ANSI di **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Questa funzione rimuove l'applicazione dall'elenco di eccezioni. Accetta un percorso completo dell'eseguibile. Questa funzione richiede privilegi di amministratore

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Versione ANSI di **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Questa funzione segnala se l'applicazione è stata disabilitata o rimossa dall'elenco di eccezioni. Deve essere chiamato ogni volta che viene eseguito il gioco. La funzione accetta un percorso completo del file eseguibile. Questa funzione non richiede privilegi di amministratore.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Versione ANSI di **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Chiamare questo solo se si usano azioni personalizzate in Windows Installer. Vedere di seguito per altri dettagli.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Chiamare questo solo se si usano azioni personalizzate in Windows Installer. Vedere di seguito per altri dettagli.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Chiamare questo solo se si usano azioni personalizzate in Windows Installer. Vedere di seguito per altri dettagli.

</dd> </dl>

Le sezioni seguenti descrivono i metodi specifici di chiamata delle funzioni DLL esportate da questo FirewallInstallHelper dall'interno di un pacchetto InstallShield, Wise o Windows Installer. Tutti i metodi eseguono gli stessi risultati e spetta allo sviluppatore determinare il metodo da implementare.

## <a name="integrating-using-installshield-installscript"></a>Integrazione con InstallShield InstallScript

Un metodo alternativo di utilizzo delle API del firewall consiste nell'aggiungere le chiamate di funzione a un InstallScript InstallShield. I passaggi necessari per l'integrazione sono piuttosto semplici:

1.  Aprire un progetto InstallScript nell'editor InstallShield.
2.  Aggiungere il FirewallInstallHelper.dll al progetto come file di supporto.

    1.  Nella scheda Project Assistant aprire la scheda file applicazione.
    2.  Fare clic sul pulsante Aggiungi file per aggiungere file alla cartella di destinazione dell'applicazione.
    3.  Passare al FirewallInstallHelper.dll compilato o usare quello fornito in DirectX SDK e aggiungerlo al progetto.

3.  Aggiungere InstallScript al progetto.

    1.  Aprire la visualizzazione progettazione installazione e fare clic sul comportamento e la logica \| InstallScript
    2.  Fare clic sul file InstallScript (in genere Setup. rul) per aprirlo nell'editor.
    3.  Incollare il codice seguente nel file InstallScript:

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  Modificare i commenti TODO con il nome dell'applicazione che verrà visualizzato nell'elenco di eccezioni del firewall e il percorso dell'eseguibile del gioco relativo alla directory di installazione.

## <a name="integrating-into-wise-for-windows-installer"></a>Integrazione in Wise for Windows Installer

Per l'integrazione con Wise per Windows Installer, è necessario eseguire queste operazioni:

1.  Aprire il progetto Wise for Windows Installer.
2.  Selezionare la scheda "esperto installazione" nella parte inferiore.
3.  Fare clic su file e aggiungere il FirewallInstallHelper.dll da DXSDK alla directory di installazione del gioco.
4.  Selezionare la scheda "script MSI" nella parte inferiore.
5.  Selezionare la scheda "Execute immediate" in basso.
6.  Dopo CostFinalize secondo aggiungere un'azione "Imposta proprietà" che imposta FULLPATH su " \[ INSTALLDIR \] percorso relativo a eseguibile dalla directory di installazione". Ad esempio, " \[ INSTALLDIR \]game.exe" senza le virgolette
7.  Selezionare la scheda "Esegui rinviata" in basso.
8.  Dopo PublishProduct, aggiungere un'istruzione "if" con la condizione "NOT installed" (maiuscole/minuscole).
9.  All'interno del blocco If aggiungere un'azione "Call Custom DLL from Destination".

    1.  Impostare il campo file DLL su " \[ INSTALLDIR \]FirewallInstallHelper.dll."
    2.  Impostare il campo nome funzione su "AddApplicationToExceptionListA".
    3.  Aggiungere un parametro con il tipo "puntatore di stringa", l'origine del valore "Property" e il nome della proprietà "FULLPATH".
    4.  Aggiungere un secondo parametro con il tipo "puntatore di stringa", l'origine del valore "costante" e impostare il valore costante sul nome descrittivo dell'applicazione che si desidera visualizzare nell'elenco di eccezioni del firewall.
    5.  Chiudere il blocco if aggiungendo un'istruzione "end".

10. Appena sopra l'azione RemoveFiles nella parte superiore, aggiungere un altro blocco if, con la condizione "REMOVE ~ =" ALL "" (maiuscole/minuscole e senza le virgolette esterne).
11. Nel secondo blocco If aggiungere un'azione "Call Custom DLL from Destination".

    1.  Impostare il campo file DLL su " \[ INSTALLDIR \]FirewallInstallHelper.dll."
    2.  Impostare il campo nome funzione su "RemoveApplicationFromExceptionListA".
    3.  Aggiungere un parametro con il tipo "puntatore di stringa", l'origine del valore "Property" e il nome della proprietà "FULLPATH".
    4.  Chiudere il secondo blocco if aggiungendo un'istruzione "end".

## <a name="integrating-into-windows-installer"></a>Integrazione in Windows Installer

Per l'integrazione con Windows Installer a livello generale, è necessario eseguire questa procedura. Verranno descritte in dettaglio di seguito:

-   Aggiungere due proprietà "FriendlyNameForFirewall" e "RelativePathToExeForFirewall" come descritto di seguito.
-   Dopo l'azione CostFinalize secondo, chiamare "SetMSIFirewallProperties" in un'azione personalizzata immediata per impostare le proprietà MSI appropriate per le altre azioni personalizzate.
-   Durante l'installazione dopo l'azione InstallFiles, chiamare un'azione personalizzata posticipata che usa la funzione "AddToExceptionListUsingMSI" di FirewallInstallHelper.
-   Durante la disinstallazione dopo l'azione InstallFiles, chiamare un'azione personalizzata posticipata che usa la funzione "RemoveFromExceptionListUsingMSI" di FirewallInstallHelper.
-   Durante il rollback, chiamare un'azione personalizzata posticipata che chiama anche la funzione "RemoveFromExceptionListUsingMSI" di FirewallInstallHelper.

Di seguito sono riportati i passaggi necessari per eseguire questa operazione usando un editor MSI, ad esempio ORCA, disponibile in Platform SDK. Si noti che alcuni editor hanno procedure guidate che semplificano alcuni di questi passaggi:

1.  Aprire il pacchetto MSI in Orca.
2.  Aggiungere quanto segue alla tabella binaria:

    

    | Nome     | Data                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FIREWALL | Puntare al FirewallInstallHelper.dll. Questo file verrà incorporato nel pacchetto MSI, pertanto sarà necessario eseguire questo passaggio ogni volta che si ricompilano FirewallInstallHelper.dll. |

    

     

3.  Aggiungere il codice seguente alla tabella CustomAction:

    

    | Azione                   | Tipo                                                                                                                                                                                                   | Source (Sorgente)   | Destinazione                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | FIREWALL | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | AddToExceptionListUsingMSI      |

    

     

4.  Aggiungere quanto segue alla tabella InstallExecuteSequence:

    

    | Azione                   | Condizione     | Sequenza | Note                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Questo si posiziona subito dopo CostFinalize secondo.                                                                                                                                       |
    | FirewallAdd              | NON installato | 4021     | Questa azione personalizzata verrà eseguita solo durante un'installazione aggiornata. Il numero di sequenza inserisce l'azione dopo InstallFiles e dopo il rollback.                              |
    | FirewallRollBackAdd      | NON installato | 4020     | Questa azione personalizzata verrà eseguita solo quando viene annullata un'installazione aggiornata. Il numero di sequenza inserisce l'azione dopo InstallFiles e prima dell'azione personalizzata Aggiungi.          |
    | FirewallRemove           | Installato     | 3461     | Questa azione personalizzata verrà eseguita solo durante la disinstallazione. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                           |
    | FirewallRollBackRemove   | NON installato | 3460     | Questa azione personalizzata verrà eseguita solo quando viene annullata una disinstallazione. Il numero di sequenza posiziona l'azione immediatamente prima di RemoveFiles e prima dell'azione personalizzata Rimuovi. |

    

     

5.  Aggiungere quanto segue alla tabella delle proprietà:

    

    | Proprietà                     | Valore                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Deve essere il nome che verrà visualizzato nell'elenco di eccezioni. Ad esempio, "esempio di gioco" |
    | RelativePathToExeForFirewall | Deve essere l'eseguibile installato del gioco. Ad esempio, "ExampleGame.exe"  |

    

     

Per ulteriori informazioni su Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Consigli

Il firewall è qui per restare. Questi consigli offriranno ai tuoi clienti un'esperienza di firewall ottimale con il tuo gioco Windows:

-   Non informare gli utenti di disabilitare il firewall per riprodurre il gioco. Questa operazione rende l'intero computer vulnerabile anche quando il gioco non viene riprodotto.
-   Rendere la configurazione del firewall senza problemi per gli utenti. Aggiungere l'applicazione all'elenco di eccezioni durante l'installazione e rimuovere l'applicazione dall'elenco di eccezioni durante l'installazione.
-   Inviare commenti e suggerimenti all'utente se il multiplayer è bloccato dallo stato del firewall. Ad esempio, disabilitare le funzionalità di rete se non funzionano perché l'applicazione non è consentita o perché il sistema è in modalità "nessuna eccezione".

 

 