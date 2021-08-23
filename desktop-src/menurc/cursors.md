---
title: Cursori
description: Questa sezione illustra i cursori che sono immagini di piccole dimensioni la cui posizione sullo schermo è controllata da un dispositivo di puntamento, ad esempio un mouse, una penna o un trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- risorse,cursori
- cursori,informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7be5b8e213dd1911d2227a3dce4b61078ab1a22711d4e765525c7fbd5bd08d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712611"
---
# <a name="cursors"></a>Cursori

Un cursore è un'immagine di piccole dimensioni la cui posizione sullo schermo è controllata da un dispositivo di puntamento, ad esempio un mouse, una penna o un trackball. Nella parte restante di questa panoramica, il termine mouse si riferisce a qualsiasi dispositivo di puntamento.

Quando l'utente sposta il mouse, il sistema sposta il cursore di conseguenza. Le funzioni cursore consentono alle applicazioni di creare, caricare, visualizzare, animare, spostare, limitare ed eliminare i cursori.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                     | Descrizione                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Informazioni sui cursori](about-cursors.md)       | Vengono illustrati i cursori standard.<br/>                    |
| [Uso dei cursori](using-cursors.md)       | Viene illustrato come eseguire attività correlate ai cursori.<br/> |
| [Riferimento al cursore](cursor-reference.md) | Contiene il riferimento all'API.<br/>                        |



 

### <a name="cursor-functions"></a>Funzioni per i cursori



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Limita il cursore a un'area rettangolare sullo schermo. Se una posizione successiva del cursore (impostata dalla [**funzione SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) o dal mouse) si trova all'esterno del rettangolo, il sistema regola automaticamente la posizione per mantenere il cursore all'interno dell'area rettangolare. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Copia il cursore specificato. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Crea un cursore con le dimensioni, i modelli di bit e l'area sensibile specificati. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Elimina un cursore e libera la memoria occupata dal cursore. Non usare questa funzione per eliminare un cursore condiviso.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Recupera le coordinate dello schermo dell'area rettangolare in cui è limitato il cursore. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Recupera un handle per il cursore corrente. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Recupera informazioni sul cursore globale.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Recupera la posizione del cursore, in coordinate dello schermo.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Recupera la posizione del cursore nelle coordinate fisiche.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Carica la risorsa cursore specificata dal file eseguibile (.EXE) associato a un'istanza dell'applicazione.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Crea un cursore basato sui dati contenuti in un file. <br/>                                                                                                                                                                                                                                        |
| [**Setcursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Imposta la forma del cursore. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Sposta il cursore alle coordinate dello schermo specificate. Se le nuove coordinate non sono all'interno del rettangolo dello schermo impostato dalla chiamata di funzione [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) più recente, il sistema regola automaticamente le coordinate in modo che il cursore rimanga all'interno del rettangolo. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Imposta la posizione del cursore nelle coordinate fisiche.<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Consente a un'applicazione di personalizzare i cursori di sistema. Sostituisce il contenuto del cursore di sistema specificato dal *parametro id* con il contenuto del cursore specificato dal *parametro hcur* e quindi elimina *hcur*. <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Visualizza o nasconde il cursore. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Notifiche del cursore



| Nome                                  | Descrizione                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ SETCURSOR**](wm-setcursor.md) | Inviato a una finestra se il mouse fa sì che il cursore si sposti all'interno di una finestra e l'input del mouse non viene acquisito. <br/> |



 

### <a name="cursor-structures"></a>Strutture cursore



| Nome                             | Descrizione                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Contiene informazioni globali sul cursore.<br/> |



 

 

 





