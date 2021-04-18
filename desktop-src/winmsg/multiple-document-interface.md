---
description: In questa sezione viene illustrata l'interfaccia a documenti multipli, ovvero una specifica che definisce un'interfaccia utente per le applicazioni che consentono all'utente di utilizzare più di un documento nello stesso momento.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interfaccia a documenti multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1898202aad6ec8d26f859bec2457124328c3a27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312489"
---
# <a name="multiple-document-interface"></a>Interfaccia a documenti multipli

\[Molti utenti nuovi e intermedi trovano difficile imparare a usare le applicazioni MDI. Pertanto, è consigliabile prendere in considerazione altri modelli per l'interfaccia utente. Tuttavia, è possibile utilizzare MDI per le applicazioni che non rientrano facilmente in un modello esistente.\]

L'interfaccia a documenti multipli (MDI, Multiple-Document Interface) è una specifica che definisce un'interfaccia utente per le applicazioni che consentono all'utente di usare più di un documento nello stesso momento.

### <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                              | Descrizione                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informazioni sull'interfaccia a più documenti](about-the-multiple-document-interface.md) | Descrive l'interfaccia a più documenti.<br/>                                     |
| [Uso dell'interfaccia a più documenti](using-the-multiple-document-interface.md) | Viene illustrato come eseguire attività associate all'interfaccia a più documenti.<br/> |
| [Riferimento MDI](multiple-document-interface-reference.md)                         | Contiene il riferimento all'API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funzioni MDI



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Crea una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Fornisce l'elaborazione predefinita per tutti i messaggi della finestra che la routine della finestra di una finestra cornice MDI non elabora. Tutti i messaggi della finestra che non vengono elaborati in modo esplicito dalla routine della finestra devono essere passati alla funzione [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) , non alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Fornisce l'elaborazione predefinita per qualsiasi messaggio della finestra che la routine della finestra di una finestra figlio MDI non elabora. Un messaggio della finestra non elaborato dalla routine della finestra deve essere passato alla funzione [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , non alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Elabora le sequenze di tasti di scelta rapida per i comandi di menu della finestra delle finestre figlio MDI associate alla finestra client MDI specificata. La funzione converte i messaggi [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) in messaggi [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) e li invia alle finestre figlio MDI appropriate. <br/> |



 

### <a name="mdi-messages"></a>Messaggi MDI



| Nome                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MDIACTIVATE WM**](wm-mdiactivate.md)       | Inviato a una finestra client MDI per indicare alla finestra del client di attivare un'altra finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**\_MDICASCADE WM**](wm-mdicascade.md)         | Inviato a una finestra client MDI per disporre tutte le relative finestre figlio in un formato Cascade. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**\_MDICREATE WM**](wm-mdicreate.md)           | Inviato a una finestra client MDI per creare una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_MDIDESTROY WM**](wm-mdidestroy.md)         | Inviato a una finestra client MDI per chiudere una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**\_MDIGETACTIVE WM**](wm-mdigetactive.md)     | Inviato a una finestra client MDI per recuperare l'handle per la finestra figlio MDI attiva. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md) | Inviato a una finestra del client MDI per disporre tutte le finestre figlio MDI ridotte a icona. Non influisce sulle finestre figlio non ridotte a icona. <br/>                                                                                                                                                                                                                                                                                                  |
| [**\_MDIMAXIMIZE WM**](wm-mdimaximize.md)       | Inviato a una finestra client MDI per ingrandire una finestra figlio MDI. Il sistema ridimensiona la finestra figlio per fare in modo che l'area client riempia la finestra del client. Il sistema posiziona l'icona del menu finestra della finestra figlio nella posizione più a destra della barra dei menu della finestra cornice e posiziona l'icona di ripristino della finestra figlio nella posizione più a sinistra. Il sistema aggiunge anche il testo della barra del titolo della finestra figlio a quello della finestra cornice. <br/> |
| [**\_MDINEXT WM**](wm-mdinext.md)               | Inviato a una finestra client MDI per attivare la finestra figlio precedente o successiva. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**\_MDIREFRESHMENU WM**](wm-mdirefreshmenu.md) | Inviato a una finestra client MDI per aggiornare il menu finestra della finestra cornice MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**\_MDIRESTORE WM**](wm-mdirestore.md)         | Inviato a una finestra client MDI per ripristinare una finestra figlio MDI dalla dimensione ingrandita o ridotta a icona. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**\_MDISETMENU WM**](wm-mdisetmenu.md)         | Inviato a una finestra del client MDI per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu finestra della finestra cornice o entrambi. <br/>                                                                                                                                                                                                                                                                                           |
| [**\_MDITILE WM**](wm-mditile.md)               | Inviato a una finestra client MDI per disporre tutte le finestre figlio MDI in un formato di riquadro. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Strutture MDI



| Nome                                       | Descrizione                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contiene informazioni sulla classe, il titolo, il proprietario, la posizione e le dimensioni di una finestra figlio MDI. <br/> |



 

 

