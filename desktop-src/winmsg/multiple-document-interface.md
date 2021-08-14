---
description: In questa sezione viene illustrata l'interfaccia a documenti multipli, una specifica che definisce un'interfaccia utente per le applicazioni che consentono all'utente di usare più documenti contemporaneamente.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interfaccia a documenti multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d579d1075f85fae7cd2d4ca6e63e1b8196c6d2118e33102cd511a1e468a18ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705360"
---
# <a name="multiple-document-interface"></a>Interfaccia a documenti multipli

\[Molti utenti nuovi e intermedi hanno difficoltà a imparare a usare le applicazioni MDI. Pertanto, è consigliabile prendere in considerazione altri modelli per l'interfaccia utente. Tuttavia, è possibile usare MDI per le applicazioni che non rientrano facilmente in un modello esistente.\]

L'interfaccia a documenti multipli (MDI) è una specifica che definisce un'interfaccia utente per le applicazioni che consentono all'utente di usare più documenti contemporaneamente.

### <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                              | Descrizione                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informazioni sull'interfaccia a documenti multipli](about-the-multiple-document-interface.md) | Viene descritta l'interfaccia a documenti multipli.<br/>                                     |
| [Uso dell'interfaccia a documenti multipli](using-the-multiple-document-interface.md) | Viene illustrato come eseguire attività associate all'interfaccia a documenti multipli.<br/> |
| [Informazioni di riferimento su MDI](multiple-document-interface-reference.md)                         | Contiene il riferimento all'API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funzioni MDI



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Crea una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Fornisce l'elaborazione predefinita per tutti i messaggi di finestra non elaborati dalla routine della finestra di una finestra cornice MDI. Tutti i messaggi finestra che non vengono elaborati in modo esplicito dalla routine della finestra devono essere passati alla [**funzione DefFrameProc,**](/windows/win32/api/winuser/nf-winuser-defframeproca) non alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Fornisce l'elaborazione predefinita per qualsiasi messaggio di finestra non elaborata dalla routine della finestra di una finestra figlio MDI. Un messaggio di finestra non elaborato dalla routine della finestra deve essere passato alla [**funzione DefMDIChildProc,**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) non alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Elabora le sequenze di tasti di scelta rapida per i comandi di menu della finestra delle finestre figlio MDI associate alla finestra del client MDI specificata. La funzione converte [**i messaggi WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) in messaggi [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) e li invia alle finestre figlio MDI appropriate. <br/> |



 

### <a name="mdi-messages"></a>Messaggi MDI



| Nome                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ MDIACTIVATE**](wm-mdiactivate.md)       | Inviato a una finestra del client MDI per indicare alla finestra client di attivare un'altra finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ MDICASCADE**](wm-mdicascade.md)         | Inviato a una finestra del client MDI per disporre tutte le finestre figlio in un formato a cascata. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ MDICREATE**](wm-mdicreate.md)           | Inviato a una finestra del client MDI per creare una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIDESTROY**](wm-mdidestroy.md)         | Inviato a una finestra del client MDI per chiudere una finestra figlio MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)     | Inviato a una finestra del client MDI per recuperare l'handle per la finestra figlio MDI attiva. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) | Inviato a una finestra del client MDI per disporre tutte le finestre figlio MDI ridotte a icona. Non influisce sulle finestre figlio non ridotte a icona. <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)       | Inviato a una finestra del client MDI per ingrandire una finestra figlio MDI. Il sistema ridimensiona la finestra figlio per fare in modo che la relativa area client riempia la finestra client. Il sistema posiziona l'icona del menu della finestra figlio nella posizione più a destra della barra dei menu della finestra cornice e posiziona l'icona di ripristino della finestra figlio nella posizione più a sinistra. Il sistema aggiunge anche il testo della barra del titolo della finestra figlio a quello della finestra cornice. <br/> |
| [**WM \_ MDINEXT**](wm-mdinext.md)               | Inviato a una finestra del client MDI per attivare la finestra figlio successiva o precedente. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md) | Inviato a una finestra del client MDI per aggiornare il menu della finestra della finestra cornice MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ MDIRESTORE**](wm-mdirestore.md)         | Inviato a una finestra del client MDI per ripristinare una finestra figlio MDI dalle dimensioni ingrandite o ridotte a icona. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ MDISETMENU**](wm-mdisetmenu.md)         | Inviato a una finestra del client MDI per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu della finestra della finestra cornice o entrambi. <br/>                                                                                                                                                                                                                                                                                           |
| [**WM \_ MDITILE**](wm-mditile.md)               | Inviato a una finestra del client MDI per disporre tutte le finestre figlio MDI in un formato tessera. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Strutture MDI



| Nome                                       | Descrizione                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contiene informazioni sulla classe, il titolo, il proprietario, la posizione e le dimensioni di una finestra figlio MDI. <br/> |



 

 

