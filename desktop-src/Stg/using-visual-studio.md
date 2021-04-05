---
title: Con Visual Studio
description: Per praticità, Microsoft Visual Studio 6,0 fornisce un file di progetto per ogni esempio.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b32359a29d14a6cd5a4d08d015a6598ade376d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707294"
---
# <a name="using-visual-studio"></a>Con Visual Studio

Per praticità, Microsoft Visual Studio 6,0 fornisce un file di progetto per ogni esempio. Questo file ha l'estensione DSP. Nella directory principale viene inoltre fornito un file dell'area di lavoro Allsamp. dsw, in modo da poter compilare tutti gli esempi contemporaneamente da Visual Studio.

> [!Note]  
> Le istruzioni seguenti sono scritte per Microsoft Visual Studio 6,0. I comandi possono differire nelle versioni precedenti e successive di Visual Studio.

 

Per caricare il progetto appropriato per un esempio, è possibile eseguire Visual Studio al prompt dei comandi nella directory dell'esempio, come illustrato nell'esempio seguente. È necessario sostituire il nome del progetto di esempio per **<project name>** .

**MSDEV <project name> . DSP**

È anche possibile fare doppio clic sul file con estensione DSP in Esplora risorse per caricare un'area di lavoro di esempio in Visual Studio. Da Visual Studio è quindi possibile esplorare le classi C++ dell'origine di esempio e in genere eseguire le altre operazioni di modifica-compilazione-debug.

Nell'ambito del Software Development Kit (SDK) della piattaforma, la compilazione di questi esempi da Visual Studio richiede l'impostazione appropriata dei percorsi di directory in Visual Studio. Per impostare i percorsi di directory, seguire questa procedura:

-   Eseguire Microsoft Visual Studio (Visual C++).
-   Scegliere **Opzioni** dal menu **strumenti** .
-   Scegliere la scheda **directory** nella finestra di dialogo **Opzioni** .
-   Nell'elenco a discesa **Mostra directory per** selezionare **file eseguibili** e immettere il percorso della directory bin per l'SDK della piattaforma installata (ad esempio, C: \\ programmi \\ Microsoft SDK \\ bin). Fare clic sul pulsante freccia su per spostare il percorso appena immesso, in modo che sia la prima voce nell'elenco **directory** .
-   Nell'elenco a discesa **Mostra directory per** selezionare **Includi file** e immettere il percorso della directory di inclusione per l'SDK della piattaforma installata (ad esempio, C: \\ programmi \\ Microsoft SDK \\ include). Fare clic sul pulsante freccia su per spostare il percorso appena immesso, in modo che sia la prima voce nell'elenco **directory** .
-   Nell'elenco a discesa **Mostra directory per** selezionare i **file di libreria** e immettere il percorso della directory lib per l'SDK della piattaforma installata (ad esempio, C: \\ programmi \\ Microsoft SDK \\ lib). Fare clic sui pulsanti freccia su per spostare il percorso appena immesso, in modo che sia la prima voce nell'elenco **directory** .
-   Per completare le impostazioni, fare clic sul pulsante OK nella finestra di dialogo **Opzioni** .

Da qui è possibile usare le funzionalità Editor, debugger e progetto per modificare, compilare, collegare ed eseguire il debug.

Altri IDE visivi possono anche generare facilmente uno dei makefile di progetto nativi, in base ai file di origine esistenti di un esempio di codice. Se si usa un IDE di questo tipo, la generazione di un makefile di progetto nativo di questo tipo può essere molto utile perché offre un modo per esplorare le classi C++ del programma. Per ulteriori informazioni sull'utilizzo di makefile esterni o sulla creazione di un makefile di progetto nativo utilizzando un set di file di origine esistenti, vedere la documentazione dell'IDE.

Oltre alla dipendenza dal codice comune nelle directory APPUTIL, INC e LIB di pari livello, molti esempi di codice sono indipendenti. Compilare APPUTIL prima di compilare altri esempi di codice. Alcuni esempi successivi nella sequenza possono funzionare con i risultati compilati degli esempi precedenti. Di seguito sono riportate le interdipendenze di esempio di codice:

-   Any: la compilazione di qualsiasi esempio di codice richiede la compilazione precedente di APPUTIL.
-   DLLUSER: la compilazione o l'esecuzione richiede una compilazione precedente di DLLSKEL.
-   Comuser: la compilazione o l'esecuzione richiede una compilazione precedente di COMOBJ.
-   DLLSERVE: la compilazione richiede una compilazione precedente del registro.
-   DLLCLIEN: Run richiede la compilazione precedente di DLLSERVE.
-   LICSERVE: la compilazione richiede una compilazione precedente del registro.
-   LICCLIEN: Run richiede la compilazione precedente di LICSERVE e DLLSERVE.
-   MARSHAL: la compilazione richiede la compilazione precedente del registro.
-   LOCSERVE: la compilazione o l'esecuzione richiede una compilazione precedente di REGISTER e MARSHAL.
-   LOCCLIEN: Run richiede la compilazione precedente di LOCSERVE.
-   APTSERVE: la compilazione o l'esecuzione richiede una compilazione precedente di REGISTER e MARSHAL.
-   APTCLIEN: Run richiede la compilazione precedente di APTSERVE.
-   REMCLIEN: la compilazione o l'esecuzione richiede una compilazione precedente di REGISTER e MARSHAL sul computer locale (client). Per eseguire è necessaria la compilazione precedente di REGISTER, MARSHAL e APTSERVE nel computer remoto (Server).
-   FRESERVE: la compilazione richiede una compilazione precedente del registro.
-   FRECLIEN: Run richiede la compilazione precedente di FRESERVE.
-   CONSERVAZIONE: la compilazione richiede una compilazione precedente di REGISTER.
-   CONCLIEN: Run richiede una compilazione precedente di conserve.
-   STOSERVE: la compilazione richiede una compilazione precedente del registro.
-   STOCLIEN: Run richiede la compilazione precedente di STOSERVE.
-   CONSERVATI: la compilazione richiede una compilazione precedente del registro.
-   PERTEXT: la compilazione richiede una compilazione precedente del registro.
-   PERDRAW: la compilazione richiede una compilazione precedente del registro.
-   PERCLIEN: Run richiede la compilazione precedente di conservati, PERTEXT e PERDRAW.
-   DCDMARSH: la compilazione richiede una compilazione precedente del registro.
-   DCDSERVE: la compilazione o l'esecuzione richiede una compilazione precedente di REGISTER e DCDMARSH.
-   DCOMDRAW: la compilazione o l'esecuzione richiede una compilazione precedente di REGISTER e DCDMARSH nel computer locale (client). Per eseguire è necessaria la compilazione precedente di REGISTER, DCDMARSH e DCOMDRAW nel computer remoto (Server).

 

 




