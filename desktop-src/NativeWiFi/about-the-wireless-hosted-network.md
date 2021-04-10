---
description: Informazioni sulla rete wireless ospitata
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Informazioni sulla rete wireless ospitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15be48bb5ef10754b11a0b3d4bb7d8e31ace9752
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232057"
---
# <a name="about-the-wireless-hosted-network"></a>Informazioni sulla rete wireless ospitata

La rete wireless ospitata è una nuova funzionalità WLAN supportata in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato. Questa funzionalità implementa due funzioni principali:

-   La virtualizzazione di una scheda wireless fisica in più schede wireless virtuali a volte definita Wi-Fi virtuale.
-   Un punto di accesso wireless (AP) basato su software talvolta denominato SoftAP che usa una scheda wireless virtuale designata.

Queste due funzioni coesisteranno tra loro in un sistema Windows. L'abilitazione o la disabilitazione della rete ospitata senza fili Abilita o Disabilita sia Wi-Fi virtuale che SoftAP. Non è possibile abilitare o disabilitare queste due funzioni separatamente in Windows.

Con questa funzionalità, un computer Windows può usare una singola scheda di rete wireless fisica per connettersi come client a un punto di accesso hardware (AP), mentre allo stesso tempo funge da punto di accesso software che consente ad altri dispositivi compatibili con wireless di connettersi a esso. Per questa funzionalità è necessario che nel computer locale sia installata una scheda di rete ospitata in grado di supportare. Il driver per la scheda wireless deve implementare il modello di driver di dispositivo LAN wireless definito da Microsoft per l'utilizzo in Windows 7. Per ricevere il logo di Windows 7, è necessario che un driver wireless implementi la funzionalità rete ospitata senza fili.

Al massimo una rete ospitata senza fili abilitata in qualsiasi momento nel computer locale e solo una scheda wireless verrà utilizzata dalla rete ospitata senza fili. Se è presente più di una scheda wireless in grado di supportare la rete ospitata, Windows sceglierà una scheda da usare con la rete ospitata senza fili. Quando vengono utilizzate le API di rete ospitata, la scheda di rete ospitata in grado di supportare è virtualizzata al massimo 3 schede logiche:

-   Una scheda di stazione (STA) per l'uso da applicazioni client o wireless ad hoc. L'adapter STA eredita tutte le impostazioni della scheda wireless fisica originale e presenta gli stessi comportamenti della scheda fisica. Concettualmente, è possibile visualizzare l'adattatore STA come identico alla scheda fisica dopo la virtualizzazione. L'adapter STA sempre nel sistema purché sia presente la scheda fisica wireless corrispondente.
-   Un adattatore AP che deve essere usato dalla rete ospitata senza fili per ospitare SoftAP. L'adapter AP è presente nel sistema Windows solo dopo che la rete ospitata senza fili viene richiamata per la prima volta (quando viene chiamata la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Una volta creato, l'adapter AP rimarrà nel sistema finché la rete ospitata senza fili non sarà disabilitata. Se la rete ospitata senza fili è abilitata in un secondo momento, l'adapter AP verrà nuovamente visualizzato nel sistema.
-   Una scheda di rete virtuale (VSTA) per l'utilizzo da parte dei fornitori di hardware per estendere la funzionalità di rete wireless ospitata in Windows. L'adapter VSTA è facoltativo e può essere creato solo nel sistema dal servizio IHV corrispondente. Diversamente dalla scheda AP, l'adapter VSTA è presente nel sistema Windows solo dal momento in cui il servizio IHV Inizializza la scheda fino al momento in cui il servizio IHV rilascia l'adapter.

Wi-Fi virtuale esegue il mapping delle schede logiche alle porte NDIS. L'associazione degli adapter STA, AP e VSTA a porte NDIS specifiche viene decisa da Windows. L'adapter STA sempre associato alla porta 0. L'adapter AP viene associato alla successiva porta NDIS disponibile all'avvio della virtualizzazione e l'associazione rimane invariata fino al termine della virtualizzazione quando la rete wireless ospitata è disabilitata. L'adapter VSTA è associato alla successiva porta NDIS disponibile quando viene inizializzato dal servizio IHV corrispondente e l'associazione rimane invariata fino a quando non viene rilasciata dal servizio IHV.

È possibile creare la scheda VSTA per l'uso da parte di IHV senza creare l'adattatore SoftAP.

Le combinazioni seguenti sono valide per una scheda fisica con virtualizzazione:

-   Adapter STA.
-   Adattatori STA e AP.
-   Adapter STA e VSTA.
-   Adapter STA, AP e VSTA.

Ad eccezione del caso di adapter STA, tutte le altre combinazioni sono valide solo quando è abilitata la rete ospitata senza fili. Come per il singolo caso di adapter STA, è la scheda fisica se la rete ospitata senza fili è disabilitata. Se la rete ospitata senza fili è abilitata, è l'adapter STA quando la rete ospitata senza fili non è mai stata richiamata nel sistema.

Il bridging di livello 2 non è consentito tra la scheda AP e qualsiasi altro adapter nel sistema. La stessa restrizione si applica all'adapter VSTA quando è presente nel sistema.

La funzionalità rete ospitata senza fili di Windows implementa un SoftAP. Tuttavia, questo SoftAP non è progettato per sostituire i dispositivi AP wireless basati su hardware. In particolare, se la rete ospitata senza fili viene eseguita quando il computer passa alla modalità di sospensione (standby), ibernazione o prima del riavvio del computer, la rete ospitata senza fili verrà arrestata. La rete ospitata senza fili non verrà riavviata automaticamente dopo la ripresa del computer da sospensione, ibernazione o riavvio. Inoltre, SoftAP non fornisce la risoluzione DNS. Nel caso in cui un server DNS esterno non venga reso disponibile usando la condivisione della connessione Internet (vedere la discussione su ICS di seguito), la risoluzione del nome di dominio completo (FQDN) tra due computer o dispositivi connessi con SoftAP, incluso il computer che ospita il SoftAP, funziona solo se entrambe le entità contrassegnano il tipo di rete della rete SoftAP come privato (abitazione o lavoro nel popup della categoria di rete). Poiché il computer che ospita il SoftAP contrassegna sempre il tipo di rete SoftAP come privato, solo i computer o i dispositivi connessi a SoftAP devono contrassegnare il tipo di rete SoftAP come privato per consentire il funzionamento della risoluzione FQDN.

SoftAP e la rete ad hoc si escludono a vicenda nella stessa scheda fisica. Se SoftAP è in esecuzione nella scheda AP e un utente o un'applicazione avvia la rete ad hoc nell'adapter STA, SoftAP verrà arrestato. Le funzionalità di rete ad hoc sono in esecuzione nell'adapter STA, un tentativo di avviare SoftAP nell'adapter AP avrà esito negativo.

Per garantire la protezione delle comunicazioni wireless tra il computer che ospita SoftAP e i dispositivi che si connettono al SoftAP, la rete ospitata senza fili richiede che tutti i dispositivi connessi usino il pacchetto di crittografia WPA2-PSK/AES. La chiave condivisa è un valore di 63 caratteri generato da Windows quando la rete ospitata senza fili viene richiamata per la prima volta (quando viene chiamata la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Un utente o un'applicazione non può modificare il valore di questa chiave condivisa, ma un'applicazione può richiedere al sistema operativo di rigenerare una nuova chiave chiamando la funzione [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) oppure un utente può richiedere al sistema operativo di rigenerare una nuova chiave utilizzando i comandi **Netsh WLAN** . Questa chiave condivisa è chiamata chiave primaria o di sistema per la rete ospitata senza fili ed è persistente durante l'avvio e l'arresto della rete ospitata senza fili. Questa chiave primaria viene chiamata "chiave di sicurezza di sistema" nei comandi **Netsh WLAN** .

Per consentire la semplicità d'uso, rete ospitata senza fili supporta anche il concetto di chiave di sicurezza secondaria o utente più intuitiva, ma potrebbe essere meno sicura. Questa chiave secondaria viene chiamata "chiave di sicurezza utente" nei comandi **Netsh WLAN** . La chiave secondaria non è generata da Windows. L'utente deve fornire il valore per questa chiave. Un utente o un'applicazione può impostare o modificare il valore della chiave chiamando la funzione [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) o utilizzando i comandi **Netsh WLAN** . La chiave secondaria può essere impostata in modo da essere permanente o temporanea. Per una chiave temporanea, se la rete ospitata senza fili è già in esecuzione, la chiave secondaria sarà valida fino a quando non si arresta la rete ospitata senza fili. Per una chiave temporanea, se la rete ospitata senza fili non è in esecuzione, sarà valida solo tra l'avvio e l'arresto della rete wireless ospitata successiva.

Esiste esattamente una chiave primaria e al massimo una chiave secondaria per la Hetwork ospitata senza fili in qualsiasi computer. Tutti i dispositivi di cui è stato effettuato il provisioning tramite Wi-Fi la configurazione protetta (WPS) riceveranno la chiave primaria. Altri dispositivi configurati manualmente possono usare una delle due chiavi. Ogni volta che viene modificata una chiave, i dispositivi con il valore di chiave precedente non saranno in grado di connettersi alla rete wireless ospitata senza che sia stato eseguito di nuovo il provisioning con la nuova chiave. Tuttavia, i dispositivi con l'altra chiave non modificata continueranno a essere in grado di connettersi alla rete ospitata senza fili.

Un'applicazione può registrarsi per le notifiche della rete wireless ospitata, quindi una notifica WLAN verrà inviata al callback dell'applicazione quando le proprietà cambiano nella rete ospitata senza fili. Un'applicazione esegue la registrazione per le notifiche della rete wireless ospitata chiamando [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) con il set di parametri *dwNotifSource* per includere l' \_ origine di notifica WLAN \_ \_ HNWK bit.

Windows offre due modi per consentire agli amministratori IT di gestire la funzionalità di rete ospitata senza fili. Per i computer membri di un dominio, gli amministratori possono utilizzare i criteri di gruppo per impedire la rete ospitata senza fili. Utilizzando i comandi **Netsh WLAN** , un amministratore può abilitare o disabilitare la rete wireless ospitata localmente nel computer.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Scenari supportati per la rete wireless ospitata

La rete wireless ospitata consente due scenari principali per i computer Windows:

• Possibilità di fornire una rete wireless (Personal Area Network) wireless per l'uso con diversi altri dispositivi wireless.

• Condivisione della connessione di rete per l'uso da parte di altri computer e dispositivi.

Il PAN wireless è lo scenario principale abilitato dalla rete ospitata senza fili. Una volta avviata la rete wireless ospitata in un computer, qualsiasi dispositivo con supporto wireless che supporta WPA2-PSK/AES sarà in grado di connettersi a softAP proprio come se si connettesse a un punto di accesso hardware normale. I dispositivi connessi alla rete wireless ospitata formano una panoramica wireless, in cui possono scambiare informazioni con il computer Windows che ospita il SoftAP e tra loro.

La condivisione della connessione di rete per l'uso da parte di altri computer e dispositivi richiede l'uso della condivisione della connessione Internet (ICS). In questo scenario, l'interfaccia pubblica di ICS è la connessione condivisa mentre l'interfaccia privata è la scheda virtuale che ospita SoftAP. La connessione condivisa può essere Ethernet, LAN wireless o connessione WAN wireless. Nel caso di una connessione LAN wireless, l'interfaccia pubblica di ICS può essere da un'altra scheda LAN wireless o dalla scheda della stazione virtuale della stazione nella stessa scheda wireless fisica che ospita il SoftAP. L'uso più comune per la condivisione di rete è la condivisione di una connessione Internet, in cui la rete nell'interfaccia pubblica di ICS ha accesso a Internet.

La rete wireless ospitata interagisce con Wi-Fi Protected Setup (WPS), un'altra importante nuova funzionalità di Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. Rete ospitata senza fili e WPS supportano uno scenario che effettua il provisioning di un dispositivo che supporta WPS per un AP hardware non compatibile con WPS. In questo caso, il SoftAP ospitato in Windows viene richiamato in background per eseguire il push del profilo AP hardware sul dispositivo che supporta WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Accesso dell'utente e dell'applicazione alla rete wireless ospitata

Gli utenti finali interagiscono con la funzionalità di rete wireless ospitata in Windows con applicazioni di terze parti o comandi **netsh** . Attualmente non è disponibile alcuna interfaccia utente nativa per la configurazione o la gestione della rete wireless ospitata in Windows 7 o in Windows Server 2008 R2 con il servizio LAN wireless installato.

Le applicazioni di terze parti e i comandi **netsh** si basano sull'uso delle funzioni di rete wireless ospitate pubbliche. Questo set di funzioni offre un set completo di funzionalità per gestire la rete wireless ospitata in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato.

Di seguito è riportato un elenco delle funzioni di rete ospitata senza fili e delle azioni comuni da un punto di vista dell'utente finale che la funzione che verrebbe utilizzata per:



| Funzioni utilizzate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Avviare la rete wireless ospitata.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Arrestare la rete ospitata senza fili.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configurare le impostazioni di rete ospitata senza fili (modificare il SSID, modificare la chiave secondaria o richiedere che la chiave primaria venga rigenerata).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Eseguire una query sulle impostazioni e le informazioni di rete ospitata senza fili (stato, SSID, chiave secondaria, chiave primaria o elenco dei dispositivi attualmente connessi).<br/> |



 

I comandi **netsh** sono destinati all'uso da parte di utenti o amministratori avanzati.

*Netsh.exe* dispone di molti sottocomandi per LAN wireless. Un elenco completo di opzioni per **netsh** e wireless LAN è disponibile dal prompt dei comandi digitando quanto segue:

**Netsh WLAN/?**

La documentazione su tutti i comandi Netsh per la LAN wireless è disponibile anche in linea su TechNet. Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

Di seguito sono riportati alcuni comandi **netsh** comunemente utilizzati con per la rete LAN wireless e la rete ospitata senza fili, sebbene siano supportate altre combinazioni di comandi:



| Comando                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**Netsh WLAN Start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Avviare la rete wireless ospitata.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**Netsh WLAN Stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Arrestare la rete ospitata senza fili.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode = \] allow non \| Allow**<br/>                                                                                                                                                                                                                                                                      | Abilitare o disabilitare la rete ospitata senza fili.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ SSID = \] <ssid> \[ Key = \] <passphrase> \[ DataUsage = \] Persistent \| Temporary** <br/> | Configurare le impostazioni di rete ospitata senza fili.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**Netsh WLAN Refresh hostednetwork \[ data = \] Key**<br/>                                                                                                                                                                                                                                                                                       | Aggiornare la chiave di rete ospitata senza fili.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ setting = \] Security\]**<br/>                                                                                                                                                                                                                                                                     | Visualizza le informazioni sulla rete ospitata senza fili.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show Settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Visualizza le impostazioni globali della LAN wireless.<br/>           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della rete ospitata wireless e della condivisione della connessione Internet](using-hosted-network-and-internet-connection-sharing.md)
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

 

 
