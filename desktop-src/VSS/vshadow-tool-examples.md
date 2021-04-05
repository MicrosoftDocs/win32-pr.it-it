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
# <a name="vshadow-tool-examples"></a><span data-ttu-id="58363-103">Esempi di strumenti VShadow</span><span class="sxs-lookup"><span data-stu-id="58363-103">VShadow Tool Examples</span></span>

<span data-ttu-id="58363-104">Gli esempi seguenti illustrano come usare lo strumento VShadow per eseguire le attività più comuni:</span><span class="sxs-lookup"><span data-stu-id="58363-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="58363-105">Accesso alle proprietà della copia shadow da uno script CMD</span><span class="sxs-lookup"><span data-stu-id="58363-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="58363-106">Accesso a copie shadow non permanenti</span><span class="sxs-lookup"><span data-stu-id="58363-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="58363-107">Copia di un file da una copia shadow</span><span class="sxs-lookup"><span data-stu-id="58363-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="58363-108">Enumerazione di tutti i file in un dispositivo di copia shadow</span><span class="sxs-lookup"><span data-stu-id="58363-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="58363-109">Importazione di una copia shadow trasportabile</span><span class="sxs-lookup"><span data-stu-id="58363-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="58363-110">Inclusione di writer o componenti</span><span class="sxs-lookup"><span data-stu-id="58363-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="58363-111">Esclusione di writer o componenti</span><span class="sxs-lookup"><span data-stu-id="58363-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="58363-112">Suddivisione di set di copie shadow tramite il metodo BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="58363-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="58363-113">Per un elenco completo delle opzioni della riga di comando e del relativo utilizzo, vedere [vshadow Tool and Sample](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="58363-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="58363-114">Accesso alle proprietà della copia shadow da uno script CMD</span><span class="sxs-lookup"><span data-stu-id="58363-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="58363-115">Se si usa il flag facoltativo **-script** quando si creano copie shadow, vshadow crea un file di script cmd contenente le variabili di ambiente correlate alle copie shadow appena create, come le seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="58363-116">ID del set di copie shadow, archiviato nella variabile di ambiente% VSHADOW \_ set \_ ID%</span><span class="sxs-lookup"><span data-stu-id="58363-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="58363-117">ID copia shadow, archiviati in variabili con formato% VSHADOW \_ ID \_ *nnn*%, dove *nnn* rappresenta l'indice del volume di origine nella riga di comando di VSHADOW</span><span class="sxs-lookup"><span data-stu-id="58363-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="58363-118">I nomi dei dispositivi copia shadow, archiviati in variabili nel formato% VSHADOW \_ dispositivo \_ *nnn*%, dove *nnn* è l'indice del volume di origine nella riga di comando di VSHADOW</span><span class="sxs-lookup"><span data-stu-id="58363-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="58363-119">È possibile utilizzare il file CMD generato per eseguire operazioni di gestione limitate sulle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="58363-120">L'evento [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer viene inviato dopo l'esecuzione dello script **-Exec** .</span><span class="sxs-lookup"><span data-stu-id="58363-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="58363-121">VSS chiama il metodo **IVssBackupComponents:: BackupComplete** per segnalare ai writer che il backup è stato completato e i writer possono potenzialmente troncare i log in questo momento.</span><span class="sxs-lookup"><span data-stu-id="58363-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="58363-122">È quindi importante verificare che l'ombreggiatura o il backup sia stato effettivamente completato.</span><span class="sxs-lookup"><span data-stu-id="58363-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="58363-123">Se il backup non è riuscito, è possibile annullare il processo di creazione restituendo un codice di uscita diverso da zero nello script o comando eseguito.</span><span class="sxs-lookup"><span data-stu-id="58363-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="58363-124">(Vedere la documentazione relativa al comando Esci nella Guida di [riferimento alla riga di comando di Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))). Se il comando personalizzato restituisce con un codice di uscita diverso da zero, la creazione della copia shadow viene annullata e **IVssBackupComponents:: BackupComplete** non verrà chiamato.</span><span class="sxs-lookup"><span data-stu-id="58363-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="58363-125">Nell'esempio seguente viene illustrato come creare una copia shadow persistente dalla riga di comando e utilizzare lo script CMD per esporla.</span><span class="sxs-lookup"><span data-stu-id="58363-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="58363-126">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="58363-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="58363-127">**chiamare SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="58363-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="58363-128">**C: \\>vshadow-El =% vshadow \_ ID \_ 1%, c: \\ directory1**</span><span class="sxs-lookup"><span data-stu-id="58363-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="58363-129">Accesso a copie shadow non permanenti</span><span class="sxs-lookup"><span data-stu-id="58363-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="58363-130">Le copie shadow non permanenti vengono eliminate automaticamente quando il programma che li crea (in questo caso, VShadow) viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="58363-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="58363-131">Per accedere al contenuto di queste copie shadow, VShadow consente di eseguire uno script dopo la creazione delle copie shadow ma prima della chiusura del programma VShadow.</span><span class="sxs-lookup"><span data-stu-id="58363-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="58363-132">Nell'esempio seguente viene illustrato come utilizzare l'opzione della riga di comando-exec per eseguire uno script denominato "enum. cmd":</span><span class="sxs-lookup"><span data-stu-id="58363-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="58363-133">**vshadow-NW-Exec = enum. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="58363-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="58363-134">Nello script eseguito è inoltre possibile eseguire lo script SETVAR generato in questo comando personalizzato.</span><span class="sxs-lookup"><span data-stu-id="58363-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="58363-135">Questo consente allo script di accedere direttamente al contenuto delle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="58363-136">Tenere presente che il dispositivo shadow può essere recuperato dalla \_ variabile di ambiente VSHADOW Device \_ nnn.</span><span class="sxs-lookup"><span data-stu-id="58363-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="58363-137">Ecco uno script enum. cmd di esempio:</span><span class="sxs-lookup"><span data-stu-id="58363-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="58363-138">Ecco la riga di comando per eseguire lo script enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="58363-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="58363-139">**vshadow-NW-Exec = c: \\ enum. cmd-script = setvar1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="58363-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="58363-140">Copia di un file da una copia shadow</span><span class="sxs-lookup"><span data-stu-id="58363-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="58363-141">Nell'esempio seguente viene illustrato come copiare un file da una copia shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="58363-142">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="58363-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="58363-143">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="58363-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="58363-144">**chiamare SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="58363-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="58363-145">**copiare% VSHADOW \_ dispositivo \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="58363-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="58363-146">Enumerazione di tutti i file in un dispositivo di copia shadow</span><span class="sxs-lookup"><span data-stu-id="58363-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="58363-147">Nell'esempio seguente viene illustrato come enumerare tutti i file in un dispositivo di copia shadow da un file batch.</span><span class="sxs-lookup"><span data-stu-id="58363-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="58363-148">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="58363-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="58363-149">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="58363-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="58363-150">**chiamare SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="58363-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="58363-151">**per/R% VSHADOW \_ dispositivo \_ 1%% \\ i in ( \* ) eseguire @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="58363-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="58363-152">Importazione di una copia shadow trasportabile</span><span class="sxs-lookup"><span data-stu-id="58363-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="58363-153">Per creare una copia shadow trasportabile in un computer e importarla in un altro computer, è necessario disporre di due computer connessi (tramite una configurazione SAN) a un array di archiviazione che supporta le copie shadow dell'hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="58363-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="58363-154">È necessario installare un provider hardware VSS in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="58363-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="58363-155">Nell'esempio seguente viene illustrato come creare e importare la copia shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="58363-156">Creare il set di copie shadow nel computer A (server di produzione) digitando il comando seguente dopo il prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="58363-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="58363-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="58363-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="58363-158">Non verrà esposto alcun dispositivo copia shadow nel computer A.</span><span class="sxs-lookup"><span data-stu-id="58363-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="58363-159">Copiare il documento componenti di backup (bc1.xml) dal computer A al computer B.</span><span class="sxs-lookup"><span data-stu-id="58363-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="58363-160">Importare il set di ombreggiatura nel computer B digitando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="58363-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="58363-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="58363-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="58363-162">Facoltativamente, è possibile esporre queste copie shadow come lettere di unità o cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="58363-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="58363-163">Inoltre, è possibile suddividere il set di ombreggiatura per rendere i nuovi volumi di copia shadow in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="58363-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="58363-164">Per automatizzare il processo di gestione dei set di Shadow, è possibile usare l'opzione **-script** della riga di comando per generare lo script cmd contenente gli ID copia shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="58363-165">È quindi possibile copiare lo script generato insieme ai componenti di backup nell'altro computer.</span><span class="sxs-lookup"><span data-stu-id="58363-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="58363-166">Nell'esempio seguente viene illustrato come creare, esporre e suddividere copie shadow trasportabili tramite script CMD.</span><span class="sxs-lookup"><span data-stu-id="58363-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="58363-167">Creare il set di copie shadow nel computer A (il server di produzione) dalla riga di comando come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="58363-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="58363-168">**vshadow-p-t =bc1.xml-script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="58363-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="58363-169">Specificare l'opzione **-script** per generare lo script contenente le definizioni delle variabili di ambiente appropriate.</span><span class="sxs-lookup"><span data-stu-id="58363-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="58363-170">Si noti che questo non esporrà alcuna copia shadow dei dispositivi nel computer A.</span><span class="sxs-lookup"><span data-stu-id="58363-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="58363-171">Copiare il documento dei componenti di backup (bc1.xml) e lo script generato (SC1. cmd) dal computer a al computer B.</span><span class="sxs-lookup"><span data-stu-id="58363-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="58363-172">Importare il set di ombreggiatura nel computer B digitando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="58363-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="58363-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="58363-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="58363-174">I dispositivi creati vengono visualizzati nel computer B.</span><span class="sxs-lookup"><span data-stu-id="58363-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="58363-175">Eseguire lo script generato per impostare le variabili di ambiente per il set di copie shadow digitando il nome del file al prompt dei comandi, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="58363-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="58363-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="58363-176">**sc1.cmd**</span></span>

    <span data-ttu-id="58363-177">In questo modo, le variabili di ambiente pertinenti vengono impostate come descritto in accedere alle proprietà della copia shadow da uno script CMD.</span><span class="sxs-lookup"><span data-stu-id="58363-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="58363-178">Esporre le copie shadow nel computer B digitando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="58363-179">**rmdir/s c: \\ punto di montaggio \_**</span><span class="sxs-lookup"><span data-stu-id="58363-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="58363-180">**mkdir c: \\ punto di montaggio \_**</span><span class="sxs-lookup"><span data-stu-id="58363-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="58363-181">**vshadow – El =% VSHADOW \_ ID \_ 1%, c: \\ punto di montaggio \_**</span><span class="sxs-lookup"><span data-stu-id="58363-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="58363-182">I dispositivi copia shadow creati nel computer B vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="58363-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="58363-183">Suddividere il set di copie shadow per rendere scrivibile i volumi digitando il comando seguente:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="58363-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="58363-184">Si noti che le copie shadow trasportabili non permanenti possono anche essere importate, ma vengono eliminate automaticamente alla chiusura del processo **vshadow** **-i** .</span><span class="sxs-lookup"><span data-stu-id="58363-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="58363-185">Per importare le copie shadow prima che vengano eliminate, è necessario usare l'opzione della riga di comando **-Exec** come descritto in accedere a copie shadow non permanenti.</span><span class="sxs-lookup"><span data-stu-id="58363-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="58363-186">Inclusione di writer o componenti</span><span class="sxs-lookup"><span data-stu-id="58363-186">Including Writers or Components</span></span>

<span data-ttu-id="58363-187">Per impostazione predefinita, tutti i writer partecipano alla creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="58363-188">Per determinare quali writer e componenti verranno inclusi in un set di copie shadow, utilizzare l'opzione della riga di comando **-WM** o **-wm2** come descritto in [elenco dello stato e dei metadati del writer](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="58363-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="58363-189">Per verificare che tutti i componenti di un writer siano inclusi, utilizzare il flag **-Wi** facoltativo in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="58363-190">**vshadow** **-Wi** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="58363-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="58363-191">**vshadow** **-Wi** **"**_Nome writer stringa_*_"_*</span><span class="sxs-lookup"><span data-stu-id="58363-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="58363-192">**vshadow** **-Wi** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="58363-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="58363-193">**vshadow** **-Wi** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="58363-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="58363-194">Per verificare che siano inclusi componenti specifici, utilizzare il flag **-Wi** facoltativo in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="58363-195">**vshadow** **-Wi** \*writer \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="58363-196">**vshadow** **-Wi** **"**_Nome writer stringa_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="58363-197">**vshadow** **-Wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="58363-198">**vshadow** **-Wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="58363-199">Negli esempi seguenti viene illustrato come utilizzare il flag **-Wi** facoltativo.</span><span class="sxs-lookup"><span data-stu-id="58363-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="58363-200">Specifica di *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="58363-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="58363-201">**vshadow-Wi = "writer del registro di sistema: Registro di sistema \\ "**</span><span class="sxs-lookup"><span data-stu-id="58363-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="58363-202">Specifica di {*WriterID*}:</span><span class="sxs-lookup"><span data-stu-id="58363-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="58363-203">**vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="58363-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="58363-204">Specifica di più di un writer o di un componente:</span><span class="sxs-lookup"><span data-stu-id="58363-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="58363-205">**vshadow-Wi = "Registry Writer: \\ Registry"-Wi = "com+ REGDB writer"**</span><span class="sxs-lookup"><span data-stu-id="58363-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="58363-206">Esclusione di writer o componenti</span><span class="sxs-lookup"><span data-stu-id="58363-206">Excluding Writers or Components</span></span>

<span data-ttu-id="58363-207">Per escludere tutti i writer, usare il flag **-NW** facoltativo durante la creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="58363-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="58363-208">Per escludere tutti i componenti di un writer, usare il flag facoltativo **-WX** in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="58363-209">**vshadow** **-WX** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="58363-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="58363-210">**vshadow** **-WX** **"**_Nome writer stringa_*_"_*</span><span class="sxs-lookup"><span data-stu-id="58363-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="58363-211">**vshadow** **-WX** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="58363-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="58363-212">**vshadow** **-WX** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="58363-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="58363-213">Per escludere componenti specifici, usare il flag **-WX** facoltativo in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="58363-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="58363-214">**vshadow** **-WX** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="58363-215">**vshadow** **-WX** **"**_Nome writer stringa_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="58363-216">**vshadow** **-WX** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="58363-217">**vshadow** **-WX** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="58363-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="58363-218">Gli esempi seguenti illustrano come usare il flag facoltativo **-WX** .</span><span class="sxs-lookup"><span data-stu-id="58363-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="58363-219">Specifica di *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="58363-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="58363-220">**vshadow-WX = "Registry Writer: \\ Registry"**</span><span class="sxs-lookup"><span data-stu-id="58363-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="58363-221">Specifica di {*WriterID*}:</span><span class="sxs-lookup"><span data-stu-id="58363-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="58363-222">**vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="58363-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="58363-223">Specifica di più di un writer o di un componente:</span><span class="sxs-lookup"><span data-stu-id="58363-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="58363-224">**vshadow-WX = "Registry Writer: \\ Registry"-WX = "com+ REGDB writer"**</span><span class="sxs-lookup"><span data-stu-id="58363-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="58363-225">Suddivisione di set di copie shadow tramite il metodo BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="58363-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="58363-226">Gli esempi seguenti illustrano come usare l'opzione della riga di comando **-Bex** .</span><span class="sxs-lookup"><span data-stu-id="58363-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="58363-227">Specifica che il LUN della copia shadow verrà mascherato dall'host:</span><span class="sxs-lookup"><span data-stu-id="58363-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="58363-228">**vshadow** **-Bex** **-mask**</span><span class="sxs-lookup"><span data-stu-id="58363-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="58363-229">Specifica che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura:</span><span class="sxs-lookup"><span data-stu-id="58363-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="58363-230">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="58363-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="58363-231">Specificando che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura e che nessuna delle firme del disco nei lun delle copie shadow verrà ripristinata a quella dei lun originali:</span><span class="sxs-lookup"><span data-stu-id="58363-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="58363-232">**vshadow** **-Bex** **-Revert**</span><span class="sxs-lookup"><span data-stu-id="58363-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
