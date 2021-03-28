---
description: La creazione di un'applicazione abilitata per l'AutoRun è una procedura semplice. In questo argomento viene usato il CD-ROM come esempio (il primo supporto per implementare questa tecnologia), ma oggi sono disponibili molti tipi di supporti diversi che possono usarlo.
title: Creazione di un'applicazione AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128467"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="dc0a1-104">Creazione di un'applicazione AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="dc0a1-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="dc0a1-105">La creazione di un'applicazione abilitata per l'AutoRun è una procedura semplice.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="dc0a1-106">In questo argomento viene usato il CD-ROM come esempio (il primo supporto per implementare questa tecnologia), ma oggi sono disponibili molti tipi di supporti diversi che possono usarlo.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="dc0a1-107">Per abilitare l'esecuzione automatica nell'applicazione, è sufficiente includere due file essenziali:</span><span class="sxs-lookup"><span data-stu-id="dc0a1-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="dc0a1-108">Un file Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="dc0a1-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="dc0a1-109">Un'applicazione di avvio</span><span class="sxs-lookup"><span data-stu-id="dc0a1-109">A startup application</span></span>

<span data-ttu-id="dc0a1-110">Quando un utente inserisce un disco in un'unità CD-ROM in un computer compatibile con AutoRun, il sistema verifica immediatamente se il disco dispone di un personal computer file system.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="dc0a1-111">In caso contrario, il sistema cerca un file denominato [Autorun. inf](#creating-an-autoruninf-file).</span><span class="sxs-lookup"><span data-stu-id="dc0a1-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="dc0a1-112">Questo file specifica un'applicazione di installazione che verrà eseguita insieme a un'ampia gamma di impostazioni facoltative.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="dc0a1-113">L'applicazione di avvio in genere installa, Disinstalla, configura ed eventualmente esegue l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="dc0a1-114">Creazione di un file Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="dc0a1-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="dc0a1-115">[\[Sezione DeviceInstall \]](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="dc0a1-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="dc0a1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc0a1-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="dc0a1-117">Creazione di un file Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="dc0a1-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="dc0a1-118">Autorun. inf è un file di testo che si trova nella directory radice del CD-ROM che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="dc0a1-119">La funzione principale è fornire al sistema il nome e il percorso del programma di avvio dell'applicazione che verrà eseguito quando viene inserito il disco.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="dc0a1-120">I file Autorun. inf non sono supportati in Windows XP per le unità che restituiscono l'unità \_ rimovibile da [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span><span class="sxs-lookup"><span data-stu-id="dc0a1-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="dc0a1-121">Il file Autorun. inf può inoltre contenere informazioni facoltative, tra cui:</span><span class="sxs-lookup"><span data-stu-id="dc0a1-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="dc0a1-122">Nome di un file che contiene un'icona che rappresenterà l'unità CD-ROM dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="dc0a1-123">Questa icona verrà visualizzata da Esplora risorse al posto dell'icona dell'unità standard.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="dc0a1-124">Comandi aggiuntivi per il menu di scelta rapida visualizzato quando l'utente fa clic con il pulsante destro del mouse sull'icona del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="dc0a1-125">È anche possibile specificare il comando predefinito che viene eseguito quando l'utente fa doppio clic sull'icona.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="dc0a1-126">I file Autorun. inf sono simili ai file ini.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="dc0a1-127">Sono costituiti da una o più sezioni, ciascuna con un nome racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="dc0a1-128">Ogni sezione contiene una serie di comandi che verranno eseguiti dalla shell quando viene inserito il disco.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="dc0a1-129">Sono presenti due sezioni attualmente definite per i file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="dc0a1-130">La sezione **\[ Autorun \]** contiene i comandi di autorun predefiniti.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="dc0a1-131">Tutti i file Autorun. inf devono avere una sezione di **\[ Autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="dc0a1-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="dc0a1-132">È possibile includere una sezione di **\[ Autorun. Alpha \]** facoltativa per i sistemi in esecuzione su computer basati su RISC.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="dc0a1-133">Quando un disco viene inserito in un'unità CD-ROM in un sistema basato su RISC, la shell eseguirà i comandi in questa sezione anziché quelli presenti nella sezione **\[ Autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="dc0a1-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="dc0a1-134">La shell verifica innanzitutto la presenza di una sezione specifica dell'architettura.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="dc0a1-135">Se non ne viene trovato uno, USA le informazioni contenute nella sezione **\[ Autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="dc0a1-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="dc0a1-136">Quando la shell trova una sezione, ignora tutte le altre, quindi ogni sezione deve essere indipendente.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="dc0a1-137">Ogni sezione contiene una serie di comandi che determinano il modo in cui viene eseguita l'operazione di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="dc0a1-138">Sono disponibili cinque comandi.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-138">There are five commands available.</span></span>



| <span data-ttu-id="dc0a1-139">Comando</span><span class="sxs-lookup"><span data-stu-id="dc0a1-139">Command</span></span>                         | <span data-ttu-id="dc0a1-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc0a1-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc0a1-141">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="dc0a1-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="dc0a1-142">Specifica l'icona predefinita per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="dc0a1-143">icona</span><span class="sxs-lookup"><span data-stu-id="dc0a1-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="dc0a1-144">Specifica il percorso e il nome file di un'icona specifica dell'applicazione per l'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="dc0a1-145">open</span><span class="sxs-lookup"><span data-stu-id="dc0a1-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="dc0a1-146">Specifica il percorso e il nome file dell'applicazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="dc0a1-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="dc0a1-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="dc0a1-148">Specifica che le funzionalità AutoPlay V2 devono essere utilizzate se supportate.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="dc0a1-149">Shell</span><span class="sxs-lookup"><span data-stu-id="dc0a1-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="dc0a1-150">Definisce il comando predefinito nel menu di scelta rapida del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="dc0a1-151">Verbo della shell \_</span><span class="sxs-lookup"><span data-stu-id="dc0a1-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="dc0a1-152">Aggiunge comandi al menu di scelta rapida del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="dc0a1-153">Di seguito è riportato un esempio di un semplice file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="dc0a1-154">Specifica Filename.exe come applicazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="dc0a1-155">La seconda icona in Filename.exe rappresenterà l'unità CD-ROM anziché l'icona dell'unità standard.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="dc0a1-156">Questo esempio di autorun. inf esegue diverse applicazioni di avvio a seconda del tipo di computer.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="dc0a1-157">\[Sezione DeviceInstall \]</span><span class="sxs-lookup"><span data-stu-id="dc0a1-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="dc0a1-158">È possibile usare la sezione **\[ DeviceInstall \]** su qualsiasi supporto rimovibile.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="dc0a1-159">È supportato solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="dc0a1-160">Usare **DriverPath** per specificare un percorso di directory in cui Windows XP cerca i file del driver, impedendo una lunga ricerca nell'intero contenuto.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="dc0a1-161">Utilizzare la sezione **\[ DeviceInstall \]** con l'installazione di un driver per specificare le directory in cui Windows XP deve cercare i file di driver nel supporto.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="dc0a1-162">In Windows XP, per impostazione predefinita non viene più eseguita la ricerca di interi supporti, pertanto è necessario che **\[ DeviceInstall \]** specifichi i percorsi di ricerca.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="dc0a1-163">Di seguito sono riportati gli unici supporti rimovibili che Windows XP cerca completamente senza una sezione **\[ DeviceInstall \]** in un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="dc0a1-164">Dischi floppy presenti nelle unità A o B.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="dc0a1-165">Supporti CD/DVD di dimensioni inferiori a 1 gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="dc0a1-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="dc0a1-166">Tutti gli altri supporti devono includere una sezione **\[ DeviceInstall \]** per Windows XP per rilevare tutti i driver archiviati in tale supporto.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="dc0a1-167">Come per la sezione **\[ Autorun \]** , la sezione **\[ DeviceInstall \]** può essere specifica dell'architettura.</span><span class="sxs-lookup"><span data-stu-id="dc0a1-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dc0a1-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc0a1-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc0a1-169">Come implementare le applicazioni di avvio autorun</span><span class="sxs-lookup"><span data-stu-id="dc0a1-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="dc0a1-170">Scrittura di un'applicazione di installazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc0a1-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
