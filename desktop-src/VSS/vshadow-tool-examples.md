---
description: 'Altre informazioni su: esempi di strumenti VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Esempi di strumenti VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751570"
---
# <a name="vshadow-tool-examples"></a>Esempi di strumenti VShadow

Gli esempi seguenti illustrano come usare lo strumento VShadow per eseguire le attività più comuni:

-   [Accesso alle proprietà della copia shadow da uno script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Accesso a copie shadow non permanenti](#accessing-nonpersistent-shadow-copies)
-   [Copia di un file da una copia shadow](#copying-a-file-from-a-shadow-copy)
-   [Enumerazione di tutti i file in un dispositivo di copia shadow](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importazione di una copia shadow trasportabile](#importing-a-transportable-shadow-copy)
-   [Inclusione di writer o componenti](#including-writers-or-components)
-   [Esclusione di writer o componenti](#excluding-writers-or-components)
-   [Suddivisione di set di copie shadow tramite il metodo BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Per un elenco completo delle opzioni della riga di comando e del relativo utilizzo, vedere [vshadow Tool and Sample](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Accesso alle proprietà della copia shadow da uno script CMD

Se si usa il flag facoltativo **-script** quando si creano copie shadow, vshadow crea un file di script cmd contenente le variabili di ambiente correlate alle copie shadow appena create, come le seguenti:

-   ID del set di copie shadow, archiviato nella variabile di ambiente% VSHADOW \_ set \_ ID%
-   ID copia shadow, archiviati in variabili con formato% VSHADOW \_ ID \_ *nnn*%, dove *nnn* rappresenta l'indice del volume di origine nella riga di comando di VSHADOW
-   I nomi dei dispositivi copia shadow, archiviati in variabili nel formato% VSHADOW \_ dispositivo \_ *nnn*%, dove *nnn* è l'indice del volume di origine nella riga di comando di VSHADOW

È possibile utilizzare il file CMD generato per eseguire operazioni di gestione limitate sulle copie shadow.

> [!Note]  
> L'evento [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer viene inviato dopo l'esecuzione dello script **-Exec** . VSS chiama il metodo **IVssBackupComponents:: BackupComplete** per segnalare ai writer che il backup è stato completato e i writer possono potenzialmente troncare i log in questo momento. È quindi importante verificare che l'ombreggiatura o il backup sia stato effettivamente completato. Se il backup non è riuscito, è possibile annullare il processo di creazione restituendo un codice di uscita diverso da zero nello script o comando eseguito. (Vedere la documentazione relativa al comando Esci nella Guida di [riferimento alla riga di comando di Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))). Se il comando personalizzato restituisce con un codice di uscita diverso da zero, la creazione della copia shadow viene annullata e **IVssBackupComponents:: BackupComplete** non verrà chiamato.

 

Nell'esempio seguente viene illustrato come creare una copia shadow persistente dalla riga di comando e utilizzare lo script CMD per esporla.

1.  **vshadow-p-NW-script = SETVAR1. cmd c:**
2.  **chiamare SETVAR1. cmd**
3.  **C: \\>vshadow-El =% vshadow \_ ID \_ 1%, c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Accesso a copie shadow non permanenti

Le copie shadow non permanenti vengono eliminate automaticamente quando il programma che li crea (in questo caso, VShadow) viene chiuso. Per accedere al contenuto di queste copie shadow, VShadow consente di eseguire uno script dopo la creazione delle copie shadow ma prima della chiusura del programma VShadow.

Nell'esempio seguente viene illustrato come utilizzare l'opzione della riga di comando-exec per eseguire uno script denominato "enum. cmd":

**vshadow-NW-Exec = enum. cmd c:**

Nello script eseguito è inoltre possibile eseguire lo script SETVAR generato in questo comando personalizzato. Questo consente allo script di accedere direttamente al contenuto delle copie shadow. Tenere presente che il dispositivo shadow può essere recuperato dalla \_ variabile di ambiente VSHADOW Device \_ nnn.

Ecco uno script enum. cmd di esempio:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Ecco la riga di comando per eseguire lo script enum. cmd:

**vshadow-NW-Exec = c: \\ enum. cmd-script = setvar1. cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copia di un file da una copia shadow

Nell'esempio seguente viene illustrato come copiare un file da una copia shadow.

1.  **dir > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **chiamare SETVAR1. cmd**
4.  **copiare% VSHADOW \_ dispositivo \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerazione di tutti i file in un dispositivo di copia shadow

Nell'esempio seguente viene illustrato come enumerare tutti i file in un dispositivo di copia shadow da un file batch.

1.  **dir > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **chiamare SETVAR1. cmd**
4.  **per/R% VSHADOW \_ dispositivo \_ 1%% \\ i in ( \* ) eseguire @echo %% i**

## <a name="importing-a-transportable-shadow-copy"></a>Importazione di una copia shadow trasportabile

Per creare una copia shadow trasportabile in un computer e importarla in un altro computer, è necessario disporre di due computer connessi (tramite una configurazione SAN) a un array di archiviazione che supporta le copie shadow dell'hardware VSS. È necessario installare un provider hardware VSS in ogni computer.

Nell'esempio seguente viene illustrato come creare e importare la copia shadow.

1.  Creare il set di copie shadow nel computer A (server di produzione) digitando il comando seguente dopo il prompt dei comandi:

    **vshadow-p-t =bc1.xml**

    Non verrà esposto alcun dispositivo copia shadow nel computer A.

2.  Copiare il documento componenti di backup (bc1.xml) dal computer A al computer B.
3.  Importare il set di ombreggiatura nel computer B digitando il comando seguente:

    **vshadow-i =bc1.xml**

Facoltativamente, è possibile esporre queste copie shadow come lettere di unità o cartelle montate. Inoltre, è possibile suddividere il set di ombreggiatura per rendere i nuovi volumi di copia shadow in lettura/scrittura.

Per automatizzare il processo di gestione dei set di Shadow, è possibile usare l'opzione **-script** della riga di comando per generare lo script cmd contenente gli ID copia shadow. È quindi possibile copiare lo script generato insieme ai componenti di backup nell'altro computer.

Nell'esempio seguente viene illustrato come creare, esporre e suddividere copie shadow trasportabili tramite script CMD.

1.  Creare il set di copie shadow nel computer A (il server di produzione) dalla riga di comando come indicato di seguito:

    **vshadow-p-t =bc1.xml-script = SC1. cmd**

    Specificare l'opzione **-script** per generare lo script contenente le definizioni delle variabili di ambiente appropriate. Si noti che questo non esporrà alcuna copia shadow dei dispositivi nel computer A.

2.  Copiare il documento dei componenti di backup (bc1.xml) e lo script generato (SC1. cmd) dal computer a al computer B.
3.  Importare il set di ombreggiatura nel computer B digitando il comando seguente:

    **vshadow-i =bc1.xml**

    I dispositivi creati vengono visualizzati nel computer B.

4.  Eseguire lo script generato per impostare le variabili di ambiente per il set di copie shadow digitando il nome del file al prompt dei comandi, come nell'esempio seguente:

    **SC1. cmd**

    In questo modo, le variabili di ambiente pertinenti vengono impostate come descritto in accedere alle proprietà della copia shadow da uno script CMD.

5.  Esporre le copie shadow nel computer B digitando i comandi seguenti:
    1.  **rmdir/s c: \\ punto di montaggio \_**
    2.  **mkdir c: \\ punto di montaggio \_**
    3.  **vshadow – El =% VSHADOW \_ ID \_ 1%, c: \\ punto di montaggio \_**

    I dispositivi copia shadow creati nel computer B vengono visualizzati.
6.  Suddividere il set di copie shadow per rendere scrivibile i volumi digitando il comando seguente:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**

Si noti che le copie shadow trasportabili non permanenti possono anche essere importate, ma vengono eliminate automaticamente alla chiusura del processo **vshadow** **-i** . Per importare le copie shadow prima che vengano eliminate, è necessario usare l'opzione della riga di comando **-Exec** come descritto in accedere a copie shadow non permanenti.

## <a name="including-writers-or-components"></a>Inclusione di writer o componenti

Per impostazione predefinita, tutti i writer partecipano alla creazione della copia shadow. Per determinare quali writer e componenti verranno inclusi in un set di copie shadow, utilizzare l'opzione della riga di comando **-WM** o **-wm2** come descritto in [elenco dello stato e dei metadati del writer](vshadow-tool-and-sample.md).

Per verificare che tutti i componenti di un writer siano inclusi, utilizzare il flag **-Wi** facoltativo in uno dei formati seguenti:

-   **vshadow** **-Wi** *WriterName*
-   **vshadow** **-Wi** **"**_Nome writer stringa_*_"_*
-   **vshadow** **-Wi** **{**_WriterID_*_}_*
-   **vshadow** **-Wi** **{**_InstanceID_*_}_*

Per verificare che siano inclusi componenti specifici, utilizzare il flag **-Wi** facoltativo in uno dei formati seguenti:

-   **vshadow** **-Wi** *writer ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-Wi** **"**_Nome writer stringa_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Negli esempi seguenti viene illustrato come utilizzare il flag **-Wi** facoltativo.

-   Specifica di *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-Wi = "writer del registro di sistema: Registro di sistema \\ "**

-   Specifica di {*WriterID*}:

    **vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Specifica di più di un writer o di un componente:

    **vshadow-Wi = "Registry Writer: \\ Registry"-Wi = "com+ REGDB writer"**

## <a name="excluding-writers-or-components"></a>Esclusione di writer o componenti

Per escludere tutti i writer, usare il flag **-NW** facoltativo durante la creazione della copia shadow.

Per escludere tutti i componenti di un writer, usare il flag facoltativo **-WX** in uno dei formati seguenti:

-   **vshadow** **-WX** *WriterName*
-   **vshadow** **-WX** **"**_Nome writer stringa_*_"_*
-   **vshadow** **-WX** **{**_WriterID_*_}_*
-   **vshadow** **-WX** **{**_InstanceID_*_}_*

Per escludere componenti specifici, usare il flag **-WX** facoltativo in uno dei formati seguenti:

-   **vshadow** **-WX** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-WX** **"**_Nome writer stringa_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Gli esempi seguenti illustrano come usare il flag facoltativo **-WX** .

-   Specifica di *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-WX = "Registry Writer: \\ Registry"**

-   Specifica di {*WriterID*}:

    **vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Specifica di più di un writer o di un componente:

    **vshadow-WX = "Registry Writer: \\ Registry"-WX = "com+ REGDB writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Suddivisione di set di copie shadow tramite il metodo BreakSnapshotSetEx

Gli esempi seguenti illustrano come usare l'opzione della riga di comando **-Bex** .

-   Specifica che il LUN della copia shadow verrà mascherato dall'host:

    **vshadow** **-Bex** **-mask**

-   Specifica che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura:

    **vshadow** **-Bex** **-RW**

-   Specificando che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura e che nessuna delle firme del disco nei lun delle copie shadow verrà ripristinata a quella dei lun originali:

    **vshadow** **-Bex** **-Revert**

 

 
