---
title: Tasti di scelta rapida
description: Questa sezione illustra i tasti di scelta rapida. Un tasto di scelta rapida è una sequenza di tasti o una combinazione di sequenze di tasti che genera un messaggio di comando per un'applicazione.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- input utente, tasti di scelta rapida
- acquisizione di input utente, tasti di scelta rapida
- tasti di scelta rapida
- Acceleratori
- WM_COMMAND messaggio
- WM_SYS comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df67f4879edc2e0e81a8715155bf2edfac05f1e5ce9d3557f9b051ae682a6afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734469"
---
# <a name="keyboard-accelerators"></a>Tasti di scelta rapida

Un *tasto di scelta* rapida (o, semplicemente, un tasto di scelta rapida) è una sequenza di tasti o una combinazione di tasti che genera un messaggio WM [**\_ COMMAND**](wm-command.md) o [**\_ SYSCOMMAND WM**](wm-syscommand.md) per un'applicazione.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                                 | Descrizione                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Informazioni sui tasti di scelta rapida](about-keyboard-accelerators.md)       | Vengono illustrati i tasti di scelta rapida.<br/>                                |
| [Uso dei tasti di scelta rapida](using-keyboard-accelerators.md)       | Vengono illustrate le attività associate ai tasti di scelta rapida.<br/> |
| [Informazioni di riferimento sull'acceleratore di tastiera](keyboard-accelerator-reference.md) | Contiene il riferimento all'API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funzioni dei tasti di scelta rapida



| Nome                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copia la tabella dei tasti di scelta rapida specificata. Questa funzione viene usata per ottenere i dati accelerator-table che corrispondono a un handle accelerator-table o per determinare le dimensioni dei dati della tabella accelerator-table. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Crea una tabella dei tasti di scelta rapida. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Elimina una tabella dei tasti di scelta rapida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Carica la tabella dei tasti di scelta rapida specificata. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Elabora i tasti di scelta rapida per i comandi di menu. La funzione converte un messaggio [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) o [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) in un messaggio [**WM \_ COMMAND**](wm-command.md) o [**\_ SYSCOMMAND WM**](wm-syscommand.md) (se è presente una voce per il tasto nella tabella dei tasti di scelta rapida specificata) e quindi invia il messaggio WM **\_ COMMAND** o **WM \_ SYSCOMMAND** direttamente alla routine della finestra specificata. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) non restituisce finché la routine della finestra non ha elaborato il messaggio. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Messaggi dell'acceleratore di tastiera



| Nome                                          | Descrizione                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Inviato per indicare che lo stato dell'interfaccia utente deve essere modificato.<br/>                                                                                                                                                                                                                                                  |
| [**WM \_ INITMENU**](wm-initmenu.md)           | Inviato quando un menu sta per diventare attivo. Si verifica quando l'utente fa clic su una voce sulla barra dei menu o preme un tasto di menu. In questo modo l'applicazione può modificare il menu prima che venga visualizzato. <br/> Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Inviato per recuperare lo stato dell'interfaccia utente per una finestra.<br/>                                                                                                                                                                                                                                                            |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Inviato per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notifiche dell'acceleratore di tastiera



| Nome                                          | Descrizione                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) | Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu. <br/>                                                                                                                                              |
| [**WM \_ MENUCHAR**](wm-menuchar.md)           | Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o mnemoico. Questo messaggio viene inviato alla finestra proprietaria del menu. <br/>                                                                                                                                             |
| [**MENU \_ WMSELEZIONA**](wm-menuselect.md)       | Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu. <br/>                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCHAR**](wm-syschar.md)             | Inviato alla finestra con lo stato attivo della tastiera quando un [**messaggio WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) viene convertito dalla [**funzione TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) Specifica il codice carattere di un tasto carattere di sistema, un tasto di scelta rapida che viene premuto mentre il tasto ALT è premuto. <br/> |
| [**WM \_ SYSCOMMAND**](wm-syscommand.md)       | Una finestra riceve questo messaggio quando l'utente sceglie un comando dal **menu** Finestra o quando l'utente sceglie il pulsante ingrandisci, riduci a icona, ripristina o chiudi.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Strutture dei tasti di scelta rapida



| Nome                   | Descrizione                                                          |
|------------------------|----------------------------------------------------------------------|
| [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) | Definisce un tasto di scelta rapida usato in una tabella dei tasti di scelta rapida. <br/> |



 

 

