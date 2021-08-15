---
description: Informazioni sulla rete wireless ospitata
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Informazioni sulla rete wireless ospitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f207dceaf0c835acc7886b48d5e6b030179240afb2a7f50b6f3744c574a185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801491"
---
# <a name="about-the-wireless-hosted-network"></a>Informazioni sulla rete wireless ospitata

La rete wireless ospitata è una nuova funzionalità WLAN supportata in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato. Questa funzionalità implementa due funzioni principali:

-   La virtualizzazione di una scheda wireless fisica in più di una scheda wireless virtuale talvolta definita Wi-Fi virtuale.
-   Un punto di accesso wireless basato su software (AP) talvolta definito come SoftAP che usa una scheda wireless virtuale designata.

Queste due funzioni coesistono in un sistema Windows insieme. L'abilitazione o la disabilitazione della rete ospitata wireless abilita o Wi-Fi virtuale e SoftAP. Non è possibile abilitare o disabilitare queste due funzioni separatamente in Windows.

Con questa funzionalità, un computer Windows può utilizzare una singola scheda wireless fisica per connettersi come client a un punto di accesso hardware (AP), pur fungendo da punto di accesso software che consente ad altri dispositivi con funzionalità wireless di connettersi a esso. Questa funzionalità richiede l'installazione di una scheda wireless con funzionalità rete ospitata nel computer locale. Il driver per la scheda wireless deve implementare il modello di driver di dispositivo LAN wireless definito da Microsoft per l'uso in Windows 7. Per ricevere il logo Windows 7, un driver wireless deve implementare la funzionalità rete ospitata wireless.

Nel computer locale è abilitata al massimo una rete wireless ospitata in qualsiasi momento e solo una scheda wireless verrà utilizzata dalla rete wireless ospitata. Se sono presenti più schede wireless che supportano la rete ospitata, Windows sceglierà una scheda da usare con la rete wireless ospitata. Quando vengono usate le API della rete ospitata, la scheda wireless che supporta la rete ospitata viene virtualizzata in un massimo di 3 schede logiche:

-   Un adattatore di stazione (STA) per l'uso da parte di applicazioni wireless client o ad hoc. L'adattatore STA eredita tutte le impostazioni della scheda wireless fisica originale e presenta gli stessi comportamenti della scheda fisica. Concettualmente, è possibile visualizzare la scheda STA come identica alla scheda fisica dopo la virtualizzazione. La scheda STA è sempre nel sistema, purché sia presente la scheda fisica wireless corrispondente.
-   Una scheda AP per l'uso da parte della rete ospitata wireless per ospitare SoftAP. La scheda AP è presente nel sistema Windows solo dopo che la rete ospitata wireless viene richiamata per la prima volta (quando viene chiamata per la prima volta la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Dopo la creazione, la scheda AP rimarrà nel sistema fino a quando la rete wireless ospitata non viene disabilitata. Se la rete wireless ospitata viene abilitata in un secondo momento, la scheda AP verrà nuovamente visualizzata nel sistema.
-   Scheda di stazione virtuale (VSTA) per l'uso da parte dei fornitori di hardware per estendere la funzionalità rete ospitata wireless in Windows. L'adapter VSTA è facoltativo e può essere creato solo nel sistema dal servizio IHV corrispondente. A differenza dell'adattatore AP, l'adapter VSTA esiste nel sistema Windows solo dal momento in cui il servizio IHV inizializza l'adattatore fino al momento in cui il servizio IHV rilascia l'adapter.

Il Wi-Fi esegue il mapping delle schede logiche alle porte NDIS. L'associazione delle schede STA, AP e VSTA a porte NDIS specifiche viene definita dal Windows. L'adattatore STA è sempre associato alla porta 0. La scheda AP è associata alla successiva porta NDIS disponibile all'avvio della virtualizzazione e l'associazione rimane invariata fino al termine della virtualizzazione quando la rete ospitata wireless è disabilitata. L'adapter VSTA è associato alla successiva porta NDIS disponibile quando viene inizializzato dal servizio IHV corrispondente e l'associazione rimane invariata fino a quando non viene rilasciata dal servizio IHV.

È possibile che l'adapter VSTA sia creato per l'uso da parte di IHV senza creare l'adapter SoftAP.

Le combinazioni seguenti sono valide per una scheda fisica con virtualizzazione:

-   Adapter STA.
-   Adattatori STA e AP.
-   Adapter STA e VSTA.
-   Adapter STA, AP e VSTA.

Ad eccezione del caso dell'adattatore STA, tutte le altre combinazioni sono valide solo quando è abilitata la rete ospitata wireless. Come per il caso della singola scheda STA, è la scheda fisica se la rete ospitata wireless è disabilitata. Se la rete wireless ospitata è abilitata, è la scheda STA quando la rete ospitata wireless non è mai stata richiamata nel sistema.

Il bridging di livello 2 non è consentito tra l'adattatore AP e qualsiasi altro adattatore nel sistema. La stessa restrizione si applica all'adapter VSTA quando è presente nel sistema.

La funzionalità rete ospitata wireless in Windows implementa un SoftAP. Tuttavia, questo SoftAP non è progettato per sostituire dispositivi AP wireless basati su hardware. In particolare, se la rete wireless ospitata è in esecuzione quando il computer passa alla modalità sospensione (standby), ibernazione o prima del riavvio del computer, la rete ospitata wireless verrà arrestata. La rete wireless ospitata non verrà riavviata automaticamente dopo la ripresa del computer da sospensione, ibernazione o riavvio. SoftAP non fornisce inoltre la risoluzione DNS. Nel caso in cui un server DNS esterno non sia reso disponibile tramite Condivisione connessione Internet (vedere la discussione di ICS riportata di seguito), la risoluzione del nome di dominio completo (FQDN) tra due computer o dispositivi connessi con SoftAP, incluso il computer che ospita SoftAP, funziona solo se entrambe le entità contrassegnano il tipo di rete della rete SoftAP come PRIVATE (HOME o WORK nella categoria di rete popup). Poiché il computer che ospita SoftAP contrassegna sempre il tipo di rete SoftAP come PRIVATE, solo i computer o i dispositivi connessi a SoftAP devono contrassegnare il tipo di rete SoftAP come PRIVATE per consentire il funzionamento della risoluzione FQDN.

Le reti SoftAP e ad hoc si escludono a vicenda sulla stessa scheda fisica. Se SoftAP è in esecuzione nella scheda AP e un utente o un'applicazione avvia una rete ad hoc sulla scheda STA, SoftAP verrà arrestato. Se la rete ad hoc Iif è in esecuzione sulla scheda STA, un tentativo di avviare SoftAP sulla scheda AP avrà esito negativo.

Per garantire la protezione per le comunicazioni wireless tra il computer che ospita SoftAP e i dispositivi che si connettono a SoftAP, la rete ospitata wireless richiede che tutti i dispositivi connessi usino la suite di crittografia WPA2-PSK/AES. La chiave condivisa è un valore di 63 caratteri generato da Windows quando la rete ospitata wireless viene richiamata per la prima volta (quando viene chiamata per la prima volta la funzione [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Un utente o un'applicazione non può modificare il valore di questa chiave condivisa, ma un'applicazione può richiedere al sistema operativo di rigenerare una nuova chiave chiamando la funzione [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) oppure un utente può richiedere al sistema operativo di rigenerare una nuova chiave usando i comandi **netsh wlan.** Questa chiave condivisa è denominata chiave primaria o di sistema per la rete wireless ospitata ed è persistente all'avvio e all'arresto della rete wireless ospitata. Questa chiave primaria è denominata "chiave di sicurezza di sistema" nei **comandi netsh wlan.**

Per semplificare l'uso, la rete ospitata wireless supporta anche il concetto di chiave di sicurezza secondaria o utente più semplice da usare, ma che potrebbe essere meno sicura. Questa chiave secondaria è denominata "chiave di sicurezza utente" nei **comandi netsh wlan.** La chiave secondaria non viene generata da Windows. L'utente deve fornire il valore per questa chiave. Un utente o un'applicazione può impostare o modificare il valore della chiave chiamando la funzione [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) o usando i **comandi netsh wlan.** La chiave secondaria può essere impostata come persistente o temporanea. Per una chiave temporanea, se la rete wireless ospitata è già in esecuzione, la chiave secondaria sarà valida fino a quando la rete wireless ospitata si arresta. Per una chiave temporanea, se la rete wireless ospitata non è in esecuzione, sarà valido solo tra l'avvio e l'arresto della rete wireless successiva.

Esiste esattamente una chiave primaria e al massimo una chiave secondaria per l'ambiente Wireless Hosted Hetwork in qualsiasi computer. Tutti i dispositivi di cui è stato Wi-Fi'installazione protetta riceveranno la chiave primaria. Altri dispositivi configurati manualmente possono usare entrambe le chiavi. Ogni volta che viene modificata una chiave, qualsiasi dispositivo con il valore di chiave precedente non sarà in grado di connettersi alla rete ospitata wireless senza dover eseguire nuovamente il provisioning con la nuova chiave. Tuttavia, i dispositivi con l'altra chiave non modificata continueranno a essere in grado di connettersi alla rete wireless ospitata.

Un'applicazione può registrarsi per le notifiche di rete ospitata wireless, in modo che una notifica WLAN verrà inviata al callback dell'applicazione quando le proprietà cambiano nella rete ospitata wireless. Un'applicazione si registra per le notifiche di rete ospitata wireless chiamando [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) con il *parametro dwNotifSource impostato* per includere il bit WLAN \_ NOTIFICATION SOURCE \_ \_ HNWK.

Windows offre agli amministratori IT due modi per gestire la funzionalità Rete ospitata wireless. Per i computer membri di un dominio, gli amministratori possono utilizzare criteri di gruppo per non consentire la rete wireless ospitata. Usando **i comandi netsh wlan,** un amministratore può abilitare o disabilitare la rete ospitata wireless in locale nel computer.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Scenari supportati per la rete ospitata wireless

La rete wireless ospitata consente due scenari principali per Windows computer:

• Possibilità di fornire una rete PAN wireless per l'uso con vari altri dispositivi wireless.

• Condivisione delle connessioni di rete per l'uso da parte di altri computer e dispositivi.

Il PAN wireless è lo scenario principale abilitato dalla rete wireless ospitata da solo. Dopo l'avvio della rete wireless ospitata in un computer, qualsiasi dispositivo che supporta WPA2-PSK/AES sarà in grado di connettersi al softAP come se si connette a un normale punto di accesso hardware. I dispositivi connessi alla rete ospitata wireless formano un PAN wireless, in cui sono in grado di scambiare informazioni con il computer Windows che ospita softAP e tra loro.

La condivisione delle connessioni di rete per l'uso da parte di altri computer e dispositivi richiede l'uso di Condivisione connessione Internet (ICS). In questo scenario, l'interfaccia pubblica di ICS è la connessione condivisa, mentre l'interfaccia privata è la scheda virtuale che ospita SoftAP. La connessione condivisa può essere una connessione Ethernet, LAN wireless o WAN wireless. Nel caso di una connessione LAN wireless, l'interfaccia pubblica di ICS può essere da un'altra scheda LAN wireless o la scheda virtuale stazione sulla stessa scheda wireless fisica che ospita il SoftAP. L'uso più comune per la condivisione di rete è la condivisione di una connessione Internet, in cui la rete nell'interfaccia pubblica di ICS ha accesso a Internet.

La rete ospitata wireless interagisce con Wi-Fi Protected Setup (WPS), un'altra importante nuova funzionalità in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. La rete ospitata wireless e WPS supportano uno scenario che effettua il provisioning di un dispositivo che supporta WPS per un punto di accesso hardware non compatibile con WPS. In questo caso, il softap ospitato in Windows viene richiamato in background per eseguire il push del profilo ap hardware nel dispositivo che supporta WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Accesso utente e applicazione alla rete wireless ospitata

Gli utenti finali interagiscono con la funzionalità Rete ospitata wireless in Windows usando applicazioni di terze parti o **comandi netsh.** Attualmente non è disponibile alcuna interfaccia utente nativa per la configurazione o la gestione della rete ospitata wireless in Windows 7 o in Windows Server 2008 R2 con il servizio LAN wireless installato.

Le applicazioni di terze parti e **i comandi netsh** si basano sull'uso delle funzioni pubbliche della rete wireless ospitata. Questo set di funzioni fornisce un set completo di funzionalità per gestire la rete ospitata wireless in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato.

Di seguito è riportato un elenco delle funzioni della rete ospitata wireless e delle azioni comuni dal punto di vista dell'utente finale per cui verrebbe usata la funzione:



| Funzioni usate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Avviare la rete ospitata wireless.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Arrestare la rete ospitata wireless.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) [**WlanHostedNetworkSetSecondaryKey,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configurare le impostazioni della rete ospitata wireless (modificare l'SSID, modificare la chiave secondaria o richiedere la rigenerazione della chiave primaria).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) [**WlanHostedNetworkQuerySecondaryKey,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey) [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Eseguire query sulle impostazioni e sulle informazioni della rete ospitata wireless (stato, SSID, chiave secondaria, chiave primaria o un elenco dei dispositivi attualmente connessi).<br/> |



 

I **comandi netsh** sono destinati all'uso da parte di utenti avanzati o amministratori.

*Netsh.exe* include molti sottocomandi per la rete LAN wireless. Un elenco completo delle opzioni per **netsh** e LAN wireless è disponibile dal prompt dei comandi digitando quanto segue:

**netsh wlan /?**

La documentazione su tutti i comandi Netsh per la rete LAN wireless è disponibile anche online su Technet. Per altre informazioni, vedere [Comandi Netsh per WLAN (Wireless Local Area Network).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

Di seguito sono riportati alcuni **comandi netsh** comunemente usati con per la rete LAN wireless e la rete ospitata wireless, anche se sono supportate altre combinazioni di comandi:



| Comando                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Avviare la rete ospitata wireless.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Arrestare la rete ospitata wireless.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode= \] allow \| disallow**<br/>                                                                                                                                                                                                                                                                      | Abilitare o disabilitare la rete wireless ospitata.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid= \] <ssid> \[ key= \] <passphrase> \[ keyUsage= \] persistent \| temporary** <br/> | Configurare le impostazioni della rete ospitata wireless.<br/> |
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

 

 
