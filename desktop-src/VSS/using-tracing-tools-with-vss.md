---
description: Per raccogliere informazioni di traccia per l'infrastruttura del servizio Copia Shadow del volume, è possibile utilizzare lo strumento VssTrace, lo strumento Logman o lo strumento tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Uso degli strumenti di traccia con VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226114"
---
# <a name="using-tracing-tools-with-vss"></a>Uso degli strumenti di traccia con VSS

Per raccogliere informazioni di traccia per l'infrastruttura del servizio Copia Shadow del volume, è possibile utilizzare lo strumento VssTrace, lo strumento Logman o lo strumento tracelog. VssTrace è disponibile nel Software Development Kit (SDK) di Microsoft Windows e può essere utilizzato per tracciare le applicazioni VSS in Windows 7 e versioni successive del sistema operativo Windows. Logman è un controller di traccia per gli eventi di traccia e i contatori delle prestazioni. può essere usato anche per tracciare le applicazioni VSS in Windows 7 e versioni successive del sistema operativo Windows. Tracelog è incluso in Windows Driver Kit (WDK).

Per usare gli strumenti di traccia con [Ripristino automatico del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), vedere [uso degli strumenti di traccia con le applicazioni ASR](using-tracing-tools-with-vss-asr-applications.md).

> [!Note]  
> VssTrace, Logman e tracelog richiedono tutti privilegi di amministratore.

 

Per informazioni su ogni strumento, vedere le sezioni seguenti:

-   [Uso di VssTrace](#using-vsstrace)
    -   [Opzioni Command-Line VssTrace](#vsstrace-command-line-options)
-   [Uso di logman](#using-logman)
-   [Uso di tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Uso di VssTrace

Per eseguire lo strumento VssTrace dalla riga di comando, usare la sintassi seguente:

 *Opzioni della riga di comando di* vsstrace

Per visualizzare la guida concisa della riga di comando per lo strumento VssTrace, usare la sintassi seguente:

**vsstrace-Guida**

Per visualizzare informazioni dettagliate della guida della riga di comando per lo strumento VssTrace, usare la sintassi seguente:

**vsstrace-Help All**

### <a name="vsstrace-command-line-options"></a>Opzioni Command-Line VssTrace

Lo strumento VssTrace usa le seguenti opzioni della riga di comando:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>*flag* **-f**
</dt> <dd>

Abilitare i moduli i cui flag sono specificati dalla maschera di maschera dei *flag* . Ogni flag corrisponde a un modulo VSS. Se *Flags* è zero, non sono abilitati moduli. Si noti che la maggior parte dei moduli è abilitata per impostazione predefinita. Questa opzione può essere combinata con l' **+** opzione del _modulo_ . Ad esempio, **vsstrace-f 0 + Writer + Coord** Disabilita la traccia di tutti i moduli abilitati per impostazione predefinita e Abilita la traccia dei writer VSS e del servizio VSS. In alternativa, **vsstrace + f 0xFFFF-Coord** Abilita la traccia di tutti i moduli tranne il servizio VSS.

> [!Note]  
> Se si usa l'opzione **-f** con l'opzione del **+** _modulo_ , il **-f** deve essere visualizzato prima dell'opzione del **+** _modulo_ .

 

La tabella seguente elenca il nome e il flag del modulo per ogni modulo disponibile.

| Modulo | Contrassegno       | Abilitato per impostazione predefinita | Elementi tracciati                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Sì                | Gestione delle eccezioni C++.                                                                                                                       |
| COORD  | 0x00000002 | Sì                | Il servizio VSS, denominato anche coordinatore VSS.                                                                                    |
| SWPRV  | 0x00000004 | Sì                | Servizio del provider di copia shadow di sistema VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Sì                | Il richiedente VSS e l'elaborazione dei metadati di backup.                                                                                             |
| WRITER | 0x00000010 | Sì                | VSS writer operazioni e implementazioni di writer ospitate VSS, ad esempio il writer del registro di sistema di Windows.                                             |
| VSSAPI | 0x00000020 | Sì                | Varie funzioni dell'API VSS esportate da VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Sì                | Infrastruttura e operazioni del provider hardware VSS.                                                                                          |
| ADMIN  | 0x00000080 | Sì                | Utilità della riga di comando VSS, ad esempio VSSADMIN.EXE e DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Sì                | Interfaccia utente di configurazione copie shadow per cartelle condivise. L'interfaccia utente è disponibile solo nei sistemi operativi Windows Server.         |
| TEST   | 0x00000200 | Sì                | Non applicabile. (Questo modulo di traccia è riservato).                                                                                            |
| IOCTL  | 0x00000400 | Sì                | Dettagli delle operazioni FSCTL e IOCTL avviate dal servizio VSS chiamando la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) . |
| GENERAZIONE    | 0x00000800 | Sì                | Funzioni di utilità VSS generali, ad esempio allocatori, classi stringa e operazioni del registro di sistema e del volume.                                        |
| WRXML  | 0x00001000 | No                 | Elaborazione XML per i metadati del writer. Questo modulo ha un livello di disturbo molto elevato.                                                               |
| VSSXML | 0x00002000 | No                 | Classi base di elaborazione XML. Questo modulo ha un livello di disturbo molto elevato.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modulo_
</dt> <dd>

Abilitare il modulo specificato dal *modulo*. È possibile abilitare più di un modulo alla volta. Per elencare i moduli disponibili, digitare **vsstrace-Help Modules** al prompt della riga di comando.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modulo_
</dt> <dd>

Disabilitare il modulo specificato dal *modulo*. Per elencare i moduli disponibili, digitare **vsstrace-Help Modules** al prompt della riga di comando.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *ProcessID*
</dt> <dd>

Consente di abilitare il processo specificato da *ProcessID*. Per abilitare tutti i processi, usare " \* " come valore di *ProcessID*. È possibile specificare più di un'opzione **PID** alla volta. L'ordine delle opzioni determina quali processi sono abilitati o disabilitati. Ad esempio, per abilitare solo il processo il cui identificatore di processo è 0xe8c, usare **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*
</dt> <dd>

Disabilitare il processo specificato da *ProcessID*. Per disabilitare tutti i processi, usare " \* " come valore di *ProcessID*. È possibile specificare più di un'opzione **PID** alla volta. L'ordine delle opzioni determina quali processi sono abilitati o disabilitati. Ad esempio, per disabilitare tutti i processi ad eccezione del processo il cui identificatore di processo è 0xe8c, usare **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ TID** *ThreadID*
</dt> <dd>

Abilitare il thread specificato da *ThreadID*. Per abilitare tutti i thread, usare " \* " come valore di *ThreadID*. È possibile specificare più di un'opzione **TID** alla volta. L'ordine delle opzioni determina quali thread sono abilitati o disabilitati. Ad esempio, per abilitare solo il thread il cui identificatore del processo è 0x31a, usare **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadID*
</dt> <dd>

Disabilitare il thread specificato da *ThreadID*. Per disabilitare tutti i thread, usare " \* " come valore di *ThreadID*. È possibile specificare più di un'opzione **TID** alla volta. L'ordine delle opzioni determina quali thread sono abilitati o disabilitati. Ad esempio, per disabilitare tutti i thread eccetto il thread il cui identificatore di processo è 0x31a, usare **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *livello*
</dt> <dd>

Utilizzare il livello di traccia specificato in base al *livello*. Maggiore è il livello, più dettagliato è l'output di traccia. Ogni livello include tutti i livelli inferiori. Il livello predefinito è 170. Sono disponibili i livelli seguenti.



| Level | Informazioni incluse nell'output di traccia |
|-------|------------------------------------------|
| 7000   | nessuno                                     |
| 020   | Errori irreversibili                             |
| 030   | Eccezioni non gestite                     |
| 040   | Errors                                   |
| 050   | Asserzioni                               |
| 060   | Avvisi                                 |
| 080   | Gestione delle eccezioni                       |
| 100   | Attività registro eventi                       |
| 120   | Informazioni generali                      |
| 140   | flusso del codice                                |
| 160   | Immettere ed uscire dalla funzione                  |
| 170   | Valori restituiti dalla funzione                   |
| 180   | Parametri della funzione (conciso)              |
| 190   | Parametri della funzione (verbose)            |
| 200   | Livello informazioni dettagliate 1              |
| 210   | Livello informazioni dettagliate 2              |
| 220   | Livello informazioni dettagliate 3              |
| 230   | Livello di codice veloce 1                        |
| 240   | Livello di codice veloce 2                        |
| 250   | Livello di codice veloce 3                        |
| 255   | Tutti                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ rientro**
</dt> <dd>

Rientrare nell'output di traccia formattato per ogni funzione e limite di funzione.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-rientro**
</dt> <dd>

Non rientrare nell'output di traccia formattato.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*
</dt> <dd>

Converte il file di output logman specificato da *EtlFile* in un formato di testo leggibile.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *outputfile*
</dt> <dd>

Salvare le informazioni di traccia nel file di output specificato da *outputfile*. Per prestazioni ottimali, il file di output deve trovarsi in un volume che non fa parte della copia shadow.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*
</dt> <dd>

Consente di visualizzare la guida della riga di comando come specificato da *HelpOption*. I valori di *HelpOption* validi sono **moduli**, **livelli** e **tutti**. Se si specificano i **moduli** , i moduli verranno elencati. Se si specificano i **livelli** , verranno elencati i livelli disponibili. Se si specifica **All** , viene visualizzata una guida dettagliata. Se non viene usata alcuna opzione, viene visualizzata la guida concisa.

</dd> </dl>

## <a name="using-logman"></a>Uso di logman

Nella procedura seguente viene descritto come utilizzare logman con l'applicazione VSS.

**Per usare logman con l'applicazione VSS**

1.  Usare il comando seguente per avviare la traccia:

    **logman start VSS-o** *x: \\ * * * VSS. etl-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xFFF 170**

    > [!Note]  
    > Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.

     

2.  Usare il comando seguente per arrestare la traccia:

    **logman stop VSS-ETS**

Il file di log di traccia è *x: \\* VSS. etl.

Per ulteriori informazioni sullo strumento Logman, vedere [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Uso di tracelog

Nella procedura seguente viene descritto come utilizzare tracelog.

**Per usare tracelog**

1.  Creare un file di testo denominato VSS. CTL contenente solo il testo seguente:

    **VSS 9138500e-3648-4edb-aa4c-859e9f7b7c38**

2.  Usare il comando seguente per avviare la traccia:

    **tracelog-Start VSS-f** *x: \\ * * * VSS. etl-GUID VSS. CTL-flag 0xAA a livello 0xFF**

    > [!Note]  
    > Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.

     

3.  Usare il comando seguente per arrestare la traccia:

    **tracelog-arresta VSS**

Il file di log di traccia è *x: \\* VSS. etl.

Per ulteriori informazioni sullo strumento tracelog, vedere [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
