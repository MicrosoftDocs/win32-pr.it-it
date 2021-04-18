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
# <a name="adding-custom-actions-to-the-progressbar"></a>Aggiunta di azioni personalizzate a ProgressBar

Le [azioni personalizzate](custom-actions.md) possono aggiungere informazioni sull'ora e sullo stato di avanzamento a un controllo [ProgressBar](progressbar-control.md) . Per ulteriori informazioni sulla creazione di una finestra di dialogo visualizzazione azione con ProgressBar, vedere [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).

Si noti che è necessario aggiungere due azioni personalizzate al pacchetto di Windows Installer per segnalare accuratamente l'ora e lo stato di avanzamento al ProgressBar. Un'azione personalizzata deve essere un'azione personalizzata posticipata. Questa azione personalizzata deve completare l'installazione personalizzata e inviare le quantità di singoli incrementi al controllo [ProgressBar](progressbar-control.md) quando il programma di installazione esegue lo script di installazione. La seconda azione personalizzata deve essere un'azione personalizzata di esecuzione immediata che informa l'oggetto ProgressBar sul numero di segni di graduazione da aggiungere al conteggio totale durante la fase di acquisizione e generazione dello script dell'installazione.

**Per aggiungere un'azione personalizzata al ProgressBar**

1.  Decidere in che modo l'azione personalizzata ne descriva lo stato di avanzamento. Ad esempio, un'azione personalizzata che consente di installare chiavi del registro di sistema potrebbe visualizzare un messaggio di stato e aggiornare il [ProgressBar](progressbar-control.md) ogni volta che il programma di installazione scrive una chiave del registro di sistema.
2.  Ogni aggiornamento dall'azione personalizzata modifica la lunghezza del [ProgressBar](progressbar-control.md) in base a un incremento costante. Specificare o calcolare il numero di cicli in ogni incremento. In genere, una modifica nella lunghezza di ProgressBar di un segno corrisponde all'installazione di un byte. Se, ad esempio, il programma di installazione installa approssimativamente 10000 byte quando scrive una chiave del registro di sistema, è possibile specificare che siano presenti 10000 cicli in un incremento.
3.  Specificare o calcolare il numero totale di cicli che l'azione personalizzata aggiunge alla lunghezza del [ProgressBar](progressbar-control.md). Il numero di cicli aggiunti dall'azione personalizzata viene in genere calcolato come: (incremento del segno di incremente) x (numero di elementi). Se, ad esempio, l'azione personalizzata scrive 10 chiavi del registro di sistema, il programma di installazione installa approssimativamente 100000 byte e il programma di installazione deve quindi aumentare la stima della lunghezza totale finale di ProgressBar per 100000 cicli.
    > [!Note]  
    > Per calcolare questa operazione in modo dinamico, l'azione personalizzata deve contenere una sezione che viene eseguita immediatamente durante la generazione di script. La quantità di cicli segnalati dall'azione personalizzata di esecuzione posticipata deve essere uguale al numero di segni di selezione aggiunti al conteggio totale dei cicli per l'azione di esecuzione immediata. In caso contrario, il tempo rimanente come riportato dal controllo di testo TimeRemaining sarà inaccurato.

     

4.  Separare l'azione personalizzata in due sezioni di codice: una sezione che viene eseguita durante la fase di generazione dello script e una sezione che viene eseguita durante la fase di esecuzione dell'installazione. È possibile eseguire questa operazione utilizzando due file oppure è possibile utilizzare un file per condizionare la modalità di esecuzione del programma di installazione. Nell'esempio seguente viene utilizzato un file e viene controllato lo stato di installazione. Le sezioni dell'esempio sono condizionate per l'esecuzione a seconda che il programma di installazione sia nella fase di esecuzione o di generazione dello script dell'installazione.
5.  La sezione eseguita durante la generazione di script deve aumentare la stima della lunghezza totale finale della [ProgressBar](progressbar-control.md) per il numero totale di cicli nell'azione personalizzata. Questa operazione viene eseguita inviando un messaggio di stato **ProgressAddition** .
6.  La sezione che viene eseguita durante la fase di esecuzione dell'installazione deve impostare il testo del messaggio e i modelli per informare l'utente sulle operazioni eseguite dall'azione personalizzata e per indicare al programma di installazione di aggiornare il controllo [ProgressBar](progressbar-control.md) . Ad esempio, informare il programma di installazione di spostare il ProgressBar inoltrare un incremento e inviare un messaggio di stato esplicito a ogni aggiornamento. In questa sezione è in genere presente un ciclo se l'azione personalizzata sta installando qualcosa. A ogni passaggio del ciclo, il programma di installazione può installare un elemento di riferimento, ad esempio una chiave del registro di sistema e aggiornare il controllo ProgressBar
7.  Aggiungere un'azione personalizzata di esecuzione immediata al pacchetto di Windows Installer. Questa azione personalizzata informa il [ProgressBar](progressbar-control.md) quanto anticipo durante le fasi di acquisizione e generazione di script dell'installazione. Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, caprogress.
8.  Aggiungere un'azione personalizzata di esecuzione posticipata al pacchetto Windows Installer. Questa azione personalizzata completa i passaggi dell'installazione effettiva e informa il [ProgressBar](progressbar-control.md) quanto avanzare la barra al momento dell'esecuzione dello script di installazione da parte del programma di installazione. Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, caprogress.
9.  Pianificare entrambe le azioni personalizzate tra [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) . L'azione personalizzata posticipata deve essere pianificata immediatamente dopo l'azione personalizzata di esecuzione immediata. Il programma di installazione non eseguirà l'azione personalizzata rinviata fino a quando non verrà eseguito lo script.

Nell'esempio seguente viene illustrato come è possibile aggiungere un'azione personalizzata al [ProgressBar](progressbar-control.md). L'origine di entrambe le azioni personalizzate è la DLL creata compilando il codice di esempio e la destinazione di entrambe le azioni personalizzate è il punto di ingresso, caprogress. In questo esempio non vengono apportate modifiche effettive al sistema, ma viene eseguito il ProgressBar come se si installassero 10 elementi di riferimento che hanno una dimensione di circa 10.000 byte. Il programma di installazione aggiorna il messaggio e ProgressBar ogni volta che viene installato un elemento di riferimento.


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



 

 



