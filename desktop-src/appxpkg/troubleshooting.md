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
ms.openlocfilehash: ce602d4a65d0287154a9eee94665d025a628f6d8ce3a7f086700625820637a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552314"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Risoluzione dei problemi di creazione pacchetti, distribuzione e query delle app Windows

Usare questi suggerimenti per risolvere i problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto di app Windows (.msix/.appx) come sviluppatore.

> [!NOTE]
> Questo articolo è destinato agli sviluppatori. Se non si è uno sviluppatore e si sta cercando assistenza per un errore di installazione dell Windows app, vedere Windows [supporto .](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)

## <a name="get-diagnostic-information"></a>Ottenere informazioni di diagnostica

Quando un'API ha esito negativo, restituisce un codice di errore che descrive il problema. Se il codice di errore non fornisce informazioni sufficienti, sono disponibili altre informazioni di diagnostica nei log eventi dettagliati.

Per accedere ai log eventi di creazione di pacchetti e distribuzione **usando Visualizzatore eventi**, seguire questa procedura:

1. Effettuare uno dei passaggi indicati di seguito.

    * Scegliere **Avvia** dal menu Windows, digitare **Visualizzatore eventi** e **premere INVIO.**
    * Eseguire **eventvwr.msc**.

2. Nella pagina a sinistra espandere Visualizzatore eventi registri applicazioni **e** servizi  >    >    >  **(locali)** microsoft Windows .
3. Controllare i log disponibili nelle categorie seguenti:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Per iniziare, vedere i log in **AppXDeployment-Server**. Se l'errore è stato **causato da 0x80073CF0** o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, nei log **appxpackagingOM** potrebbero essere presenti altri dettagli.

È anche possibile usare il [comando Get-AppxLog](/powershell/module/appx/get-appxlog) in PowerShell per ottenere i primi eventi registrati. Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente.

```PowerShell
Get-Appxlog
```

Nell'esempio seguente vengono visualizzati i log associati all'operazione di distribuzione più recente in una tabella interattiva in una finestra separata.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Codici di errore comuni

In questa tabella sono elencati alcuni dei codici di errore più comuni. Se è necessaria ulteriore assistenza per uno di questi errori o se si verifica un codice di errore non in questo elenco, vedere [le opzioni della](#get-additional-help)Guida aggiuntive .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice di errore</th>
<th>Valore</th>
<th>Descrizione e possibili cause</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>Il file o il percorso non è stato trovato. Ciò può verificarsi durante una convalida della libreria dei tipi COM richiede che il percorso della directory esista effettivamente all'interno del pacchetto MSIX.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>Il pacchetto non è formattato correttamente e deve essere ri-compilato o firmato di nuovo.<br/> Questo errore può verificarsi se non è presente una corrispondenza tra il nome soggetto del certificato di firma e il nome dell'AppxManifest.xml dell'editore.<br/> Vedere <a href="how-to-sign-a-package-using-signtool.md">Come firmare un pacchetto dell'app usando SignTool.</a><br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Uno o più argomenti non sono validi. Se si controlla il registro eventi AppXDeployment-Server e viene visualizzato l'evento seguente: "Durante l'installazione del pacchetto, il sistema non è riuscito a registrare l'estensione windows.repositoryExtension a causa dell'errore seguente: Il parametro non è corretto". <br/> Questo errore può essere visualizzato se gli elementi del manifesto DisplayName o Description contengono caratteri non consentiti Windows firewall. in |  e all , a causa del quale Windows non riesce a creare il profilo AppContainer per il pacchetto. Rimuovere questi caratteri dal manifesto e provare a installare il pacchetto. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>Impossibile aprire il pacchetto.<br/> Cause possibili:<br/>
<ul>
<li>Il pacchetto non è firmato.</li>
<li>Il nome dell'editore non corrisponde al soggetto del certificato di firma.</li>
<li>Il file:// è mancante o il pacchetto non è stato trovato nel percorso specificato.</li>
</ul>
Per altre informazioni, controllare il <strong>registro eventi appxPackagingOM.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>Impossibile trovare il pacchetto.<br/> È possibile che venga visualizzato questo errore durante la rimozione di un pacchetto non installato per l'utente corrente.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>Pacchetto</strong><br/></td>
<td>0x80073CF2</td>
<td>I dati del pacchetto non sono validi.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>Non è stato possibile completare la convalida dell'aggiornamento, delle dipendenze o dei conflitti per il pacchetto.<br/> Cause possibili:<br/>
<ul>
<li>Il pacchetto in arrivo è in conflitto con un pacchetto installato.</li>
<li>Impossibile trovare una dipendenza del pacchetto specificata.</li>
<li>Il pacchetto non supporta l'architettura del processore corretta.</li>
</ul>
Per altre informazioni, controllare il <strong>registro eventi AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>Lo spazio su disco nel computer non è sufficiente. Liberare spazio e riprovare.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>Fallimento</strong><br/></td>
<td>0x80073CF5</td>
<td>Non è possibile scaricare il pacchetto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>Non è possibile registrare il pacchetto.<br/> Per altre informazioni, controllare il <strong>registro eventi AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>Non è possibile annullare la registrazione del pacchetto.<br/> È possibile che venga visualizzato questo errore durante la rimozione di un pacchetto.<br/> Per altre informazioni, controllare il <strong>registro eventi AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>L'utente ha annullato la richiesta di installazione.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>Installazione del pacchetto non riuscita. Contattare il fornitore del software.<br/> Per altre informazioni, controllare il <strong>registro eventi AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>Rimozione del pacchetto non riuscita.<br/> È possibile che venga visualizzato questo errore per gli errori che si verificano durante la disinstallazione del pacchetto.<br/> Per altre informazioni, vedere <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>Il pacchetto fornito è già installato, pertanto la reinstallazione del pacchetto è stata bloccata. <br/> Questo errore può verificarsi se si installa un pacchetto che non è bit per bit identico al pacchetto già installato. Si noti che anche la firma digitale fa parte del pacchetto. Pertanto, se un pacchetto viene ricompilato o dimesso, non è più identico bit per bit al pacchetto installato in precedenza. Due possibili opzioni per correggere l'errore sono: (1) Incrementare il numero di versione dell'app, quindi ricompilare e dimettere il pacchetto (2) Rimuovere il pacchetto precedente per ogni utente del sistema prima di installare il nuovo pacchetto. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>L'app non può essere avviata. Provare a reinstallare l'app.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>Non è stato possibile soddisfatto un prerequisito di installazione specificato.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>Il repository dei pacchetti è danneggiato.<br/> Questo errore può verificarsi se la cartella a cui fa riferimento questa chiave del Registro di sistema non esiste o è danneggiata: <br/> <strong>HKLM\Software\Microsoft\Windows\</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> Per eseguire il ripristino da questo stato, aggiornare il PC.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Per installare questa app, è necessaria una licenza per sviluppatori o un sistema abilitato per il sideload. <br/> Questo errore può essere visualizzato se il pacchetto non soddisfa uno dei requisiti seguenti:<br/>
<ul>
<li>L'app viene distribuita usando F5 in Visual Studio in un computer con una licenza Windows per sviluppatori.</li>
<li>Il pacchetto viene firmato con una firma Microsoft e distribuito come parte del Windows o dal Microsoft Store.</li>
<li>Il pacchetto viene firmato con una firma attendibile e installato in un computer con una licenza per sviluppatori, un computer aggiunto a un dominio con il criterio AllowAllTrustedApps abilitato o un computer con una licenza di sideload Windows con i criteri AllowAllTrustedApps abilitati.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>L'app non può essere avviata perché è in fase di aggiornamento.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>L'operazione di distribuzione del pacchetto è bloccata dai criteri. Contattare l'amministratore del sistema.<br/> Cause possibili:<br/>
<ul>
<li>La distribuzione dei pacchetti è bloccata dai criteri di controllo delle applicazioni.</li>
<li>La distribuzione dei pacchetti è bloccata dal criterio &quot; Consenti operazioni di distribuzione nei profili &quot; speciali.</li>
</ul>
Uno dei motivi possibili è la necessità di un profilo mobile. Per informazioni sulla configurazione dei profili utente mobili per gli account utente, vedere <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Distribuire profili utente mobili</a>. Se nel sistema non sono configurati criteri e viene ancora visualizzato questo errore, è possibile che si sia connessi con un profilo temporaneo. Disconnettersi e accedere di nuovo, quindi riprovare a eseguire l'operazione.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>Non è stato possibile installare il pacchetto perché le risorse che modifica sono attualmente in uso.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>Non è stato possibile ripristinare il pacchetto perché i dati necessari per il ripristino sono danneggiati.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>La firma non è valida. Per eseguire la registrazione in modalità sviluppatore, AppxSignature.p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.<br/> Se si usa F5 con Visual Studio, assicurarsi che la directory del progetto compilata non contenga file di firma o di mapping a blocchi delle versioni precedenti del pacchetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>Si è verificato un errore durante l'eliminazione dei dati dell'applicazione esistenti del pacchetto.<br/> È possibile ottenere questo errore se il <a href="/previous-versions/hh441475(v=vs.110)">simulatore</a> è in esecuzione. Chiudere il simulatore. È anche possibile visualizzare questo errore se sono presenti file aperti nei dati dell'app, ad esempio se è aperto un file di log in un editor di testo.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>Non è stato possibile installare il pacchetto perché è già installata una versione più recente di questo pacchetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>È stato rilevato un errore in un file binario di sistema. Per risolvere il problema, provare ad aggiornare il PC. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>È stato rilevato un Windows binario non danneggiato nel sistema. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>Impossibile riprendere l'operazione perché i dati necessari per il ripristino sono danneggiati. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>Non è stato possibile installare il pacchetto perché il Windows firewall non è in esecuzione. Abilitare il Windows Firewall e riprovare.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>L'operazione di spostamento del pacchetto non è riuscita.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>L'operazione di distribuzione non è riuscita perché il volume non è vuoto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Offline</strong><br/></td>
<td>0x80073D0D</td>
<td>L'operazione di distribuzione non è riuscita perché il volume è offline. Per un aggiornamento del pacchetto, il volume fa riferimento al volume installato di tutte le versioni del pacchetto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Corrotto</strong><br/></td>
<td>0x80073D0E</td>
<td>L'operazione di distribuzione non è riuscita perché il volume specificato è danneggiato.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>L'operazione di distribuzione non è riuscita perché l'applicazione specificata deve essere registrata per prima.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>L'operazione di distribuzione non è riuscita perché il pacchetto è destinato all'architettura del processore errata.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>È stato raggiunto il numero massimo di pacchetti sideloaded per sviluppatori consentiti in questo dispositivo. Disinstallare un pacchetto sideloaded e riprovare.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>Per installare questo pacchetto facoltativo è necessario un pacchetto dell'app principale. Installare prima il pacchetto principale e riprovare.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>Questo tipo di pacchetto dell'app non è supportato in questo file system.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>L'operazione di spostamento del pacchetto viene bloccata fino al termine dello streaming dell'applicazione.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>Un pacchetto dell'app principale o un altro pacchetto facoltativo ha lo stesso ID applicazione di questo pacchetto facoltativo. Modificare l'ID applicazione per il pacchetto facoltativo per evitare conflitti.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>Questa sessione di staging è stata mantenuta per consentire l'assegnazione della priorità a un'altra operazione di staging.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>Impossibile aggiornare un set correlato perché il set aggiornato non è valido. Tutti i pacchetti nel set correlato devono essere aggiornati contemporaneamente.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>Un pacchetto facoltativo con un punto di ingresso FullTrust richiede che il pacchetto principale abbia la <strong>funzionalità runFullTrust.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>Si è verificato un errore perché un utente è stato disconnesso.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>Un provisioning facoltativo del pacchetto richiede anche il provisioning del pacchetto principale delle dipendenze.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>I pacchetti non hanno superato <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">il controllo della reputazione SmartScreen.</a><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td>Timeout <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">dell'operazione di controllo</a> della reputazione SmartScreen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>L'opzione di distribuzione corrente non è supportata.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>L'attivazione è bloccata a causa delle impostazioni di aggiornamento di .appinstaller per questa app.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>Le unità remote non sono supportate. Usare <strong> \\ server\share</strong> per registrare un pacchetto remoto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>Impossibile elaborare e scrivere i dati del pacchetto scaricato su disco.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>L'operazione di distribuzione è stata bloccata a causa di criteri per famiglia di pacchetti che limitano le distribuzioni in un volume non di sistema. In base ai criteri, questa app deve essere installata nell'unità di sistema, ma non è impostata come predefinita. In Archiviazione impostazioni, impostare l'unità di sistema come percorso predefinito per salvare il nuovo contenuto, quindi ripetere l'installazione.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>L'operazione di distribuzione è stata bloccata a causa di criteri a livello di computer che limitano le distribuzioni in un volume non di sistema. In base ai criteri, questa app deve essere installata nell'unità di sistema, ma non è impostata come predefinita. In Archiviazione impostazioni, impostare l'unità di sistema come percorso predefinito per salvare il nuovo contenuto, quindi ripetere l'installazione.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>L'operazione di distribuzione è stata bloccata perché la distribuzione di profili speciali non è consentita (i profili speciali sono profili utente in cui le modifiche vengono rimosse dopo la connessione dell'utente). Provare ad accedere a un account che non sia un profilo speciale. È possibile provare a disconnettersi e accedere nuovamente all'account corrente oppure provare ad accedere a un account diverso.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>Directory</strong><br/></td>
<td>0x80073D24</td>
<td>L'operazione di distribuzione non è riuscita a causa di un conflitto nella directory del pacchetto <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">modificabile di un pacchetto.</a> Per installare questo pacchetto, rimuovere il pacchetto esistente con la directory del pacchetto modificabile in conflitto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>L'installazione del pacchetto non è riuscita perché è stata specificata una risorsa singleton e un altro utente con tale pacchetto installato è connesso. Assicurarsi che tutti gli utenti attivi con il pacchetto installato siano disconnessi e ripetere l'installazione.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>L'installazione del pacchetto non è riuscita perché è installata una versione diversa del servizio. Provare a installare una versione più recente del pacchetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>L'installazione del pacchetto non è riuscita perché una versione del servizio esiste all'esterno di un pacchetto con estensione msix/.appx. Contattare il fornitore del software.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>L'installazione del pacchetto non è riuscita perché sono necessari privilegi di amministratore. Per installare questo pacchetto, contattare un amministratore.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>La distribuzione del pacchetto non è riuscita perché l'operazione sarebbe stata reindirizzata all'account predefinito, quando il chiamante ha detto di non eseguire questa operazione.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>La distribuzione del pacchetto non è riuscita perché il pacchetto richiede una funzionalità per l'host in modo nativo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>La distribuzione del pacchetto non è riuscita perché il relativo contenuto non è valido per un pacchetto non firmato.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi senza segno.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi firmato.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>La distribuzione del pacchetto non è riuscita perché il relativo server di pubblicazione non si trova nello spazio dei nomi firmato.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>Una dipendenza di runtime dell'host che risolve un pacchetto con contenuto con attendibilità totale richiede che il pacchetto principale abbia la <strong>funzionalità runFullTrust.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>L'API di creazione pacchetti ha rilevato un errore interno.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>Il pacchetto non è valido perché il relativo contenuto è interleaved.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>Il pacchetto non è valido perché contiene relazioni OPC.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>Il pacchetto non è valido perché manca un manifesto o una mappa a blocchi oppure è presente un file di integrità del codice, ma manca un file di firma.<br/> Assicurarsi che nel pacchetto non mancano uno o più di questi file necessari:<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
Se il pacchetto contiene \AppxMetadata\CodeIntegrity.cat, deve contenere anche \AppxSignature.p7x.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>Il file di AppxManifest.xml pacchetto non è valido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>Il file di AppxBlockMap.xml pacchetto non è valido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>Non è possibile leggere il contenuto del pacchetto perché è danneggiato.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>Il valore hash calcolato del blocco non corrisponde al valore has archiviato nella mappa a blocchi.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>L'intervallo di byte richiesto è superiore a 4 GB quando viene convertito in un intervallo di byte di blocchi.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>Nell'oggetto non è presente alcuna firma.<br/> Questo errore può verificarsi se il pacchetto non è firmato o se la firma non è valida. Il pacchetto deve essere firmato per essere distribuito.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Una catena di certificati è stata elaborata, ma terminata in un certificato radice che non è considerato attendibile dal provider di attendibilità.<br/> Vedere <a href="/previous-versions/br230260(v=vs.110)">Firma di un pacchetto.</a><br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>Non è stato possibile creare una catena di certificati per un'autorità di certificazione radice attendibile.<br/> Vedere <a href="/previous-versions/br230260(v=vs.110)">Firma di un pacchetto.</a><br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>La <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>usata per firmare il pacchetto non contiene i dati necessari<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>La <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilizzata per crittografare o decrittografare il pacchetto contiene dati non validi.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>La mappa del gruppo di contenuto del pacchetto con estensione msix/.appx non è valida.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>APPINSTALLER</strong><br/></td>
<td>0x8008020C</td>
<td>Il <a href="/windows/msix/app-installer/app-installer-root">file con estensione appinstaller</a> per il pacchetto non è valido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>La versione del pacchetto di base nel pacchetto delta non corrisponde alla versione nel pacchetto di base da aggiornare.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>Nel pacchetto delta manca un file dal pacchetto aggiornato.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>Il pacchetto delta non è valido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>Il pacchetto accodato delta non è consentito per l'operazione corrente.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>Il file di layout di creazione pacchetti non è valido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGESIGNCONFIG</strong><br/></td>
<td>0x80080212</td>
<td>Il file packageSignConfig non è valido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>Il file resources.pri non è consentito quando non sono presenti elementi di risorse nel manifesto del pacchetto.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>Lo stato di compressione del file nella baseline e nel pacchetto aggiornato non corrisponde.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>Le estensioni non appx non sono consentite per i pacchetti di payload che hanno come destinazione piattaforme precedenti.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>Il file encryptionExclusionFileList non è valido.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Le applicazioni non vengono avviate e i relativi nomi sono in grigio

In un computer Windows 10, non è possibile avviare alcune applicazioni e i nomi delle applicazioni vengono visualizzati in grigio.

![Alcuni nomi di applicazione vengono visualizzati in grigio nel menu Start](./images/app-names-dimmed.png)

Quando si tenta di aprire un'applicazione selezionando il nome in grigio, è possibile che venga visualizzato uno dei messaggi di errore seguenti:

> Si è verificato un problema con \<*application name*> . Contattare l'amministratore di sistema per il ripristino o la reinstallazione  
> Errore: Impossibile aprire l'app

Inoltre, le voci di evento seguenti vengono registrate nel registro "Microsoft-Windows-TWinUI/Operational" in Applicazioni e **servizi\Microsoft\Windows\Apps:**

> Nome log: Microsoft-Windows-TWinUI/Operational  
> Origine: Microsoft-Windows-Immersive-Shell  
> Data: <*data*>  
> ID evento: 5960  
> Categoria attività: (5960)  
> Livello: Errore  
> Parole chiave:  
> Descrizione:  
> Attivazione dell'app Microsoft.BingNews_8wekyb3d8bbwe! AppexNews per il Windows. Il contratto di avvio è stato bloccato con errore 0x80073CFC perché il relativo pacchetto è nello stato Modificato.  

### <a name="cause"></a>Causa

Questo problema si verifica perché la voce del Registro di sistema per il valore di stato del pacchetto corrispondente dell'applicazione è stata modificata.

### <a name="resolution"></a>Risoluzione

> [!WARNING]
> Se si modifica il registro di sistema in modo non corretto utilizzando l'Editor del Registro di sistema o un altro metodo, si possono causare gravi problemi. che per essere risolti potrebbero richiedere la reinstallazione del sistema operativo. Microsoft non garantisce la possibilità di risolvere questi problemi. La modifica del Registro di sistema è a rischio e pericolo dell'utente.

Per risolvere il problema:

1. Avviare l'editor del Registro di sistema e quindi **individuareHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** sottochiave .
2. Per eseguire il backup dei dati della sottochiave, fare clic con il pulsante destro del mouse su **PackageList**, **scegliere Esporta** e quindi salvare i dati come file del Registro di sistema.
3. Per ognuna delle applicazioni elencate nelle voci di log id evento 5960, seguire questa procedura:  
   1. Individuare la **voce PackageStatus.**
   2. Impostare il valore di **PackageStatus** su zero (**0**).
   > [!NOTE]  
   > Se non sono presenti voci per l'applicazione in **PackageList**, il problema ha un'altra causa. Nel caso dell'evento di esempio in questo articolo, la sottochiave completa è **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Riavviare il computer.

## <a name="get-additional-help"></a>Ottenere altre informazioni

Per altre informazioni sulla risoluzione di un problema che si verifica durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto di app Windows (con estensione msix/.appx) come sviluppatore, fare riferimento a queste risorse di supporto aggiuntive per gli sviluppatori.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offre risposte pertinenti e rapide ai problemi tecnici di una community di esperti e tecnici Microsoft.
- Per assistenza della community per le domande sullo sviluppo, sono disponibili [i forum](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)e [StackOverflow](https://stackoverflow.com/questions).
- Il [Windows di supporto per sviluppatori](https://developer.microsoft.com/windows/support) illustra altre opzioni di supporto.

## <a name="related-topics"></a>Argomenti correlati

- [Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)
- [Come risolvere gli errori di firma del pacchetto dell'app](how-to-troubleshoot-app-package-signature-errors.md)
