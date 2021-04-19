---
description: Elenco di contenuto di riferimento per l'API Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Indice di API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cace235af1c729e450bdf99b276eca1bfc000
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323867"
---
# <a name="windows-api-index"></a>Indice di API Windows

Di seguito è riportato un elenco del contenuto di riferimento per l'API di Windows Application Programming Interface per applicazioni desktop e server.

Utilizzando l'API Windows, è possibile sviluppare applicazioni in grado di funzionare correttamente in tutte le versioni di Windows sfruttando al contempo le funzionalità e le funzionalità univoche per ogni versione. Si noti che in precedenza era denominata API Win32. Il nome API Windows riflette più accuratamente le sue radici in Windows a 16 bit e il relativo supporto in Windows a 64 bit.

## <a name="user-interface"></a>Interfaccia utente

L'API dell'interfaccia utente di Windows crea e usa Windows per visualizzare l'output, richiedere l'input dell'utente ed eseguire le altre attività che supportano l'interazione con l'utente. La maggior parte delle applicazioni crea almeno una finestra.

-   [Accessibilità](../winauto/windows-accessibility-features-reference.md)
-   [Gestione finestre desktop (DWM)](../dwm/reference.md)
-   [Servizi di globalizzazione](../intl/globalization-services.md)
-   [Valori DPI alti](../hidpi/high-dpi-reference.md)
-   [Interfaccia utente multilingue (MUI)](../intl/multilingual-user-interface-reference.md)
-   [NLS (National Language Support)](../intl/national-language-support-reference.md)
-   [Elementi dell'interfaccia utente](../devnotes/user-interface.md):

    -   [Pulsanti](../controls/bumper-button-button-control-reference.md)
    -   [CARETS](../menurc/caret-functions.md)
    -   [Caselle combinate](../controls/bumper-combobox-combobox-control-reference.md)
    -   [Finestre di dialogo comuni](../dlgbox/common-dialog-box-reference.md)
    -   [Controlli comuni](../controls/individual-control-info.md)
    -   [Cursori](../menurc/cursor-reference.md)
    -   [Finestre di dialogo](../dlgbox/dialog-box-reference.md)
    -   [Controlli di modifica](../controls/bumper-edit-control-edit-control-reference.md)
    -   [Controlli intestazione](../controls/bumper-header-control-header-control-reference.md)
    -   [Icone](../menurc/icon-reference.md)
    -   [Tasti di scelta rapida](../menurc/keyboard-accelerator-reference.md)
    -   [Caselle di riepilogo](../controls/bumper-list-box-list-box-control-reference.md)
    -   [Controlli elenco-visualizzazione](../controls/bumper-list-view-list-view-control-reference.md)
    -   [Menu](../menurc/menu-reference.md)
    -   [Indicatori di stato](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [Finestre delle proprietà](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Controlli Rich Edit](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [Barre di scorrimento](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [Controlli statici](../controls/bumper-static-control-static-control-reference.md)
    -   [Stringhe](../menurc/string-reference.md)
    -   [Barre degli strumenti](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [Descrizioni comandi](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [TrackBar](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [Controlli di visualizzazione albero](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Gestione animazioni Windows](../uianimation/windows-animation-reference.md)
-   [Framework della barra multifunzione di Windows](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>Ambiente Windows (Shell)

-   [Sistema di proprietà di Windows](../properties/property-system-reference.md)
-   [Shell di Windows](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows Search](../search/-search-reference-entry-page.md)
-   [Console](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>Input utente e messaggistica

-   [Interazione dell'utente](../user-interaction.md)
    -   [Manipolazione diretta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [Input input penna](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [Configurazione feedback input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [Contesto di interazione](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [Stack di input del dispositivo puntatore](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [Notifiche e messaggi di input del puntatore](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [Input del controller radiale](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Text Services Framework](../tsf/text-services-framework.md)
    -   [Hit testing tocco](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [Touch Injection](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [Interazione utente legacy](../legacy-user-interaction-features.md)
    -   [Input tocco](../wintouch/windows-touch-portal.md)
    -   [Input da tastiera](../inputdev/keyboard-input.md)
    -   [Input del mouse](../inputdev/mouse-input.md)
    -   [Input non elaborato](../inputdev/raw-input.md)
-   [Windows e messaggi](../winmsg/windowing.md):

    -   [Messaggi e code di messaggi](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [Classi finestra](../winmsg/window-class-reference.md)
    -   [Routine della finestra](../winmsg/window-procedure-reference.md)
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
-   [Scambio di dati](../dataxchg/data-exchange.md):

    -   [Appunti](../dataxchg/clipboard-reference.md)
    -   [Dynamic Data Exchange (DDE)](../dataxchg/dynamic-data-exchange-reference.md)
    -   [Gestione Dynamic Data Exchange (DDEML)](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [Gestione directory](../fileio/directory-management-reference.md)
-   [Gestione disco](../fileio/disk-management-reference.md)
-   [File system distribuito (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [Replica DFS](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [Motore di archiviazione estendibile](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [File e I/O (file system locale)](../fileio/file-management-reference.md)
-   [API della libreria di individuazione iSCSI](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
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

L'API di [diagnostica](/previous-versions//bb648685(v=vs.85)) consente di risolvere i problemi dell'applicazione o del sistema e di monitorare le prestazioni.

-   [Ripristino e riavvio di un'applicazione](../recovery/application-recovery-and-restart-reference.md)
-   [Debug](../debug/debugging-reference.md)
-   [Gestione degli errori](../debug/error-handling-reference.md)
-   [Registrazione degli eventi](../eventlog/event-logging-reference.md)
-   [Traccia eventi](../etw/event-tracing-reference.md)
-   [Profilatura del contatore hardware (HPC)](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [Framework di diagnostica di rete (NDF)](../ndf/ndf-reference.md)
-   [Network Monitor](../netmon2/reference.md)
-   [Contatori delle prestazioni](../perfctrs/performance-counters-reference.md)
-   [Avvisi e registri di prestazioni (PLA)](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [Elabora istantanee](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [Stato del processo (PSAPI)](../psapi/psapi-reference.md)
-   [Gestione strutturata delle eccezioni](../debug/structured-exception-handling-reference.md)
-   [Monitor di sistema](../sysmon/system-monitor-reference.md)
-   [Attraversamento della catena di attesa](../debug/wait-chain-traversal.md)
-   [Segnalazione errori Windows](../wer/wer-reference.md)
-   [Registro eventi di Windows](../wes/windows-event-log-reference.md)
-   [Piattaforma di risoluzione dei problemi Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>Elementi grafici e multimediali

Le API [grafiche, multimediali,](/previous-versions//aa969176(v=vs.85)) [audio e video](../audio-and-video.md) consentono alle applicazioni di incorporare testo formattato, grafica, audio e video.

-   [Audio di base](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [Graphics Device Interface (GDI)](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [Flussi multimediali](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft Media Foundation](../medfound/media-foundation-programming-reference.md)
-   [Tecnologie Microsoft TV](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [OpenGL](../opengl/opengl-reference.md)
-   [Configurazione del monitoraggio](../monitor/monitor-configuration-reference.md)
-   [Più monitor di visualizzazione](../gdi/multiple-display-monitors-reference.md)
-   [Acquisizione immagine](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Sistema colori Windows](../wcs/reference.md)
-   [Windows Imaging Component (WIC)](../wic/-wic-codec-reference.md)
-   [Windows Media Audio e codec video e DSP](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Formato Windows Media](../wmformat/programming-reference.md)
-   [Servizi di condivisione libreria Windows Media](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Windows Media Player](../wmp/windows-media-player-object-model-reference.md)
-   [Servizi Windows Media](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Multimedia di Windows](../multimedia/multimedia-reference.md)

## <a name="devices"></a>Dispositivi

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [Risorse di comunicazione](../devio/communications-reference.md)
-   [Accesso dei dispositivi](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [Gestione dei dispositivi](../devio/device-management-reference.md)
-   [Archiviazione avanzata](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [Individuazione funzioni](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [Master immagini](../imapi/imapi-reference.md)
-   [Posizione](../locationapi/windows-location-programming-reference.md)
-   [Database di associazione PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [Stampa](/windows-hardware/drivers/print/introduction-to-printing)
    -   [Spooler di stampa](../printdocs/printing-and-print-spooler-reference.md)
    -   [Stampa pacchetto di documenti](../printdocs/tailored-app-printing-api.md)
    -   [Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [Stampa ticket](../printdocs/print-ticket-api.md)
    -   [Stampa XPS](../printdocs/xpsprint-api.md)
-   [Sensori](../sensorsapi/sensor-api-programming-reference.md)
-   [Servizio di notifica eventi di sistema (SENS)](../sens/sens-reference.md)
-   [Guida dello strumento](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [Servizi Web nei dispositivi](../wsdapi/web-services-for-devices-reference.md)
-   [Acquisizione di immagini di Windows (WIA)](../wia/-wia-reference.md)
-   [Gestione dispositivi Windows Media](../wmdm/programming-reference.md)
-   [Dispositivi portatili Windows](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>Servizi di sistema

Le API dei [servizi di sistema](/previous-versions//aa969179(v=vs.85)) consentono alle applicazioni di accedere alle risorse del computer e alle funzionalità del sistema operativo sottostante, ad esempio la memoria, i file System, i dispositivi, i processi e i thread.

-   [COM](../com/reference.md)
-   [COM+](../cossdk/com--reference.md)
-   [API di compressione](../cmpapi/-compression-portal.md)
-   [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [Librerie a collegamento dinamico (dll)](../dlls/dynamic-link-library-functions.md)
-   [API della Guida](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [Comunicazioni interprocesso](../ipc/interprocess-communications.md):
    -   [Mailslot](../ipc/mailslot-functions.md)
    -   [Pipe](../ipc/pipe-functions.md)
-   [Gestione transazioni kernel](../ktm/ktm-reference.md)
-   [Gestione della memoria](../memory/memory-management-reference.md)
-   [Registratore operazioni](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [Risparmio energia](../power/power-management-reference.md)
-   [Servizi Desktop remoto](../termserv/terminal-services-reference.md)
-   [Processi](../procthread/process-and-thread-reference.md)
-   [Services](../services/service-reference.md)
-   [Sincronizzazione](../sync/synchronization-reference.md)
-   [Thread](../procthread/process-and-thread-reference.md)
-   [Condivisione desktop di Windows](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Informazioni sul sistema Windows](../sysinfo/windows-system-information.md)
    -   [Handle e oggetti](../sysinfo/handle-and-object-functions.md)
    -   [Registro](../sysinfo/registry-reference.md)
    -   [Time](../sysinfo/time-reference.md)
    -   [Provider di servizi temporali](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>Sicurezza e identità

Le API di [sicurezza e identità](../devnotes/security.md) consentono l'autenticazione della password all'accesso, la protezione discrezionale per tutti gli oggetti di sistema condivisibili, il controllo di accesso con privilegi, Rights Management e il controllo della sicurezza.

-   [autenticazione](../secauthn/authentication-reference.md)
-   [Autorizzazione](../secauthz/authorization-reference.md)
-   [Registrazione del certificato](../seccertenroll/certificate-enrollment-api-reference.md)
-   [Crittografia](../seccrypto/cryptography-reference.md)
-   [CNG (Cryptography Next Generation)](../seccng/cng-reference.md)
-   [Servizi directory](/previous-versions//ms682458(v=vs.85))
    -   [Active Directory Domain Services](../ad/active-directory-domain-services-reference.md)
    -   [Interfacce di Active Directory Service (ADSI)](../adsi/adsi-reference.md)
-   [EAP (Extensible Authentication Protocol)](../eap/extensible-authentication-protocol-reference.md)
-   [EAPHost (Extensible Authentication Protocol Host)](../eaphost/about-eap-host.md)
-   [Gestione delle password MS-CHAP](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [Protezione accesso alla rete (NAP)](../nap/nap-reference.md)
-   [Server dei criteri di rete (NPS)](../nps/ias-internet-authentication-service-reference.md)
-   [Controlli padre](../parcon/parental-controls-reference.md)
-   [Provider WMI per la sicurezza](../secprov/security-wmi-providers-reference.md)
-   [Servizi di base TPM (TBS)](../tbs/tbs-reference.md)
-   [Windows Biometric Framework](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>Installazione e manutenzione di applicazioni

-   [Games Explorer](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [Assembly affiancati](../sbscs/side-by-side-assemblies-reference.md)
-   [Creazione di pacchetti, distribuzione e API di query](../appxpkg/api-reference.md
)
-   [Licenza per sviluppatori](../devlic/developer-license-apis.md)
-   [Gestione riavvio](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>Amministrazione e gestione del sistema

Le interfacce di [amministrazione del sistema](../srvnodes/system-administration.md) consentono di installare, configurare e servire applicazioni o sistemi.

-   [Provider WMI dati configurazione di avvio](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [Cluster di failover](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [Gestione risorse file server](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [Microsoft Management Console (MMC) 2,0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [Infrastruttura di gestione delle impostazioni](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [Gestione licenze software](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [Gestione riavvio](../rstmgr/restart-manager-portal.md)
-   [Infrastruttura di gestione delle impostazioni](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Ripristino configurazione di sistema](../sr/system-restore-portal.md)
-   [Arresto del sistema](../shutdown/system-shutdown.md)
-   [Utilità di pianificazione](../taskschd/task-scheduler-start-page.md)
-   [Registrazione accesso utenti](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Microsoft Virtual Server](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [Provider di bilanciamento carico di rete](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [Windows Defender WMI V2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Servizi di distribuzione Windows](../wds/windows-deployment-services-portal.md)
-   [Windows Genuine Advantage](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Infrastruttura di gestione di Windows](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [Strumentazione gestione Windows (WMI)](../wmisdk/wmi-reference.md)
-   [Gestione remota Windows](../winrm/portal.md)
-   [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Strumento valutazione sistema Windows](../winsat/winsat-reference.md)
-   [Agente di Windows Update](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>Rete e Internet

Le API di [rete](../devnotes/networking.md) consentono la comunicazione tra le applicazioni in una rete. È anche possibile creare e gestire l'accesso alle risorse condivise, ad esempio le directory e le stampanti di rete.

-   [Domain Name System (DNS)](../dns/dns-reference.md)
-   [Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [Servizio fax](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [Connessione guidata](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [Server HTTP](../http/http-server-api-reference.md)
-   [Condivisione connessione Internet e firewall](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [Helper IP](../iphlp/ip-helper-function-reference.md)
-   [Firewall connessione Internet IPv6](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [Base informazioni di gestione](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [Accodamento messaggi (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [Protocollo MADCAP (Dynamic Client Allocation Protocol) per indirizzi multicast](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [Network Address Translation (NAT)](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [Gestione elenco reti (NLM)](../nla/network-list-manager-api-reference.md)
-   [Gestione della rete](../netmgmt/network-management-reference.md)
-   [Gestione delle condivisioni di rete](../netshare/network-share-management-reference.md)
-   [Peer-to-peer](../p2psdk/portal.md)
-   [Qualità del servizio (QOS)](/previous-versions/windows/desktop/qos/qos-reference)
-   [Chiamata di procedura remota](../rpc/reference.md)
-   [Servizio Routing e accesso remoto (RAS)](../rras/portal.md)
-   [Simple Network Management Protocol (SNMP)](../snmp/snmp-reference.md)
-   [Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [Interfaccia TAPI (Telephony Application Programming Interface)](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [Componente del protocollo WebSocket](../websock/web-socket-protocol-component-api-portal.md)
-   Rete wireless:
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [IrDA](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [Banda larga mobile](../mbn/mobile-broadband-networks-api-reference.md)
    -   [WiFi nativo](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect Now](../wcn/windows-connect-now-reference.md)
    -   [Gestione connessioni Windows](../wcm/windows-connection-manager-reference.md)
-   [Piattaforma filtro Windows](../fwp/fwp-reference.md)
-   [Windows Firewall con sicurezza avanzata](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [Servizi HTTP di Windows (WinHTTP)](../winhttp/winhttp-reference.md)
-   [Windows Internet (WinINet)](../wininet/wininet-reference.md)
-   [Rete Windows (WNet)](../wnet/windows-networking-reference.md)
-   [Virtualizzazione rete Windows](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [Piattaforma Windows RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows Sockets (Winsock)](../winsock/winsock-reference.md)
-   [Servizi Web Windows](../wsw/windows-web-services-reference.md)
-   [Richiesta estesa HTTP XML](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>API deprecate o legacy

Di seguito sono riportate le tecnologie e le API che sono obsolete o sono state sostituite o deprecate dai sistemi operativi client e server Windows.

-   [DirectMusic](/previous-versions/ms807133(v=msdn.10))
-   [DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   [Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) è ora incluso in [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).
-   [Dynamic Data Exchange di rete (DDE)](../ipc/network-dde-reference.md)
-   [Servizio di installazione remota](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): usare invece [servizi di distribuzione Windows](../wds/windows-deployment-services-portal.md) .
-   [Servizio dischi virtuali (VDS)](../vds/vds-reference.md): usare invece [Gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) .
-   Servizi terminal: usare [Servizi Desktop remoto](../termserv/terminal-services-reference.md).
-   [Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))
-   [Messaggistica Windows (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): usare invece [MAPI di Office](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) .
-   [Piattaforma Gadget Windows](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): creare app UWP.
-   [Windows Sidebar](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): creare app UWP.
-   [Windows SideShow](/previous-versions//ms744179(v=vs.85)): nessuna sostituzione.
-   [Effetti bitmap WPF](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
