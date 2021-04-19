---
description: I codici motivo di arresto vengono usati dalle funzioni ExitWindowsEx e InitiateSystemShutdownEx nel parametro dwReason. Il numero massimo di \_ \_ motivi per i quali i codici verranno elaborati dal sistema. Il numero massimo \_ \_ di motivi è definito in Reason. h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Codici motivo dell'arresto del sistema (Reason. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee2b8b2795dcf350d627b3cf59f85eb374a22cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308623"
---
# <a name="system-shutdown-reason-codes"></a>Codici motivo dell'arresto del sistema

I codici motivo di arresto vengono usati dalle funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) nel parametro *dwReason* .

Il numero massimo di \_ \_ motivi per i quali i codici verranno elaborati dal sistema. Il numero massimo \_ \_ di motivi è definito in Reason. h.

Di seguito sono riportati i flag principali motivo. Indica il tipo di problema generale.



| Costante/valore                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ MOTIVO per cui l' \_ \_ applicazione principale**</dt> <dt>0x00040000</dt> </dl>             | Problema dell'applicazione.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principale \_**</dt> <dt>0x00010000</dt> hardware </dl>                      | Problema hardware.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ MOTIVO per l' \_ \_ \_ API legacy principale**</dt> <dt>0x00070000</dt> </dl>               | È stata usata la funzione [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) anziché [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principale \_ OPERATINGSYSTEM**</dt> <dt>0x00020000</dt> </dl> | Problema del sistema operativo.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ per \_ altre**</dt> <dt>0x00000000</dt> </dl>                               | Altro problema.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principale di \_ Power**</dt> <dt>0x00060000</dt> </dl>                               | Interruzione dell'alimentazione.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principale del \_ software**</dt> <dt>0x00030000</dt> </dl>                      | Problema relativo al software.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principale \_**</dt> <dt>0x00050000</dt> di sistema </dl>                            | Errore di sistema.<br/>                                                                                                                                         |



Di seguito sono riportati i flag per motivi minori. Modificano il flag motivo principale specificato. È possibile usare qualsiasi ragione secondaria insieme a qualsiasi motivo principale, ma alcune combinazioni non hanno senso.



| Costante/valore                                                                                                                                                                                                                                                                                                    | Descrizione                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ bluescreen**</dt> <dt>0x0000000F</dt> </dl>                                   | Evento di arresto anomalo della schermata blu.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ CORDUNPLUGGED**</dt> <dt>0x0000000B</dt> </dl>                          | Scollegato.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ MOTIVO \_ del \_ disco secondario**</dt> <dt>0x00000007</dt> </dl>                                                     | Disk (Disco).<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ MOTIVO per l' \_ \_ ambiente secondario**</dt> <dt>0x0000000c</dt> </dl>                                | Ambiente.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ REASON \_ \_ \_ driver hardware secondario**</dt> <dt>0x0000000D</dt> </dl>                   | Driver.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ 0x00000011 \_ hotfix minore**</dt> <dt></dt> </dl>                                               | Correzione rapida.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO per la \_ \_ \_ disinstallazione dell'hotfix minore**</dt> <dt>0x00000017</dt> </dl>                | Disinstallazione della correzione a caldo.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ MOTIVO \_ 0x00000005 \_ appeso minore**</dt> <dt></dt> </dl>                                                     | Insensibile.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ installazione secondaria**</dt> <dt>0x00000002</dt> </dl>                             | Installazione.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ manutenzione secondaria**</dt> <dt>0x00000001</dt> </dl>                                | Manutenzione.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ MOTIVO 0x00000019 di \_ \_ MMC secondario**</dt> <dt></dt> </dl>                                                        | Problema MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ MOTIVO \_ della \_ \_ connettività di rete secondaria**</dt> <dt>0x00000014</dt> </dl>    | Connettività di rete.<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ NETWORKCARD**</dt> <dt>0x00000009</dt> </dl>                                | Scheda di rete.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ altre**</dt> <dt>0x00000000</dt> </dl>                                                  | Altro problema.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ OTHERDRIVER**</dt> <dt>0x0000000E</dt> </dl>                                | Altro evento driver.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ \_**</dt> <dt>0x0000000A</dt> di alimentazione secondaria </dl>                            | Alimentatore.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ MOTIVO \_ 0x00000008 \_ processore secondario**</dt> <dt></dt> </dl>                                      | Processore.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ MOTIVO \_ della \_ riconfigurazione secondaria**</dt> <dt>0x00000004</dt> </dl>                                         | Riconfigurare.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ MOTIVO \_ della \_ sicurezza secondaria**</dt> <dt>0x00000013</dt> </dl>                                         | Problema di sicurezza.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | Patch di sicurezza.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ SECURITYFIX di \_ disinstallazione secondaria**</dt> <dt>0x00000018</dt> </dl> | Disinstallazione delle patch di sicurezza.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ SERVICEPACK di \_ disinstallazione secondaria**</dt> <dt>0x00000016</dt> </dl> | Disinstallazione del Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secondario \_ termsrv**</dt> <dt>0x00000020</dt> </dl>                                            | Servizi terminal.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ MOTIVO \_ minore \_ instabile**</dt> <dt>0x00000006</dt> </dl>                                         | Instabile.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ aggiornamento secondario**</dt> <dt>0x00000003</dt> </dl>                                            | Aggiornamento.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ MOTIVO \_ 0x00000015 \_ WMI secondario**</dt> <dt></dt> </dl>                                                        | Problema di WMI.<br/>                     |



I flag facoltativi seguenti forniscono informazioni aggiuntive sull'evento.



| Costante/valore                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ \_Flag motivo \_ \_ definito dall'utente**</dt> <dt>0x40000000</dt> </dl> | Il codice motivo è definito dall'utente. Per ulteriori informazioni, vedere Definizione di un codice motivo personalizzato. <br/> Se questo flag non è presente, il codice motivo viene definito dal sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ FLAG REASON 0x80000000 \_ \_ pianificato**</dt> <dt></dt> </dl>                 | La chiusura è stata pianificata. Il sistema genera un file di dati dello stato del sistema (SSD). Questo file contiene informazioni sullo stato del sistema, ad esempio processi, thread, utilizzo della memoria e configurazione. <br/> Se questo flag non è presente, l'arresto non è pianificato. Le opzioni di notifica e Reporting sono controllate da un set di criteri. Ad esempio, dopo l'accesso, il sistema Visualizza una finestra di dialogo che segnala l'arresto non pianificato se il criterio è stato abilitato. Viene creato un file SSD solo se il criterio SSD è abilitato nel sistema. L'amministratore può usare [segnalazione errori Windows](../wer/windows-error-reporting.md) per inviare i dati SSD a una posizione centrale o a Microsoft.<br/> |



## <a name="remarks"></a>Commenti

Le combinazioni seguenti sono riconosciute dal sistema. La tabella indica la stringa che viene visualizzata nell'individuazione evento di arresto e fornisce una descrizione più dettagliata. La stringa predefinita è "nessun titolo per questo motivo è stato trovato".



| Combinazione                                                                                                | Descrizione                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ motivo \_ principale \_ dell'applicazione \| SHTDN \_ motivo \_ minore \_ appeso                                            | "Applicazione: non risponde" un riavvio o un arresto non pianificato per risolvere i problemi di un'applicazione che non risponde.<br/>                                                                                                                             |
| SHTDN \_ motivo \_ principale \_ dell'applicazione \| SHTDN \_ motivo dell' \_ \_ installazione secondaria \| SHTDN \_ reason \_ flag \_ pianificato    | "Applicazione: installazione (pianificata)" un riavvio o un arresto pianificato per eseguire l'installazione dell'applicazione.<br/>                                                                                                                              |
| SHTDN \_ motivo \_ principale \_ dell' \| applicazione \_ SHTDN \_ motivo \_ manutenzione secondaria                                     | "Applicazione: manutenzione (non pianificata)" un riavvio o un arresto non pianificato per il servizio di un'applicazione.<br/>                                                                                                                                    |
| SHTDN \_ motivo \_ principale \_ dell' \| applicazione \_ SHTDN \_ motivo \_ manutenzione secondaria \| SHTDN \_ motivo del \_ flag \_ pianificato     | "Applicazione: manutenzione (pianificata)" un riavvio o un arresto pianificato per eseguire la manutenzione pianificata di un'applicazione.<br/>                                                                                                                  |
| SHTDN \_ motivo \_ principale \_ dell'applicazione \| SHTDN \_ motivo \_ minore \_ instabile                                        | "Applicazione: instabile" un riavvio o un arresto non pianificato per risolvere i problemi di un'applicazione instabile.<br/>                                                                                                                                     |
| SHTDN \_ motivo \_ principale \_ hardware \| SHTDN \_ motivo \_ \_ installazione secondaria                                       | "Hardware: installazione (non pianificata)" un riavvio o un arresto non pianificato per avviare o completare l'installazione dell'hardware.<br/>                                                                                                                     |
| SHTDN \_ motivo \_ principale \_ hardware \| SHTDN \_ motivo \_ di \_ installazione secondaria \| SHTDN \_ reason \_ flag \_ pianificato       | "Hardware: installazione (pianificata)" un riavvio o un arresto pianificato per avviare o completare l'installazione dell'hardware.<br/>                                                                                                                          |
| SHTDN \_ motivo \_ principale \_ hardware \| SHTDN \_ motivo \_ \_ manutenzione secondaria                                        | "Hardware: manutenzione (non pianificata)" un riavvio o un arresto non pianificato per l'hardware del servizio nel sistema.<br/>                                                                                                                               |
| SHTDN \_ motivo \_ principale \_ hardware \| SHTDN \_ motivo \_ \_ manutenzione secondaria \| SHTDN \_ motivo del \_ flag \_ pianificato        | "Hardware: manutenzione (pianificata)" un riavvio o un arresto pianificato per l'hardware del servizio nel sistema.<br/>                                                                                                                                    |
| SHTDN \_ motivo \_ principale \_ \_ API legacy                                                                          | "Arresto API legacy". questo arresto è stato avviato dalla funzione [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) legacy. Le applicazioni devono utilizzare la funzione [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .<br/> |
| SHTDN \_ motivo \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ hotfix                                      | "Sistema operativo: correzione a caldo (non pianificato)" un riavvio o un arresto non pianificato per installare una correzione rapida.<br/>                                                                                                                                        |
| SHTDN \_ reason \_ Major \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ hotfix \| SHTDN \_ reason \_ flag \_ pianificato      | "Sistema operativo: correzione a caldo (pianificato)" un riavvio o un arresto pianificato per installare una correzione rapida.<br/>                                                                                                                                             |
| SHTDN \_ motivo \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ motivo \_ secondario \_ riconfigurazione                                    | "Sistema operativo: riconfigurazione (non pianificata)" un riavvio o un arresto non pianificato per modificare la configurazione del sistema operativo.<br/>                                                                                                        |
| SHTDN \_ motivo \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ reconfig \| SHTDN \_ reason \_ flag \_ pianificato    | "Sistema operativo: riconfigurazione (pianificata)" un riavvio o un arresto pianificato per modificare la configurazione del sistema operativo.<br/>                                                                                                             |
| SHTDN \_ reason \_ Major \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ SECURITYFIX                                 | "Sistema operativo: correzione della sicurezza (non pianificata)" un riavvio o un arresto non pianificato per l'installazione di una patch di sicurezza.<br/>                                                                                                                            |
| SHTDN \_ reason \_ Major \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ SECURITYFIX \| SHTDN \_ reason \_ flag \_ pianificato | "Sistema operativo: correzione della sicurezza (pianificata)" un riavvio o un arresto pianificato per l'installazione di una patch di sicurezza.<br/>                                                                                                                                 |
| SHTDN \_ reason \_ Major \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ SERVICEPACK \| SHTDN \_ reason \_ flag \_ pianificato | "Sistema operativo: Service Pack (pianificato)" un riavvio o un arresto pianificato per installare un Service Pack.<br/>                                                                                                                                   |
| SHTDN \_ reason \_ Major \_ OPERATINGSYSTEM \| SHTDN \_ reason \_ minor \_ upgrade \| SHTDN \_ reason \_ flag \_ pianificato     | "Sistema operativo: aggiornamento (pianificato)" un riavvio o un arresto pianificato per aggiornare la configurazione del sistema operativo.<br/>                                                                                                                    |
| SHTDN \_ motivo \_ principale \_ altro \| SHTDN \_ motivo \_ secondario \_ altro                                                 | "Altro (non pianificato)" un arresto o un riavvio non pianificato.<br/>                                                                                                                                                                                 |
| SHTDN \_ motivo \_ principale \_ altro \| SHTDN \_ motivo \_ secondario \_ altro \| SHTDN \_ motivo del \_ flag \_ pianificato                 | "Altro (pianificato)" un arresto o un riavvio pianificato.<br/>                                                                                                                                                                                      |
| SHTDN \_ motivo \_ principale \_ altro \| SHTDN \_ motivo \_ minore \_ appeso                                                  | "Altro errore: sistema che non risponde" il sistema non risponde.<br/>                                                                                                                                                                  |
| SHTDN \_ motivo \_ principale di \_ Power \| SHTDN \_ motivo \_ secondario \_ CORDUNPLUGGED                                         | "Interruzione dell'alimentazione: cavo scollegato" il computer è stato scollegato.<br/>                                                                                                                                                                           |
| SHTDN \_ motivo \_ principale di \_ Power \| SHTDN \_ motivo \_ minore \_ ambiente                                           | "Interruzione dell'alimentazione: ambiente" si è verificata un'interruzione dell'alimentazione.<br/>                                                                                                                                                                                |
| SHTDN \_ motivo \_ principale \_ \| SHTDN \_ motivo \_ secondario \_ bluescreen                                           | "Errore di sistema: errore irreversibile" il computer ha visualizzato un evento di arresto anomalo della schermata blu.<br/>                                                                                                                                                        |
| SHTDN \_ motivo \_ principale \_ \| SHTDN \_ motivo della \_ \_ connettività di rete secondaria \_                                | "Perdita della connettività di rete (non pianificata)" il computer deve essere arrestato a causa di un problema di connettività di rete.<br/>                                                                                                                    |
| SHTDN \_ motivo \_ principale \_ \| SHTDN \_ motivo della \_ \_ sicurezza secondaria                                             | "Problema di sicurezza" il computer deve essere arrestato a causa di un problema di sicurezza.<br/>                                                                                                                                                          |



 

È anche possibile definire i propri motivi di arresto e aggiungerli al registro di sistema. Ogni codice motivo deve essere archiviato come valore del registro di sistema nella chiave seguente:**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ affidabilità \\ UserDefined \\<\_ \_ ID lingua di sistema predefinito \_>**

Questa chiave contiene nomi di valore nel formato seguente: *xxxxx*; *nnn*; *nnnnn*. I punti e virgola delimitano i componenti di un nome di valore.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*xxxxx*
</dt> <dd>

Da uno a cinque dei seguenti flag di controllo (non è possibile usare altri caratteri).



| Flag | Descrizione                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Arresto pianificato; in caso contrario, un arresto non pianificato.                                               |
| C    | È necessario un commento. Questo flag deve essere utilizzato con S.<br/>                                  |
| B    | È necessario specificare un ID. Questo flag deve essere usato con D.<br/>                                      |
| S    | Visualizza la finestra di dialogo arresto prevista. È necessario usare S, D o entrambi i e D.<br/>   |
| D    | Visualizza la finestra di dialogo arresto imprevisto. È necessario usare S, D o entrambi i e D.<br/> |



 

L'ordine in cui vengono usati i flag non è importante. Ad esempio, CSP indica un arresto pianificato in cui viene visualizzata la finestra di dialogo di arresto prevista ed è richiesto un commento.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*nnn*
</dt> <dd>

Motivo principale. Questo componente deve essere un numero compreso nell'intervallo 64-255. L'intervallo 0-63 è riservato per l'utilizzo da parte del sistema.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Motivo secondario. Il componente deve essere compreso nell'intervallo 0-65535.

</dd> </dl>

I motivi personalizzati sono ordinati nell'interfaccia utente per numero motivo principale, quindi per numero motivo minore. Due motivi personalizzati non possono usare gli stessi motivi principali e secondari, a meno che non sia pianificato e non pianificato. In caso contrario, il sistema utilizzerà la prima istanza e ignorerà gli altri.

I dati per ogni valore del registro di sistema sono due stringhe, separate da \\ n \\ r. La prima stringa è una stringa del titolo da visualizzare nella finestra di dialogo di arresto e scritta nel registro eventi. La dimensione massima è 64 caratteri. Le stringhe del titolo devono essere univoche. I titoli personalizzati non possono corrispondere ai titoli standard definiti dal sistema o a un altro titolo personalizzato. La seconda stringa è una stringa di descrizione da visualizzare nella finestra di dialogo di arresto; è facoltativo. La dimensione massima è 256 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows XP \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2003 \|\]<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Motivo. h</dt> </dl> |



 

 
