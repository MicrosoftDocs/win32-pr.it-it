---
title: Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows
description: Usare questi suggerimenti per risolvere i problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto dell'app.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: c6438f9a8d600e9df6956f61bb6317cec575c57f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480597"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows

Usare questi suggerimenti per risolvere i problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto dell'app Windows (con estensione msix/.appx) come sviluppatore.

> [!NOTE]
> Questo articolo è destinato agli sviluppatori. Se non si è uno sviluppatore e si sta cercando assistenza per un errore di installazione dell Windows app, vedere Windows [supporto](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Ottenere informazioni di diagnostica

Quando un'API ha esito negativo, restituisce un codice di errore che descrive il problema. Se il codice di errore non fornisce informazioni sufficienti, è possibile trovare altre informazioni di diagnostica nei log eventi dettagliati.

Per accedere ai log eventi di creazione pacchetti e distribuzione **usando Visualizzatore eventi**, seguire questa procedura:

1. Effettuare uno dei passaggi indicati di seguito.

    * Fare **clic** su Start nel menu Windows, **digitare Visualizzatore eventi** e premere **INVIO.**
    * Eseguire **eventvwr.msc**.

2. Nella pagina a sinistra espandere Visualizzatore eventi registri applicazioni e servizi **(locali)**  >    >  **di Microsoft**  >  **Windows**.
3. Controllare i log disponibili nelle categorie seguenti:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Per iniziare, vedere i log in **AppXDeployment-Server.** Se l'errore è stato **causato da 0x80073CF0** o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, potrebbero essere presenti altri dettagli nei log **di AppxpackagingOM.**

È anche possibile usare il [comando Get-AppxLog](/powershell/module/appx/get-appxlog) in PowerShell per ottenere i primi eventi registrati. Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente.

```PowerShell
Get-Appxlog
```

Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente in una tabella interattiva in una finestra separata.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Codici di errore comuni

Questa tabella elenca alcuni dei codici di errore più comuni. Se è necessaria ulteriore assistenza per uno di questi errori o se si verifica un codice di errore non in questo elenco, vedere le [opzioni della Guida aggiuntive](#get-additional-help).


| Codice di errore | valore | Descrizione e possibili cause | 
|------------|-------|---------------------------------|
| <strong>E_FILENOTFOUND</strong> | 0x80070002 | Il file o il percorso non è stato trovato. Ciò può verificarsi durante una convalida della libreria dei tipi COM richiede che il percorso della directory esista effettivamente all'interno del pacchetto MSIX.<br /> | 
| <strong>ERROR_BAD_FORMAT</strong> | 0x8007000B | Il pacchetto non è formattato correttamente e deve essere ri-compilato o firmato di nuovo.<br /> Questo errore può verificarsi in caso di mancata corrispondenza tra il nome del soggetto del certificato di firma e il nome dell'AppxManifest.xml pubblicazione.<br /> Vedere <a href="how-to-sign-a-package-using-signtool.md">Come firmare un pacchetto dell'app usando SignTool.</a><br /> | 
| <strong>E_INVALIDARG</strong> | 0x80070057 | Uno o più argomenti non sono validi. Se si controlla il registro eventi di AppXDeployment-Server e viene visualizzato l'evento seguente: "Durante l'installazione del pacchetto, il sistema non è riuscito a registrare l'estensione windows.repositoryExtension a causa dell'errore seguente: Il parametro non è corretto". <br /> Questo errore può verificarsi se gli elementi del manifesto DisplayName o Description contengono caratteri non consentiti Windows firewall; Cioè  |  e tutti , a causa del Windows non riesce a creare il profilo AppContainer per il pacchetto. Rimuovere questi caratteri dal manifesto e provare a installare il pacchetto. <br /> | 
| <strong>ERROR_INSTALL_OPEN_</strong><br /><strong>PACKAGE_FAILED</strong><br /> | 0x80073CF0 | Non è stato possibile aprire il pacchetto.<br /> Cause possibili:<br /><ul><li>Il pacchetto non è firmato.</li><li>Il nome dell'editore non corrisponde al soggetto del certificato di firma.</li><li>Il file:// è mancante o il pacchetto non è stato trovato nel percorso specificato.</li></ul>Per altre informazioni, vedere il <strong>registro eventi appxPackagingOM.</strong><br /> | 
| <strong>ERROR_INSTALL_PACKAGE_</strong><br /><strong>NOT_FOUND</strong><br /> | 0x80073CF1 | Non è stato possibile trovare il pacchetto.<br /> Questo errore può verificarsi durante la rimozione di un pacchetto non installato per l'utente corrente.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>PACCHETTO</strong><br /> | 0x80073CF2 | I dati del pacchetto non sono validi.<br /> | 
| <strong>ERROR_INSTALL_RESOLVE_</strong><br /><strong>DEPENDENCY_FAILED</strong><br /> | 0x80073CF3 | Non è stato possibile completare la convalida dell'aggiornamento, delle dipendenze o dei conflitti per il pacchetto.<br /> Cause possibili:<br /><ul><li>Il pacchetto in arrivo è in conflitto con un pacchetto installato.</li><li>Non è possibile trovare una dipendenza del pacchetto specificata.</li><li>Il pacchetto non supporta l'architettura del processore corretta.</li></ul>Per altre informazioni, controllare il <strong>registro eventi di AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_OUT_</strong><br /><strong>OF_DISK_SPACE</strong><br /> | 0x80073CF4 | Lo spazio su disco nel computer non è sufficiente. Liberare spazio e riprovare.<br /> | 
| <strong>ERROR_INSTALL_NETWORK_</strong><br /><strong>FALLIMENTO</strong><br /> | 0x80073CF5 | Non è possibile scaricare il pacchetto.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>REGISTRATION_FAILURE</strong><br /> | 0x80073CF6 | Non è possibile registrare il pacchetto.<br /> Per altre informazioni, vedere il <strong>registro eventi AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>DEREGISTRATION_EFAILURE</strong><br /> | 0x80073CF7 | Non è possibile annullare la registrazione del pacchetto.<br /> È possibile che venga visualizzato questo errore durante la rimozione di un pacchetto.<br /> Per altre informazioni, vedere il <strong>registro eventi AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_CANCEL</strong> | 0x80073CF8 | L'utente ha annullato la richiesta di installazione.<br /> | 
| <strong>ERROR_INSTALL_FAILED</strong> | 0x80073CF9 | Installazione del pacchetto non riuscita. Contattare il fornitore del software.<br /> Per altre informazioni, vedere il <strong>registro eventi AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_REMOVE_FAILED</strong> | 0x80073CFA | Rimozione del pacchetto non riuscita.<br /> È possibile che venga visualizzato questo errore per gli errori che si verificano durante la disinstallazione del pacchetto.<br /> Per altre informazioni, vedere <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync.</strong></a><br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>ALREADY_EXISTS</strong><br /> | 0x80073CFB | Il pacchetto fornito è già installato, pertanto la reinstallazione del pacchetto è stata bloccata. <br /> Questo errore può verificarsi se si installa un pacchetto che non è identico bit per bit al pacchetto già installato. Si noti che anche la firma digitale fa parte del pacchetto. Di conseguenza, se un pacchetto viene ricompilato o ricreato, non è più identico bit per bit al pacchetto installato in precedenza. Due possibili opzioni per correggere l'errore sono: (1) Incrementare il numero di versione dell'app, quindi ricompilare e ricompilare il pacchetto (2) Rimuovere il pacchetto precedente per ogni utente nel sistema prima di installare il nuovo pacchetto. <br /> | 
| <strong>ERROR_NEEDS_REMEDIATION</strong> | 0x80073CFC | L'app non può essere avviata. Provare a reinstallare l'app.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PREREQUISITE_FAILED</strong><br /> | 0x80073CFD | Non è stato possibile soddisfatto un prerequisito di installazione specificato.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>REPOSITORY_CORRUPTED</strong><br /> | 0x80073CFE | Il repository dei pacchetti è danneggiato.<br /> Questo errore può verificarsi se la cartella a cui fa riferimento questa chiave del Registro di sistema non esiste o è danneggiata: <br /><strong>HKLM\Software\Microsoft\Windows\</strong><br /><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br /> Per eseguire il ripristino da questo stato, aggiornare il PC.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>POLICY_FAILURE</strong><br /> | 0x80073CFF | Per installare questa app, è necessaria una licenza per sviluppatori o un sistema abilitato per il sideload. <br /> Questo errore può verificarsi se il pacchetto non soddisfa uno dei requisiti seguenti:<br /><ul><li>L'app viene distribuita usando F5 in Visual Studio in un computer con una licenza Windows developer.</li><li>Il pacchetto viene firmato con una firma Microsoft e distribuito come parte Windows o dal Microsoft Store.</li><li>Il pacchetto viene firmato con una firma attendibile e installato in un computer con una licenza per sviluppatori, un computer aggiunto a un dominio con il criterio AllowAllTrustedApps abilitato o un computer con una licenza di sideload di Windows con il criterio AllowAllTrustedApps abilitato.</li></ul> | 
| <strong>ERROR_PACKAGE_UPDATING</strong> | 0x80073D00 | L'app non può essere avviata perché è attualmente in fase di aggiornamento.<br /> | 
| <strong>ERROR_DEPLOYMENT_</strong><br /><strong>BLOCKED_BY_POLICY</strong><br /> | 0x80073D01 | L'operazione di distribuzione del pacchetto è bloccata dai criteri. Contattare l'amministratore del sistema.<br /> Cause possibili:<br /><ul><li>La distribuzione dei pacchetti è bloccata dai criteri di controllo delle applicazioni.</li><li>La distribuzione dei pacchetti è bloccata dal criterio "Consenti operazioni di distribuzione in profili speciali".</li></ul>Uno dei possibili motivi è la necessità di un profilo mobile. Per informazioni sulla configurazione dei profili utente mobili per gli account utente, vedere <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Distribuire profili utente mobili.</a> Se nel sistema non sono configurati criteri e viene ancora visualizzato questo errore, è possibile che si sia connessi con un profilo temporaneo. Disconnettersi e accedere di nuovo, quindi ripetere l'operazione.<br /> | 
| <strong>ERROR_PACKAGES_IN_USE</strong> | 0x80073D02 | Non è stato possibile installare il pacchetto perché le risorse che modifica sono attualmente in uso.<br /> | 
| <strong>ERROR_RECOVERY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D03 | Non è stato possibile recuperare il pacchetto perché i dati necessari per il ripristino sono danneggiati.<br /> | 
| <strong>ERROR_INVALID_</strong><br /><strong>STAGED_SIGNATURE</strong><br /> | 0x80073D04 | La firma non è valida. Per eseguire la registrazione in modalità sviluppatore, AppxSignature.p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.<br /> Gli sviluppatori che usano F5 con Visual Studio, assicurarsi che la directory del progetto compilato non contenga file di firma o mappe a blocchi delle versioni precedenti del pacchetto.<br /> | 
| <strong>ERROR_DELETING_EXISTING_</strong><br /><strong>APPLICATIONDATA_STORE_FAILED</strong><br /> | 0x80073D05 | Si è verificato un errore durante l'eliminazione dei dati dell'applicazione esistenti del pacchetto.<br /> È possibile ottenere questo errore se il <a href="/previous-versions/hh441475(v=vs.110)">simulatore</a> è in esecuzione. Chiudere il simulatore. Questo errore può essere visualizzato anche se sono presenti file aperti nei dati dell'app, ad esempio se è aperto un file di log in un editor di testo.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PACKAGE_DOWNGRADE</strong><br /> | 0x80073D06 | Non è stato possibile installare il pacchetto perché è già installata una versione successiva del pacchetto.<br /> | 
| <strong>ERROR_SYSTEM_</strong><br /><strong>NEEDS_REMEDIATION</strong><br /> | 0x80073D07 | È stato rilevato un errore in un file binario di sistema. Per risolvere il problema, provare ad aggiornare il PC. <br /> | 
| <strong>ERROR_APPX_INTEGRITY_</strong><br /><strong>FAILURE_EXTERNAL</strong><br /> | 0x80073D08 | È stato rilevato un Windows binario non danneggiato nel sistema. <br /> | 
| <strong>ERROR_RESILIENCY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D09 | Non è stato possibile riprendere l'operazione perché i dati necessari per il ripristino sono danneggiati. <br /> | 
| <strong>ERROR_INSTALL_FIREWALL_</strong><br /><strong>SERVICE_NOT_RUNNING</strong><br /> | 0x80073D0A | Non è stato possibile installare il pacchetto perché il Windows firewall non è in esecuzione. Abilitare il Windows firewall e riprovare.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_FAILED</strong> | 0x80073D0B | L'operazione di spostamento del pacchetto non è riuscita.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>NOT_EMPTY</strong><br /> | 0x80073D0C | L'operazione di distribuzione non è riuscita perché il volume non è vuoto.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>OFFLINE</strong><br /> | 0x80073D0D | L'operazione di distribuzione non è riuscita perché il volume è offline. Per un aggiornamento del pacchetto, il volume fa riferimento al volume installato di tutte le versioni del pacchetto.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>CORROTTO</strong><br /> | 0x80073D0E | L'operazione di distribuzione non è riuscita perché il volume specificato è danneggiato.<br /> | 
| <strong>ERROR_NEEDS_REGISTRATION</strong><br /><strong></strong><br /> | 0x80073D0F | L'operazione di distribuzione non è riuscita perché l'applicazione specificata deve essere registrata per prima.<br /> | 
| <strong>ERROR_INSTALL_WRONG_</strong><br /><strong>PROCESSOR_ARCHITECTURE</strong><br /> | 0x80073D10 | L'operazione di distribuzione non è riuscita perché il pacchetto è destinato all'architettura del processore errata.<br /> | 
| <strong>ERROR_DEV_SIDELOAD_</strong><br /><strong>LIMIT_EXCEEDED</strong><br /> | 0x80073D11 | È stato raggiunto il numero massimo di pacchetti sideloaded per sviluppatori consentiti in questo dispositivo. Disinstallare un pacchetto sideloaded e riprovare.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_</strong><br /><strong>MAIN_PACKAGE</strong><br /> | 0x80073D12 | Per installare questo pacchetto facoltativo è necessario un pacchetto dell'app principale. Installare prima il pacchetto principale e riprovare.<br /> | 
| <strong>ERROR_PACKAGE_NOT_</strong><br /><strong>SUPPORTED_ON_FILESYSTEM</strong><br /> | 0x80073D13 | Questo tipo di pacchetto dell'app non è supportato in questo file system.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_</strong><br /><strong>BLOCKED_BY_STREAMING</strong><br /> | 0x80073D14 | L'operazione di spostamento del pacchetto viene bloccata fino al termine dello streaming dell'applicazione.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_APPLICATIONID_</strong><br /><strong>NOT_UNIQUE</strong><br /> | 0x80073D15 | Un pacchetto dell'app principale o un altro pacchetto facoltativo ha lo stesso ID applicazione di questo pacchetto facoltativo. Modificare l'ID applicazione per il pacchetto facoltativo per evitare conflitti.<br /> | 
| <strong>ERROR_PACKAGE_STAGING_</strong><br /><strong>ONHOLD</strong><br /> | 0x80073D16 | Questa sessione di staging è stata mantenuta per consentire l'assegnazione della priorità a un'altra operazione di staging.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>RELATED_SET_UPDATE</strong><br /> | 0x80073D17 | Impossibile aggiornare un set correlato perché il set aggiornato non è valido. Tutti i pacchetti nel set correlato devono essere aggiornati contemporaneamente.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D18 | Un pacchetto facoltativo con un punto di ingresso FullTrust richiede che il pacchetto principale abbia la <strong>funzionalità runFullTrust.</strong><br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_USER_LOG_OFF</strong><br /> | 0x80073D19 | Si è verificato un errore perché un utente è stato disconnesso.<br /> | 
| <strong>ERROR_PROVISION_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_PROVISIONED</strong><br /> | 0x80073D1A | Un provisioning facoltativo del pacchetto richiede anche il provisioning del pacchetto principale delle dipendenze.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_FAILED</strong><br /> | 0x80073D1B | I pacchetti non hanno superato <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">il controllo della reputazione SmartScreen.</a><br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_TIMEDOUT</strong><br /> | 0x80073D1C | Timeout <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">dell'operazione di controllo</a> della reputazione SmartScreen.<br /> | 
| <strong>ERROR_DEPLOYMENT_OPTION_</strong><br /><strong>NOT_SUPPORTED</strong><br /> | 0x80073D1D | L'opzione di distribuzione corrente non è supportata.<br /> | 
| <strong>ERROR_APPINSTALLER_</strong><br /><strong>ACTIVATION_BLOCKED</strong><br /> | 0x80073D1E | L'attivazione è bloccata a causa delle impostazioni di aggiornamento di .appinstaller per questa app.<br /> | 
| <strong>ERROR_REGISTRATION_FROM_</strong><br /><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br /> | 0x80073D1F | Le unità remote non sono supportate. Usare <strong> \\ server\share</strong> per registrare un pacchetto remoto.<br /> | 
| <strong>ERROR_APPX_RAW_</strong><br /><strong>DATA_WRITE_FAILED</strong><br /> | 0x80073D20 | Impossibile elaborare e scrivere i dati del pacchetto scaricato su disco.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_PACKAGE</strong><br /> | 0x80073D21 | L'operazione di distribuzione è stata bloccata a causa di criteri per famiglia di pacchetti che limitano le distribuzioni in un volume non di sistema. In base ai criteri, questa app deve essere installata nell'unità di sistema, ma non è impostata come predefinita. In Archiviazione impostazioni, impostare l'unità di sistema come percorso predefinito per salvare il nuovo contenuto, quindi ripetere l'installazione.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_MACHINE</strong><br /> | 0x80073D22 | L'operazione di distribuzione è stata bloccata a causa di criteri a livello di computer che limitano le distribuzioni in un volume non di sistema. In base ai criteri, questa app deve essere installata nell'unità di sistema, ma non è impostata come predefinita. Nelle Archiviazione, impostare l'unità di sistema come percorso predefinito per salvare il nuovo contenuto, quindi ripetere l'installazione.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_PROFILE_POLICY</strong><br /> | 0x80073D23 | L'operazione di distribuzione è stata bloccata perché la distribuzione di profili speciali non è consentita (i profili speciali sono profili utente in cui le modifiche vengono rimosse dopo la connessione dell'utente). Provare ad accedere a un account che non sia un profilo speciale. È possibile provare a disconnettersi e accedere nuovamente all'account corrente oppure provare ad accedere a un account diverso.<br /> | 
| <strong>ERROR_DEPLOYMENT_FAILED_</strong><br /><strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br /><strong>DIRECTORY</strong><br /> | 0x80073D24 | L'operazione di distribuzione non è riuscita a causa di un conflitto nella directory del pacchetto <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">modificabile di un pacchetto.</a> Per installare questo pacchetto, rimuovere il pacchetto esistente con la directory del pacchetto modificabile in conflitto.<br /> | 
| <strong>ERROR_SINGLETON_RESOURCE_</strong><br /><strong>INSTALLED_IN_ACTIVE_USER</strong><br /> | 0x80073D25 | L'installazione del pacchetto non è riuscita perché è stata specificata una risorsa singleton e un altro utente con tale pacchetto installato è connesso. Assicurarsi che tutti gli utenti attivi con il pacchetto installato siano disconnessi e ripetere l'installazione.<br /> | 
| ERROR_DIFFERENT_VERSION_<strong></strong><br /><strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br /> | 0x80073D26 | L'installazione del pacchetto non è riuscita perché è installata una versione diversa del servizio. Provare a installare una versione più recente del pacchetto.<br /> | 
| <strong>ERROR_SERVICE_EXISTS_</strong><br /><strong>AS_NON_PACKAGED_SERVICE</strong><br /> | 0x80073D27 | L'installazione del pacchetto non è riuscita perché una versione del servizio esiste all'esterno di un pacchetto con estensione msix/.appx. Contattare il fornitore del software.<br /> | 
| <strong>ERROR_PACKAGED_SERVICE_</strong><br /><strong>REQUIRES_ADMIN_PRIVILEGES</strong><br /> | 0x80073D28 | L'installazione del pacchetto non è riuscita perché sono necessari privilegi di amministratore. Per installare questo pacchetto, contattare un amministratore.<br /> | 
| <strong>ERROR_REDIRECTION_TO_</strong><br /><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br /> | 0x80073D29 | La distribuzione del pacchetto non è riuscita perché l'operazione sarebbe stata reindirizzata all'account predefinito, quando il chiamante ha detto di non eseguire questa operazione.<br /> | 
| <strong>ERROR_PACKAGE_LACKS_</strong><br /><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br /> | 0x80073D2A | La distribuzione del pacchetto non è riuscita perché il pacchetto richiede una funzionalità per l'host in modo nativo.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_CONTENT</strong><br /> | 0x80073D2B | La distribuzione del pacchetto non è riuscita perché il relativo contenuto non è valido per un pacchetto non firmato.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2C | La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi senza segno.<br /> | 
| <strong>ERROR_SIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2D | La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi firmato.<br /> | 
| <strong>ERROR_PACKAGE_EXTERNAL_</strong><br /><strong>LOCATION_NOT_ALLOWED</strong><br /> | 0x80073D2E | La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi firmato.<br /> | 
| <strong>ERROR_INSTALL_FULLTRUST_</strong><br /><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D2F | Una dipendenza di runtime dell'host che risolve un pacchetto con contenuto con attendibilità totale richiede che il pacchetto principale abbia la <strong>funzionalità runFullTrust.</strong><br /> | 
| <strong>APPX_E_PACKAGING_INTERNAL</strong> | 0x80080200 | L'API di creazione pacchetti ha rilevato un errore interno.<br /> | 
| <strong>APPX_E_INTERLEAVING_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080201 | Il pacchetto non è valido perché il relativo contenuto è interleaved.<br /> | 
| <strong>APPX_E_RELATIONSHIPS_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080202 | Il pacchetto non è valido perché contiene relazioni OPC.<br /> | 
| <strong>APPX_E_MISSING_</strong><br /><strong>REQUIRED_FILE</strong><br /> | 0x80080203 | Il pacchetto non è valido perché manca un manifesto o una mappa a blocchi oppure è presente un file di integrità del codice, ma manca un file di firma.<br /> Assicurarsi che nel pacchetto non mancano uno o più di questi file necessari:<br /><ul><li>\AppxManifest.xml</li><li>\AppxBlockMap.xml</li></ul>Se il pacchetto contiene \AppxMetadata\CodeIntegrity.cat, deve contenere anche \AppxSignature.p7x.<br /> | 
| <strong>APPX_E_INVALID_MANIFEST</strong> | 0x80080204 | Il file di AppxManifest.xml pacchetto non è valido.<br /> | 
| <strong>APPX_E_INVALID_BLOCKMAP</strong> | 0x80080205 | Il file di AppxBlockMap.xml pacchetto non è valido.<br /> | 
| <strong>APPX_E_CORRUPT_CONTENT</strong> | 0x80080206 | Non è possibile leggere il contenuto del pacchetto perché è danneggiato.<br /> | 
| <strong>APPX_E_BLOCK_</strong><br /><strong>HASH_INVALID</strong><br /> | 0x80080207 | Il valore hash calcolato del blocco non corrisponde al valore has archiviato nella mappa a blocchi.<br /> | 
| <strong>APPX_E_REQUESTED_</strong><br /><strong>RANGE_TOO_LARGE</strong><br /> | 0x80080208 | L'intervallo di byte richiesto è superiore a 4 GB quando viene convertito in un intervallo di byte di blocchi.<br /> | 
| <strong>TRUST_E_NOSIGNATURE</strong> | 0x800B0100 | Nell'oggetto non è presente alcuna firma.<br /> Questo errore può essere visualizzato se il pacchetto non è firmato o se la firma non è valida. Il pacchetto deve essere firmato per la distribuzione.<br /> | 
| <strong>CERT_E_UNTRUSTEDROOT</strong> | 0x800B0109 | Catena di certificati elaborata, ma terminata in un certificato radice non considerato attendibile dal provider di attendibilità.<br /> Vedere <a href="/previous-versions/br230260(v=vs.110)">Firma di un pacchetto</a>.<br /> | 
| <strong>CERT_E_CHAINING</strong> | 0x800B010A | Non è stato possibile creare una catena di certificati per un'autorità di certificazione radice attendibile.<br /> Vedere <a href="/previous-versions/br230260(v=vs.110)">Firma di un pacchetto</a>.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>SIP_CLIENT_DATA</strong><br /> | 0x80080209 | La <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>usata per firmare il pacchetto non contiene i dati necessari<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>KEY_INFO</strong><br /> | 0x8008020A | La <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilizzata per crittografare o decrittografare il pacchetto contiene dati non validi.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>CONTENTGROUPMAP</strong><br /> | 0x8008020B | La mappa del gruppo di contenuto del pacchetto con estensione msix/.appx non è valida.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>APPINSTALLER</strong><br /> | 0x8008020C | Il <a href="/windows/msix/app-installer/app-installer-root">file con estensione appinstaller</a> per il pacchetto non è valido.<br /> | 
| <strong>APPX_E_DELTA_BASELINE_</strong><br /><strong>VERSION_MISMATCH</strong><br /> | 0x8008020D | La versione del pacchetto di base nel pacchetto differenziale non corrisponde alla versione nel pacchetto di base da aggiornare.<br /> | 
| <strong>APPX_E_DELTA_PACKAGE_</strong><br /><strong>MISSING_FILE</strong><br /> | 0x8008020E | Nel pacchetto delta manca un file dal pacchetto aggiornato.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>DELTA_PACKAGE</strong><br /> | 0x8008020F | Il pacchetto delta non è valido.<br /> | 
| <strong>APPX_E_DELTA_APPENDED_</strong><br /><strong>PACKAGE_NOT_ALLOWED</strong><br /> | 0x80080210 | Il pacchetto accodato delta non è consentito per l'operazione corrente.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGING_LAYOUT</strong><br /> | 0x80080211 | Il file di layout di creazione pacchetti non è valido.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGESIGNCONFIG</strong><br /> | 0x80080212 | Il file packageSignConfig non è valido.<br /> | 
| <strong>APPX_E_RESOURCESPRI_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080213 | Il file resources.pri non è consentito quando non sono presenti elementi di risorse nel manifesto del pacchetto.<br /> | 
| <strong>APPX_E_FILE_</strong><br /><strong>COMPRESSION_MISMATCH</strong><br /> | 0x80080214 | Lo stato di compressione del file nella baseline e nel pacchetto aggiornato non corrisponde.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PAYLOAD_PACKAGE_EXTENSION</strong><br /> | 0x80080215 | Le estensioni non .appx non sono consentite per i pacchetti payload che hanno come destinazione piattaforme precedenti.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br /> | 0x80080216 | Il file encryptionExclusionFileList non è valido.<br /> | 


## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Le applicazioni non vengono avviate e i relativi nomi sono in grigio

In un computer Windows 10 non è possibile avviare alcune applicazioni e i nomi delle applicazioni vengono visualizzati in grigio.

![Alcuni nomi di applicazione vengono visualizzati in grigio nel menu Start](./images/app-names-dimmed.png)

Quando si tenta di aprire un'applicazione selezionando il nome in grigio, è possibile che venga visualizzato uno dei messaggi di errore seguenti:

> Si è verificato un problema con \<*application name*> . Contattare l'amministratore di sistema per ripristinarlo o reinstallarlo  
> Errore: Questa app non può essere aperta

Inoltre, le voci di evento seguenti vengono registrate nel registro "Microsoft-Windows-TWinUI/Operational" in Applicazioni e **servizi\Microsoft\Windows\Apps**:

> Nome log: Microsoft-Windows-TWinUI/Operational  
> Origine: Microsoft-Windows-Immersive-Shell  
> Data: <*data*>  
> ID evento: 5960  
> Categoria attività: (5960)  
> Livello: Errore  
> Parole chiave:  
> Descrizione:  
> Attivazione dell'app Microsoft.BingNews_8wekyb3d8bbwe! AppexNews per l'Windows. Il contratto di avvio è stato bloccato con 0x80073CFC perché il pacchetto è in stato: Modificato.  

### <a name="cause"></a>Causa

Questo problema si verifica perché la voce del Registro di sistema per il valore di stato del pacchetto corrispondente dell'applicazione è stata modificata.

### <a name="resolution"></a>Risoluzione

> [!WARNING]
> Se si modifica il registro di sistema in modo non corretto utilizzando l'Editor del Registro di sistema o un altro metodo, si possono causare gravi problemi. che per essere risolti potrebbero richiedere la reinstallazione del sistema operativo. Microsoft non garantisce la possibilità di risolvere questi problemi. La modifica del Registro di sistema è a rischio e pericolo dell'utente.

Per risolvere il problema:

1. Avviare l'editor del Registro di sistema e quindi **individuareHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** sottochiave.
2. Per eseguire il backup dei dati della sottochiave, fare clic con il pulsante destro del mouse su **PackageList**, scegliere **Esporta** e quindi salvare i dati come file del Registro di sistema.
3. Per ognuna delle applicazioni elencate nelle voci di log ID evento 5960, seguire questa procedura:  
   1. Individuare la **voce PackageStatus.**
   2. Impostare il valore di **PackageStatus** su zero (**0**).
   > [!NOTE]  
   > Se non sono presenti voci per l'applicazione in **PackageList**, il problema ha un'altra causa. Nel caso dell'evento di esempio in questo articolo, la sottochiave completa è **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Riavviare il computer.

## <a name="get-additional-help"></a>Ottenere altre informazioni

Per altre informazioni sulla risoluzione di un problema che si verifica durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto di app Windows (con estensione msix/.appx) come sviluppatore, fare riferimento a queste risorse aggiuntive di supporto per sviluppatori.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offre risposte pertinenti e rapide ai problemi tecnici di una community di esperti e tecnici Microsoft.
- Per assistenza della community per le domande sullo sviluppo, sono disponibili [i forum](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)e [StackOverflow](https://stackoverflow.com/questions).
- Il [Windows di supporto per sviluppatori](https://developer.microsoft.com/windows/support) illustra altre opzioni di supporto.

## <a name="related-topics"></a>Argomenti correlati

- [Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)
- [Come risolvere gli errori di firma del pacchetto dell'app](how-to-troubleshoot-app-package-signature-errors.md)
