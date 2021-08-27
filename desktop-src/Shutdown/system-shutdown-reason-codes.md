---
description: I codici motivo dell'arresto vengono usati dalle funzioni ExitWindowsEx e InitiateSystemShutdownEx nel parametro dwReason. Un massimo di codici \_ motivo MAX NUM REASONS verrà elaborato dal \_ sistema. MAX \_ NUM REASONS è definito in \_ reason.h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Codici motivo arresto sistema (Reason.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef40cf53afd3abaf261e15f2caba735dea7963ee5b5f19cebc78c63a373962fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073201"
---
# <a name="system-shutdown-reason-codes"></a>Codici motivo arresto sistema

I codici motivo di arresto vengono usati dalle funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) nel *parametro dwReason.*

Un massimo di codici \_ motivo MAX NUM REASONS verrà elaborato dal \_ sistema. MAX \_ NUM REASONS è definito in \_ reason.h.

Di seguito sono riportati i principali flag di motivo. Indicano il tipo di problema generale.



| Costante/valore                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ APPLICATION**</dt> <dt>0x00040000</dt> </dl>             | Problema dell'applicazione.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPALE \_ DELL'0X00010000**</dt> <dt></dt> </dl>                      | Problema hardware.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPALE \_ \_ DELL'API**</dt> <dt>LEGACY 0x00070000</dt> </dl>               | È [**stata usata la funzione InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) anziché [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM**</dt> <dt>0x00020000</dt> </dl> | Problema del sistema operativo.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                               | Altro problema.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPALE \_ DELL'0X00060000**</dt> <dt></dt> </dl>                               | Interruzione dell'alimentazione.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ SOFTWARE**</dt> <dt>0x00030000</dt> </dl>                      | Problema software.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ SYSTEM**</dt> <dt>0x00050000</dt> </dl>                            | Errore di sistema.<br/>                                                                                                                                         |



Di seguito sono riportati i flag di motivo secondari. Modificano il flag di motivo principale specificato. È possibile usare qualsiasi motivo secondario in combinazione con qualsiasi motivo principale, ma alcune combinazioni non hanno senso.



| Costante/valore                                                                                                                                                                                                                                                                                                    | Descrizione                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ VISUALIZZAZIONE BLUESCREEN**</dt> <dt>0X0000000F</dt> </dl>                                   | Evento di arresto anomalo della schermata blu.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ CORDUNPLUGGED**</dt> <dt>0X0000000B</dt> </dl>                          | Scollegato.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DEL \_ DISCO SECONDARIO**</dt> <dt>0x00000007</dt> </dl>                                                     | Disk (Disco).<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ DELL'AMBIENTE SECONDARIO**</dt> <dt>0x0000000c</dt> </dl>                                | Ambiente.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DEL DRIVER HARDWARE \_ \_ SECONDARIO**</dt> <dt>0x0000000d</dt> </dl>                   | autista.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ DELL'AGGIORNAMENTO RAPIDO SECONDARIO**</dt> <dt>0X00000011</dt> </dl>                                               | Correzione rapida.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ DISINSTALLAZIONE \_ DELL'HOTFIX**</dt> <dt>SECONDARIO 0X00000017</dt> </dl>                | Disinstallazione della correzione rapida.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ HUNG**</dt> <dt>0x00000005</dt> </dl>                                                     | Insensibile.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ DELL'INSTALLAZIONE**</dt> <dt>SECONDARIA 0X00000002</dt> </dl>                             | Installazione.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ MANUTENZIONE**</dt> SECONDARIA <dt>0X00000001</dt> </dl>                                | Manutenzione.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ SECONDARIO MMC**</dt> <dt>0x00000019</dt> </dl>                                                        | Problema di MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ CONNETTIVITÀ DI \_ RETE**</dt> <dt>SECONDARIA 0X00000014</dt> </dl>    | Connettività di rete.<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA SCHEDA DI \_ RETE**</dt> <dt>SECONDARIA 0X00000009</dt> </dl>                                | Scheda di rete.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                                                  | Altro problema.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHERDRIVER**</dt> <dt>0x0000000e</dt> </dl>                                | Altro evento del driver.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ \_ DELL'ALIMENTAZIONE SECONDARIA**</dt> <dt>0X0000000A</dt> </dl>                            | Alimentazione.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ PROCESSORE SECONDARIO**</dt> <dt>0X00000008</dt> </dl>                                      | Processore.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ MOTIVO \_ MINOR \_ RECONFIG**</dt> <dt>0x00000004</dt> </dl>                                         | Riconfigurare.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ SICUREZZA**</dt> SECONDARIA <dt>0X00000013</dt> </dl>                                         | Problema di sicurezza.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PER CUI MINOR \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | Patch di sicurezza.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ DISINSTALLAZIONE DI MINOR SECURITYFIX \_**</dt> <dt>0X00000018</dt> </dl> | Disinstallazione della patch di sicurezza.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PER CUI IL \_ SERVICEPACK**</dt> <dt>SECONDARIO 0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DELLA \_ DISINSTALLAZIONE DI SERVICEPACK \_**</dt> <dt>0X00000016</dt> </dl> | Disinstallazione del Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ MOTIVO \_ CONDIZIONI \_ SECONDARIERV**</dt> <dt>0x00000020</dt> </dl>                                            | Servizi terminal.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ MOTIVO \_ MINOR \_ UNSTABLE**</dt> <dt>0x00000006</dt> </dl>                                         | Instabile.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ DELL'AGGIORNAMENTO SECONDARIO**</dt> <dt>0X00000003</dt> </dl>                                            | Aggiornamento.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ DELL'ERRORE WMI**</dt> <dt>SECONDARIO 0X00000015</dt> </dl>                                                        | Problema WMI.<br/>                     |



I flag facoltativi seguenti forniscono informazioni aggiuntive sull'evento.



| Costante/valore                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ FLAG \_ MOTIVO \_ DEFINITO \_ DALL'UTENTE**</dt> <dt>0x40000000</dt> </dl> | Il codice motivo è definito dall'utente. Per altre informazioni, vedere Definizione di un codice motivo personalizzato. <br/> Se questo flag non è presente, il codice motivo viene definito dal sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ FLAG \_ MOTIVO \_ PIANIFICATO**</dt> <dt>0X80000000</dt> </dl>                 | L'arresto è stato pianificato. Il sistema genera un file SSD (System State Data). Questo file contiene informazioni sullo stato del sistema, ad esempio processi, thread, utilizzo della memoria e configurazione. <br/> Se questo flag non è presente, l'arresto non è stato pianificato. Le opzioni di notifica e creazione di report sono controllate da un set di criteri. Ad esempio, dopo l'accesso, il sistema visualizza una finestra di dialogo che segnala l'arresto non pianificato se i criteri sono stati abilitati. Un file SSD viene creato solo se i criteri SSD sono abilitati nel sistema. L'amministratore può [usare Segnalazione errori Windows](../wer/windows-error-reporting.md) per inviare i dati SSD a una posizione centrale o a Microsoft.<br/> |



## <a name="remarks"></a>Commenti

Le combinazioni seguenti vengono riconosciute dal sistema. La tabella indica la stringa visualizzata in Shutdown Event Tracker e fornisce una descrizione più dettagliata. La stringa predefinita è "Non è stato trovato alcun titolo per questo motivo".



| Combinazione                                                                                                | Descrizione                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ HUNG                                            | "Applicazione: non risponde" Riavvio o arresto non pianificato per risolvere i problemi di un'applicazione che non risponde.<br/>                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Applicazione: Installazione (pianificata)" Riavvio o arresto pianificato per eseguire l'installazione dell'applicazione.<br/>                                                                                                                              |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE                                     | "Applicazione: Manutenzione (non pianificata)" Riavvio o arresto non pianificato per la manutenzione di un'applicazione.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Applicazione: Manutenzione (pianificata)" Riavvio o arresto pianificato per eseguire la manutenzione pianificata di un'applicazione.<br/>                                                                                                                  |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ UNSTABLE                                        | "Applicazione: instabile" Riavvio o arresto non pianificato per risolvere i problemi di un'applicazione instabile.<br/>                                                                                                                                     |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION                                       | "Hardware: Installazione (non pianificata)" Riavvio o arresto non pianificato per avviare o completare l'installazione dell'hardware.<br/>                                                                                                                     |
| MOTIVO SHTDN \_ PRINCIPALE \_ HARDWARE \_ \| SHTDN MOTIVO INSTALLAZIONE \_ SECONDARIA \_ \_ \| SHTDN \_ MOTIVO FLAG \_ \_ PIANIFICATO       | "Hardware: Installazione (pianificata)" Riavvio o arresto pianificato per avviare o completare l'installazione dell'hardware.<br/>                                                                                                                          |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE                                        | "Hardware: Manutenzione (non pianificata)" Riavvio o arresto non pianificato dell'hardware del sistema.<br/>                                                                                                                               |
| SHTDN \_ REASON \_ MAJOR \_ HARDWARE \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE \| SHTDN \_ REASON \_ FLAG \_ PLANNED        | "Hardware: Manutenzione (pianificata)" Riavvio pianificato o arresto dell'hardware del servizio nel sistema.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ LEGACY \_ API                                                                          | "Arresto api legacy" Questo arresto è stato avviato dalla funzione [**initiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) legacy. Le applicazioni devono usare [**la funzione InitiateSystemShutdownEx.**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)<br/> |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX                                      | "Sistema operativo: correzione rapida (non pianificato)" Riavvio o arresto non pianificato per installare una correzione rapida.<br/>                                                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED      | "Sistema operativo: correzione rapida (pianificata)" Riavvio pianificato o arresto per installare una correzione rapida.<br/>                                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG                                    | "Sistema operativo: riconfigurazione (non pianificata)" Riavvio o arresto non pianificato per modificare la configurazione del sistema operativo.<br/>                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Sistema operativo: Riconfigurazione (pianificata)" Riavvio o arresto pianificato per modificare la configurazione del sistema operativo.<br/>                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITYFIX                                 | "Sistema operativo: Correzione della sicurezza (non pianificata)" Riavvio o arresto non pianificato per installare una patch di sicurezza.<br/>                                                                                                                            |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITYFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Sistema operativo: correzione della sicurezza (pianificata)" Riavvio o arresto pianificato per installare una patch di sicurezza.<br/>                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SERVICEPACK \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Sistema operativo: Service Pack (pianificato)" Riavvio o arresto pianificato per installare un Service Pack.<br/>                                                                                                                                   |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ UPGRADE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Sistema operativo: aggiornamento (pianificato)" Riavvio pianificato o arresto per aggiornare la configurazione del sistema operativo.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER                                                 | "Altro (non pianificato)" Arresto o riavvio non pianificato.<br/>                                                                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER \| SHTDN \_ REASON \_ FLAG \_ PLANNED                 | "Altro (pianificato)" Arresto o riavvio pianificato.<br/>                                                                                                                                                                                      |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ HUNG                                                  | "Other Failure: System Unresponsive" (Altro errore: Il sistema non risponde) Il sistema non risponde.<br/>                                                                                                                                                                  |
| SHTDN \_ REASON \_ MAJOR \_ POWER \| SHTDN \_ REASON \_ MINOR \_ CORDUNPLUGGED                                         | "Power Failure: Cord Unplugged" Il computer è stato scollegato.<br/>                                                                                                                                                                           |
| SHTDN \_ REASON \_ MAJOR \_ POWER \| SHTDN \_ REASON \_ MINOR \_ ENVIRONMENT                                           | "Interruzione alimentazione: ambiente" Si è verificata un'interruzione dell'alimentazione.<br/>                                                                                                                                                                                |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ BLUESCREEN                                           | "Errore di sistema: Errore di arresto" Il computer ha visualizzato un evento di arresto anomalo della schermata blu.<br/>                                                                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ NETWORK \_ CONNECTIVITY                                | "Perdita di connettività di rete (non pianificata)" Il computer deve essere arrestato a causa di un problema di connettività di rete.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITY                                             | "Problema di sicurezza" Il computer deve essere arrestato a causa di un problema di sicurezza.<br/>                                                                                                                                                          |



 

È anche possibile definire motivi di arresto personalizzati e aggiungerli al Registro di sistema. Ogni codice motivo deve essere archiviato come valore del Registro di sistema nella chiave seguente:**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Reliability \\ \\ UserDefined<default system \\ language ID \_ \_ \_>**

Questa chiave contiene nomi di valore nel formato seguente: *xxxxx*; *nnn*; *nnnnn*. Il punto e virgola delimita i componenti di un nome di valore.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*Xxxxx*
</dt> <dd>

Da uno a cinque dei flag di controllo seguenti (non è possibile usare altri caratteri).



| Flag | Descrizione                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Arresto pianificato; in caso contrario, un arresto non pianificato.                                               |
| C    | È necessario un commento. Questo flag deve essere usato con S.<br/>                                  |
| B    | È necessario un ID. Questo flag deve essere usato con D.<br/>                                      |
| S    | Consente di visualizzare la finestra di dialogo di arresto prevista. È necessario usare S, D o S e D.<br/>   |
| D    | Consente di visualizzare la finestra di dialogo di arresto imprevisto. È necessario usare S, D o S e D.<br/> |



 

L'ordine in cui vengono usati i flag non è importante. Ad esempio, CSP indica un arresto pianificato in cui viene visualizzata la finestra di dialogo di arresto prevista ed è necessario un commento.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*Nnn*
</dt> <dd>

Motivo principale. Questo componente deve essere un numero compreso nell'intervallo 64-255. L'intervallo da 0 a 63 è riservato per l'uso da parte del sistema.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Motivo secondario. Questo componente deve essere compreso nell'intervallo 0-65535.

</dd> </dl>

I motivi personalizzati vengono ordinati nell'interfaccia utente in base al numero di motivo principale, quindi in base al numero di motivo secondario. Due motivi personalizzati non possono usare gli stessi motivi principali e secondari, a meno che uno non sia pianificato e l'altro non sia pianificato. In caso contrario, il sistema userà la prima istanza e ignorerà le altre.

I dati per ogni valore del Registro di sistema sono due stringhe, separate da \\ n \\ r. La prima stringa è una stringa del titolo da visualizzare nella finestra di dialogo di arresto e scritta nel registro eventi. La dimensione massima è di 64 caratteri. Le stringhe del titolo devono essere univoche. I titoli personalizzati non possono corrispondere ai titoli standard definiti dal sistema o a un altro titolo personalizzato. La seconda stringa è una stringa di descrizione da visualizzare nella finestra di dialogo di arresto. è facoltativo. La dimensione massima è di 256 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ UWP per app desktop \| XP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2003 \[ \|\]<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Reason.h</dt> </dl> |



 

 
