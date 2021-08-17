---
description: Elenco del contenuto di riferimento per l'API Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Indice di API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e61a3f738905e98ad9cd1db85dbaa1746d7c613b1cc5b628805bcc3ddbea74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737638"
---
# <a name="windows-api-index"></a>Indice di API Windows

Di seguito è riportato un elenco del contenuto di riferimento per l Windows APP (Application Programming Interface) per applicazioni desktop e server.

Usando l'API Windows, è possibile sviluppare applicazioni che vengono eseguite correttamente in tutte le versioni di Windows sfruttando al tempo stesso le funzionalità e le funzionalità specifiche di ogni versione. Si noti che in precedenza si chiamava API Win32. Il nome Windows'API riflette in modo più accurato le radici nel Windows a 16 bit e il relativo supporto su Windows a 64 bit.

## <a name="user-interface"></a>Interfaccia utente

L Windows'API dell'interfaccia utente crea e usa le finestre per visualizzare l'output, richiedere l'input dell'utente ed eseguire le altre attività che supportano l'interazione con l'utente. La maggior parte delle applicazioni crea almeno una finestra.

-   [Accessibilità](../winauto/windows-accessibility-features-reference.md)
-   [Gestione finestre desktop (DWM)](../dwm/reference.md)
-   [Servizi di globalizzazione](../intl/globalization-services.md)
-   [Valori DPI alti](../hidpi/high-dpi-reference.md)
-   [interfaccia utente multilingue (MUI)](../intl/multilingual-user-interface-reference.md)
-   [Supporto linguistico nazionale (NLS)](../intl/national-language-support-reference.md)
-   [Interfaccia utente elementi :](../devnotes/user-interface.md)

    -   [Pulsanti](../controls/bumper-button-button-control-reference.md)
    -   [Caret](../menurc/caret-functions.md)
    -   [Caselle combinate](../controls/bumper-combobox-combobox-control-reference.md)
    -   [Finestre di dialogo comuni](../dlgbox/common-dialog-box-reference.md)
    -   [Controlli comuni](../controls/individual-control-info.md)
    -   [Cursori](../menurc/cursor-reference.md)
    -   [Finestre di dialogo](../dlgbox/dialog-box-reference.md)
    -   [Modificare i controlli](../controls/bumper-edit-control-edit-control-reference.md)
    -   [Controlli Intestazione](../controls/bumper-header-control-header-control-reference.md)
    -   [Icone](../menurc/icon-reference.md)
    -   [Tasti di scelta rapida](../menurc/keyboard-accelerator-reference.md)
    -   [Caselle di riepilogo](../controls/bumper-list-box-list-box-control-reference.md)
    -   [Controlli di visualizzazione elenco](../controls/bumper-list-view-list-view-control-reference.md)
    -   [Menu](../menurc/menu-reference.md)
    -   [Barre di stato](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [Finestre delle proprietà](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Controlli Rich Edit](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [Barre di scorrimento](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [Controlli statici](../controls/bumper-static-control-static-control-reference.md)
    -   [Stringhe](../menurc/string-reference.md)
    -   [Barre degli strumenti](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [Descrizioni comandi](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [Trackbar](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [Controlli visualizzazione struttura ad albero](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Windows Gestione animazioni](../uianimation/windows-animation-reference.md)
-   [Windows Framework della barra multifunzione](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>Windows ambiente (Shell)

-   [Windows Sistema di proprietà](../properties/property-system-reference.md)
-   [Windows Guscio](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows Search](../search/-search-reference-entry-page.md)
-   [Console](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>Input e messaggi utente

-   [Interazione dell'utente](../user-interaction.md)
    -   [Manipolazione diretta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [Input penna](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [Configurazione dei commenti e suggerimenti di input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [Contesto di interazione](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [Stack di input del dispositivo puntatore](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [Messaggi e notifiche di input del puntatore](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [Input del controller radiale](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Text Services Framework](../tsf/text-services-framework.md)
    -   [Hit testing tocco](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [Inserimento tocco](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [Interazione dell'utente legacy](../legacy-user-interaction-features.md)
    -   [Input tocco](../wintouch/windows-touch-portal.md)
    -   [Input da tastiera](../inputdev/keyboard-input.md)
    -   [Mouse Input](../inputdev/mouse-input.md)
    -   [Input non elaborato](../inputdev/raw-input.md)
-   [Windows e Messaggi](../winmsg/windowing.md):

    -   [Messaggi e code di messaggi](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [Classi window](../winmsg/window-class-reference.md)
    -   [Procedure della finestra](../winmsg/window-procedure-reference.md)
    -   [Timer](../winmsg/timer-reference.md)
    -   [Proprietà finestra](../winmsg/window-property-reference.md)
    -   [Hook](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a>Accesso ai dati e archiviazione di questi

-   [Servizio trasferimento intelligente in background (BITS)](../bits/bits-reference.md)
-   [Backup dei dati](../backup/backup.md)
    -   [Backup](../backup/backup-reference.md)
    -   [Deduplicazione dati](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [Copia shadow del volume](../vss/volume-shadow-copy-reference.md)
    -   [Windows Server Backup](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   [Dati Exchange](../dataxchg/data-exchange.md):

    -   [Appunti](../dataxchg/clipboard-reference.md)
    -   [Dynamic Data Exchange (DDE)](../dataxchg/dynamic-data-exchange-reference.md)
    -   [Dynamic Data Exchange Management (DDEML)](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [Gestione directory](../fileio/directory-management-reference.md)
-   [Gestione disco](../fileio/disk-management-reference.md)
-   [File system distribuito (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [Replica DFS](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [Motore Archiviazione estendibile](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [File e I/O (file system)](../fileio/file-management-reference.md)
-   [API libreria di individuazione iSCSI](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [File offline](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [Packaging](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [Compressione differenziale remota](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [NTFS transazionale](../fileio/transactional-ntfs-reference.md)
-   [Gestione dei volumi](../fileio/volume-management-reference.md)
-   [Disco rigido virtuale (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))
-   [Gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))
    -   [Microsoft Open Database Connectivity (ODBC)](/sql/odbc/reference/syntax/odbc-reference)
    -   [Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))
    -   [Microsoft ActiveX Data Objects (ADO)](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a>Diagnostica

[L'API Diagnostica](/previous-versions//bb648685(v=vs.85)) consente di risolvere i problemi dell'applicazione o del sistema e di monitorare le prestazioni.

-   [Ripristino e riavvio di un'applicazione](../recovery/application-recovery-and-restart-reference.md)
-   [Debug](../debug/debugging-reference.md)
-   [Gestione degli errori](../debug/error-handling-reference.md)
-   [Registrazione degli eventi](../eventlog/event-logging-reference.md)
-   [Traccia eventi](../etw/event-tracing-reference.md)
-   [Profilatura del contatore hardware (HCP)](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [Framework di diagnostica di rete (NDF)](../ndf/ndf-reference.md)
-   [Network Monitor](../netmon2/reference.md)
-   [Contatori delle prestazioni](../perfctrs/performance-counters-reference.md)
-   [Avvisi e registri di prestazioni (PLA)](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [Creazione di snapshot dei processi](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [Stato processo (PSAPI)](../psapi/psapi-reference.md)
-   [Gestione delle eccezioni strutturata](../debug/structured-exception-handling-reference.md)
-   [Monitor di sistema](../sysmon/system-monitor-reference.md)
-   [Attraversamento della catena di attesa](../debug/wait-chain-traversal.md)
-   [Segnalazione errori Windows](../wer/wer-reference.md)
-   [Registro eventi di Windows](../wes/windows-event-log-reference.md)
-   [Piattaforma di risoluzione dei problemi Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>Elementi grafici e multimediali

Le [API grafica,](/previous-versions//aa969176(v=vs.85)) [multimediale, audio](../audio-and-video.md) e video consentono alle applicazioni di incorporare testo formattato, grafica, audio e video.

-   [Audio di base](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [Graphics Device Interface (GDI)](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [Streaming multimediale](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft Media Foundation](../medfound/media-foundation-programming-reference.md)
-   [Tecnologie tv Microsoft](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [Opengl](../opengl/opengl-reference.md)
-   [Monitorare la configurazione](../monitor/monitor-configuration-reference.md)
-   [Più monitor di visualizzazione](../gdi/multiple-display-monitors-reference.md)
-   [Acquisizione di immagini](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Windows Sistema di colori](../wcs/reference.md)
-   [Windows Imaging Component (WIC)](../wic/-wic-codec-reference.md)
-   [Windows Codec e DSP audio e video multimediali](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Formato Windows Media](../wmformat/programming-reference.md)
-   [Windows Servizi di condivisione libreria multimediale](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Windows Media Player](../wmp/windows-media-player-object-model-reference.md)
-   [Servizi Windows Media](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Windows Multimediale](../multimedia/multimedia-reference.md)

## <a name="devices"></a>Dispositivi

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [Risorse per le comunicazioni](../devio/communications-reference.md)
-   [Accesso dei dispositivi](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [Gestione dei dispositivi](../devio/device-management-reference.md)
-   [Archiviazione avanzata](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [Individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [Mastering delle immagini](../imapi/imapi-reference.md)
-   [Posizione](../locationapi/windows-location-programming-reference.md)
-   [Database di associazione PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [Stampa](/windows-hardware/drivers/print/introduction-to-printing)
    -   [Spooler di stampa](../printdocs/printing-and-print-spooler-reference.md)
    -   [Stampare un pacchetto di documenti](../printdocs/tailored-app-printing-api.md)
    -   [Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [Print Ticket](../printdocs/print-ticket-api.md)
    -   [Stampa XPS](../printdocs/xpsprint-api.md)
-   [Sensori](../sensorsapi/sensor-api-programming-reference.md)
-   [System Event Notification Service (SENS)](../sens/sens-reference.md)
-   [Guida dello strumento](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [Servizi Web nei dispositivi](../wsdapi/web-services-for-devices-reference.md)
-   [Acquisizione di immagini di Windows (WIA)](../wia/-wia-reference.md)
-   [Windows Gestione dispositivi multimediali](../wmdm/programming-reference.md)
-   [Windows Dispositivi portatili](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>Servizi di sistema

Le [API di](/previous-versions//aa969179(v=vs.85)) Servizi di sistema consentono alle applicazioni di accedere alle risorse del computer e alle funzionalità del sistema operativo sottostante, ad esempio memoria, file system, dispositivi, processi e thread.

-   [COM](../com/reference.md)
-   [COM+](../cossdk/com--reference.md)
-   [API di compressione](../cmpapi/-compression-portal.md)
-   [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [Librerie a collegamento dinamico (DLL)](../dlls/dynamic-link-library-functions.md)
-   [API della Guida](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [Comunicazioni interprocesso:](../ipc/interprocess-communications.md)
    -   [Mailslot](../ipc/mailslot-functions.md)
    -   [Pipe](../ipc/pipe-functions.md)
-   [Gestione transazioni kernel (KTM)](../ktm/ktm-reference.md)
-   [Gestione della memoria](../memory/memory-management-reference.md)
-   [Registratore dell'operazione](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [Risparmio energia](../power/power-management-reference.md)
-   [Servizi Desktop remoto](../termserv/terminal-services-reference.md)
-   [Processi](../procthread/process-and-thread-reference.md)
-   [Services](../services/service-reference.md)
-   [Sincronizzazione](../sync/synchronization-reference.md)
-   [Thread](../procthread/process-and-thread-reference.md)
-   [Windows Condivisione desktop](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Windows System Information](../sysinfo/windows-system-information.md)
    -   [Handle e oggetti](../sysinfo/handle-and-object-functions.md)
    -   [Registro](../sysinfo/registry-reference.md)
    -   [Time](../sysinfo/time-reference.md)
    -   [Provider di tempo](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>Sicurezza e identità

Le [API Di sicurezza e](../devnotes/security.md) identità abilitano l'autenticazione delle password all'accesso, la protezione discrezionale per tutti gli oggetti di sistema con condivisione, il controllo degli accessi con privilegi, rights management e il controllo di sicurezza.

-   [autenticazione](../secauthn/authentication-reference.md)
-   [Autorizzazione](../secauthz/authorization-reference.md)
-   [Registrazione di certificati](../seccertenroll/certificate-enrollment-api-reference.md)
-   [Crittografia](../seccrypto/cryptography-reference.md)
-   [Cryptographic Next Generation (CNG)](../seccng/cng-reference.md)
-   [Servizi directory](/previous-versions//ms682458(v=vs.85))
    -   [Active Directory Domain Services](../ad/active-directory-domain-services-reference.md)
    -   [Active Directory Service Interfaces (ADSI)](../adsi/adsi-reference.md)
-   [EAP (Extensible Authentication Protocol)](../eap/extensible-authentication-protocol-reference.md)
-   [EAPHost (Extensible Authentication Protocol Host)](../eaphost/about-eap-host.md)
-   [Gestione delle password MS-CHAP](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [Protezione accesso alla rete (NAP)](../nap/nap-reference.md)
-   [Estensioni del server dei criteri di rete](../nps/ias-internet-authentication-service-reference.md)
-   [Controllo genitori](../parcon/parental-controls-reference.md)
-   [Provider WMI di sicurezza](../secprov/security-wmi-providers-reference.md)
-   [Servizi di base TPM (TBS)](../tbs/tbs-reference.md)
-   [Windows Biometric Framework](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>Installazione e manutenzione di applicazioni

-   [Games Explorer](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [Assembly side-by-side](../sbscs/side-by-side-assemblies-reference.md)
-   [Creazione di pacchetti, distribuzione ed API di query](../appxpkg/api-reference.md
)
-   [Licenza per sviluppatori](../devlic/developer-license-apis.md)
-   [Gestione riavvio](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>Amministratore e gestione del sistema

Le [interfacce di amministrazione](../srvnodes/system-administration.md) del sistema consentono di installare, configurare e eseguire il servizio di applicazioni o sistemi.

-   [dati configurazione di avvio provider WMI](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [Cluster di failover](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [Gestione risorse file server](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [Microsoft Management Console (MMC) 2.0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [Impostazioni Infrastruttura di gestione](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [Gestione licenze software](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [Gestione riavvio](../rstmgr/restart-manager-portal.md)
-   [Impostazioni Infrastruttura di gestione](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Ripristino configurazione di sistema](../sr/system-restore-portal.md)
-   [Arresto del sistema](../shutdown/system-shutdown.md)
-   [Utilità di pianificazione](../taskschd/task-scheduler-start-page.md)
-   [Registrazione accesso utenti](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Server virtuale Microsoft](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [Provider di Bilanciamento carico di rete](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [Windows Defender WMI v2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Servizi di distribuzione Windows](../wds/windows-deployment-services-portal.md)
-   [Windows Vantaggio originale](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Windows Infrastruttura di gestione](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [Strumentazione gestione Windows (WMI)](../wmisdk/wmi-reference.md)
-   [Gestione remota Windows](../winrm/portal.md)
-   [Windows Protezione delle risorse](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Windows Strumento di valutazione del sistema](../winsat/winsat-reference.md)
-   [Agente di Windows Update](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>Rete e Internet

Le [API](../devnotes/networking.md) di rete consentono la comunicazione tra le applicazioni in rete. È anche possibile creare e gestire l'accesso alle risorse condivise, ad esempio directory e stampanti di rete.

-   [Domain Name System (DNS)](../dns/dns-reference.md)
-   [Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [Servizio Fax](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [Connessione guidata](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [HTTP Server](../http/http-server-api-reference.md)
-   [Condivisione connessione Internet e firewall](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [Helper IP](../iphlp/ip-helper-function-reference.md)
-   [IPv6 Internet Connection Firewall](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [Management Information Base](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [Accodamento messaggi (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [Multicast Address Dynamic Client Allocation Protocol (MADCAP)](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [Nat (Network Address Translation)](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [Network List Manager (NLM)](../nla/network-list-manager-api-reference.md)
-   [Gestione di rete](../netmgmt/network-management-reference.md)
-   [Gestione condivisione di rete](../netshare/network-share-management-reference.md)
-   [Peer-to-peer](../p2psdk/portal.md)
-   [Qualità del servizio (QOS)](/previous-versions/windows/desktop/qos/qos-reference)
-   [Chiamata di procedura remota](../rpc/reference.md)
-   [Servizio routing e accesso remoto (RAS)](../rras/portal.md)
-   [Simple Network Management Protocol (SNMP)](../snmp/snmp-reference.md)
-   [Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [TapI (Telephony Application Programming Interface)](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [Componente del protocollo WebSocket](../websock/web-socket-protocol-component-api-portal.md)
-   Rete wireless:
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [Irda](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [Mobile Broadband](../mbn/mobile-broadband-networks-api-reference.md)
    -   [Wifi nativo](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect Now](../wcn/windows-connect-now-reference.md)
    -   [Gestione connessioni Windows](../wcm/windows-connection-manager-reference.md)
-   [Piattaforma filtro Windows](../fwp/fwp-reference.md)
-   [Windows Firewall con sicurezza avanzata](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [Windows Servizi HTTP (WinHTTP)](../winhttp/winhttp-reference.md)
-   [Windows Internet (WinINet)](../wininet/wininet-reference.md)
-   [Windows Rete (WNet)](../wnet/windows-networking-reference.md)
-   [Windows Virtualizzazione di rete](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [Windows Piattaforma RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows Socket (Winsock)](../winsock/winsock-reference.md)
-   [Windows Servizi Web](../wsw/windows-web-services-reference.md)
-   [Richiesta estesa HTTP XML](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>API deprecate o legacy

Di seguito sono riportate le tecnologie e le API non più recenti o che sono state sostituite o deprecate dai sistemi operativi Windows client e server.

-   [Directmusic](/previous-versions/ms807133(v=msdn.10))
-   [Directsound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   [Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) è ora incluso in [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).
-   [DDE (Network Dynamic Data Exchange)](../ipc/network-dde-reference.md)
-   [Servizio di installazione remota:](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)) [usare Windows distribuzione.](../wds/windows-deployment-services-portal.md)
-   [Virtual Disk Service (VDS):](../vds/vds-reference.md)usare [gestione Windows Archiviazione virtuale.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   Servizi terminal: usare [Servizi Desktop remoto](../termserv/terminal-services-reference.md).
-   [Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))
-   [Windows di messaggistica (MAPI):](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi) [usare Office MAPI.](/previous-versions/office/developer/office-2007/cc765775(v=office.12))
-   [Windows Platform Platform:](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal)crea invece app UWP.
-   [Windows sidebar:](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry)crea invece app UWP.
-   [Windows SideShow: nessuna](/previous-versions//ms744179(v=vs.85))sostituzione.
-   [Effetti bitmap WPF](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
