---
description: In molte applicazioni del pannello di controllo viene visualizzata una finestra delle proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni del dispositivo e del sistema.
title: Come registrare e implementare un gestore della finestra delle proprietà per un'applicazione del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881561"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Come registrare e implementare un gestore della finestra delle proprietà per un'applicazione del pannello di controllo

In molte applicazioni del pannello di controllo viene visualizzata una finestra delle proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni del dispositivo e del sistema. Due di queste applicazioni, ovvero il mouse e la visualizzazione, consentono ai gestori della finestra delle proprietà di sostituire una o più pagine con una pagina personalizzata. Lo screenshot seguente mostra la finestra delle proprietà di **proprietà del mouse** .

![finestra delle proprietà proprietà del mouse](images/propsheethandler3.jpg)

I gestori della finestra delle proprietà per le applicazioni del pannello di controllo sono simili a quelli per i tipi di file, con due eccezioni principali:

-   Vengono chiamati da un'applicazione del pannello di controllo, non dalla Shell.
-   Sono registrati in modo diverso.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   Shell

### <a name="prerequisites"></a>Prerequisiti

-   Informazioni sul pannello di controllo
-   Conoscenza dei menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Passaggio 1: registrazione di un gestore della finestra delle proprietà per un'applicazione del pannello di controllo

Un gestore della finestra delle proprietà dell'applicazione del pannello di controllo deve essere registrato nella sottochiave del pannello di controllo. Questa chiave può trovarsi in una delle due posizioni, a seconda se il gestore deve essere per utente o per computer. Per la registrazione per utente, la sottochiave del pannello di controllo è **HKEY \_ Current \_ User** \\ **Control Panel**. Il percorso REGSTR della macro \_ \_ CONTROLPANEL come definito in REGSTR. h può essere utilizzato nel codice al posto di "pannello di controllo". Per la registrazione per computer, il percorso è:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

È possibile fare riferimento a questo percorso nel codice come \_ HKEY \_ percorso REGSTR del computer locale \\ \_ \_ CONTROLSFOLDER, usando la \_ macro REGSTR Path \_ CONTROLSFOLDER definita in REGSTR. h.

Le applicazioni del pannello di controllo che consentono ai gestori della finestra delle proprietà di sostituire le pagine hanno una sottochiave sotto la sottochiave del pannello di controllo, denominata per l'applicazione, ad esempio il mouse e la visualizzazione. La sottochiave dell'applicazione deve avere una sottochiave **ShellEx** con una sottochiave **PropertySheetHandlers** . Per registrare un gestore della finestra delle proprietà, aggiungere il GUID alla sottochiave **PropertySheetHandlers** associata all'applicazione del pannello di controllo. A tale scopo, creare una sottochiave della sottochiave **PropertySheetHandlers** , denominata per il gestore della finestra delle proprietà, e impostarne il valore predefinito sul formato stringa del GUID del gestore.

Nell'esempio seguente viene registrato un gestore della finestra delle proprietà per l'applicazione del pannello di controllo del mouse in base ai singoli computer. Per registrarlo in base ai singoli utenti, sostituire **HKEY \_ Local \_ computer** \\ **REGSTR \_ path \_ CONTROLSFOLDER** con **HKEY \_ Current \_ User** \\ **REGSTR \_ path \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Passaggio 2: implementazione di un gestore della finestra delle proprietà per un'applicazione del pannello di controllo

La procedura per implementare un gestore della finestra delle proprietà del pannello di controllo è molto simile a quella illustrata in [come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). La differenza principale consiste nel fatto che ora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) necessita di un'implementazione senza token invece di [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Quando un'applicazione del pannello di controllo sta per visualizzare la finestra delle proprietà, chiama il metodo [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del gestore della finestra delle proprietà una volta per ogni pagina che può essere sostituita. Il parametro *uPageID* è impostato sull'ID della pagina. Gli ID per le pagine disponibili sono definiti in Cplext. h. Gli ID attualmente disponibili sono elencati nella tabella seguente. 

| ID pagina                      | Descrizione         | Applicazione del pannello di controllo |
|------------------------------|---------------------|---------------------------|
| \_pulsanti del mouse CPLPAGE \_      | Pagina dei pulsanti    | Mouse                     |
| \_PTRMOTION mouse \_ CPLPAGE    | Pagina di movimento     | Mouse                     |
| \_rotellina del mouse CPLPAGE \_        | Pagina della rotellina      | Mouse                     |
| CPLPAGE \_ velocità della tastiera \_     | Pagina velocità      | Tastiera                  |
| sfondo per la \_ visualizzazione CPLPAGE \_ | Pagina di sfondo | Visualizza                   |



 

## <a name="remarks"></a>Commenti

La procedura per la creazione e la sostituzione di una pagina è identica a quella per l'aggiunta di una pagina. Per ulteriori informazioni, vedere [come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



