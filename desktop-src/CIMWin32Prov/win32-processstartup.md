---
description: La \_ classe WMI astratta Win32 ProcessStartup rappresenta la configurazione di avvio di un processo basato su Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Classe Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334363"
---
# <a name="win32_processstartup-class"></a>Win32 \_ ProcessStartup (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) astratta **Win32 \_ ProcessStartup** rappresenta la configurazione di avvio di un processo basato su Windows. La classe viene definita come definizione del tipo di metodo, ovvero viene utilizzata solo per passare informazioni al metodo [**create**](create-method-in-class-win32-process.md) della classe del [**\_ processo Win32**](win32-process.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ProcessStartup** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ProcessStartup** dispone di queste proprietà.

<dl> <dt>

**CreateFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")
</dt> </dl>

Valori aggiuntivi che controllano la classe di priorità e la creazione del processo. È possibile specificare i valori di creazione seguenti in qualsiasi combinazione, ad eccezione di quanto indicato.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Esegui debug \_ Processo** (1)


</dt> <dd>

Se questo flag è impostato, il processo chiamante viene considerato come un debugger e viene eseguito il debug del nuovo processo. Il sistema notifica al debugger tutti gli eventi di debug che si verificano nel processo di cui è in corso il debug.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Esegui debug \_ Solo \_ questo \_ processo** (2)


</dt> <dd>

Se questo flag non è impostato ed è in corso il debug del processo chiamante, il nuovo processo diventa un altro processo di cui è in corso il debug. Se il processo chiamante non è un processo di cui è in corso il debug, non si verificheranno azioni correlate al debug.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Crea \_ Sospeso** (4)


</dt> <dd>

Il thread principale del nuovo processo viene creato in uno stato sospeso e non viene eseguito fino a quando non viene chiamato il metodo [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**\_ Scollegato Processo** (8)


</dt> <dd>

Per i processi della console, il nuovo processo non ha accesso alla console del processo padre. Non è possibile usare questo flag se è impostato il flag **Crea \_ nuova \_ console** .

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Crea \_ Nuova \_ console** (16)


</dt> <dd>

Questo nuovo processo ha una nuova console, anziché ereditare la console padre. Questo flag non può essere utilizzato con il flag di **\_ processo scollegato** .

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Crea \_ Nuovo \_ \_ gruppo di processi** (512)


</dt> <dd>

Questo nuovo processo è il processo radice di un nuovo gruppo di processi. Il gruppo di processi include tutti i processi discendenti di questo processo radice. L'identificatore di processo del nuovo gruppo di processi è uguale all'identificatore di processo restituito nella proprietà **ProcessID** della classe del [**\_ processo Win32**](win32-process.md) . I gruppi di processi vengono usati dal metodo [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) per consentire l'invio di un segnale CTRL + C o Ctrl + Break a un gruppo di processi della console.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Crea \_ \_Ambiente Unicode** (1024)


</dt> <dd>

Le impostazioni dell'ambiente elencate nella proprietà **EnvironmentVariables** utilizzano caratteri Unicode. Se questo flag non è impostato, il blocco dell'ambiente usa caratteri ANSI.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Crea \_ \_ \_ Modalità di errore predefinita** (67108864)


</dt> <dd>

Ai processi appena creati viene assegnata la modalità di errore predefinita del sistema del processo chiamante anziché ereditare la modalità di errore del processo padre. Questo flag è utile per le applicazioni shell multithreading eseguite con errori hardware disabilitati.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Crea \_ FUGA \_ dal \_ processo** (16777216)


</dt> <dd>

Utilizzato per evitare che il processo creato sia limitato dall'oggetto processo.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")
</dt> </dl>

Elenco delle impostazioni per la configurazione di un computer. Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili. Il sistema mantiene un blocco di impostazioni di ambiente per ogni utente e uno per il computer. Il blocco dell'ambiente di sistema rappresenta le variabili di ambiente per tutti gli utenti di un computer specifico. Il blocco dell'ambiente di un utente rappresenta le variabili di ambiente gestite dal sistema per un utente specifico e include il set di variabili di ambiente di sistema. Per impostazione predefinita, ogni processo riceve una copia del blocco di ambiente per il processo padre. Si tratta in genere del blocco dell'ambiente per l'utente che ha eseguito l'accesso. Un processo può specificare blocchi di ambiente diversi per i processi figlio.

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error Functions \| SetErrorMode")
</dt> </dl>

In alcuni processori non x86, i riferimenti di memoria non allineati provocano un'eccezione di errore di allineamento. Il flag **nessun \_ errore di allineamento \_ \_ eccetto** consente di controllare se un sistema operativo corregge automaticamente tali errori di allineamento o li rende visibili a un'applicazione. In una piattaforma di milioni di istruzioni al secondo (MIPS), un'applicazione deve chiamare in modo esplicito [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) con il flag **nessun errore di \_ allineamento ad \_ \_ eccezione** che il sistema operativo corregge automaticamente gli errori di allineamento.

Modalità di elaborazione di diversi tipi di errori gravi da un sistema operativo. È possibile specificare che gli errori di elaborazione del sistema operativo o un'applicazione possono ricevere ed elaborare errori.

Per impostazione predefinita, il sistema operativo rende visibili gli errori di allineamento a un'applicazione. Poiché la piattaforma x86 non rende visibili gli errori di allineamento a un'applicazione, il flag nessun errore di **\_ allineamento \_ \_ ad eccezione** di non consente al sistema operativo di generare un errore di allineamento, anche se il flag non è impostato. Lo stato predefinito per [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) consiste nell'impostare tutti i flag su 0 (zero).

<dt>



 (1)


</dt> <dd>

Predefinito

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Non riuscita \_ \_Errori critici** (2)


</dt> <dd>

Se questo flag è impostato, il sistema operativo non visualizzerà la finestra di messaggio del gestore errori critico quando si verifica un errore di questo tipo. Al contrario, il sistema operativo invia l'errore al processo chiamante.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No \_ Errore di allineamento \_ \_ eccetto** (4)


</dt> <dd>

Se questo flag è impostato, il sistema operativo corregge automaticamente gli errori di allineamento della memoria e li rende invisibile all'applicazione. Questa operazione viene eseguita per i processi chiamante e discendente. Questo flag è valido solo per RISC (Reduced Instruction Set Computing) e non ha alcun effetto sui processori x86.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No \_ \_ \_ \_ Casella errore GP** (8)


</dt> <dd>

Se questo flag è impostato, nel sistema operativo non viene visualizzata la finestra di messaggio di errore di protezione generale (GP) quando si verifica un errore del GP. Questo flag deve essere impostato solo tramite il debug di applicazioni che gestiscono gli errori di GP.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No \_ \_Casella di \_ errore \_ Apri file** (16)


</dt> <dd>

Se questo flag è impostato, il sistema operativo non visualizza una finestra di messaggio quando non riesce a trovare un file. Al contrario, l'errore viene restituito al processo chiamante. Questo flag è attualmente ignorato.

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")
</dt> </dl>

Testo e colori di sfondo se viene creata una nuova finestra della console in un'applicazione console. Questi valori vengono ignorati nelle applicazioni GUI (Graphical User Interface). Per specificare i colori di primo piano e di sfondo, aggiungere insieme i valori. Ad esempio, per avere un tipo rosso (4) su uno sfondo blu (16), impostare FillAttribute su 20.

<dt>

1
</dt> <dd>

Blu in primo piano \_

</dd> <dt>

2
</dt> <dd>

Verde primo piano \_

</dd> <dt>

4
</dt> <dd>

Rosso in primo piano \_

</dd> <dt>

8
</dt> <dd>

Intensità in primo piano \_

</dd> <dt>

16
</dt> <dd>

\_Blu sfondo

</dd> <dt>

32
</dt> <dd>

\_Verde sfondo

</dd> <dt>

64
</dt> <dd>

\_Rosso sfondo

</dd> <dt>

128
</dt> <dd>

Intensità di sfondo \_

</dd> </dl>

</dd> <dt>

**PriorityClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture di thread \| [**JOBOBJECT \_ Basic \_ limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")
</dt> </dl>

Classe di priorità del nuovo processo. Utilizzare questa proprietà per determinare le priorità di pianificazione dei thread nel processo. Se la proprietà è null, il valore predefinito della classe priority è Normal, a meno che la classe priority del processo di creazione non sia inattiva o inferiore al \_ normale. In questi casi, il processo figlio riceve la classe di priorità predefinita del processo chiamante.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (32)


</dt> <dd>

Indica un processo normale senza particolari esigenze di pianificazione.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattività** (64)


</dt> <dd>

Indica un processo con thread eseguiti solo quando il sistema è inattivo e viene interrotto dai thread di qualsiasi processo in esecuzione in una classe con priorità più elevata. Un esempio è un screen saver. La classe di priorità inattiva viene ereditata dai processi figlio.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)


</dt> <dd>

Indica un processo che esegue attività critiche al tempo che devono essere eseguite immediatamente per l'esecuzione corretta. I thread di un processo di classe ad alta priorità hanno la precedenza sui thread dei processi di classe di priorità normale o di priorità di inattività. Un esempio è Windows Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente, indipendentemente dal carico sul sistema operativo. Prestare particolare attenzione quando si utilizza la classe con priorità alta, perché un'applicazione con associazione alla CPU con priorità alta può utilizzare quasi tutti i cicli disponibili. Solo una priorità in tempo reale precede i thread impostati su questo livello.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo reale** (256)


</dt> <dd>

Indica un processo con la massima priorità possibile. I thread di un processo della classe di priorità in tempo reale hanno la precedenza sui thread di tutti gli altri processi, inclusi i thread con priorità alta e i processi del sistema operativo che eseguono attività importanti. Ad esempio, un processo in tempo reale eseguito per più di un intervallo molto breve può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>Di **seguito \_ Normale** (16384)


</dt> <dd>

Indica un processo con priorità maggiore di inattività ma inferiore al normale.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Sopra \_ Normale** (32768)


</dt> <dd>

Indica un processo con priorità superiore al normale ma inferiore al valore massimo.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Visualizzazione della finestra all'utente. Può essere uno qualsiasi dei valori che possono essere specificati nel parametro *nCmdShow* per la funzione [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**Title**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")
</dt> </dl>

Testo visualizzato nella barra del titolo quando viene creata una nuova finestra della console. usato per i processi della console. Se **null**, il nome del file eseguibile viene usato come titolo della finestra. Questa proprietà deve essere **null** per i processi GUI o console che non creano una nuova finestra della console.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")
</dt> </dl>

Nome del desktop o nome del desktop e della stazione della finestra per il processo. Una barra rovesciata nella stringa indica che la stringa include i nomi delle stazioni desktop e di Windows. Se **WinstationDesktop** è **null**, il nuovo processo eredita il desktop e la stazione della finestra del processo padre. Se **WinstationDesktop** è una stringa vuota, il processo non eredita il desktop e la stazione della finestra del processo padre. Il sistema determina se è necessario creare un nuovo desktop e una nuova stazione di finestra. Una finestra è un oggetto protetto che contiene gli appunti, un set di atomi globali e un gruppo di oggetti desktop. La stazione interattiva della finestra assegnata alla sessione di accesso dell'utente interattivo contiene anche la tastiera, il mouse e il dispositivo di visualizzazione. Un desktop è un oggetto protetto contenuto all'interno di una finestra. Un desktop ha una superficie di visualizzazione logica e contiene finestre, menu e hook. Una stazione della finestra può avere più desktop. Solo i desktop della stazione finestra interattiva possono essere visibili e ricevere l'input dell'utente.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")
</dt> </dl>

Offset X dell'angolo superiore sinistro di una finestra se viene creata una nuova finestra, in pixel. Gli offset si trovano nell'angolo superiore sinistro dello schermo. Per i processi GUI, la posizione specificata viene usata la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *X* di **CreateWindow** è **CW \_ usedefault (**.

> \[! Nota X\]  
> e **Y** non possono essere specificati in modo indipendente.

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")
</dt> </dl>

Larghezza del buffer dello schermo nelle colonne di tipo carattere. Questa proprietà viene usata per i processi che creano una finestra della console e viene ignorata nei processi GUI.

> [!Note]  
> Non è possibile specificare **XCountChars** e **YCountChars** in modo indipendente.

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")
</dt> </dl>

Larghezza in pixel di una finestra se viene creata una nuova finestra. Per i processi GUI, viene usato solo la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro NWidth di **CreateWindow** è **CW \_ usedefault (**.

> [!Note]  
> Non è possibile specificare **XSize** e **ysize** in modo indipendente.

 

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| Dwy")
</dt> </dl>

Offset in pixel dell'angolo superiore sinistro di una finestra se viene creata una nuova finestra. Gli offset sono dall'angolo superiore sinistro dello schermo. Per i processi GUI, la posizione specificata viene usata la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *y* di **CreateWindow** è **CW \_ usedefault (**.

> \[! Nota X\]  
> e **Y** non possono essere specificati in modo indipendente.

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")
</dt> </dl>

Altezza buffer dello schermo in righe di caratteri. Questa proprietà viene usata per i processi che creano una finestra della console, ma viene ignorata nei processi GUI.

> [!Note]  
> Non è possibile specificare **XCountChars** e **YCountChars** in modo indipendente.

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")
</dt> </dl>

Altezza in pixel di una finestra se viene creata una nuova finestra. Per i processi GUI, viene usato solo la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *nWidth* di **CreateWindow** è **CW \_ usedefault (**.

> [!Note]  
> Non è possibile specificare **XSize** e **ysize** in modo indipendente.

 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe è derivata da [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).

Panoramica

Il metodo di [**creazione**](create-method-in-class-win32-process.md) [**\_ processo Win32**](win32-process.md) consente di configurare le opzioni di avvio per qualsiasi nuovo processo in esecuzione in un computer. Ad esempio, è possibile configurare un processo in modo che venga avviato in una finestra "nascosta", che impedisce a un utente di visualizzare e possibilmente interromperlo. Se il processo viene eseguito in una finestra di comando, è possibile configurare le dimensioni, il titolo e i colori di primo piano e di sfondo della finestra.

Le opzioni di avvio vengono configurate utilizzando la classe **Win32 \_ ProcessStartup** . **Win32 \_ ProcessStartup** è una classe del tipo di metodo. la classe del tipo di metodo esiste esclusivamente per passare informazioni a un metodo. In questo caso, tutte le proprietà di un'istanza di **Win32 \_ ProcessStartup** vengono passate a un'istanza del [**\_ processo Win32**](win32-process.md).

**Uso di Win32 \_ ProcessStartup**

1.  Creare un'istanza di **Win32 \_ ProcessStartup**.
2.  Configurare le proprietà della nuova istanza di.
3.  Includere l'istanza di come parte del metodo di creazione del [**\_ processo Win32**](win32-process.md) .

Se, ad esempio, è stata creata un'istanza **Win32 \_ ProcessStartup** denominata objConfig, il nome dell'oggetto verrà passato nel metodo create come indicato di seguito:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Esempio

Per configurare varie opzioni di avvio per un processo, è possibile usare la classe **Win32 \_ ProcessStartup** . Queste opzioni comprendono, ma non sono limitate, ad esempio la creazione di un processo in una finestra nascosta e la creazione di un processo con priorità più alta. Il codice VBScript seguente consente di creare un processo in una finestra nascosta.


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



Il codice VBScript seguente consente di creare un processo con priorità più alta.


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



Nell'esempio di codice VBScript seguente viene creato un processo blocco note nel computer locale. **Win32 \_ ProcessStartup** viene usato per configurare le impostazioni del processo.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MethodParameterClass Win32**](win32-methodparameterclass.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[Attività WMI: processi](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
