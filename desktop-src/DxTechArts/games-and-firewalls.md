---
title: Windows Firewall per sviluppatori di giochi
description: Questo articolo descrive il Windows firewall, il motivo per cui esiste, il risultato e il modo in cui lo fa. L'aspetto più importante è che descrive come configurare il gioco in modo che funzioni correttamente con il firewall.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e7fc00631ef69f878c54de90c2577221e5bc9a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882672"
---
# <a name="windows-firewall-for-game-developers"></a>Windows Firewall per sviluppatori di giochi

Questo articolo descrive il Windows firewall, il motivo per cui esiste, il risultato e il modo in cui lo fa. L'aspetto più importante è che descrive come configurare il gioco in modo che funzioni correttamente con il firewall.

Contenuto:

-   [Che cos'è un firewall?](#what-is-a-firewall)
-   [Come è possibile determinare se il gioco è interessato?](#how-can-i-tell-if-my-game-is-affected)
-   [Firewall prima di Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Windows XP SP2 Firewall Is Better](#windows-xp-sp2-firewall-is-better)
-   [Uso del firewall Windows](#working-with-the-windows-firewall)
-   [Integrazione con InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integrazione in Wise for Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integrazione nel programma Windows installazione](#integrating-into-windows-installer)
-   [Indicazioni](#recommendations)

## <a name="what-is-a-firewall"></a>Che cos'è un firewall?

Il firewall rappresenta una barriera contro le intrusioni basate sulla rete. Blocca il traffico in ingresso non richiesto e rende il sistema quasi invisibile su Internet rifiutando Internet Control Message Protocol richieste (ICMP). Ciò significa che ping e tracert non funzionano. Il firewall cerca e rifiuta anche i pacchetti non validi.

Questa barriera impedisce attacchi opportunistici. Gli attacchi si diffondono individuando molti sistemi con la stessa vulnerabilità. Il firewall può contrastare molti attacchi inserendo un segno "non disturbare" per le funzionalità attualmente non in uso. L'attacco viene ignorato e non viene ignorato. Il vantaggio essenziale del firewall Windows è che le funzionalità e le applicazioni non in uso non possono essere percorsi di attacco.

L'utente configura il sistema per identificare quali applicazioni e funzionalità sono necessarie e devono essere aperte alla rete. Ciò si verifica quando un'applicazione viene installata o quando tenta di aprirsi alla rete.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Come è possibile determinare se il gioco è interessato?

Con l'arrivo di Windows XP SP2, il firewall Windows è stato ampiamente distribuito. Tutte le Windows multiplayer sono interessate in qualche misura. Anche se i client sono in genere in buona forma, i server, gli host e i peer nel peer-to-peer necessitano tutti del firewall configurato per continuare a funzionare. In particolare, il traffico in ingresso non richiesto viene eliminato. Il firewall intercetta i pacchetti di filtro del traffico di rete in base al contenuto del pacchetto e alle attività di rete recenti. Il firewall usa il contenuto e l'attività per decidere di inoltrare o eliminare un pacchetto. Una volta configurato correttamente il firewall, un gioco sarà in grado di accettare il traffico in ingresso non richiesto come in precedenza.

Who traffico in ingresso non richiesto?

-   Client/Server: tutti i partecipanti si connettono a un server centrale. Il server centrale è quello con traffico in ingresso non richiesto. I client che si connettono al server devono chiedere il traffico di ritorno, che è previsto e può passare attraverso il firewall se vengono seguite le regole per i client. Il server centrale deve essere configurato per accettare il traffico non richiesto per consentire al traffico client di passare attraverso il firewall.
-   Massively Multiplayer (MMP): tutti i partecipanti sono connessi a un data center. Si tratta di una relazione client/server complessa, in quanto il data center ha il traffico in ingresso non richiesto. I partecipanti sono client e in generale non devono accettare traffico non richiesto.
-   Peer-to-peer, in cui tutti i partecipanti sono connessi direttamente tra loro: tutti i partecipanti devono essere pronti ad accettare il traffico non richiesto da qualsiasi nuovo giocatore che si unisce al gruppo. In un certo senso, ognuno dei partecipanti deve funzionare come host, quindi tutti devono essere configurati come se fossero host.

I client sono in genere in buona forma. Le connessioni Transmission Control Protocol/Internet Protocol in uscita (TCP/IP) funzioneranno correttamente, così come i messaggi UDP (User Datagram Protocol) in uscita insieme alle risposte in tempo reale a tali messaggi. Il firewall mantiene aperta la porta per 90 secondi dopo ogni messaggio in uscita in previsione di una risposta.

## <a name="the-firewall-before-windows-xp-sp2"></a>Firewall prima di Windows XP SP2

Il Internet Connection Firewall (ICF) in Windows XP e Windows Server 2003 è un filtro di pacchetti con stato e gestisce sia il protocollo IPv4 che il protocollo Internet versione 6 (IPv6). Tuttavia, non è disponibile per impostazione predefinita e non supporta stack di rete di terze parti, di cui esiste un numero significativo in tutto il mondo, ad esempio provider Internet di grandi dimensioni, tra cui società telefoniche nazionali.

Per gli utenti che non Windows XP SP2, è consigliabile attivare ICF. Vedere le istruzioni "Usare un firewall Internet" in https://www.microsoft.com/security/protect come primo passaggio per proteggere il PC. Il Internet Connection Firewall (ICF) fornisce il mapping delle porte per eseguire l'override del filtro di pacchetti. In sostanza, si specifica la porta da aprire e la porta rimane aperta fino a quando non viene chiusa. Se l'utente viene riavviato prima della chiusura, rimarrà aperto fino alla chiusura specifica. Il controllo del firewall e la gestione dei mapping delle porte avviene tramite [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) e [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Il firewall Windows per Windows XP SP2 è una soluzione più completa che supporta stack di rete di terze parti e gestisce le porte in modo più intelligente: le porte vengono mantenute aperte solo finché l'applicazione che le richiede è ancora attiva.

## <a name="windows-xp-sp2-firewall-is-better"></a>Windows XP SP2 Firewall Is Better

Windows XP SP2 mette in primo piano le opzioni e le impostazioni di sicurezza. L'obiettivo è proteggere per impostazione predefinita e consentire all'utente di effettuare scelte informate sulle applicazioni che possono essere eseguite nel computer.

Il nuovo firewall Windows è disponibile sia in Windows XP SP2 che in Windows Server 2003 Service Pack 1 (SP1). Analogamente a ICF, si tratta di un firewall software che supporta sia IPv4 che IPv6, ma a differenza di ICF il firewall Windows:

-   Protezione in fase di avvio del sistema, eliminando una piccola finestra di vulnerabilità durante l'avvio.
-   Supporta stack di rete di terze parti.
-   Ha una modalità "attiva senza eccezioni" che blocca tutti i pacchetti in ingresso non richiesto. Questo è ideale quando si usa una rete pubblica, ad esempio in un aeroporto o in un bar.

Nella modalità "attiva senza eccezioni", tutti i fori statici vengono chiusi. Le chiamate API per aprire un foro statico sono consentite ma posticipate. ciò significa che non vengono applicate fino a quando il firewall non torna al normale funzionamento. Tutte le richieste di ascolto da parte delle applicazioni verranno ignorate. Le connessioni in uscita avranno comunque esito positivo.

Per le nuove applicazioni, aggiungere l'applicazione all'elenco delle eccezioni durante l'installazione. È possibile aggiungere l'applicazione [**usando l'interfaccia INetFwAuthorizedApplications,**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) fornendo il percorso completo. Verranno fornite informazioni dettagliate nell'esempio.

Come si può notare, ci si potrebbe chiedere se si tratta di un rischio per la sicurezza che le applicazioni possono aggiungere e rimuovere applicazioni dall'elenco delle eccezioni per qualsiasi intervento dell'utente o se si pensa che il rischio maggiore sia che le applicazioni possano disabilitare completamente il firewall. Per eseguire queste funzionalità, l'applicazione deve avere privilegi di amministratore. Se nel sistema è in esecuzione codice dannoso in modalità amministratore, il gioco è già finito e il pirata informatico ha già vinto. La capacità del pirata informatico di disabilitare il firewall sarebbe poco più di una nota a piè di pagina.

Le applicazioni legacy, incluse le applicazioni installate prima dell'aggiornamento dell'utente a Windows XP SP2, vengono gestite con il popup Elenco eccezioni (vedere la figura 1). Questa finestra di dialogo mostra quando un'applicazione tenta di aprire una porta per il traffico in ingresso, quando si chiama bind() con una porta diversa da zero per UDP o accept() per il protocollo TCP/IP. È necessario essere in esecuzione come amministratore per sbloccare le applicazioni, mentre "Chiedi più tardi" non consente questa volta, ma chiede di nuovo la volta successiva.

Si tratta di una finestra di dialogo modale di sistema non bloccante. Quando si esegue un'applicazione Microsoft Direct3D a schermo intero, la finestra di dialogo viene visualizzata sotto; e l'utente può quindi gestirlo quando l'applicazione esce dalla modalità schermo intero o le schede ALT tornano al desktop. Tuttavia, non è sempre ovvio per l'utente che questa finestra di dialogo sia stata visualizzata quando un gioco è in esecuzione a schermo intero, quindi è importante evitare di fare in modo che questa finestra di dialogo venga visualizzata usando l'interfaccia [**INetFwAuthorizedApplications,**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) come illustrato di seguito.

**Figura 1. Finestra di dialogo popup Elenco eccezioni**

![Finestra di dialogo popup elenco eccezioni](images/firewalls1.jpg)

Si noterà che il popup conosce il nome e l'editore dell'applicazione. In questo caso non c'è alcun magic, che viene estratto dalle informazioni sulla versione del file eseguibile. Queste informazioni sono un importante strumento di amministrazione del sistema. viene usato anche per le attività di compatibilità delle applicazioni in corso. Alcune applicazioni non sono in grado di mantenere aggiornate queste informazioni sulla versione.

Gli utenti possono anche aggiungere le proprie applicazioni tramite l'interfaccia utente (vedere la figura 2)

**Figura 2. Configurazione del firewall**

![configurazione del firewall](images/firewalls2.jpg)

**Figura 3. Aggiunta di un programma all'elenco di eccezioni del firewall**

![aggiunta di un programma all'elenco di eccezioni del firewall](images/firewalls3.jpg)

Lo scenario migliore consiste nell'eseguire aggiunte e rimozioni dall'elenco delle eccezioni in modo automatico. Il momento migliore per eseguire queste aggiunte e rimozioni è durante il processo di installazione e disinstallazione. L'aggiunta o la rimozione dall'elenco di eccezioni del firewall richiede privilegi di amministratore, quindi assicurarsi di prendere in considerazione questo.

## <a name="working-with-the-windows-firewall"></a>Uso del firewall Windows

Anche in questo caso, la maggior parte dei giochi deve essere aggiunta all'elenco di eccezioni del firewall solo se possono funzionare come server o se implementano un protocollo di comunicazione peer-to-peer. Il FirewallInstallHelper.dll è una DLL di esempio che può essere chiamata da un programma di installazione. L'origine viene fornita se si vuole integrare l'origine direttamente nell'applicazione. L'esempio è disponibile qui:



|             | File                                                                             |
|-------------|------------------------------------------------------------------------------|
| **Source:**     | (radice SDK) \\ Esempi \\ C++ \\ Misc \\ FirewallInstallHelper                        |
| **Eseguibile:** | (radice SDK) \\ Esempi \\ C++ \\ misc \\ Bin arch \\ &lt; &gt; \\FirewallInstallHelper.dll |



 

Le funzioni esportate da questa DLL sono le seguenti:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Questa funzione aggiunge un'applicazione all'elenco di eccezioni. Accetta un percorso completo del file eseguibile e un nome descrittivo che verrà visualizzato nell'elenco delle eccezioni del firewall. Questa funzione richiede privilegi di amministratore.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Versione ANSI di **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Questa funzione rimuove l'applicazione dall'elenco di eccezioni. Accetta un percorso completo del file eseguibile. Questa funzione richiede privilegi di amministratore

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Versione ANSI di **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Questa funzione segnala se l'applicazione è stata disabilitata o rimossa dall'elenco delle eccezioni. Deve essere chiamato ogni volta che viene eseguito il gioco. La funzione accetta un percorso completo del file eseguibile. Questa funzione non richiede privilegi di amministratore.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Versione ANSI di **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Chiamare questo metodo solo se si usano azioni personalizzate in Windows programma di installazione. Vedere di seguito per altri dettagli.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Chiamare questo metodo solo se si usano azioni personalizzate in Windows programma di installazione. Vedere di seguito per altri dettagli.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Chiamare questo metodo solo se si usano azioni personalizzate in Windows programma di installazione. Vedere di seguito per altri dettagli.

</dd> </dl>

Le sezioni seguenti descrivono metodi specifici per chiamare le funzioni dll esportate da questo FirewallInstallHelper dall'interno di un pacchetto InstallShield, Wise o Windows Installer. Tutti i metodi eseguono il rendering degli stessi risultati e lo sviluppatore deve determinare quale metodo implementare.

## <a name="integrating-using-installshield-installscript"></a>Integrazione con InstallShield InstallScript

Un metodo alternativo per l'uso delle API firewall è l'aggiunta delle chiamate di funzione a InstallShield InstallScript. I passaggi necessari per l'integrazione sono piuttosto semplici:

1.  Aprire un progetto InstallScript nell'editor InstallShield.
2.  Aggiungere il FirewallInstallHelper.dll al progetto come file di supporto.

    1.  Nella Project Assistant (Assistente applicazioni) aprire la scheda Application Files (File applicazione).
    2.  Fare clic sul pulsante Aggiungi file per aggiungere file alla cartella di destinazione dell'applicazione.
    3.  Passare al FirewallInstallHelper.dll compilato o usare quello fornito in DirectX SDK e aggiungerlo al progetto.

3.  Aggiungere InstallScript al progetto.

    1.  Aprire la visualizzazione Progettazione installazione e fare clic su Behavior and Logic InstallScript (Comportamento e \| logica InstallScript)
    2.  Fare clic sul file InstallScript (in genere setup.rul) per aprirlo nell'editor
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

    4.  Modificare i commenti TODO con il nome dell'applicazione che verrà visualizzato nell'elenco delle eccezioni del firewall e il percorso del file eseguibile del gioco relativo alla directory di installazione.

## <a name="integrating-into-wise-for-windows-installer"></a>Integrazione in Wise for Windows Installer

Per l'integrazione con Wise for Windows Installer, è necessario eseguire questi passaggi:

1.  Aprire il progetto Wise for Windows Installer.
2.  Selezionare la scheda "Installation Expert" (Esperto installazione) nella parte inferiore.
3.  Fare clic su File e aggiungere il FirewallInstallHelper.dll da DXSDK alla directory di installazione del gioco.
4.  Selezionare la scheda "Script MSI" nella parte inferiore.
5.  Selezionare la scheda "Esegui controllo immediato" nella parte inferiore.
6.  Dopo CostFinalize, aggiungere un'azione "Set Property" che imposta FULLPATH su \[ "INSTALLDIR \] relative path to executable from install directory". Ad esempio, \[ "INSTALLDIR \]game.exe" senza virgolette
7.  Selezionare la scheda "Esegui posticipata" nella parte inferiore.
8.  Dopo PublishProduct aggiungere un'istruzione "If" con la condizione "NOT Installed" (con distinzione tra maiuscole e minuscole).
9.  All'interno del blocco If aggiungere un'azione "Call Custom DLL from Destination".

    1.  Impostare il campo File DLL su \[ "INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Impostare il campo Nome funzione su "AddApplicationToExceptionListA".
    3.  Aggiungere un parametro di tipo "string pointer", l'origine del valore "Property" e il nome della proprietà "FULLPATH".
    4.  Aggiungere un secondo parametro con il tipo "string pointer", l'origine del valore "Constant" e impostare il valore costante sul nome descrittivo dell'applicazione da visualizzare nell'elenco delle eccezioni del firewall.
    5.  Chiudere il blocco If aggiungendo un'istruzione "End Statement".

10. Appena sopra l'azione RemoveFiles nella parte superiore, aggiungere un altro blocco If, con la condizione "REMOVE~="ALL"" (con distinzione tra maiuscole e minuscole e senza virgolette esterne).
11. Nel secondo blocco If aggiungere un'azione "Call Custom DLL from Destination".

    1.  Impostare il campo File DLL su \[ "INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Impostare il campo Nome funzione su "RemoveApplicationFromExceptionListA".
    3.  Aggiungere un parametro di tipo "string pointer", l'origine del valore "Property" e il nome della proprietà "FULLPATH".
    4.  Chiudere il secondo blocco If aggiungendo un'istruzione "End Statement".

## <a name="integrating-into-windows-installer"></a>Integrazione nel programma Windows installazione

Per eseguire l Windows installer a livello superiore, è necessario eseguire questi passaggi. Verranno illustrate in dettaglio di seguito:

-   Aggiungere 2 proprietà "FriendlyNameForFirewall" e "RelativePathToExeForFirewall" come descritto di seguito.
-   Dopo l'azione CostFinalize, chiamare "SetMSIFirewallProperties" in un'azione personalizzata immediata per impostare le proprietà MSI appropriate per le altre azioni personalizzate.
-   Durante l'installazione dopo l'azione InstallFiles, chiamare un'azione personalizzata posticipata che usa la funzione "AddToExceptionListUsingMSI" di FirewallInstallHelper.
-   Durante la disinstallazione dopo l'azione InstallFiles, chiamare un'azione personalizzata posticipata che usa la funzione "RemoveFromExceptionListUsingMSI" di FirewallInstallHelper.
-   Durante il rollback, chiamare un'azione personalizzata posticipata che chiama anche la funzione "RemoveFromExceptionListUsingMSI" di FirewallInstallHelper.

Di seguito è riportata la procedura necessaria per eseguire questa operazione usando un editor msi, ad esempio Orca, disponibile in Platform SDK. Si noti che alcuni editor hanno procedure guidate che semplificano alcuni di questi passaggi:

1.  Aprire il pacchetto MSI in Orca.
2.  Aggiungere quanto segue alla tabella Binary:

    

    | Nome     | Dati                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FIREWALL | Puntare alla FirewallInstallHelper.dll. Questo file verrà incorporato nel pacchetto MSI, quindi sarà necessario eseguire questo passaggio ogni volta che si ricompila FirewallInstallHelper.dll. |

    

     

3.  Aggiungere quanto segue alla tabella CustomAction:

    

    | Azione                   | Tipo                                                                                                                                                                                                   | Source (Sorgente)   | Destinazione                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | FIREWALL | SetMSIFirewallProperties        |
    | FirewallAggiungi              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | AddToExceptionListUsingMSI      |

    

     

4.  Aggiungere quanto segue alla tabella InstallExecuteSequence:

    

    | Azione                   | Condition     | Sequenza | Note                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Ciò si verifica subito dopo CostFinalize.                                                                                                                                       |
    | FirewallAggiungi              | NON installato | 4021     | Questa azione personalizzata verrà eseguita solo durante una nuova installazione. Il numero di sequenza posiziona l'azione dopo InstallFiles e dopo i rollback.                              |
    | FirewallRollBackAdd      | NON installato | 4020     | Questa azione personalizzata verrà eseguita solo quando viene annullata una nuova installazione. Il numero di sequenza posiziona l'azione dopo InstallFiles e prima dell'azione aggiungi personalizzata.          |
    | FirewallRemove           | Installato     | 3461     | Questa azione personalizzata verrà eseguita solo durante la disinstallazione. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e dopo i rollback.                           |
    | FirewallRollBackRemove   | NON installato | 3460     | Questa azione personalizzata verrà eseguita solo quando viene annullata una disinstallazione. Il numero di sequenza posiziona l'azione direttamente prima di RemoveFiles e prima dell'azione personalizzata Remove. |

    

     

5.  Aggiungere quanto segue alla tabella Proprietà:

    

    | Proprietà                     | Valore                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Deve essere il nome che verrà visualizzato nell'elenco delle eccezioni. Ad esempio, "Esempio di gioco" |
    | RelativePathToExeForFirewall | Deve essere l'eseguibile installato del gioco. Ad esempio, "ExampleGame.exe"  |

    

     

Per altre informazioni sul programma di Windows, vedere Windows [Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Consigli

Il firewall è qui per rimanere. Queste raccomandazioni offriranno ai clienti un'esperienza di firewall ottimale con il Windows gioco:

-   Non indicare agli utenti di disabilitare il firewall per il gioco. In questo modo l'intero computer è vulnerabile anche quando non sta riproducendo il gioco.
-   Semplificare la configurazione del firewall per gli utenti. Aggiungere l'applicazione all'elenco delle eccezioni durante l'installazione e rimuovere l'applicazione dall'elenco delle eccezioni durante l'installazione.
-   Inviare commenti e suggerimenti all'utente se il multiplayer è bloccato dallo stato del firewall. Ad esempio, disabilitare le funzionalità di rete se non funzionano perché l'applicazione non è consentita o perché il sistema è in modalità "nessuna eccezione".

 

 
