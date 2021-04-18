---
description: Le azioni personalizzate possono aggiungere informazioni sull'ora e sullo stato di avanzamento a un controllo ProgressBar. Per ulteriori informazioni sulla creazione di una finestra di dialogo visualizzazione azione con ProgressBar, vedere Creazione di un controllo ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Aggiunta di azioni personalizzate a ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311081"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="2477f-104">Aggiunta di azioni personalizzate a ProgressBar</span><span class="sxs-lookup"><span data-stu-id="2477f-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="2477f-105">Le [azioni personalizzate](custom-actions.md) possono aggiungere informazioni sull'ora e sullo stato di avanzamento a un controllo [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="2477f-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="2477f-106">Per ulteriori informazioni sulla creazione di una finestra di dialogo visualizzazione azione con ProgressBar, vedere [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="2477f-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="2477f-107">Si noti che è necessario aggiungere due azioni personalizzate al pacchetto di Windows Installer per segnalare accuratamente l'ora e lo stato di avanzamento al ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="2477f-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="2477f-108">Un'azione personalizzata deve essere un'azione personalizzata posticipata.</span><span class="sxs-lookup"><span data-stu-id="2477f-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="2477f-109">Questa azione personalizzata deve completare l'installazione personalizzata e inviare le quantità di singoli incrementi al controllo [ProgressBar](progressbar-control.md) quando il programma di installazione esegue lo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="2477f-110">La seconda azione personalizzata deve essere un'azione personalizzata di esecuzione immediata che informa l'oggetto ProgressBar sul numero di segni di graduazione da aggiungere al conteggio totale durante la fase di acquisizione e generazione dello script dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="2477f-111">**Per aggiungere un'azione personalizzata al ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="2477f-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="2477f-112">Decidere in che modo l'azione personalizzata ne descriva lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2477f-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="2477f-113">Ad esempio, un'azione personalizzata che consente di installare chiavi del registro di sistema potrebbe visualizzare un messaggio di stato e aggiornare il [ProgressBar](progressbar-control.md) ogni volta che il programma di installazione scrive una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2477f-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="2477f-114">Ogni aggiornamento dall'azione personalizzata modifica la lunghezza del [ProgressBar](progressbar-control.md) in base a un incremento costante.</span><span class="sxs-lookup"><span data-stu-id="2477f-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="2477f-115">Specificare o calcolare il numero di cicli in ogni incremento.</span><span class="sxs-lookup"><span data-stu-id="2477f-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="2477f-116">In genere, una modifica nella lunghezza di ProgressBar di un segno corrisponde all'installazione di un byte.</span><span class="sxs-lookup"><span data-stu-id="2477f-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="2477f-117">Se, ad esempio, il programma di installazione installa approssimativamente 10000 byte quando scrive una chiave del registro di sistema, è possibile specificare che siano presenti 10000 cicli in un incremento.</span><span class="sxs-lookup"><span data-stu-id="2477f-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="2477f-118">Specificare o calcolare il numero totale di cicli che l'azione personalizzata aggiunge alla lunghezza del [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="2477f-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="2477f-119">Il numero di cicli aggiunti dall'azione personalizzata viene in genere calcolato come: (incremento del segno di incremente) x (numero di elementi).</span><span class="sxs-lookup"><span data-stu-id="2477f-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="2477f-120">Se, ad esempio, l'azione personalizzata scrive 10 chiavi del registro di sistema, il programma di installazione installa approssimativamente 100000 byte e il programma di installazione deve quindi aumentare la stima della lunghezza totale finale di ProgressBar per 100000 cicli.</span><span class="sxs-lookup"><span data-stu-id="2477f-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="2477f-121">Per calcolare questa operazione in modo dinamico, l'azione personalizzata deve contenere una sezione che viene eseguita immediatamente durante la generazione di script.</span><span class="sxs-lookup"><span data-stu-id="2477f-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="2477f-122">La quantità di cicli segnalati dall'azione personalizzata di esecuzione posticipata deve essere uguale al numero di segni di selezione aggiunti al conteggio totale dei cicli per l'azione di esecuzione immediata.</span><span class="sxs-lookup"><span data-stu-id="2477f-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="2477f-123">In caso contrario, il tempo rimanente come riportato dal controllo di testo TimeRemaining sarà inaccurato.</span><span class="sxs-lookup"><span data-stu-id="2477f-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="2477f-124">Separare l'azione personalizzata in due sezioni di codice: una sezione che viene eseguita durante la fase di generazione dello script e una sezione che viene eseguita durante la fase di esecuzione dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="2477f-125">È possibile eseguire questa operazione utilizzando due file oppure è possibile utilizzare un file per condizionare la modalità di esecuzione del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="2477f-126">Nell'esempio seguente viene utilizzato un file e viene controllato lo stato di installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="2477f-127">Le sezioni dell'esempio sono condizionate per l'esecuzione a seconda che il programma di installazione sia nella fase di esecuzione o di generazione dello script dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="2477f-128">La sezione eseguita durante la generazione di script deve aumentare la stima della lunghezza totale finale della [ProgressBar](progressbar-control.md) per il numero totale di cicli nell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="2477f-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="2477f-129">Questa operazione viene eseguita inviando un messaggio di stato **ProgressAddition** .</span><span class="sxs-lookup"><span data-stu-id="2477f-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="2477f-130">La sezione che viene eseguita durante la fase di esecuzione dell'installazione deve impostare il testo del messaggio e i modelli per informare l'utente sulle operazioni eseguite dall'azione personalizzata e per indicare al programma di installazione di aggiornare il controllo [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="2477f-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="2477f-131">Ad esempio, informare il programma di installazione di spostare il ProgressBar inoltrare un incremento e inviare un messaggio di stato esplicito a ogni aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2477f-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="2477f-132">In questa sezione è in genere presente un ciclo se l'azione personalizzata sta installando qualcosa.</span><span class="sxs-lookup"><span data-stu-id="2477f-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="2477f-133">A ogni passaggio del ciclo, il programma di installazione può installare un elemento di riferimento, ad esempio una chiave del registro di sistema e aggiornare il controllo ProgressBar</span><span class="sxs-lookup"><span data-stu-id="2477f-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="2477f-134">Aggiungere un'azione personalizzata di esecuzione immediata al pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2477f-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="2477f-135">Questa azione personalizzata informa il [ProgressBar](progressbar-control.md) quanto anticipo durante le fasi di acquisizione e generazione di script dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="2477f-136">Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, caprogress.</span><span class="sxs-lookup"><span data-stu-id="2477f-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="2477f-137">Aggiungere un'azione personalizzata di esecuzione posticipata al pacchetto Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2477f-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="2477f-138">Questa azione personalizzata completa i passaggi dell'installazione effettiva e informa il [ProgressBar](progressbar-control.md) quanto avanzare la barra al momento dell'esecuzione dello script di installazione da parte del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="2477f-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="2477f-139">Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, caprogress.</span><span class="sxs-lookup"><span data-stu-id="2477f-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="2477f-140">Pianificare entrambe le azioni personalizzate tra [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2477f-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="2477f-141">L'azione personalizzata posticipata deve essere pianificata immediatamente dopo l'azione personalizzata di esecuzione immediata.</span><span class="sxs-lookup"><span data-stu-id="2477f-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="2477f-142">Il programma di installazione non eseguirà l'azione personalizzata rinviata fino a quando non verrà eseguito lo script.</span><span class="sxs-lookup"><span data-stu-id="2477f-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="2477f-143">Nell'esempio seguente viene illustrato come è possibile aggiungere un'azione personalizzata al [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="2477f-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="2477f-144">L'origine di entrambe le azioni personalizzate è la DLL creata compilando il codice di esempio e la destinazione di entrambe le azioni personalizzate è il punto di ingresso, caprogress.</span><span class="sxs-lookup"><span data-stu-id="2477f-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="2477f-145">In questo esempio non vengono apportate modifiche effettive al sistema, ma viene eseguito il ProgressBar come se si installassero 10 elementi di riferimento che hanno una dimensione di circa 10.000 byte.</span><span class="sxs-lookup"><span data-stu-id="2477f-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="2477f-146">Il programma di installazione aggiorna il messaggio e ProgressBar ogni volta che viene installato un elemento di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2477f-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



