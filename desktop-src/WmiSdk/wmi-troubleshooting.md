---
description: Quando si accede ai dati locali o remoti WMI in un'applicazione o in uno script, è possibile che si verifichino errori che vanno dalle classi mancanti all'accesso negato. I provider hanno anche opzioni di debug e classi di risoluzione dei problemi disponibili.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Risoluzione dei problemi di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58919617c663b52ffb840b3c3382b5707f0a305e
ms.sourcegitcommit: a3e96b6c9c6a3fb629e760dd6cc6327f9e4b62b6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/27/2021
ms.locfileid: "114714795"
---
# <a name="wmi-troubleshooting"></a>Risoluzione dei problemi di WMI

Quando si accede ai dati locali o remoti WMI in un'applicazione o in uno script, è possibile che si verifichino errori che vanno dalle classi mancanti all'accesso negato. I provider hanno anche opzioni di debug e classi di risoluzione dei problemi disponibili.

> [!Note]  
> La documentazione seguente è destinata agli sviluppatori e agli amministratori IT. Se si è un utente finale che ha visualizzato un messaggio di errore relativo a WMI, passare [a Supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore. Per altre informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilità di diagnosi di WMI

L'utilità di diagnosi WMI (WMIDiag.exe) non è più supportata a partire da Windows 8 e Windows Server 2012.

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008: **

Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono avere origine in altre parti del sistema operativo e possono verificarsi come errori tramite WMI. In qualsiasi caso, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.

Per ottenere altre informazioni sull'origine del problema, è possibile scaricare ed eseguire lo Utilità di diagnosi di WMI [strumento](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) da riga di comando di diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report aiuta anche i servizi di supporto Tecnico Microsoft a fornire assistenza. È possibile scaricare il Utilità di diagnosi di WMI [dall'Area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

I writer di provider possono anche riscontrare problemi di debug, a meno che non si scrivo un [*provider disaccociato.*](gloss-d.md) Per altre informazioni, vedere [Debug di provider](debugging-providers.md).

## <a name="logging-and-tracing"></a>Registrazione e traccia

I file di log WMI non esistono più. sono stati sostituiti [da Traccia eventi per Windows (ETW).](/windows/desktop/ETW/event-tracing-portal) Per altre informazioni, vedere [Traccia dell'attività WMI](tracing-wmi-activity.md), [Registrazione dell'attività WMI](logging-wmi-activity.md)e File di log [WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Risoluzione dei problemi in script e applicazioni

WMI contiene un set di classi per la risoluzione [dei problemi delle](wmi-troubleshooting-classes.md) applicazioni client che usano provider WMI. Per altre informazioni, vedere [Risoluzione dei problemi relativi alle applicazioni client WMI.](troubleshooting-wmi-client-applications.md)

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Come i writer di provider possono impedire problemi WMI

I writer di provider possono evitare molti problemi, visualizzati nei messaggi di errore tramite WMI, eseguendo le azioni seguenti:

-   Registrazione corretta del provider. Per altre informazioni, vedere [Registrazione di un provider](registering-a-provider.md).
-   Aggiunta [**\# dell'istruzione pragma autorecover**](pragma-autorecover.md) al file Managed Object Format (MOF) che definisce le classi del provider.

Per altre informazioni, vedere [Debug di provider](debugging-providers.md), Fornire dati a [WMI](providing-data-to-wmi.md)e Configurazione del provider e Risoluzione dei problemi relativi [alle classi](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Accesso negato

Gli errori di accesso negato segnalati da script e applicazioni che accedono a spazi dei nomi e dati WMI rientrano in genere in tre categorie. Nella tabella seguente sono elencate le tre categorie di errori e i problemi che potrebbero causare gli errori e le possibili soluzioni.



| Errore                                                                                                                        | Possibili problemi                                                                                                                                                                                                                                                                                                                                                                     | Soluzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706ba `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema del firewall o server non disponibile.<br/>      | Il computer non esiste o il firewall Windows blocca la connessione<br/>                                                                                                                                                                                                                                                                                        | Connessione a Vista: **netsh advfirewall firewall set rule group="Strumentazione gestione Windows (wmi)" new enable=yes** Connessione al livello inferiore: Consenti la regola "Amministrazione remota" in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **ACCESSO E \_ \_ NEGATO**<br/> Accesso negato dalla sicurezza DCOM.<br/>                                       | L'utente non ha accesso remoto al computer tramite DCOM. In genere, si verificano errori DCOM durante la connessione a un computer remoto con una versione diversa del sistema operativo.<br/>                                                                                                                                                                                          | Concedere all'utente le autorizzazioni Di avvio remoto e Attivazione remota in dcomcnfg. Fare clic con il pulsante Computer locale-> proprietà. In Sicurezza COM fare clic su "Modifica limiti" per entrambe le sezioni. Concedere all'utente l'accesso remoto, l'avvio remoto e l'attivazione remota. Passare quindi a Configurazione DCOM, trovare "Windows Management Instrumentation" e assegnare all'utente desiderato l'avvio remoto e l'attivazione remota. Per altre informazioni, vedere [Connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 ACCESSO **E WBEM \_ NEGATO \_ \_**<br/> Accesso negato da un [ *provider*](gloss-p.md)<br/> | L'utente non dispone dell'autorizzazione per eseguire l'operazione in WMI. Questo problema può verificarsi quando si esegue una query su determinate classi come utente con diritti limitati, ma nella maggior parte dei casi si verifica quando si tenta di richiamare metodi o di modificare istanze WMI come utente con diritti limitati. Lo spazio dei nomi a cui ci si connette è crittografato e l'utente sta tentando di connettersi con una connessione non crittografata<br/> | Concedere all'utente l'accesso con il controllo WMI (assicurarsi che l'accesso remoto sia impostato su true) Connessione un \_ client che supporta la crittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   In genere, si verificano errori DCOM durante la connessione a un computer remoto con una versione diversa del sistema operativo.

-   I provider possono anche negare l'accesso ai dati in spazi dei nomi specifici o possono richiedere determinati livelli di sicurezza della connessione. Per altre informazioni, vedere [Impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md) e Hosting e sicurezza del [provider](provider-hosting-and-security.md).

-   Errori di accesso negato da Internet Connection Firewall (ICF).

    Per altre informazioni, vedere [Connessione tramite Windows firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   Un errore di accesso negato viene restituito dalla sicurezza DCOM quando un client con integrità bassa tenta di accedere a WMI. Ad esempio, un controllo ActiveX in esecuzione in Internet Explorer, il cui livello di sicurezza è impostato su basso, non ha accesso per eseguire operazioni WMI locali.

    **Windows 7:** Gli utenti con integrità bassa dispongono di autorizzazioni di sola lettura per le operazioni WMI locali.

## <a name="information-on-errors"></a>Informazioni sugli errori

Quando viene visualizzato un messaggio di errore da WMI, è possibile individuare il messaggio in Costanti di errore [**WMI**](wmi-error-constants.md) o, per lo scripting, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). Tuttavia, le informazioni fornite solo dall'errore non sono in genere sufficienti per determinare cosa accade. Il danneggiamento del repository WMI può mascherarsi come classi o istanze "non trovate".

Per altre informazioni sugli errori WMI:

-   I log WMI rilevano gli eventi dall'interno del core WMI e dai provider. Per altre informazioni, vedere [Registrazione dell'attività WMI](logging-wmi-activity.md).
-   Usare le classi [di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md) per controllare lo stato interno WMI o ricevere notifiche di eventi del provider o del servizio WMI. Per altre informazioni, vedere Configurazione del provider e Risoluzione [dei problemi relativi alle classi e](provider-configuration-and-troubleshooting-classes.md) Risoluzione dei problemi relativi alle applicazioni client [WMI.](troubleshooting-wmi-client-applications.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di WMI](wmi-troubleshooting.md)
</dt> <dt>

[Traccia dell'attività WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrazione dell'attività WMI](logging-wmi-activity.md)
</dt> </dl>

 

