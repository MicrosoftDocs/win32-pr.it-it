---
description: Quando si accede a dati locali o remoti WMI in un'applicazione o in uno script, è possibile che si verifichino errori da classi mancanti a accesso negato. Ai provider sono inoltre disponibili opzioni di debug e classi di risoluzione dei problemi.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Risoluzione dei problemi di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ccb8afa1af64e6eb80050c96973a9ad9456a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880650"
---
# <a name="wmi-troubleshooting"></a>Risoluzione dei problemi di WMI

Quando si accede a dati locali o remoti WMI in un'applicazione o in uno script, è possibile che si verifichino errori da classi mancanti a accesso negato. Ai provider sono inoltre disponibili opzioni di debug e classi di risoluzione dei problemi.

> [!Note]  
> La seguente documentazione è destinata agli sviluppatori e agli amministratori IT. Se si è un utente finale che ha riscontrato un messaggio di errore relativo a WMI, è necessario passare a [supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore. Per ulteriori informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere la pagina relativa al [funzionamento di WMI.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilità di diagnosi di WMI

L'utilità diagnostica WMI (WMIDiag.exe) non è più supportata a partire da Windows 8 e Windows Server 2012.

* * Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008: * *

Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.

Per ottenere ulteriori informazioni sull'origine del problema, è possibile scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft. È possibile scaricare il Utilità di diagnosi di WMI nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

I writer del provider possono inoltre riscontrare problemi di debug a meno che non si stia scrivendo un [*provider disaccoppiato*](gloss-d.md). Per ulteriori informazioni, vedere [provider di debug](debugging-providers.md).

## <a name="logging-and-tracing"></a>Registrazione e traccia

I file di log WMI non esistono più. sono stati sostituiti da [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal). Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md), [registrazione dell'attività WMI](logging-wmi-activity.md)e [file di log WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Risoluzione dei problemi negli script e nelle applicazioni

WMI contiene un set di classi per la [risoluzione dei problemi relativi](wmi-troubleshooting-classes.md) alle applicazioni client che utilizzano provider WMI. Per ulteriori informazioni, vedere [risoluzione dei problemi relativi alle applicazioni client WMI](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Come i writer del provider possono impedire problemi WMI

I writer del provider possono impedire molti problemi, che vengono visualizzati nei messaggi di errore tramite WMI, eseguendo le azioni seguenti:

-   Registrazione corretta del provider. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).
-   Aggiunta dell'istruzione [**\# pragma autocover**](pragma-autorecover.md) al file Managed Object Format (MOF) che definisce le classi del provider.

Per ulteriori informazioni, vedere [provider di debug](debugging-providers.md), [fornire dati a WMI](providing-data-to-wmi.md)e [classi di configurazione e risoluzione dei problemi del provider](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Accesso negato

Gli errori di accesso negato segnalati da script e applicazioni che accedono ai dati e agli spazi dei nomi WMI in genere rientrano in tre categorie. La tabella seguente elenca le tre categorie di errori insieme ai problemi che potrebbero causare errori e soluzioni possibili.



| Errore                                                                                                                        | Possibili problemi                                                                                                                                                                                                                                                                                                                                                                     | Soluzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema del firewall o server non disponibile.<br/>      | Il computer non esiste effettivamente perché il Windows Firewall blocca la connessione<br/>                                                                                                                                                                                                                                                                                        | Connessione a vista: **netsh advfirewall firewall set Rule Group = "Strumentazione gestione Windows (WMI)" nuovo enable = sì** connessione a livello inferiore: consentire la regola "amministrazione remota" in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| **\_ accesso \_ negato** per 0x80070005 E<br/> Accesso negato dalla sicurezza DCOM.<br/>                                       | L'utente non dispone di accesso remoto al computer tramite DCOM. In genere, gli errori DCOM si verificano durante la connessione a un computer remoto con una versione del sistema operativo diversa.<br/>                                                                                                                                                                                          | Concedere all'utente le autorizzazioni di avvio remoto e attivazione remota in DCOMCNFG. Fare clic con il pulsante destro del mouse su Proprietà Computer locale >. In sicurezza COM fare clic su "Modifica limiti" per entrambe le sezioni. Fornire all'utente l'accesso remoto, l'avvio remoto e l'attivazione remota. Passare quindi a DCOM config, trovare "Strumentazione gestione Windows" e fornire all'utente l'avvio remoto e l'attivazione remota. Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ accesso \_ negato**<br/> Accesso negato da un [ *provider*](gloss-p.md)<br/> | L'utente non dispone delle autorizzazioni necessarie per eseguire l'operazione in WMI. Questo problema può verificarsi quando si esegue una query su determinate classi come utente con diritti limitati, ma spesso si verifica quando si tenta di richiamare metodi o di modificare le istanze WMI come utente con diritti limitati. Lo spazio dei nomi a cui ci si connette è crittografato e l'utente sta tentando di connettersi con una connessione non crittografata<br/> | Concedere all'utente l'accesso con il controllo WMI (assicurarsi che accesso remoto sia \_ impostato su true) connettersi usando un client che supporta la crittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   In genere, gli errori DCOM si verificano durante la connessione a un computer remoto con una versione del sistema operativo diversa.

-   I provider possono anche negare l'accesso ai dati in spazi dei nomi specifici o potrebbero richiedere determinati livelli di sicurezza della connessione. Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md) e [hosting e sicurezza del provider](provider-hosting-and-security.md).

-   Errori di accesso negato da modifiche a Internet Connection Firewall (ICF).

    Per ulteriori informazioni, vedere la pagina relativa alla [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   Un errore di accesso negato viene restituito dalla sicurezza DCOM quando un client con integrità bassa tenta di accedere a WMI. Ad esempio, un controllo ActiveX eseguito in Internet Explorer, il cui livello di sicurezza è impostato su Low, non dispone dell'accesso per eseguire operazioni WMI locali.

    **Windows 7:** Gli utenti con integrità bassa hanno autorizzazioni di sola lettura per le operazioni WMI locali.

## <a name="information-on-errors"></a>Informazioni sugli errori

Quando si riceve un messaggio di errore da WMI, è possibile individuare il messaggio nelle [**costanti di errore WMI**](wmi-error-constants.md) oppure, per lo scripting, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). Tuttavia, le informazioni fornite solo dall'errore non sono in genere sufficienti a determinare cosa accade. Il danneggiamento del repository WMI può essere mascherato da classi o istanze "non trovate".

Per ulteriori informazioni sugli errori WMI:

-   I registri WMI registrano gli eventi all'interno del nucleo WMI e dai provider. Per ulteriori informazioni, vedere [registrazione dell'attività WMI](logging-wmi-activity.md).
-   Utilizzare le [classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md) per controllare lo stato interno WMI o ricevere notifiche di eventi del provider o del servizio WMI. Per ulteriori informazioni, vedere la pagina relativa alla [configurazione e alla risoluzione dei problemi delle classi](provider-configuration-and-troubleshooting-classes.md) e risoluzione dei problemi delle [applicazioni client WMI](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Traccia dell'attività WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrazione dell'attività WMI](logging-wmi-activity.md)
</dt> </dl>

 

