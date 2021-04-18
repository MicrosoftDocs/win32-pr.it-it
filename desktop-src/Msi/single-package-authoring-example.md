---
description: Il PUASample.msi di esempio è un esempio di un pacchetto a doppio scopo Windows Installer 5,0 che è in grado di essere installato nel contesto di installazione per utente o per computer in Windows Server 2008 R2 e Windows 7.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Esempio di creazione di pacchetti singoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314775"
---
# <a name="single-package-authoring-example"></a>Esempio di creazione di pacchetti singoli

Il PUASample.msi di esempio è un esempio di un pacchetto a doppio scopo Windows Installer 5,0 che è in grado di essere installato nel [contesto di installazione](installation-context.md) per utente o per computer in windows Server 2008 R2 e Windows 7. Questo pacchetto di esempio segue le linee guida di sviluppo descritte in [creazione di pacchetti singoli](single-package-authoring.md).

## <a name="obtaining-a-copy-of-the-sample"></a>Acquisizione di una copia dell'esempio

Una copia di questo esempio e un Windows Installer editor di tabelle di database, Orca.exe, si trovano nei [componenti Windows SDK per gli sviluppatori Windows Installer](platform-sdk-components-for-windows-installer-developers.md). L'editor di esempio e di tabella è fornito con Windows Software Development Kit per Windows Server 2008 R2 e Windows 7 come file di installazione Windows Installer PUASample1.msi e Orca.msi.

## <a name="system-requirements"></a>Requisiti di sistema

Per l'editor di database, [Orca.exe](orca-exe.md), sono necessari windows Server 2008 R2 e versioni precedenti e Windows 7 e versioni precedenti. Il pacchetto a doppio scopo, PUASample1.msi, può essere installato nel [contesto di installazione](installation-context.md) per computer o per utente in windows Server 2008 R2 e Windows 7. PUASample1.msi può essere installato solo nel contesto per computer in Windows Server 2008 e versioni precedenti e in Windows Vista e versioni precedenti. È possibile installare l'editor di database per esaminare il contenuto di PUASample1.msi senza installare l'esempio. Per installare i pacchetti di esempio o dell'editor, verificare che il criterio [DisableMSI](disablemsi.md) non sia impostato su un valore che blocca le installazioni dell'applicazione.

## <a name="identifying-a-dual-purpose-package"></a>Identificazione di un pacchetto di Dual-Purpose

I pacchetti a doppio scopo devono inizializzare il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) su 1. Identifica il pacchetto in modo che sia in grado di essere installato nel contesto per computer o per utente in Windows Server 2008 R2 e Windows 7. Impostare la proprietà **MSIINSTALLPERUSER** nel pacchetto solo se è stata scritta seguendo le linee guida per lo sviluppo descritte in [creazione di pacchetti singoli](single-package-authoring.md) e se si desidera fornire agli utenti l'opzione per installare il pacchetto nel contesto per utente o per computer. Un pacchetto a doppio scopo deve anche inizializzare il valore della proprietà [**ALLUSERS**](allusers.md) su 2. In questo modo viene specificato per utente come contesto di installazione predefinito per l'applicazione. Se il valore della proprietà **ALLUSERS** è un valore diverso da 2, Windows Installer ignora la proprietà **MSIINSTALLPERUSER** .

Per esaminare il contenuto dei PUASample1.msi, utilizzare un editor di database Windows Installer, ad esempio [Orca.exe](orca-exe.md). La tabella delle [Proprietà](property-table.md) nel pacchetto di esempio contiene le due voci seguenti.

[Proprietà](property-table.md) di Tabella (parziale)

| Proprietà          | Valore |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Finestra di dialogo personalizzata per il contesto di installazione

L' [interfaccia utente](user-interface.md) del pacchetto di esempio include un esempio di finestra di dialogo personalizzata, VerifyReadyDialog, che consente agli utenti di selezionare il contesto di installazione per utente o per computer al momento dell'installazione. La tabella della [finestra di dialogo](dialog-table.md) contiene un record che descrive la finestra di dialogo VerifyReadyDialog. Il valore immesso nel campo attributi è 39 perché in questa finestra di dialogo vengono utilizzati i [bit di stile](dialog-style-bits.md)msidbDialogAttributesVisible (1), msidbDialogAttributesModal (2), msidbDialogAttributesMinimize (4) e msidbDialogAttributesTrackDiskSpace (32). Nella barra del titolo della finestra di dialogo viene visualizzato un titolo fornito dal valore della proprietà [**ProductName**](productname.md) .

[Finestra di dialogo](dialog-table.md) Tabella (parziale) 

| Finestra di dialogo            | HCentering | VCenter | Larghezza | Altezza | Attributi | Titolo           | \_Primo controllo | Controllo \_ predefinito | \_Annulla controllo |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | Prossima             | Annulla          |



 

La tabella di [controllo](control-table.md) contiene le voci per i [controlli](controls.md) visualizzati dalla finestra di dialogo VerifyReadyDialog. Nella finestra di dialogo vengono visualizzati i controlli [pulsante](pushbutton-control.md) e un controllo [testo](text-control.md) . Tutti i controlli utilizzano gli [attributi di controllo](control-attributes.md)msidbControlAttributesEnabled (2) e msidbControlAttributesVisible (1). Il controllo InstallPerMachine usa anche l'attributo del controllo [ElevationShield](elevationshield-attribute.md) , msidbControlAttributesElevationShield (8388608). Questo attributo di controllo aggiunge l'icona di elevazione del [*controllo dell'account utente*](u-gly.md) (UAC) al controllo InstallPerMachine e informa l'utente che sono necessarie le credenziali UAC per installare l'applicazione nel contesto per computer. Il valore nel campo di testo della tabella dei controlli è lo stile testo e il testo visualizzati dal controllo. Per ulteriori informazioni sull'aggiunta di testo a un controllo utilizzando stili predefiniti, vedere la descrizione del campo di testo nell'argomento della tabella di controllo.

[Controllo](control-table.md) di Tabella (parziale)

| Finestra di dialogo\_          | Control           | Tipo       | Attributo | Testo                                                   | Controllo \_ successivo     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | Annulla            | Pulsante | 3         | { \\ Tahoma10} &Annulla                                    | Prossima              |
| VerifyReadyDialog | Indietro          | Pulsante | 3         | { \\ Tahoma10} <<&precedente                          | Annulla            |
| VerifyReadyDialog | Prossima              | Pulsante | 3         | { \\ Tahoma10} &successiva >>                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Testo       | 3         | Si è pronti per completare l'installazione sospesa? |                   |
| VerifyReadyDialog | InstallPerUser    | Pulsante | 3         | { \\ Tahoma10} installazione solo per &me                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | Pulsante | 8388611   | \\Installazione di {Tahoma10} per &Everyone                      | Indietro          |
| VerifyReadyDialog | Annulla            | Pulsante | 3         | { \\ Tahoma10} &Annulla                                    | Prossima              |



 

La tabella [ControlEvent](controlevent-table.md) specifica il [ControlEvents](control-events.md)o le azioni che il programma di installazione esegue quando l'utente interagisce con un controllo. Quando un utente attiva il pulsante InstallPerUser, l'interfaccia utente visualizza una finestra di dialogo OutOfDisk se la proprietà [**OutOfDiskSpace**](outofdiskspace.md) è 1, imposta il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) su 1, imposta il valore della proprietà [**ALLUSERS**](allusers.md) su 2, imposta la proprietà [**MSIFASTINSTALL**](msifastinstall.md) su 1 e restituisce. Poiché la proprietà **MSIFASTINSTALL** è impostata, non viene generato alcun punto di ripristino di sistema per l'installazione. Quando un utente attiva il pulsante InstallPerMachine, l'interfaccia utente visualizza una finestra di dialogo OutOfDisk se la proprietà **OutOfDiskSpace** è 1, imposta il valore della proprietà **ALLUSERS** su 1 e restituisce.

[ControlEvent](controlevent-table.md) Tabella (parziale) 

| Finestra di dialogo\_          | controllo\_         | Evento                 | Argomento  | Condizione                 | JSON |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| VerifyReadyDialog | InstallPerUser    | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerUser    | EndDialog             | Return    | OutOfDiskSpace <> 1 | 5     |
| VerifyReadyDialog | InstallPerUser    | \[MSIINSTALLPERUSER\] | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| VerifyReadyDialog | InstallPerMachine | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerMachine | EndDialog             | Return    | OutOfDiskSpace <> 1 | 3     |
| VerifyReadyDialog | InstallPerMachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[MSIFASTINSTALL\]    | 1         | 1                         | 4     |



 

Il controllo InstallPerUser deve essere rimosso dall'interfaccia utente di qualsiasi installazione usando una versione Windows Installer precedente alla Windows Installer Windows Installer 5,0. La tabella [ControlCondition](controlcondition-table.md) nel pacchetto di esempio contiene quattro voci che disabilitano e nascondono il controllo InstallPerUser se la versione corrente è minore di Windows Installer 5,0. La tabella usa il valore della proprietà [**VersionMsi**](versionmsi.md) e la [sintassi dell'istruzione condizionale](conditional-statement-syntax.md) per definire questa condizione. L'azione specificata nel campo azione viene eseguita solo se l'istruzione nel campo condizione è true.

[ControlCondition](controlcondition-table.md) Tabella (parziale)

| Finestra di dialogo\_          | controllo\_      | Azione  | Condizione               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | Abilitare  | VersionMsi >= "5,00" |
| VerifyReadyDialog | InstallPerUser | Disabilita | VersionMsi < "5,00"  |
| VerifyReadyDialog | InstallPerUser | Mostra    | VersionMsi >= "5,00" |
| VerifyReadyDialog | InstallPerUser | Nascondi    | VersionMsi < "5,00"  |



 

## <a name="specifying-directory-structure"></a>Specifica della struttura di directory

Utilizzare l'editor di database per esaminare la tabella di [directory](directory-table.md) di PUASample1.msi. Il record della tabella di directory con una stringa vuota nel \_ campo padre della directory rappresenta la directory radice dell'albero delle directory di origine e di destinazione. Se la proprietà [**targetdir**](targetdir.md) è indefinita, il programma di installazione ne imposta il valore al momento dell'installazione sul valore della proprietà [**ROOTDRIVE**](rootdrive.md) . Se la proprietà [**SourceDir**](sourcedir.md) è indefinita, il programma di installazione ne imposta il valore sul percorso della directory contenente il pacchetto di Windows Installer (file con estensione msi). I nomi di directory vengono specificati utilizzando il \| formato Short Long.

[Directory](directory-table.md) di Tabella (parziale)

| Directory          | \_Padre directory  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | Fornitore           | Sample1 \| MSDN-PUASample1 |
| Fornitore           | ProgramFilesFolder | \|Microsoft MSFT          |



 

Nell'origine questa tabella di [directory](directory-table.md) viene risolta nei percorsi di directory seguenti.

<dl> \[SourceDir \] \\ MSFT \\ Sample1  
\[SourceDir\]  
</dl>

Nella destinazione la tabella [directory](directory-table.md) viene risolta nei percorsi della tabella seguente. Il programma di installazione imposta i valori delle proprietà [**ProgramFilesFolder**](programfilesfolder.md) e [**ProgramMenuFolder**](programmenufolder.md) su percorsi che dipendono dal [contesto di installazione](installation-context.md) e se il sistema è costituito dalle versioni a 32 bit o 64 bit di Windows Server 2008 R2 e Windows 7. I percorsi delle cartelle di destinazione variano a seconda che l'utente selezioni un'installazione per utente o per computer.

| Contesto di installazione | Sistema                                                                              | Percorsi di esempio                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versione a 32 bit<br/>           | % Programmi% \\ MSFT \\ Sample1<br/> % ALLUSERSPROFILE% \\ \\ \\ programmi menu Start di Microsoft Windows \\<br/>                  |
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versione a 64 bit<br/>           | % ProgramFiles (x86)% \\ MSFT \\ Sample1<br/> % ALLUSERSPROFILE% \\ \\ \\ programmi menu Start di Microsoft Windows \\<br/>             |
| Per-User             | Windows Server 2008 R2 e Windows 7<br/> versione a 32 bit o a 64 bit<br/> | % USERPROFILE% \\ AppData \\ \\ programmi locali \\ MSFT \\ Sample1<br/> % APPDATA% \\ \\ \\ programmi menu Start di Microsoft Windows \\<br/> |



 

Le applicazioni per utente devono essere archiviate in sottocartelle nella cartella programmi specificata dal valore della proprietà [**ProgramFilesFolder**](programfilesfolder.md) . In genere, il percorso dell'applicazione assume il formato seguente.

% LocalAppData% \\ programmi \\ *ISV nome* \\ *appname*.

I dati di configurazione per utente devono essere archiviati nella cartella programmi specificata dal valore della proprietà [**ProgramMenuFolder**](programmenufolder.md) . In genere, questa cartella si trova nel percorso seguente.

% APPDATA% \\ \\ \\ programmi menu Start di Microsoft Windows \\

Se si installano componenti del [pacchetto Windows Installer a 32 bit](32-bit-windows-installer-packages.md) , utilizzare la proprietà [**ProgramFilesFolder**](programfilesfolder.md) e [**CommonFilesFolder**](commonfilesfolder.md) nella tabella [directory](directory-table.md) . Se si installano componenti del [pacchetto Windows Installer a 64 bit](64-bit-windows-installer-packages.md) , usare le proprietà [**ProgramFiles64Folder**](programfiles64folder.md) e [**CommonFiles64Folder**](commonfiles64folder.md) . Se l'applicazione contiene versioni a 32 bit e a 64 bit dello stesso componente, con lo stesso nome, assicurarsi che queste versioni siano salvate in directory diverse o assegnare loro nomi diversi.

La tabella [directory](directory-table.md) seguente fornisce un esempio di un layout di directory compatibile con un pacchetto che include componenti a 32 bit e 64 bit e include alcuni componenti condivisi tra le applicazioni.

| Directory            | \_Padre directory    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | .: Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | Fornitore             | Sample1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATION       | ShVendor             | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| MSDN-PUASample1          |
| Fornitore             | ProgramFilesFolder   | \|Microsoft MSFT                   |
| Vendorx64            | ProgramFiles64Folder | \|Microsoft MSFT                   |
| ShVendor             | CommonFilesFolder    | \|Microsoft MSFT                   |
| ShVendorx64          | CommonFiles64Folder  | \|Microsoft MSFT                   |
| Shrx86               | SHAREDLOCATION       | x32 \| -componenti a 32 bit            |
| Shrx64               | SHAREDLOCATIONX64    | \|componenti x64 a 64 bit            |
| Binx86               | INSTALLLOCATION      | x32 \| -componenti a 32 bit            |
| Binx64               | INSTALLLOCATIONX64   | \|componenti x64 a 64 bit            |
| App32                | Binx86               | MyApp \| componenti non condivisi a 32 bit |
| App64                | Binx64               | MyApp \| componenti non condivisi a 64 bit |
| Share32              | Shrx86               | componenti condivisi condivisi \| a 32 bit  |
| Share64              | Shrx64               | componenti condivisi condivisi \| a 64 bit  |



 

Nell'origine questa tabella di [directory](directory-table.md) viene risolta nei percorsi di directory seguenti.

<dl> \[SourceDir \] Prog32 \\ MSFT \\ Sample1 \\ x32 \\ MyApp  
\[SourceDir \] Share32 \\ file comuni \\ MSFT \\ Sample1 \\ x32 \\ condiviso  
\[SourceDir \] Prog64 \\ MSFT \\ Sample1 \\ x64 \\ MyApp  
\[SourceDir \] Share64- \\ file comuni \\ MSFT \\ Sample1 \\ x64 \\ condivisi  
\[\]Sample1 SourceDir  
</dl>

Nella destinazione, questa tabella di [directory](directory-table.md) viene risolta nei percorsi di directory seguenti. I percorsi di destinazione dipendono dal [contesto di installazione](installation-context.md) e dal sistema.

| Contesto di installazione | Sistema                                                                              | Percorsi di esempio                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versione a 32 bit<br/>           | % Programmi% \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles% \\ file comuni \\ MSFT \\ Sample1 \\ x32 \\ condiviso<br/> % ProgramFiles (x86)% \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles (x86)% \\ file comuni \\ MSFT \\ Sample1 \\ x64 \\ condiviso<br/> % ProgramData% \\ Microsoft \\ Windows \\ programmi menu \\ Start \\ Sample1<br/>               |
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versione a 64 bit<br/>           | % ProgramFiles (x86)% \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles (x86)% \\ file comuni \\ MSFT \\ Sample1s \\ x32 \\ condiviso<br/> % ProgramFiles% \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles% \\ file comuni \\ MSFT \\ Sample1 \\ x64 \\ condiviso<br/> % ProgramData% \\ Microsoft \\ Windows \\ programmi menu \\ Start \\ Sample1<br/>               |
| Per-User             | Windows Server 2008 R2 e Windows 7<br/> versione a 32 bit o a 64 bit<br/> | % LOCALAPPDATA% \\ programmi \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % LOCALAPPDATA% \\ programmi \\ comuni \\ MSFT \\ Sample1 \\ x32 \\ condivisi<br/> % LOCALAPPDATA% \\ programmi \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % LOCALAPPDATA% \\ programmi \\ comuni \\ MSFT \\ Sample1 \\ x64 \\ condivisi<br/> % APPDATA% \\ Microsoft \\ Windows \\ programmi menu \\ Start \\ Sample1<br/> |



 

## <a name="application-registration"></a>Registrazione dell'applicazione

Il PUASample.msi aggiunge una sottochiave alla chiave del registro di sistema dei percorsi dell'applicazione ed esegue le registrazioni che consentono di salvare le informazioni dell'applicazione nel registro di sistema in base a questa chiave. Per ulteriori informazioni sui percorsi delle app e la registrazione dell'applicazione, vedere la sezione relativa alla registrazione dell'applicazione, [PerceivedTypes e SystemFileAssociations](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) nella sezione [Extensibility](https://msdn.microsoft.com/library/bb762762.aspx) della shell della [Guida per gli sviluppatori della shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Al momento dell'installazione, l'utente decide di installare l'applicazione nel contesto di installazione per utente o per computer. Quando viene creato il pacchetto a doppio scopo, lo sviluppatore del pacchetto non è in grado di stabilire se le registrazioni devono essere eseguite nel \_ computer locale HKEY \_ o nelle \_ chiavi utente correnti di HKEY \_ .

Lo sviluppatore del pacchetto definisce l'identificatore del file eseguibile dell'applicazione nel campo file della tabella [file](file-table.md) .

[File](file-table.md) Tabella (parziale) 

| File      | Componente\_      | FileName                     | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppFile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

I valori da salvare nel registro di sistema possono essere specificati nel campo del valore della tabella del [Registro di sistema](registry-table.md) come stringa [formattata](formatted.md) . Usare l'identificatore di file definito nel campo file della tabella [file](file-table.md) e la \[ \#  \] convenzione FileKey del tipo formattato per specificare il valore predefinito per la chiave del registro di sistema percorsi app. L'azione di [installazione](install-action.md) di primo livello esegue le azioni nella tabella [InstallExecuteSequence](installexecutesequence-table.md) . Una volta completate le azioni [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [InstallFinalize](installfinalize-action.md) in questa tabella, il Windows Installer sostituisce la sottostringa formattata \[ \# MyAppFile \] nella tabella del registro di sistema con il percorso completo del file dell'applicazione.

L'esempio definisce una proprietà personalizzata, RegRoot, per contenere il percorso della chiave radice e usa un'azione personalizzata per reimpostare il valore della proprietà se l'utente sceglie un'installazione per computer. Usare la proprietà personalizzata, RegRoot, in tutti i valori stringa formattati che fanno riferimento al percorso radice. Nella tabella delle [Proprietà](property-table.md) il pacchetto di PUASample.msi definisce la proprietà personalizzata e imposta il valore di RegRoot su HKCU. Viene così inizializzato il valore della proprietà per il contesto di installazione per utente, il contesto predefinito consigliato per i pacchetti a doppio scopo.

[Proprietà](property-table.md) di Tabella (parziale)

| Proprietà | Valore |
|----------|-------|
| RegRoot  | HKCU  |



 

Nella tabella [CustomAction](customaction-table.md) il pacchetto definisce un'azione personalizzata denominata set \_ RegRoot \_ HKLM. Il valore nel campo tipo identifica questo [tipo di azione personalizzata 51](custom-action-type-51.md) azione personalizzata standard. Il significato dei campi di origine e di destinazione nella tabella CustomAction dipende dal tipo di azione personalizzata. Per altre informazioni sui tipi standard di azioni personalizzate, vedere [tipi di azione personalizzati](summary-list-of-all-custom-action-types.md). Il campo di origine per l' \_ azione personalizzata set RegRoot \_ HKLM specifica che il valore della proprietà RegRoot. Se il programma di installazione esegue l' \_ azione personalizzata set RegRoot \_ HKLM, il valore della proprietà RegRoot viene reimpostato su HKLM.

[CustomAction](customaction-table.md) Tabella (parziale)

| Azione             | Tipo | Source (Sorgente)      | Destinazione |
|--------------------|------|-------------|--------|
| Imposta \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

L'azione di [installazione](install-action.md) di primo livello esegue le azioni nella tabella [InstallExecuteSequence](installexecutesequence-table.md) , nella sequenza specificata nel campo Sequence della tabella. Il valore creato nel campo sequenza per l' \_ azione personalizzata set RegRoot \_ HKLM (1501) specifica che l'azione personalizzata deve essere eseguita dopo l'azione [InstallInitialize](installinitialize-action.md) (1500) e prima dell'azione [ProcessComponents](processcomponents-action.md) (1600). Questa sequenza garantisce che il record per l' \_ azione personalizzata set RegRoot \_ HKLM venga valutato al momento dell'installazione. Per ulteriori informazioni sulla sequenza di azioni consigliata nella tabella InstallExecuteSequence, vedere l'argomento [InstallExecuteSequence suggerito](suggested-installexecutesequence.md) . La [sintassi dell'istruzione condizionale](conditional-statement-syntax.md) creata nel campo condizione specifica che l' \_ azione set RegRoot \_ HKLM viene eseguita solo se il valore della proprietà [**ALLUSERS**](allusers.md) restituisce 1 al momento dell'installazione. Un valore della proprietà **ALLUSERS** pari a 1 specifica un'installazione per computer.

[InstallExecuteSequence](installexecutesequence-table.md) Tabella (parziale)

| Azione             | Condizione  | Sequenza |
|--------------------|------------|----------|
| Imposta \_ RegRoot \_ HKLM | ALLUSERS = 1 | 1501     |



 

I record seguenti nella tabella [del registro di sistema](registry-table.md) eseguono le registrazioni se il componente ProductComponent è installato. Il valore-1 nel campo radice è necessario per eseguire la registrazione in HKEY \_ Local \_ computer per un'installazione per utente e in HKEY \_ Current \_ User per un'installazione per utente. Il record con una stringa vuota nel campo Registro di sistema aggiunge una sottochiave per l'applicazione sotto la chiave del registro di sistema percorsi app e imposta il valore "(impostazione predefinita)" sul percorso completo del file eseguibile dell'applicazione. La registrazione MyAppPathAlias esegue il mapping del file eseguibile a un alias dell'applicazione e consente l'avvio dell'applicazione se l'utente digita l'alias "puapct" al prompt della riga di comando. La registrazione MyAppPathRegistration esegue il mapping del nome del file eseguibile al percorso completo del file.



| Registro              | Radice | Codice                                                                     | Nome | Valore                                                                            | Componente        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Software \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[RegRoot \] \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ percorsi app \\PUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ percorsi app \\PUAPCT.exe     |      | \[\#MyAppFile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ percorsi app \\PUASample1.exe |      | \[\#MyAppFile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>Annulla registrazione AutoPlay

Il PUASample.msi esegue le registrazioni che consentono all'utente dell'applicazione di impedire l'avvio di [AutoPlay hardware](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) per i dispositivi selezionati. Per informazioni sulla registrazione di un gestore per annullare AutoPlay in risposta a un evento, vedere l'argomento [preparazione dell'hardware e del software da usare con AutoPlay](/previous-versions//cc144208(v=vs.85)) nella sezione [Extensibility della shell](https://msdn.microsoft.com/library/bb762762.aspx) della Guida per [gli sviluppatori della shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Il record seguente registra il gestore specificato nel campo nome quando viene installato il componente ProductComponent. Il valore-1 nel campo radice è necessario per specificare la Windows Installer che la registrazione deve essere reindirizzata a una posizione che dipende dal contesto di installazione.

[Registro di sistema](registry-table.md) tavolo 

| Registro                     | Radice | Codice                                                                                             | Nome                                 | Valore | Componente        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ cancelautoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>Anteprima registrazione gestore

Il PUASample.msi esegue le registrazioni necessarie per installare un gestore di [anteprime](../shell/preview-handlers.md) che Abilita un'anteprima di sola lettura dei file con estensione PUA senza avviare l'applicazione. Per informazioni sulla registrazione dei gestori di anteprime, vedere l'argomento [registrazione dei gestori di anteprime](../shell/how-to-register-a-preview-handler.md) nella sezione [Extensibility](https://msdn.microsoft.com/library/bb762762.aspx) della shell della [Guida per gli sviluppatori della shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). I record seguenti nella tabella [del registro di sistema](registry-table.md) registrano il gestore quando viene installato il componente ProductComponent. Il valore-1 nel campo radice è necessario per specificare la Windows Installer che la registrazione deve essere reindirizzata a una posizione che dipende dal contesto di installazione.

[Registro di sistema](registry-table.md) tavolo

| Registro                       | Radice | Codice                                                                              | Nome                                   | Valore                                        | Componente        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | \\Classi software \\ . PUA                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Gestore di anteprima TEST di Microsoft Windows PUA   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | \\Classi software \\ puafile \\ ShellEx \\ {8895b1c6-b41f-4c1c-a562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Gestore di anteprime di esempio Per-User Applicaton 1 | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32,-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | Icona                                   | notepad.exe, 2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ThreadingModel                         | Apartment                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 |                                        | \#%% SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | \\Classi software \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 
