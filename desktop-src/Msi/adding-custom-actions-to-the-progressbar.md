---
description: Le azioni personalizzate possono aggiungere informazioni su tempo e stato a un controllo ProgressBar. Per altre informazioni sulla creazione di una finestra di dialogo di visualizzazione delle azioni con un controllo ProgressBar, vedere Creazione di un controllo ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Aggiunta di azioni personalizzate a ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811061"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Aggiunta di azioni personalizzate a ProgressBar

[Le azioni personalizzate](custom-actions.md) possono aggiungere informazioni su tempo e stato a un [controllo ProgressBar.](progressbar-control.md) Per altre informazioni sulla creazione di una finestra di dialogo di visualizzazione delle azioni con un controllo ProgressBar, vedere [Creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).

Si noti che è necessario aggiungere due azioni personalizzate al pacchetto Windows Installer per segnalare in modo accurato le informazioni relative a tempo e stato al controllo ProgressBar. Un'azione personalizzata deve essere un'azione personalizzata posticipata. Questa azione personalizzata deve completare l'installazione personalizzata e inviare le quantità di singoli incrementi al controllo [ProgressBar](progressbar-control.md) quando il programma di installazione esegue lo script di installazione. La seconda azione personalizzata deve essere un'azione personalizzata di esecuzione immediata che indica a ProgressBar il numero di tick da aggiungere al conteggio totale durante la fase di acquisizione e generazione di script dell'installazione.

**Per aggiungere un'azione personalizzata a ProgressBar**

1.  Decidere in che modo l'azione personalizzata descriverà lo stato di avanzamento. Ad esempio, un'azione personalizzata che installa le chiavi del Registro di sistema potrebbe visualizzare un messaggio di stato e aggiornare [ProgressBar](progressbar-control.md) ogni volta che il programma di installazione scrive una chiave del Registro di sistema.
2.  Ogni aggiornamento da parte dell'azione personalizzata modifica la lunghezza di [ProgressBar](progressbar-control.md) di un incremento costante. Specificare o calcolare il numero di tick in ogni incremento. In genere, una modifica della lunghezza di ProgressBar di un tick corrisponde all'installazione di un byte. Ad esempio, se il programma di installazione installa circa 10000 byte quando scrive una chiave del Registro di sistema, è possibile specificare che sono presenti 10000 tick in un incremento.
3.  Specificare o calcolare il numero totale di tick aggiunti dall'azione personalizzata alla lunghezza di [ProgressBar](progressbar-control.md). Il numero di tick aggiunti dall'azione personalizzata viene in genere calcolato come: (incremento tick) x (numero di elementi). Ad esempio, se l'azione personalizzata scrive 10 chiavi del Registro di sistema, il programma di installazione installa circa 100000 byte e il programma di installazione deve pertanto aumentare di 100000 tick la stima della lunghezza totale finale di ProgressBar.
    > [!Note]  
    > Per calcolare questo valore in modo dinamico, l'azione personalizzata deve contenere una sezione che viene eseguita immediatamente durante la generazione dello script. La quantità di tick segnalati dall'azione personalizzata di esecuzione posticipata deve essere uguale al numero di tick aggiunti al conteggio totale dei tick dall'azione di esecuzione immediata. In caso contrario, il tempo rimanente indicato dal controllo di testo TimeRemaining non sarà accurato.

     

4.  Separare l'azione personalizzata in due sezioni di codice: una sezione eseguita durante la fase di generazione dello script e una sezione che viene eseguita durante la fase di esecuzione dell'installazione. È possibile eseguire questa operazione usando due file oppure è possibile usare un file condizionando la modalità di esecuzione del programma di installazione. L'esempio seguente usa un file e controlla lo stato di installazione. Le sezioni dell'esempio sono condizionate per l'esecuzione a seconda che il programma di installazione si trova nella fase di esecuzione o generazione di script dell'installazione.
5.  La sezione eseguita durante la generazione di script deve aumentare la stima della lunghezza totale finale di [ProgressBar](progressbar-control.md) del numero totale di tick nell'azione personalizzata. Questa operazione viene eseguita inviando un **messaggio di stato ProgressAddition.**
6.  La sezione che viene eseguita durante la fase di esecuzione dell'installazione deve configurare il testo del messaggio e i modelli per informare l'utente sulle operazioni dell'azione personalizzata e indirizzare il programma di installazione all'aggiornamento del [controllo ProgressBar.](progressbar-control.md) Ad esempio, informare il programma di installazione di spostare progressBar in avanti di un incremento e inviare un messaggio di stato esplicito a ogni aggiornamento. In genere in questa sezione è presente un ciclo se l'azione personalizzata sta installando qualcosa. Con ogni passaggio attraverso questo ciclo, il programma di installazione può installare un elemento di riferimento, ad esempio una chiave del Registro di sistema e aggiornare il controllo ProgressBar
7.  Aggiungere un'azione personalizzata di esecuzione immediata al pacchetto Windows installer. Questa azione personalizzata indica a [ProgressBar](progressbar-control.md) quanto avanzare durante le fasi di acquisizione e generazione di script dell'installazione. Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, CAProgress.
8.  Aggiungere un'azione personalizzata di esecuzione posticipata al pacchetto Windows installer. Questa azione personalizzata completa i passaggi dell'installazione effettiva e indica a [ProgressBar](progressbar-control.md) quanto far avanzare la barra nel momento in cui il programma di installazione esegue lo script di installazione. Per l'esempio seguente, l'origine è la DLL creata compilando il codice di esempio e la destinazione è il punto di ingresso, CAProgress.
9.  Pianificare entrambe le azioni personalizzate [tra InstallInitialize](installinitialize-action.md) [e InstallFinalize](installfinalize-action.md) nella [tabella InstallExecuteSequence.](installexecutesequence-table.md) L'azione personalizzata posticipata deve essere pianificata immediatamente dopo l'azione personalizzata di esecuzione immediata. Il programma di installazione non eseguirà l'azione personalizzata posticipata finché non viene eseguito lo script.

L'esempio seguente illustra come aggiungere un'azione personalizzata a [ProgressBar](progressbar-control.md). L'origine di entrambe le azioni personalizzate è la DLL creata compilando il codice di esempio e la destinazione di entrambe le azioni personalizzate è il punto di ingresso, CAProgress. Questo esempio non apporta modifiche effettive al sistema, ma gestisce ProgressBar come se installasse 10 elementi di riferimento di dimensioni di circa 10.000 byte. Il programma di installazione aggiorna il messaggio e ProgressBar ogni volta che installa un elemento di riferimento.


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



 

 



