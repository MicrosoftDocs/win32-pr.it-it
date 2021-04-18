---
title: Impostazioni di Segnalazione errori Windows
description: Impostazioni per personalizzare l'esperienza di segnalazione dei problemi. Tutte queste impostazioni possono essere impostate utilizzando Criteri di gruppo. Alcuni possono anche essere modificati in centro operativo per Windows 7 e Windows 8. Per Windows 10, utilizzare la funzione di ricerca in impostazioni per individuare Visualizza impostazioni di sistema avanzate.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Segnalazione errori Windows segnalazione errori Windows, impostazioni
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/13/2021
ms.locfileid: "106322047"
---
# <a name="wer-settings"></a>Impostazioni di Segnalazione errori Windows

Segnalazione errori Windows (WER) fornisce molte impostazioni per personalizzare l'esperienza di segnalazione dei problemi. Tutte queste impostazioni possono essere impostate utilizzando Criteri di gruppo. Alcuni possono anche essere modificati in **centro operativo** per Windows 7 e Windows 8. Per Windows 10, utilizzare la funzione di ricerca in impostazioni per individuare **Visualizza impostazioni di sistema avanzate**. Le impostazioni WER si trovano in una delle sottochiavi del registro di sistema seguenti:

-   **HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **segnalazione errori Windows**
-   **HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **segnalazione errori Windows**

## <a name="windows-error-reporting-subkey"></a>Sottochiave Segnalazione errori Windows

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>

0-Disabilita la limitazione dei dati ignorata. Se il bypass è disabilitato o non è configurato come impostazione di criteri, WER limita i dati per impostazione predefinita. WER non carica più di un file CAB per un report che contiene dati sugli stessi tipi di evento.

</dd> <dd>

1-abilitare la limitazione dei dati bypass. WER non limita i dati. WER carica i file CAB aggiuntivi che possono contenere dati sugli stessi tipi di evento di un report caricato in precedenza.

</dd> </dl>

Indica se abilitare il bypass della limitazione dei dati del client WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1-solo parametri (impostazione predefinita in Windows 7)</dd> <dd>2-tutti i dati (impostazione predefinita in Windows Vista)</dd> </dl>

Indica se archiviare solo i parametri o tutti i dati

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consenso \\ DefaultConsent**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1-Richiedi sempre (impostazione predefinita)</dd> <dd>2-solo parametri</dd> <dd>3-parametri e dati sicuri</dd> <dd>4-tutti i dati</dd> </dl>

Scelta di consenso predefinita

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consenso \\ DefaultOverrideBehavior**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0: il consenso verticale sostituirà il consenso predefinito (impostazione predefinita)</dd> <dd>1-il consenso predefinito sostituirà il consenso specifico dell'applicazione</dd> </dl>

Indica se il consenso predefinito sostituisce il consenso verticale

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consenso \\ \[ verticale\]**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1-Richiedi sempre (impostazione predefinita)</dd> <dd>2-solo parametri</dd> <dd>3-parametri e dati sicuri</dd> <dd>4-tutti i dati</dd> </dl>

Scelta di consenso per il plug-in WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**REG \_ SZ**

Percorso della directory

Directory di destinazione nel server

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**REG \_ DWORD**

Numero di porta

Numero di porta da utilizzare con il server aziendale

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**REG \_ SZ**

Nome host del server.

Nome del server aziendale

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Indica se utilizzare l'autenticazione integrata di Windows

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Indica se utilizzare SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ exename \] (sostituire " \[ exename \] " con il nome effettivo di un file con estensione exe, ad esempio "notepad.exe")**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:

<dl> <dd>0: i processi con un nome di immagine eseguibile di **\[ exename \]** non richiedono all'utente di scegliere **debug** o **continua** (impostazione predefinita)</dd> <dd>1-i processi con un nome di immagine eseguibile di **\[ exename \]** richiedono all'utente di scegliere **debug** o **continua**</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " è il nome del valore letterale)**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:

<dl> <dd>0: tutti i processi ad eccezione di quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ \] exename** non richiedono all'utente di scegliere **debug** o **continua** (impostazione predefinita)</dd> <dd>1-tutti i processi ad eccezione di quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ \] exename** richiedono all'utente di scegliere **debug** o **continua**</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Attivato</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare l'archivio

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0: abilitato (impostazione predefinita)</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Attivato</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare l'accodamento di report

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-interfaccia utente (impostazione predefinita)</dd> <dd>1: nessuna interfaccia utente</dd> </dl>

Abilitare o disabilitare l'interfaccia utente di WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-invia (impostazione predefinita)</dd> <dd>1-non inviare</dd> </dl>

Indica se impedire l'invio di dati di secondo livello

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Nome dell'applicazione ExcludedApplications\]**
</dt> <dd>

**REG \_ SZ**

Usare [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Elenco di applicazioni escluse

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Indica se inviare tutti i report alla coda dell'utente

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpFolder o LocalDumps DumpFolder**
</dt> <dd>

**REG \_ Espandi \_ SZ**

Percorso della directory. Il valore predefinito è% LOCALAPPDATA% \\ CrashDumps. Se il valore predefinito non viene utilizzato, l'applicazione deve verificare che la cartella disponga di un ACL sufficiente.

**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

Percorso in cui archiviare i file di dump.

Si noti che le impostazioni per processo sostituiranno le impostazioni globali esistenti per ulteriori informazioni, vedere [raccolta di dump di User-Mode](collecting-user-mode-dumps.md).

Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpCount o LocalDumps DumpCount**
</dt> <dd>

**REG \_ DWORD**

Numero massimo. Il valore predefinito è 10. Quando viene superato il valore massimo, il file di dump meno recente nella cartella verrà sostituito con il nuovo file di dump.

**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Numero massimo di file di dump nella cartella.

Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpType o LocalDumps DumpType**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0-dump personalizzato</dd> <dd>1-minidump (impostazione predefinita)</dd> <dd>2-dump completo</dd> </dl>

**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Tipo di dump.

Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ CustomDumpFlags o LocalDumps CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

Uno o più valori dell'enumerazione [**del \_ tipo di MINIDUMP**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . Il valore predefinito è {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Opzioni di dump personalizzate da utilizzare. Questo valore viene utilizzato solo quando **DumpType** è impostato su 0.

Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0: abilitato (impostazione predefinita)</dd> <dd>1: disabilitato</dd> </dl>

Abilitare o disabilitare la registrazione

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

Intervallo di valori possibili: 1 – 5000. Il valore predefinito è 1000.

Dimensioni massime dell'archivio in file

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

Intervallo di valori possibili: 1 – 500. Il valore predefinito è 50.

Dimensioni massime della coda

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

Numero di giorni

Intervallo tra i promemoria dell'utente per verificare la presenza di soluzioni, in giorni

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nome pwszOutOfProcessCallbackDll con percorso\]**
</dt> <dd>

**REG \_ DWORD**

Il contenuto del valore viene ignorato.

Il nome del valore viene usato per recuperare il valore pwszOutOfProcessCallbackDll.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Il valore del registro di sistema non è supportato.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Impostazioni report del kernel Live di WER

Le impostazioni dei report del kernel Live di WER, descritte di seguito, si trovano entrambi nella sottochiave del registro di sistema seguente:

-   **HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>Sottochiave FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Soglia (in ore) della frequenza con cui un singolo componente può creare un dump Live completo. Questo valore deve essere maggiore o uguale a **SystemThrottleThreshold**. Se si imposta su zero (0), tutte le limitazioni basate sul tempo vengono disabilitate. Il valore predefinito è 168 (7 giorni).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

Numero massimo di dump Live completi che possono trovarsi sul disco in un determinato momento. Il valore predefinito è 1. Se questo valore viene impostato su zero (0), la funzionalità di dump in tempo reale verrà disabilitata.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

Oggetto [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che indica l'ora dell'ultimo report live completo, per il sistema o un reportType specifico. Viene usato per calcolare se una soglia dei criteri è stata soddisfatta.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Soglia (in ore) della frequenza con cui un componente del sistema può creare un dump Live completo. Il valore predefinito è 120 (5 giorni).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Sottochiave LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ SZ**


Percorso di archiviazione reindirizzato dei report del kernel attivo. Il percorso predefinito è%systemroot%\LiveKernelReports. Questo valore deve essere un percorso valido. Il percorso deve essere in formato NT. Ad esempio, \? ? \c: \LiveDumpsFolder.  Per ulteriori informazioni sui formati di percorso, vedere  [formati di percorso dei file nei sistemi Windows](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a WER](wer-reference.md)
</dt> </dl>

 

 
