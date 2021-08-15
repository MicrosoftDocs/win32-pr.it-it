---
description: Molte Pannello di controllo visualizzano una finestra delle proprietà Proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni di sistema e dispositivo.
title: Come registrare e implementare un gestore della finestra delle proprietà per un'Pannello di controllo personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6865e8e50aefdea3e3d25c29c9abd3bbbabf5c6af3b770537ed187f8b055bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859590"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Come registrare e implementare un gestore della finestra delle proprietà per un'Pannello di controllo personalizzata

Molte Pannello di controllo visualizzano una finestra delle proprietà Proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni di sistema e dispositivo. Due di queste applicazioni, mouse e visualizzazione, consentono ai gestori della finestra delle proprietà di sostituire una o più pagine con una pagina personalizzata. Lo screenshot seguente mostra la finestra **delle proprietà Proprietà** mouse.

![Finestra delle proprietà del mouse](images/propsheethandler3.jpg)

I gestori della finestra delle proprietà Pannello di controllo applicazioni sono simili a quelli per i tipi di file, con due eccezioni principali:

-   Vengono chiamati da un'Pannello di controllo, non da Shell.
-   Vengono registrati in modo diverso.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   Shell

### <a name="prerequisites"></a>Prerequisiti

-   Conoscenza del Pannello di controllo
-   Conoscenza dei menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Passaggio 1: Registrazione di un gestore della finestra delle proprietà per un Pannello di controllo app Pannello di controllo proprietà

Un Pannello di controllo gestore della finestra delle proprietà dell'applicazione deve essere registrato nella sottochiave Pannello di controllo. Questa chiave può essere in una delle due posizioni, a seconda che il gestore sia per utente o per computer. Per la registrazione per utente, la sottochiave Pannello di controllo **HKEY \_ CURRENT \_ USER** \\ **Pannello di controllo**. La macro REGSTR PATH CONTROLPANEL definita in Regstr.h può essere usata nel codice al posto di \_ \_ "Pannello di controllo". Per la registrazione per computer, il percorso è:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Questo percorso può essere definito nel codice come HKEY LOCAL MACHINE REGSTR PATH CONTROLSFOLDER, usando la \_ macro \_ \\ \_ REGSTR PATH CONTROLSFOLDER definita in \_ \_ \_ Regstr.h.

Le Pannello di controllo che consentono ai gestori della finestra delle proprietà di sostituire le pagine hanno una sottochiave sotto la sottochiave del Pannello di controllo, denominata per l'applicazione, ad esempio Mouse e Schermo. La sottochiave dell'applicazione deve avere una **sottochiave shellex** con una **sottochiave PropertySheetHandlers.** Per registrare un gestore della finestra delle proprietà, aggiungerne il GUID alla sottochiave **PropertySheetHandlers** associata all'applicazione Pannello di controllo proprietà. A tale scopo, creare una sottochiave della sottochiave **PropertySheetHandlers,** denominata per il gestore della finestra delle proprietà, e impostarne il valore predefinito sul formato stringa del GUID del gestore.

Nell'esempio seguente viene registrato un gestore della finestra delle proprietà per l'applicazione Pannello di controllo mouse in base al computer. Per registrarlo per utente, sostituire **HKEY \_ LOCAL \_ MACHINE** \\ **REGSTR \_ PATH \_ CONTROLSFOLDER** con **HKEY CURRENT \_ \_ USER** \\ **REGSTR \_ PATH \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Passaggio 2: Implementazione di un gestore della finestra delle proprietà per un Pannello di controllo app Pannello di controllo proprietà

La procedura per l'implementazione Pannello di controllo gestore della finestra delle proprietà è molto simile a quella illustrata in Come registrare e implementare un gestore della finestra delle proprietà per [un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). La differenza principale è che [**ora IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) richiede un'implementazione nontoken anziché [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Quando un Pannello di controllo applicatore sta per visualizzare la relativa finestra delle proprietà, chiama il metodo [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del gestore della finestra delle proprietà una volta per ogni pagina che può essere sostituita. Il *parametro uPageID* è impostato sull'ID della pagina. Gli ID per le pagine disponibili sono definiti in Cplext.h. Gli ID attualmente disponibili sono elencati nella tabella seguente. 

| ID pagina                      | Descrizione         | Pannello di controllo app Pannello di controllo |
|------------------------------|---------------------|---------------------------|
| PULSANTI DEL MOUSE CPLPAGE \_ \_      | Pagina Pulsanti    | Mouse                     |
| CPLPAGE \_ MOUSE \_ PTRMOTION    | Pagina Movimento     | Mouse                     |
| ROTELLINA DEL MOUSE CPLPAGE \_ \_        | Pagina Ruota      | Mouse                     |
| VELOCITÀ DELLA TASTIERA \_ \_ CPLPAGE     | Pagina Velocità      | Tastiera                  |
| SFONDO DI VISUALIZZAZIONE CPLPAGE \_ \_ | Pagina Sfondo | Visualizza                   |



 

## <a name="remarks"></a>Commenti

La procedura per la creazione e la sostituzione di una pagina è identica a quella per l'aggiunta di una pagina. Per altre informazioni, vedere [Come registrare e implementare un gestore della finestra delle](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)proprietà per un tipo di file .

 

 



