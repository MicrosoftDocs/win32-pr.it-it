---
description: 'Altre informazioni su: Esempi di strumenti VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Esempi di strumenti VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056349"
---
# <a name="vshadow-tool-examples"></a>Esempi di strumenti VShadow

Gli esempi seguenti illustrano come usare lo strumento VShadow per eseguire le attività più comuni:

-   [Accesso alle proprietà della copia shadow da uno script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Accesso a copie shadow non di persistenti](#accessing-nonpersistent-shadow-copies)
-   [Copia di un file da una copia shadow](#copying-a-file-from-a-shadow-copy)
-   [Enumerazione di tutti i file in un dispositivo di copia shadow](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importazione di una copia shadow trasportabile](#importing-a-transportable-shadow-copy)
-   [Inclusione di writer o componenti](#including-writers-or-components)
-   [Esclusione di writer o componenti](#excluding-writers-or-components)
-   [Interruzione di set di copie shadow tramite il metodo BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Per un elenco completo delle opzioni della riga di comando e il relativo uso, vedere [Strumento VShadow ed esempio](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Accesso alle proprietà della copia shadow da uno script CMD

Se si usa il flag facoltativo **-script** quando si creano copie shadow, VShadow crea un file script CMD contenente le variabili di ambiente correlate alle copie shadow appena create, ad esempio:

-   ID del set di copie shadow, archiviato nella variabile di ambiente %VSHADOW \_ SET \_ ID%
-   ID della copia shadow, archiviati in variabili nel formato %VSHADOW ID NNN %, dove NNN rappresenta l'indice del volume di origine nella riga di comando \_ \_ di VShadow 
-   I nomi dei dispositivi della copia shadow, archiviati in variabili nel formato %VSHADOW DEVICE NNN %, dove NNN è l'indice del volume di origine nella riga di comando \_ \_ di VShadow 

È possibile usare il file CMD generato per eseguire operazioni di gestione limitate sulle copie shadow.

> [!Note]  
> L'evento writer [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) viene inviato dopo l'esecuzione dello script **-exec.** VSS chiama il metodo **IVssBackupComponents::BackupComplete** per segnalare ai writer che il backup è stato completato e i writer possono potenzialmente troncare i log a questo punto. È quindi importante verificare che lo shadow/backup sia stato effettivamente completato. Se il backup non è riuscito, è possibile annullare il processo di creazione restituisce un codice di uscita diverso da zero nello script o nel comando eseguito. Vedere la documentazione per il comando exit nella guida di [riferimento Windows riga di comando.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)) Se il comando personalizzato restituisce un codice di uscita diverso da zero, la creazione della copia shadow viene annullata e **IVssBackupComponents::BackupComplete** non verrà chiamato.

 

L'esempio seguente illustra come creare una copia shadow permanente dalla riga di comando e usare lo script CMD per esporla.

1.  **vshadow -p -nw -script=SETVAR1.cmd c:**
2.  **chiamare SETVAR1.cmd**
3.  **C: \\>vshadow -el=%VSHADOW \_ ID \_ 1%,c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Accesso a copie shadow non di persistenti

Le copie shadow non permanente vengono eliminate automaticamente quando il programma che le crea (in questo caso VShadow) viene chiuso. Per accedere al contenuto di queste copie shadow, VShadow consente di eseguire uno script dopo la creazione delle copie shadow, ma prima della chiusura del programma VShadow.

L'esempio seguente illustra come usare l'opzione della riga di comando -exec per eseguire uno script denominato "enum.cmd":

**vshadow -nw -exec=enum.cmd c:**

Nello script eseguito è anche possibile eseguire lo script SETVAR generato in questo comando personalizzato. In questo modo lo script può accedere direttamente al contenuto delle copie shadow. Tenere presente che il dispositivo shadow può essere recuperato dalla variabile di ambiente VSHADOW \_ DEVICE \_ NNN.

Ecco un esempio di script enum.cmd:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Ecco la riga di comando per eseguire lo script enum.cmd:

**vshadow -nw -exec=c: \\ enum.cmd -script=setvar1.cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copia di un file da una copia shadow

Nell'esempio seguente viene illustrato come copiare un file da una copia shadow.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **chiamare SETVAR1.cmd**
4.  **copy %VSHADOW \_ DEVICE \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerazione di tutti i file in un dispositivo di copia shadow

L'esempio seguente illustra come enumerare tutti i file in un dispositivo di copia shadow da un file batch.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **chiamare SETVAR1.cmd**
4.  **per /R %VSHADOW \_ DEVICE \_ 1% \\ %%i in ( \* ) do @echo %%i**

## <a name="importing-a-transportable-shadow-copy"></a>Importazione di una copia shadow trasportabile

Per creare una copia shadow trasportabile in un computer e importarla in un altro computer, è necessario disporre di due computer connessi (tramite una configurazione SAN) a un array di archiviazione che supporta copie shadow dell'hardware vss. In ogni computer deve essere installato un provider hardware vss.

Nell'esempio seguente viene illustrato come creare e importare la copia shadow.

1.  Creare il set di copie shadow nel computer A (il server di produzione) digitando il comando seguente dopo il prompt dei comandi:

    **vshadow -p -t=bc1.xml**

    In questo modo non verranno esposti dispositivi di copia shadow nel computer A.

2.  Copiare il documento dei componenti di backup (bc1.xml) dal computer A al computer B.
3.  Importare il set di ombreggiatura nel computer B digitando il comando seguente:

    **vshadow -i=bc1.xml**

Facoltativamente, è possibile esporre queste copie shadow come lettere di unità o cartelle montate. Inoltre, è possibile che si interrompa potenzialmente il set di shadow per rendere i nuovi volumi di copia shadow di lettura/scrittura.

Per automatizzare il processo di gestione dei set di shadow, è possibile usare l'opzione della riga di comando **-script** per generare lo script CMD contenente gli ID copia shadow. È quindi possibile copiare lo script generato insieme ai componenti di backup nell'altro computer.

Nell'esempio seguente viene illustrato come creare, esporre e interrompere copie shadow trasportabili utilizzando script CMD.

1.  Creare il set di copie shadow nel computer A (il server di produzione) dalla riga di comando come indicato di seguito:

    **vshadow -p -t=bc1.xml -script=sc1.cmd**

    Specificare **l'opzione -script** per generare lo script contenente le definizioni delle variabili di ambiente appropriate. Si noti che non esporrà alcun dispositivo di copia shadow nel computer A.

2.  Copiare il documento dei componenti di backup (bc1.xml) e lo script generato (sc1.cmd) dal computer A al computer B.
3.  Importare il set di ombreggiatura nel computer B digitando il comando seguente:

    **vshadow -i=bc1.xml**

    In questo modo i dispositivi creati saranno disponibili nel computer B.

4.  Eseguire lo script generato per impostare le variabili di ambiente per il set di copie shadow digitando il nome del file al prompt dei comandi, come nell'esempio seguente:

    **sc1.cmd**

    Verranno impostate le variabili di ambiente pertinenti come descritto in Accedere alle proprietà della copia shadow da uno script CMD.

5.  Esporre le copie shadow nel computer B digitando i comandi seguenti:
    1.  **rmdir /s c: \\ punto di \_ montaggio**
    2.  **mkdir c: punto \\ di \_ montaggio**
    3.  **vshadow –el=%VSHADOW \_ ID \_ 1%,c: \\ punto di \_ montaggio**

    In questo modo verranno eresi i dispositivi di copia shadow creati nel computer B.
6.  Interrompere il set di copie shadow per rendere i volumi scrivibili digitando il comando **seguente: C: \\>vshadow –bw=%VSHADOW \_ SET \_ ID%**

Si noti che è possibile importare anche copie shadow trasportabili non permanente, ma vengono eliminate automaticamente quando il **processo vshadow** **-i** viene chiuso. Per importare le copie shadow prima che siano eliminate, è necessario usare l'opzione della riga di comando **-exec** come descritto in Accedere a copie shadow non permanente.

## <a name="including-writers-or-components"></a>Inclusione di writer o componenti

Per impostazione predefinita, tutti i writer partecipano alla creazione della copia shadow. Per determinare quali writer e componenti verranno inclusi in un set di copie shadow, usare l'opzione della riga di comando **-wm** o **-wm2** come descritto in Elenco dello stato e dei [metadati](vshadow-tool-and-sample.md)del writer.

Per verificare che tutti i componenti di un writer siano inclusi, usare il flag facoltativo **-wi** in uno dei formati seguenti:

-   **vshadow** **-wi** *WriterName*
-   **vshadow** **-wi** **"** Writer Name _String_*_"_*
-   **vshadow** **-wi** **{**_WriterID_*_}_*
-   **vshadow** **-wi** **{**_InstanceID_*_}_*

Per verificare che siano inclusi componenti specifici, usare il flag facoltativo **-wi** in uno dei formati seguenti:

-   **vshadow** **-wi** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wi** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Gli esempi seguenti illustrano come usare il flag **facoltativo -wi.**

-   Specifica di *WriterName:* \\ *LogicalPath* \\ *ComponentName*:

    **vshadow -wi="Registry Writer: \\ Registry"**

-   Specifica di {*WriterID*}:

    **vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Specifica di più writer o componenti:

    **vshadow -wi="Registry Writer: \\ Registry" -wi="COM+ REGDB Writer"**

## <a name="excluding-writers-or-components"></a>Esclusione di writer o componenti

Per escludere tutti i writer, usare il flag **facoltativo -nw** durante la creazione della copia shadow.

Per escludere tutti i componenti di un writer, usare il flag facoltativo **-wx** in uno dei formati seguenti:

-   **vshadow** **-wx** *WriterName*
-   **vshadow** **-wx** **" Writer**_Name String_*_"_*
-   **vshadow** **-wx** **{**_WriterID_*_}_*
-   **vshadow** **-wx** **{**_InstanceID_*_}_*

Per escludere componenti specifici, usare il flag facoltativo **-wx** in uno dei formati seguenti:

-   **vshadow** **-wx** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wx** **" Writer**_Name String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Gli esempi seguenti illustrano come usare il flag **facoltativo -wx.**

-   Specifica di *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow -wx="Registry Writer: \\ Registry"**

-   Specifica di {*WriterID*}:

    **vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Specifica di più writer o componenti:

    **vshadow -wx="Registry Writer: \\ Registry" -wx="COM+ REGDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Interruzione di set di copie shadow tramite il metodo BreakSnapshotSetEx

Gli esempi seguenti illustrano come usare l'opzione della riga di **comando -bex.**

-   Specifica che il LUN della copia shadow verrà mascherato dall'host:

    **vshadow** **-bex** **-mask**

-   Specifica che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura:

    **vshadow** **-bex** **-rw**

-   Specificando che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura e che nessuna delle firme del disco nei LUN della copia shadow verrà ripristinata a quella dei LUN originali:

    **vshadow** **-bex** **-norevert**

 

 
