---
title: Impostazioni di Segnalazione errori Windows
description: Impostazioni personalizzare l'esperienza di segnalazione dei problemi. Tutte queste impostazioni possono essere impostate usando Criteri di gruppo. Alcune possono anche essere modificate nel Centro notifiche per Windows 7 e Windows 8. Per Windows 10, usare la funzione di ricerca in Impostazioni per individuare Visualizza impostazioni di sistema avanzate.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows segnalazione errori Segnalazione errori Windows , impostazioni
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442230"
---
# <a name="wer-settings"></a>Impostazioni di Segnalazione errori Windows

Segnalazione errori Windows (WER) offre molte impostazioni per personalizzare l'esperienza di segnalazione dei problemi. Tutte queste impostazioni possono essere impostate usando Criteri di gruppo. Alcune possono anche essere modificate nel **Centro operativo** per Windows 7 e Windows 8. Per Windows 10, usare la funzione di ricerca in Impostazioni per individuare **Visualizza impostazioni di sistema avanzate**. Le impostazioni di WeR si trovano in una delle sottochiavi del Registro di sistema seguenti:

-   **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Segnalazione errori Windows**
-   **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Segnalazione errori Windows**

## <a name="windows-error-reporting-subkey"></a>Segnalazione errori Windows sottochiave

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>

0 - Disabilitare la limitazione del bypass dei dati. Se il bypass è disabilitato o non configurato come impostazione dei criteri, wer limitazione dei dati per impostazione predefinita. WeR non carica più di un file CAB per un report che contiene dati sugli stessi tipi di evento.

</dd> <dd>

1 - Abilitare la limitazione del bypass dei dati. WeR non limitazione dei dati. WeR carica file CAB aggiuntivi che possono contenere dati sugli stessi tipi di evento di un report caricato in precedenza.

</dd> </dl>

Se abilitare il bypass della limitazione dei dati del client WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1 - Solo parametri (impostazione predefinita Windows 7)</dd> <dd>2 - Tutti i dati (impostazione predefinita in Windows Vista)</dd> </dl>

Se archiviare solo i parametri o tutti i dati

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consenso \\ DefaultConsent**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1 - Chiedi sempre (impostazione predefinita)</dd> <dd>2 - Solo parametri</dd> <dd>3 - Parametri e dati sicuri</dd> <dd>4 - Tutti i dati</dd> </dl>

Scelta del consenso predefinita

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consenso \\ DefaultOverrideBehavior**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Il consenso verticale eseguirà l'override del consenso predefinito (impostazione predefinita)</dd> <dd>1 - Il consenso predefinito eseguirà l'override del consenso specifico dell'applicazione</dd> </dl>

Se il consenso predefinito sostituisce il consenso verticale

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent \\ \[ VerticalName\]**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>1 - Chiedi sempre (impostazione predefinita)</dd> <dd>2 - Solo parametri</dd> <dd>3 - Parametri e dati sicuri</dd> <dd>4 - Tutti i dati</dd> </dl>

Scelta del consenso per il plug-in WER

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

Numero di porta da usare con il server aziendale

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

Valori possibili:<dl> <dd>0 - No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Se usare l'Windows integrata

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Se usare SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ ExeName (sostituire " ExeName " con un nome effettivo di un file .exe, ad esempio \[ \] , \[ \] "notepad.exe")**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:

<dl> <dd>0 - I processi con un nome di immagine eseguibile **\[ ExeName \]** non richiedono all'utente di scegliere **Debug** o **Continua** (impostazione predefinita)</dd> <dd>1 - I processi con un nome di immagine eseguibile **\[ ExeName \]** richiedono all'utente di scegliere **Debug** o **Continua**</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" " è il nome del \* valore letterale)**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:

<dl> <dd>0 - Tutti i processi tranne quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ ExeName \]** non richiedono all'utente di scegliere **Debug** o **Continua** (impostazione predefinita)</dd> <dd>1 - Tutti i processi tranne quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ ExeName \]** richiedono all'utente di scegliere **Debug** o **Continua**</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Attivato</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare l'archivio

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabili**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Abilitato (impostazione predefinita)</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare WeR

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Attivato</dd> <dd>1 - Disattivato</dd> </dl>

Abilitare o disabilitare l'accodamento dei report

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Interfaccia utente (impostazione predefinita)</dd> <dd>1 - Nessuna interfaccia utente</dd> </dl>

Abilitare o disabilitare l'interfaccia utente di WeR

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Invia (impostazione predefinita)</dd> <dd>1 - Non inviare</dd> </dl>

Se impedire l'invio di dati di secondo livello

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nome applicazione ExcludedApplications \\ \[\]**
</dt> <dd>

**REG \_ SZ**

Usare [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Elenco delle applicazioni escluse

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - No (impostazione predefinita)</dd> <dd>1 - Sì</dd> </dl>

Se inviare tutti i report alla coda dell'utente

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder o** **Nome applicazione LocalDumps \\ \[ \] \\ DumpFolder**
</dt> <dd>

**REG \_ EXPAND \_ SZ**

Percorso della directory. Il valore predefinito è %LOCALAPPDATA% \\ CrashDumps. Se non si usa l'impostazione predefinita, l'applicazione deve assicurarsi che la cartella disponga di un ACL sufficiente.

**Windows Vista:** I valori del Registro di sistema **nella chiave LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

Percorso in cui archiviare i file di dump.

Si noti che le impostazioni per processo eseguiranno l'override di tutte le impostazioni globali esistenti. Per altre informazioni, vedere Raccolta User-Mode [dump.](collecting-user-mode-dumps.md)

Questa impostazione non è supportata nell'hive del Registro di sistema **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount o** **LocalDumps \\ \[ Application Name \] \\ DumpCount**
</dt> <dd>

**REG \_ DWORD**

Numero massimo. Il valore predefinito è 10. Quando viene superato il valore massimo, il file dump meno recente nella cartella verrà sostituito con il nuovo file dump.

**Windows Vista:** I valori del Registro di sistema **nella chiave LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Numero massimo di file di dump nella cartella.

Questa impostazione non è supportata nell'hive del Registro di sistema **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType o** **LocalDumps \\ \[ Application Name \] \\ DumpType**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0 - Dump personalizzato</dd> <dd>1 - Minidump (impostazione predefinita)</dd> <dd>2 - Dump completo</dd> </dl>

**Windows Vista:** I valori del Registro di sistema **nella chiave LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Tipo di dump.

Questa impostazione non è supportata nell'hive del Registro di sistema **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ Nome applicazione CustomDumpFlags** o **LocalDumps \\ \[ \] \\ CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

Uno o più valori [**dell'enumerazione MINIDUMP \_ TYPE.**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) Il valore predefinito è {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** I valori del Registro di sistema **nella chiave LocalDumps** non sono supportati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.

Opzioni di dump personalizzate da utilizzare. Questo valore viene usato solo quando **DumpType** è impostato su 0.

Questa impostazione non è supportata nell'hive del Registro di sistema **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

Valori possibili:<dl> <dd>0- Abilitato (impostazione predefinita)</dd> <dd>1- Disabilitato</dd> </dl>

Abilitare o disabilitare la registrazione

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

Intervallo di valori possibili: 1-5000. Il valore predefinito è 1000.

Dimensioni massime dell'archivio, in file

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

Intervallo di valori possibili: 1-500. Il valore predefinito è 50.

Dimensioni massime della coda

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

Numero di giorni

Intervallo tra i promemoria all'utente per verificare la presenza di soluzioni, in giorni

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ pwszOutOfProcessCallbackDll name including path\]**
</dt> <dd>

**REG \_ DWORD**

Il contenuto del valore viene ignorato.

Il nome del valore viene usato per recuperare il valore pwszOutOfProcessCallbackDll.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore del Registro di sistema non è supportato.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Report del kernel live di Segnalazione errori Windows Impostazioni

Le impostazioni dei report del kernel live di WeR, descritte di seguito, si trovano entrambe nella sottochiave del Registro di sistema seguente:

-   **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM Controllo** \\ **CurrentControlSet** \\  \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>Sottochiave FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Soglia (in ore) della frequenza con cui un singolo componente può creare un dump live completo. Questo valore deve essere maggiore o uguale a **SystemThrottleThreshold**. L'impostazione di entrambi su zero (0) disabilita tutte le limitazioni basate sul tempo. Il valore predefinito è 168 (7 giorni).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

Numero massimo di dump live completi che possono essere su disco in un determinato momento. Il valore predefinito è 1. L'impostazione di questo valore su zero (0) disabilita la funzionalità di dump live.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

Valore [SystemTime che](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indica l'ora dell'ultimo report live completo, per il sistema o un ReportType specifico. Viene usato per calcolare se una soglia dei criteri è stata soddisfatta.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Soglia (in ore) della frequenza con cui un componente nel sistema può creare un dump live completo. Il valore predefinito è 120 (5 giorni).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Sottochiave LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ SZ**


Percorso di archiviazione reindirizzato dei report del kernel in tempo reale. Il percorso predefinito è %systemroot%\LiveKernelReports. Questo valore deve essere un percorso valido. Il percorso deve essere nel formato di percorso NT. Ad esempio, \? ?\C:\LiveDumpsFolder.  Per altre informazioni sui formati di percorso, vedere Formati di percorso dei [file Windows sistemi .](/dotnet/standard/io/file-path-formats)

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WER](wer-reference.md)
</dt> </dl>

 

 
