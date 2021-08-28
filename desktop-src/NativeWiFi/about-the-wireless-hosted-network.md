---
description: Informazioni sulla rete wireless ospitata
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Informazioni sulla rete wireless ospitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88af34a1e0df2029c230b7b7800130d3b550dbf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882768"
---
# <a name="about-the-wireless-hosted-network"></a>Informazioni sulla rete wireless ospitata

La rete ospitata wireless è una nuova funzionalità WLAN supportata in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato. Questa funzionalità implementa due funzioni principali:

-   La virtualizzazione di una scheda wireless fisica in più schede wireless virtuali a volte definite Wi-Fi virtuali.
-   Un punto di accesso wireless basato su software viene talvolta definito SoftAP che usa una scheda wireless virtuale designata.

Queste due funzioni coesistono in un sistema Windows insieme. L'abilitazione o la disabilitazione della rete ospitata wireless abilita o disabilita sia l'Wi-Fi virtuale che SoftAP. Non è possibile abilitare o disabilitare queste due funzioni separatamente in Windows.

Con questa funzionalità, un computer Windows può usare una singola scheda wireless fisica per connettersi come client a un punto di accesso hardware (AP), fungendo allo stesso tempo da punto di accesso software che consente ad altri dispositivi con supporto wireless di connettersi ad esso. Questa funzionalità richiede l'installazione di una scheda wireless con funzionalità rete ospitata nel computer locale. Il driver per la scheda wireless deve implementare il modello di driver di dispositivo LAN wireless definito da Microsoft per l'uso Windows 7. Per ricevere il logo Windows 7, un driver wireless deve implementare la funzionalità Rete ospitata wireless.

Esiste al massimo una rete ospitata wireless abilitata in qualsiasi momento nel computer locale e solo una scheda wireless verrà usata dalla rete ospitata wireless. Se è presente più di una scheda wireless con supporto per la rete ospitata, Windows una scheda da usare con la rete ospitata wireless. Quando vengono usate le API di rete ospitata, la scheda wireless con supporto per la rete ospitata viene virtualizzata al massimo in 3 schede logiche:

-   Adattatore di stazione (STA) per l'uso da parte di applicazioni wireless client o ad hoc. L'adattatore STA eredita tutte le impostazioni della scheda wireless fisica originale e presenta gli stessi comportamenti della scheda fisica. Concettualmente, è possibile visualizzare la scheda STA come identica alla scheda fisica dopo la virtualizzazione. La scheda STA è sempre presente nel sistema, purché sia presente la scheda fisica wireless corrispondente.
-   Una scheda AP per l'uso da parte della rete ospitata wireless per ospitare SoftAP. L'adattatore AP è presente nel sistema Windows solo dopo che la rete ospitata wireless viene richiamata per la prima volta (quando viene chiamata per la prima volta la funzione [**WlanHostedNetworkStartUsing,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Dopo la creazione, la scheda AP rimarrà nel sistema fino a quando la rete ospitata wireless non viene disabilitata. Se la rete ospitata wireless viene abilitata in un secondo momento, la scheda AP verrà visualizzata di nuovo nel sistema.
-   Scheda di stazione virtuale (VSTA) per l'uso da parte dei fornitori di hardware per estendere la funzionalità rete ospitata wireless in Windows. L'adapter VSTA è facoltativo e può essere creato solo nel sistema dal servizio IHV corrispondente. A differenza dell'adapter AP, l'adapter VSTA esiste nel sistema Windows solo dal momento in cui il servizio IHV inizializza la scheda fino al momento in cui il servizio IHV rilascia l'adapter.

La Wi-Fi esegue il mapping delle schede LOGICHE alle porte NDIS. L'associazione degli adapter STA, AP e VSTA a porte NDIS specifiche viene deciso Windows. L'adapter STA è sempre associato alla porta 0. La scheda AP è associata alla successiva porta NDIS disponibile all'avvio della virtualizzazione e l'associazione rimane invariata fino al termine della virtualizzazione quando la rete ospitata wireless è disabilitata. L'adapter VSTA è associato alla successiva porta NDIS disponibile quando viene inizializzato dal servizio IHV corrispondente e l'associazione rimane invariata fino a quando non viene rilasciata dal servizio IHV.

È possibile creare l'adapter VSTA per l'uso da parte di IHV senza creare l'adapter SoftAP.

Le combinazioni seguenti sono valide per una scheda fisica con virtualizzazione:

-   Adattatore STA.
-   Adattatori STA e AP.
-   Adattatori STA e VSTA.
-   Adattatori STA, AP e VSTA.

Ad eccezione del caso dell'adattatore STA, tutte le altre combinazioni sono valide solo quando è abilitata la rete ospitata wireless. Per quanto riguarda il singolo caso di scheda STA, è la scheda fisica se la rete ospitata wireless è disabilitata. Se la rete ospitata wireless è abilitata, è la scheda STA quando la rete ospitata wireless non è mai stata richiamata nel sistema.

Il bridging di livello 2 non è consentito tra l'adattatore AP e qualsiasi altro adattatore nel sistema. La stessa restrizione si applica all'adapter VSTA quando è presente nel sistema.

La funzionalità Rete ospitata wireless in Windows implementa un SoftAP. Tuttavia, questo SoftAP non è progettato per sostituire i dispositivi AP wireless basati su hardware. In particolare, se la rete wireless ospitata è in esecuzione quando il computer passa alla sospensione (standby), all'ibernazione o prima del riavvio del computer, la rete ospitata wireless verrà arrestata. La rete ospitata wireless non verrà riavviata automaticamente dopo la ripresa della sospensione, dell'ibernazione o del riavvio del computer. SoftAP non fornisce inoltre la risoluzione DNS. Nel caso in cui un server DNS esterno non sia reso disponibile tramite Condivisione connessione Internet (vedere la discussione di ICS riportata di seguito), la risoluzione del nome di dominio completo (FQDN) tra due computer o dispositivi connessi con SoftAP, incluso il computer che ospita SoftAP, funzionerà solo se entrambe le entità contrassegnano il tipo di rete della rete SoftAP come PRIVATE (HOME o WORK nella finestra popup della categoria di rete). Poiché il computer che ospita SoftAP contrassegna sempre il tipo di rete SoftAP come PRIVATE, solo i computer o i dispositivi connessi a SoftAP devono contrassegnare il tipo di rete SoftAP come PRIVATE per consentire il funzionamento della risoluzione FQDN.

Le reti SoftAP e ad hoc si escludono a vicenda nella stessa scheda fisica. Se SoftAP è in esecuzione sulla scheda AP e un utente o un'applicazione avvia una rete ad hoc sulla scheda STA, SoftAP verrà arrestato. Se la rete ad hoc Iif è in esecuzione sulla scheda STA, il tentativo di avviare SoftAP sulla scheda AP avrà esito negativo.

Per fornire protezione per le comunicazioni wireless tra il computer che ospita SoftAP e i dispositivi che si connettono a SoftAP, la rete ospitata wireless richiede che tutti i dispositivi connessi usino la suite di crittografia WPA2-PSK/AES. La chiave condivisa è un valore di 63 caratteri generato da Windows quando la rete ospitata wireless viene richiamata per la prima volta (quando viene chiamata per la prima volta la funzione [**WlanHostedNetworkStartUsing,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Un utente o un'applicazione non può modificare il valore di questa chiave condivisa, ma un'applicazione può richiedere al sistema operativo di rigenerare una nuova chiave chiamando la funzione [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) oppure un utente può richiedere al sistema operativo di rigenerare una nuova chiave usando i comandi **netsh wlan.** Questa chiave condivisa è detta chiave primaria o di sistema per la rete ospitata wireless ed è persistente durante l'avvio e l'arresto della rete ospitata wireless. Questa chiave primaria è detta "chiave di sicurezza di sistema" nei **comandi netsh wlan.**

Per semplificare l'uso, la rete ospitata wireless supporta anche il concetto di chiave di sicurezza secondaria o utente più semplice da usare, ma che potrebbe essere meno sicura. Questa chiave secondaria è detta "chiave di sicurezza utente" nei **comandi netsh wlan.** La chiave secondaria non viene generata da Windows. L'utente deve fornire il valore per questa chiave. Un utente o un'applicazione può impostare o modificare il valore della chiave chiamando la funzione [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) o usando i **comandi netsh wlan.** La chiave secondaria può essere impostata come permanente o temporanea. Per una chiave temporanea, se la rete ospitata wireless è già in esecuzione, la chiave secondaria sarà valida fino all'arresto della rete ospitata wireless. Per una chiave temporanea, se la rete wireless ospitata non è in esecuzione, sarà valida solo tra l'avvio e l'arresto successivi della rete ospitata wireless.

Esiste esattamente una chiave primaria e al massimo una chiave secondaria per il wireless Hosted Hetwork in qualsiasi computer. Qualsiasi dispositivo di cui viene effettuato il provisioning Wi-Fi configurazione protetta (WPS) riceverà la chiave primaria. Altri dispositivi configurati manualmente possono usare una delle due chiavi. Ogni volta che viene modificata una chiave, qualsiasi dispositivo con il valore della chiave precedente non sarà in grado di connettersi alla rete wireless ospitata senza dover eseguire di nuovo il provisioning con la nuova chiave. Tuttavia, i dispositivi con l'altra chiave invariata continueranno a essere in grado di connettersi alla rete wireless ospitata.

Un'applicazione può registrarsi per le notifiche di rete ospitata wireless, quindi una notifica WLAN verrà inviata al callback dell'applicazione quando le proprietà cambiano nella rete ospitata wireless. Un'applicazione si registra per le notifiche di rete ospitata wireless chiamando [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) con il *parametro dwNotifSource* impostato per includere il bit WLAN \_ NOTIFICATION SOURCE \_ \_ HNWK.

Windows due modi per gli amministratori IT di gestire la funzionalità Rete ospitata wireless. Per i computer membri di un dominio, gli amministratori possono usare i criteri di gruppo per non consentire la rete ospitata wireless. Usando **i comandi netsh wlan,** un amministratore può abilitare o disabilitare la rete ospitata wireless in locale nel computer.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Scenari supportati per la rete wireless ospitata

La rete wireless ospitata consente due scenari principali per i Windows computer:

• Possibilità di fornire una rete PAN wireless per l'uso con vari altri dispositivi wireless.

• Condivisione connessione di rete per l'uso da parte di altri computer e dispositivi.

Il PAN wireless è lo scenario principale abilitato dalla rete ospitata wireless di per sé. Dopo l'avvio della rete ospitata wireless in un computer, qualsiasi dispositivo con supporto per WPA2-PSK/AES sarà in grado di connettersi al softAP come se si connette a un normale punto di accesso hardware. I dispositivi connessi alla rete ospitata wireless formano un PAN wireless, in cui sono in grado di scambiare informazioni con il computer Windows che ospita SoftAP e tra loro.

La condivisione delle connessioni di rete per l'uso da parte di altri computer e dispositivi richiede l'uso di Condivisione connessione Internet (ICS). In questo scenario, l'interfaccia pubblica di ICS è la connessione condivisa, mentre l'interfaccia privata è la scheda virtuale che ospita SoftAP. La connessione condivisa può essere una connessione Ethernet, LAN wireless o WAN wireless. Nel caso di una connessione LAN wireless, l'interfaccia pubblica di ICS può essere da un'altra scheda LAN wireless o dalla scheda virtuale della stazione sulla stessa scheda wireless fisica che ospita SoftAP. L'uso più comune per la condivisione di rete è la condivisione di una connessione Internet, in cui la rete nell'interfaccia pubblica di ICS ha accesso a Internet.

La rete ospitata wireless interagisce con Wi-Fi Protected Setup (WPS), un'altra importante nuova funzionalità in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. La rete ospitata wireless e WPS supportano uno scenario che effettua il provisioning di un dispositivo con supporto WPS per un punto di accesso hardware non compatibile con WPS. In questo caso, il SoftAP ospitato in Windows viene richiamato in background per eseguire il push del profilo AP hardware nel dispositivo con supporto WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Accesso utente e applicazione alla rete wireless ospitata

Gli utenti finali interagiscono con la funzionalità rete ospitata wireless in Windows tramite applicazioni di terze parti o **comandi netsh.** Attualmente non è disponibile un'interfaccia utente nativa per la configurazione o la gestione della rete ospitata wireless in Windows 7 o in Windows Server 2008 R2 con il servizio LAN wireless installato.

Le applicazioni di terze parti e **i comandi netsh** si basano sull'uso delle funzioni pubbliche di rete ospitata wireless. Questo set di funzioni offre un set completo di funzionalità per gestire la rete ospitata wireless in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato.

Di seguito è riportato un elenco delle funzioni della rete ospitata wireless e delle azioni comuni dal punto di vista dell'utente finale per cui verrà usata la funzione:



| Funzioni usate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Avviare la rete ospitata wireless.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Arrestare la rete ospitata wireless.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) [**WlanHostedNetworkSetSecondaryKey,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configurare le impostazioni della rete ospitata wireless (modificare l'SSID, modificare la chiave secondaria o richiedere la rigenerazione della chiave primaria).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) [**WlanHostedNetworkQuerySecondaryKey,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey) [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Eseguire query sulle impostazioni e sulle informazioni della rete ospitata wireless (stato, SSID, chiave secondaria, chiave primaria o un elenco dei dispositivi attualmente connessi).<br/> |



 

I **comandi netsh** sono destinati all'uso da parte di utenti avanzati o amministratori.

*Netsh.exe* contiene molti sottocomandi per la rete LAN wireless. Un elenco completo delle opzioni per **netsh** e LAN wireless è disponibile dal prompt dei comandi digitando quanto segue:

**netsh wlan /?**

La documentazione su tutti i comandi Netsh per la rete LAN wireless è disponibile anche online su Technet. Per altre informazioni, vedere [Comandi Netsh per WLAN (Wireless Local Area Network).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

Di seguito sono riportati alcuni **comandi netsh** comunemente usati con per la rete LAN wireless e la rete ospitata wireless, anche se sono supportate altre combinazioni di comandi:



| Comando                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Avviare la rete ospitata wireless.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Arrestare la rete ospitata wireless.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode= \] allow \| disallow**<br/>                                                                                                                                                                                                                                                                      | Abilitare o disabilitare la rete wireless ospitata.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid= \] &lt; ssid &gt; \[ key= \] &lt; passphrase &gt; \[ keyUsage= \] persistent \| temporary** <br/> | Configurare le impostazioni della rete ospitata wireless.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan refresh hostednetwork \[ data= \] key**<br/>                                                                                                                                                                                                                                                                                       | Aggiornare la chiave di rete ospitata wireless.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ setting= \] security\]**<br/>                                                                                                                                                                                                                                                                     | Visualizzare le informazioni sulla rete ospitata wireless.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Visualizzare le impostazioni globali della rete LAN wireless.<br/>           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Rete ospitata wireless e Condivisione connessione Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[Esempio di rete ospitata wireless](wireless-hosted-network-sample.md)
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

 

 
