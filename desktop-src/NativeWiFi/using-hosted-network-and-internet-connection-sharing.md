---
title: Usa rete ospitata senza fili, condivisione connessione Internet
description: Uso della rete ospitata wireless e della condivisione della connessione Internet
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972774e921199e32eb70841c74c7478e2178cda9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967402"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>Usa rete ospitata senza fili, condivisione connessione Internet

La rete wireless ospitata è una nuova funzionalità di WLAN supportata in Windows 7 e Windows 8. È supportato anche in Windows Server 2012 e Windows Server 2008 R2 con il servizio LAN wireless installato. Questa funzionalità implementa due funzioni principali:

-   La virtualizzazione di una scheda wireless fisica in più schede wireless virtuali a volte definita Wi-Fi virtuale.
-   Un punto di accesso wireless (AP) basato su software talvolta denominato SoftAP che usa una scheda wireless virtuale designata.

Condivisione connessione Internet (ICS) è una funzionalità di Windows fornita tramite il servizio SharedAccess. In modo esplicito, SharedAccess consente la condivisione di rete tramite un computer in cui l'accesso alla rete condivisa non fornisce necessariamente l'accesso a Internet. I termini ICS e SharedAccess vengono usati in modo intercambiabile in questa sezione, perché la condivisione della connessione Internet è uno scenario principale per la rete wireless ospitata e il termine ICS è più noto alla community degli utenti.

Rete ospitata senza fili è strettamente legata a ICS per abilitare sia la rete privata wireless (PAN) sia gli scenari di condivisione Internet. In questa sezione vengono forniti suggerimenti generali per gli sviluppatori di applicazioni su come integrare reti e ICS ospitate senza fili usando le API di rete e ICS pubbliche.

## <a name="internet-connection-sharing"></a>Condivisione connessione Internet

Il servizio ICS funziona in una delle due modalità possibili:

-   Modalità autonoma

    Quando il servizio ICS viene richiamato, solo la funzione del server estensione DHCPv4 funziona. Si tratta di una modalità operativa speciale per ICS e viene resa disponibile solo tramite la rete wireless ospitata. Un utente o un'applicazione non è in grado di avviare e arrestare direttamente ICS autonomo tramite le API di ICS pubblico o i comandi **netsh** . L'avvio della rete ospitata senza fili in genere comporta l'avvio di ICS in modalità autonoma per usare la funzione server estensione DHCPv4 per fornire indirizzi IPv4 privati per i dispositivi connessi. La comunicazione di rete per i dispositivi connessi è limitata all'invio e alla ricezione di pacchetti di rete tra un dispositivo connesso e il computer locale che ospita la rete wireless ospitata e tra i dispositivi connessi. In questo modo viene abilitato lo scenario rete personale wireless per la rete ospitata senza fili.

-   Modalità completa

    Tutte le funzionalità di ICS funzionano quando viene richiamato il servizio, ad esempio Network Address Translation e le funzioni server DHCP per IPv4 e IPv6. Si tratta della modalità di funzionamento normale per ICS. Un utente o un'applicazione può avviare e arrestare la modalità ICS completa attraverso le API pubbliche o i comandi NetShell. Ad esempio, è possibile arrestare questo servizio usando net stop SharedAccess da un prompt dei comandi con privilegi elevati. Combinando la rete wireless ospitata con ICS completo, la comunicazione di rete per i dispositivi connessi non è limitata al PAN wireless. Qualsiasi dispositivo connesso può accedere alla rete, ad esempio Internet, tramite la connessione di rete condivisa dal computer in cui è in esecuzione la rete wireless ospitata. Questo consente di abilitare lo scenario di condivisione di rete per la rete ospitata senza fili.

In questa sezione viene usato il termine ICS completo per indicare il caso in cui tutte le funzioni ICS vengono richiamate nel servizio ICS per consentire l'accesso a tutte le funzionalità ICS complete con la rete ospitata senza fili.

Le due modalità operative di ICS si escludono a vicenda con i circuiti integrati completi che assumono precedenza maggiore. Il servizio ICS può passare dalla modalità autonoma alla modalità completa, ma non dalla modalità completa alla modalità autonoma. La modalità autonoma ICS è stata introdotta in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato insieme alla funzionalità rete ospitata wireless. Non è disponibile nelle versioni precedenti di Windows.

Qualsiasi operazione di ICS completa implica due schede di rete diverse nel sistema:

-   Interfaccia pubblica. Si tratta dell'interfaccia di rete con accesso a Internet. Si tratta di un'interfaccia che il computer locale che esegue ICS USA per condividere Internet con client e dispositivi che si connettono tramite SoftAP.
-   Interfaccia privata. Si tratta dell'interfaccia di rete usata da altri dispositivi per connettersi al computer locale che esegue ICS. Un server estensione DHCPv4 è in esecuzione su questa interfaccia privata per fornire indirizzi IP locali privati agli altri computer remoti.

Quando l'interfaccia pubblica non ha accesso a Internet, il server DHCP sull'interfaccia privata continua a fornire gli indirizzi IP locali ai dispositivi connessi. L'ICS autonomo riguarda solo l'interfaccia privata su cui è in esecuzione SoftAP. non implica alcuna interfaccia pubblica.

In qualsiasi momento è presente al massimo un'istanza di ICS completo in esecuzione nel computer locale. Se l'ICS completo è già in esecuzione nel computer locale, l'avvio di un'altra ICS completa presenta i comportamenti funzionali seguenti:

-   Se le interfacce pubbliche e private del nuovo ICS completo sono identiche a quelle del ICS completo esistente, l'avvio della seconda ICS completa equivale a un no-op.
-   Se la nuova interfaccia pubblica è diversa dall'interfaccia pubblica precedente, ma la nuova interfaccia privata è la stessa dell'interfaccia privata precedente, l'avvio di un secondo ICS completo ha un piccolo effetto sui dispositivi connessi sulla stessa interfaccia privata. La possibilità di accedere a Internet può cambiare con la nuova interfaccia pubblica.
-   Se la nuova interfaccia privata è diversa dalla vecchia interfaccia privata, le funzioni ICS smetteranno di funzionare sull'interfaccia privata precedente e inizieranno a essere applicate alla nuova interfaccia privata. Tutti i dispositivi remoti che si connettono al computer locale utilizzando l'interfaccia privata precedente perderanno la connettività IP al computer locale.

Quando l'ICS completo è già in esecuzione, la chiamata di un secondo ICS completo è un'operazione distruttiva per i dispositivi connessi in modalità remota tramite l'interfaccia privata precedente, purché la seconda integrazione di ICS usi una nuova interfaccia privata diversa.

Per gestire e usare il servizio ICS per supportare l'integrazione di ICS con la rete wireless ospitata, un'applicazione software deve prima ottenere un'interfaccia [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) . L'interfaccia **INetSharingManager** fornisce l'accesso diretto o indiretto a tutte le altre interfacce com nell'API ICS. Il metodo [**get \_ SharingInstalled**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled) sull'interfaccia **INetSharingManager** segnala se il computer locale supporta la condivisione della connessione. Il metodo [**get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) sull'interfaccia **INetSharingManager** recupera un'interfaccia di enumerazione per tutte le connessioni nella cartella Connections. Il metodo [**get \_ INetSharingConfigurationForINetConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection) recupera un'interfaccia [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) per la connessione specificata. I metodi dell'interfaccia **INetSharingConfiguration** possono essere usati per eseguire query e modificare le impostazioni di ICS.

È necessario avviare la rete ospitata senza fili prima di chiamare il metodo [**get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) sull'interfaccia [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) per enumerare tutte le connessioni nella cartella Connections.

Per informazioni su ICS e sulle interfacce pubbliche e sui metodi che possono essere usati per eseguire query e modificare le impostazioni di ICS, vedere la documentazione relativa a [informazioni su Condivisione connessione Internet e firewall connessione Internet](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall).

## <a name="hosted-network-and-ics-integration"></a>Integrazione di rete e ICS ospitata

Quando l'ICS completo non è in esecuzione, l'avvio di una rete wireless ospitata avvia anche internamente il servizio ICS in modalità autonoma con solo la funzione server estensione DHCPv4 per allocare gli indirizzi IP per i dispositivi connessi nell'interfaccia di rete ospitata senza fili. L'intervallo di indirizzi della subnet per il server estensione DHCPv4 autonomo è 192.168.173.0/24. Questa operazione è diversa dall'intervallo di subnet di 192.168.137.0/24 usato con l'ICS completo.

L'avvio di una rete ospitata senza fili con ICS completo usa la logica seguente:

-   Se il servizio ICS completo non è già in esecuzione, l'avvio di una rete wireless ospitata avvia anche il servizio ICS con il server estensione DHCPv4 autonomo.
-   Se l'ICS completo è già in esecuzione e l'interfaccia privata è l'interfaccia di rete ospitata senza fili, è sufficiente avviare la rete wireless ospitata.
-   Se l'ICS completo è già in esecuzione, ma l'interfaccia privata non è l'interfaccia di rete wireless ospitata, la rete wireless ospitata verrà avviata senza la funzione del server estensione DHCPv4 sull'interfaccia di rete ospitata senza fili.

L'effetto della logica precedente evidenzia i fatti seguenti:

-   ICS non esegue la transizione dalla modalità completa alla modalità autonoma.
-   La modalità autonoma può essere richiamata solo dalla rete ospitata senza fili quando ICS non è in esecuzione in modalità completa.
-   Se ICS viene eseguito in modalità autonoma, verrà interrotto in modalità completa se un utente o un'applicazione avvia ICS in modalità completa.
-   La transizione dalla modalità autonoma alla modalità completa in ICS sarà problematica per i dispositivi connessi nel PAN wireless se l'interfaccia privata di ICS completo non corrisponde a quella di SoftAP.

È necessario tempo per avviare o arrestare il servizio ICS nel computer locale in modalità completa o autonoma. Un'applicazione deve controllare lo stato del servizio ICS usando la funzione **NotifyServiceStatusChange** per verificare che il servizio ICS non si trovi nello stato di avvio/arresto in sospeso prima di avviare o arrestare la rete ospitata senza fili da usare con l'integrazione con ICS.

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>Avvio e arresto della rete ospitata senza fili

Windows offre una piattaforma in cui più applicazioni simultanee possono gestire una rete ospitata senza fili nello stesso momento. In particolare, ogni applicazione può avviare e arrestare la rete wireless ospitata autonomamente, senza conoscere prima le altre applicazioni.

Sono disponibili due set di funzioni per avviare e arrestare una rete ospitata.

Più applicazioni possono richiedere l'uso della rete ospitata senza fili. Le funzioni [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) e [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) avviano e arrestano un host wireless rete in ingresso un modo compatibile con altre applicazioni simultanee. Le funzioni **WlanHostedNetworkStartUsing** e **WlanHostedNetworkStopUsing** consentono a un'applicazione di avere un riferimento alla rete ospitata senza fili. Questo meccanismo consente di mantenere in esecuzione la rete wireless ospitata, purché almeno un'altra applicazione disponga di un riferimento corrente alla rete ospitata senza fili. Qualsiasi utente può chiamare queste funzioni. Le chiamate a **WlanHostedNetworkStartUsing** con esito positivo devono corrispondere alle chiamate alla funzione **WlanHostedNetworkStopUsing** . Qualsiasi modifica dello stato della rete ospitata causata dalla funzione **WlanHostedNetworkStartUsing** viene annullata automaticamente se l'applicazione chiamante chiude il relativo handle chiamante (chiamando [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) con lo stesso parametro *hClientHandle* passato a **WlanHostedNetworkStartUsing**) o se il processo termina.

Le funzioni [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) e [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) forzano l'avvio e l'arresto di una rete ospitata senza fili. Queste funzioni possono essere chiamate solo se l'utente dispone del privilegio con privilegi elevati appropriato. Le chiamate a **WlanHostedNetworkForceStart** con esito positivo possono essere eventualmente corrispondenti a una chiamata alla funzione **WlanHostedNetworkForceStop** , a seconda della progettazione dell'applicazione. Queste funzioni eseguono la transizione dello stato della rete wireless ospitata senza associare la richiesta all'handle chiamante dell'applicazione. Qualsiasi modifica dello stato della rete ospitata causata dalla funzione **WlanHostedNetworkForceStart** non viene annullata automaticamente se l'applicazione chiamante chiude il relativo handle chiamante (chiamando [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) con lo stesso parametro *hClientHandle* passato a [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)) o se il processo termina. Se l'applicazione che ha chiamato la funzione **WlanHostedNetworkForceStart** si chiude senza chiamare una delle funzioni per arrestare la rete ospitata senza fili, viene lasciata in esecuzione la rete ospitata. Un'applicazione può chiamare la funzione **WlanHostedNetworkForceStart** dopo avere verificato che un utente di sistema con privilegi elevati accetti i maggiori requisiti di alimentazione necessari per l'esecuzione della rete ospitata senza fili per periodi di tempo prolungati.

Di seguito sono riportate le indicazioni generali sulle funzioni da chiamare per avviare e arrestare una rete ospitata senza fili:

-   Usare le funzioni [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) e [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) all'interno di un'applicazione per avviare e arrestare una rete ospitata senza fili.
-   Non usare la funzione [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) per avviare una rete wireless ospitata, a meno che non sia assolutamente richiesta dall'applicazione. Anche la funzione **WlanHostedNetworkForceStart** richiede privilegi elevati.
-   Utilizzare la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) solo come metodo di ripristino. La funzione **WlanHostedNetworkForceStop** causa l'arresto immediato di una rete ospitata senza fili. Potrebbe essere necessario eseguire azioni di ripristino per altre applicazioni in ascolto delle notifiche di rete ospitata senza fili. Per ulteriori informazioni, vedere la discussione seguente sulla sequenza di recupero per la rete wireless ospitata.

## <a name="start-sequence-for-wireless-hosted-network"></a>Sequenza di avvio per la rete wireless ospitata

Per un'applicazione che avvia una rete ospitata senza fili con ICS completo, è consigliabile avviare la rete wireless ospitata, quindi avviare l'ICS completo. Se una rete ospitata senza fili è già in esecuzione, è necessario che un'applicazione usi la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per arrestare la rete ospitata senza fili solo se è necessario un ICS completo, ma non è stata abilitata prima dell'avvio della rete ospitata. Ciò consente ad altre applicazioni di eseguire il ripristino da potenziali rotture causate dall'avvio di un ICS completo. Per ulteriori informazioni, vedere la discussione seguente sulla sequenza di recupero per la rete wireless ospitata. L'operazione combinata deve avere esito positivo e negativo nel suo complesso.

> [!Note]  
> È necessario avviare la rete ospitata senza fili prima di provare a enumerare la scheda corrispondente usando l'interfaccia [**IEnumNetSharingEveryConnection**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection) .

 

I passaggi ordinati seguenti rappresentano la sequenza di avvio consigliata in un'applicazione che usa la rete wireless ospitata con l'ICS completo:

-   Chiamare la funzione [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) per assicurarsi che la rete ospitata senza fili sia configurata e pronta per l'utilizzo.
-   Chiamare le funzioni [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) e [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) per determinare se la rete ospitata senza fili è consentita e disponibile. Se la rete ospitata senza fili non è consentita e non è disponibile, viene restituito un errore.
-   Testare per verificare se il servizio ICS usato per l'ICS completo è consentito. Se non è possibile avviare il servizio ICS, viene restituito un errore.
-   Chiamare la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per forzare l'arresto della rete ospitata senza fili.
-   Chiamare la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) per avviare la rete ospitata senza fili.
-   Se la rete ospitata senza fili non viene avviata, viene restituito un errore.
-   Se l'ICS completo è già in esecuzione e l'interfaccia pubblica o privata corrente è diversa dalla nuova interfaccia da usare, memorizzare nella cache le interfacce pubbliche e private correnti. Un'applicazione può anche scegliere di restituire un errore o richiedere all'utente se l'integrazione con ICS è già in esecuzione.
-   Avviare l'ICS completo con le nuove impostazioni per le interfacce pubbliche e private.
-   Se il servizio ICS completo non viene avviato con queste impostazioni, provare ad avviare il servizio ICS completo con le interfacce pubbliche e private memorizzate nella cache se prima era in esecuzione l'ICS completa. Chiamare la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per arrestare la rete ospitata senza fili e restituire un errore.
-   Restituisce l'esito positivo della riuscita della rete ospitata senza fili e dell'ICS completo.

## <a name="stop-sequence-for-wireless-hosted-network"></a>Sequenza di arresto per la rete wireless ospitata

Quando si usa la rete wireless ospitata con l'ICS completo, un'applicazione che ha terminato il lavoro potrebbe voler arrestare la rete ospitata senza fili e il servizio ICS usato per i circuiti integrati completi. In questo caso, è consigliabile chiamare la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per arrestare la rete ospitata anziché chiamare la funzione [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) . La funzione **WlanHostedNetworkForceStop** arresta la rete ospitata senza fili e serve anche per consentire il ripristino di altre applicazioni. Per ulteriori informazioni, vedere la discussione seguente sulla sequenza di recupero per la rete wireless ospitata.

I passaggi ordinati seguenti rappresentano la sequenza di arresto consigliata in un'applicazione che utilizza la rete wireless ospitata e l'ICS completo:

-   Arrestare l'intero ICS.
-   Chiamare la funzione [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per arrestare la rete ospitata senza fili.

Un'applicazione che usa la rete wireless ospitata senza ICS completo completata con il suo lavoro deve solo chiamare la funzione [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) o [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) per arrestare la rete ospitata senza fili. Se è stata chiamata la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) per avviare la rete wireless ospitata, l'applicazione deve chiamare la funzione **WlanHostedNetworkStopUsing** per arrestare la rete ospitata senza fili. Se la rete ospitata senza fili era già stata avviata prima che l'applicazione o l'applicazione avesse chiamato la funzione [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) per forzare l'avvio della rete ospitata senza fili, l'applicazione può chiamare la funzione **WlanHostedNetworkForceStop** per arrestare la rete ospitata senza fili oppure non eseguire alcuna operazione (lasciare avviata la rete wireless ospitata) a seconda dello scenario.

## <a name="recovery-sequence-for-wireless-hosted-network"></a>Sequenza di recupero per la rete wireless ospitata

Un'applicazione che usa la rete wireless ospitata può essere interessata dalle azioni di altre applicazioni. Il servizio ICS e le interfacce per la gestione di ICS non forniscono alcun metodo per la registrazione delle notifiche di modifica ICS da parte di un'applicazione. Se un'altra applicazione chiama i metodi [**EnableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing) o [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing) sull'interfaccia [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) per abilitare o disabilitare la condivisione in una connessione, viene inviato un messaggio all'interfaccia utente (schermata) nel computer locale e non ad altre applicazioni. Pertanto, un'applicazione deve basarsi sulle notifiche della rete wireless ospitata per eseguire azioni di ripristino quando si verificano modifiche all'ICS o alla rete ospitata senza fili.

Un'applicazione che usa la rete wireless ospitata deve registrarsi per le notifiche di rete ospitata senza fili chiamando [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification). Se sono necessarie notifiche per solo la rete wireless ospitata, l'applicazione deve passare l' **\_ origine di notifica WLAN \_ \_ HNWK** nel parametro *dwNotifSource* passato a **WlanRegisterNotification**. Se sono necessarie anche altre segnalazioni wireless, l' **\_ origine di notifica WLAN \_ \_ HNWK** deve essere combinata con le costanti di origine della notifica per altri tipi di notifiche wireless desiderate e passare questo valore nel parametro *dwNotifSource* .

La sequenza di recupero è la stessa per le applicazioni con o senza ICS completo, presupponendo che le applicazioni non riavviino il servizio ICS. Quando si riceve una notifica di rete ospitata senza fili che la rete ospitata è stata arrestata, effettuare le seguenti operazioni:

-   Se l'applicazione ha chiamato [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) per avviare la rete wireless ospitata, riavviare la rete ospitata chiamando **WlanHostedNetworkForceStart**. In caso contrario, chiamare [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) per riavviare la rete ospitata senza fili.

## <a name="recovery-sequence-for-connected-devices"></a>Sequenza di ripristino per i dispositivi connessi

È possibile che i dispositivi remoti o i computer connessi alla rete ospitata senza fili siano interessati dalle azioni di altre applicazioni che influiscono su ICS e sulla rete ospitata senza fili. Fortunatamente, la maggior parte dei dispositivi ha creato la logica di ripetizione dei tentativi nell'applicazione del dispositivo per gestire una perdita temporanea del segnale o del roaming.

Una possibile sequenza di ripristino per i dispositivi o i computer connessi alla rete ospitata senza fili che perde il contatto è la seguente:

-   Il driver di dispositivo wireless indica una disconnessione dei supporti ai livelli superiori dello stack di rete nel dispositivo.
-   L'applicazione del dispositivo avvia verifiche periodiche per la disponibilità della rete ospitata senza fili.
-   Quando l'applicazione del dispositivo rileva nuovamente la rete ospitata senza fili, il dispositivo avvia una connessione wireless.
-   Una volta stabilita la connessione alla rete ospitata senza fili, l'applicazione del dispositivo aggiorna le impostazioni IP di conseguenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla rete wireless ospitata](about-the-wireless-hosted-network.md)
</dt> <dt>

[Esempio di rete wireless ospitata](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
