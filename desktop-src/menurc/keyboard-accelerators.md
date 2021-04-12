---
title: Tasti di scelta rapida
description: In questa sezione vengono illustrati i tasti di scelta rapida. Un tasto di scelta rapida è una sequenza di tasti o una combinazione di sequenze di tasti che genera un messaggio di comando per un'applicazione.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- input utente, tasti di scelta rapida
- acquisizione dell'input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- acceleratori
- Messaggio WM_COMMAND
- WM_SYS messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd8cecd2fc1273750c75b8e5f33106d22343a14
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398991"
---
# <a name="keyboard-accelerators"></a>Tasti di scelta rapida

Un tasto di *scelta rapida* (o, semplicemente, acceleratore) è una sequenza di tasti o una combinazione di sequenze di tasti che genera un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) per un'applicazione.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                                 | Descrizione                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Informazioni sui tasti di scelta rapida](about-keyboard-accelerators.md)       | Descrive i tasti di scelta rapida.<br/>                                |
| [Uso di tasti di scelta rapida](using-keyboard-accelerators.md)       | Vengono illustrate le attività associate agli acceleratori tastiera.<br/> |
| [Riferimento tasto di scelta rapida](keyboard-accelerator-reference.md) | Contiene il riferimento all'API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funzioni tasto di scelta rapida



| Nome                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copia la tabella di tasti di scelta rapida specificata. Questa funzione viene usata per ottenere i dati della tabella dei tasti di scelta rapida che corrispondono a un handle della tabella di tasti di scelta rapida o per determinare le dimensioni dei dati della tabella di tasti di scelta rapida. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Crea una tabella di tasti di scelta rapida. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Elimina definitivamente una tabella dei tasti di scelta rapida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Carica la tabella di tasti di scelta rapida specificata. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Elabora i tasti di scelta rapida per i comandi di menu. La funzione converte un messaggio [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) o [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) in un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) (se è presente una voce per la chiave nella tabella di tasti di scelta rapida specificata), quindi invia il **\_ comando WM** o il messaggio **WM \_ SYSCOMMAND** direttamente alla routine della finestra specificata. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) non restituisce alcun risultato finché la routine della finestra non ha elaborato il messaggio. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Messaggi tasto di scelta rapida



| Nome                                          | Descrizione                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CHANGEUISTATE WM**](wm-changeuistate.md) | Inviato per indicare che lo stato dell'interfaccia utente deve essere modificato.<br/>                                                                                                                                                                                                                                                  |
| [**\_INITMENU WM**](wm-initmenu.md)           | Inviato quando un menu sta per diventare attivo. Si verifica quando l'utente fa clic su un elemento nella barra dei menu o preme un tasto di menu. Questo consente all'applicazione di modificare il menu prima che venga visualizzato. <br/> Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**\_QUERYUISTATE WM**](wm-queryuistate.md)   | Inviato per recuperare lo stato dell'interfaccia utente per una finestra.<br/>                                                                                                                                                                                                                                                            |
| [**\_UPDATEUISTATE WM**](wm-updateuistate.md) | Inviato per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notifiche tasti di scelta rapida



| Nome                                          | Descrizione                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_INITMENUPOPUP WM**](wm-initmenupopup.md) | Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu. <br/>                                                                                                                                              |
| [**\_MENUCHAR WM**](wm-menuchar.md)           | Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o tasto di scelta rapida. Questo messaggio viene inviato alla finestra che possiede il menu. <br/>                                                                                                                                             |
| [**\_MENUSELECT WM**](wm-menuselect.md)       | Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu. <br/>                                                                                                                                                                                                                                                      |
| [**\_SYSCHAR WM**](wm-syschar.md)             | Inserito nella finestra con lo stato attivo quando un messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Specifica il codice carattere di una chiave carattere di sistema, ovvero un tasto carattere premuto mentre il tasto ALT è premuto. <br/> |
| [**\_SYSCOMMAND WM**](wm-syscommand.md)       | Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu **finestra** o quando l'utente sceglie il pulsante Ingrandisci, Riduci a icona, pulsante Ripristina o Chiudi.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Strutture di tasti di scelta rapida



| Nome                   | Descrizione                                                          |
|------------------------|----------------------------------------------------------------------|
| [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) | Definisce un tasto di scelta rapida utilizzato in una tabella dei tasti di scelta rapida. <br/> |



 

 

