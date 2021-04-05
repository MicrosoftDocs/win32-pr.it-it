---
title: Cursori
description: In questa sezione vengono illustrati i cursori che sono immagini di piccole dimensioni il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- risorse, cursori
- cursori, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044795"
---
# <a name="cursors"></a>Cursori

Un cursore è una piccola immagine il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball. Nella parte restante di questa panoramica il termine mouse fa riferimento a qualsiasi dispositivo di puntamento.

Quando l'utente sposta il mouse, il sistema sposta di conseguenza il cursore. Le funzioni di cursore consentono alle applicazioni di creare, caricare, visualizzare, animare, spostare, limitare ed eliminare i cursori.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                     | Descrizione                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Informazioni sui cursori](about-cursors.md)       | Vengono illustrati i cursori standard.<br/>                    |
| [Uso dei cursori](using-cursors.md)       | Viene illustrato come eseguire attività correlate ai cursori.<br/> |
| [Riferimento cursore](cursor-reference.md) | Contiene il riferimento all'API.<br/>                        |



 

### <a name="cursor-functions"></a>Funzioni per i cursori



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Consente di limitare il cursore a un'area rettangolare sullo schermo. Se una posizione successiva del cursore (impostata dalla funzione [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) o dal mouse) si trova all'esterno del rettangolo, il sistema regola automaticamente la posizione per mantenere il cursore all'interno dell'area rettangolare. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Copia il cursore specificato. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Crea un cursore con le dimensioni, gli schemi di bit e l'area sensibile specificati. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Elimina un cursore e libera la memoria occupata dal cursore. Non usare questa funzione per eliminare definitivamente un cursore condiviso.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Recupera le coordinate dello schermo dell'area rettangolare in cui è confinato il cursore. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Recupera un handle per il cursore corrente. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Recupera le informazioni sul cursore globale.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Recupera la posizione del cursore, in coordinate dello schermo.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Recupera la posizione del cursore nelle coordinate fisiche.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Carica la risorsa di cursore specificata dall'eseguibile (. File EXE) associato a un'istanza dell'applicazione.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Crea un cursore in base ai dati contenuti in un file. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Imposta la forma del cursore. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Sposta il cursore sulle coordinate dello schermo specificate. Se le nuove coordinate non si trovano all'interno del rettangolo dello schermo impostato dalla chiamata di funzione [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) più recente, il sistema regola automaticamente le coordinate in modo che il cursore rimanga all'interno del rettangolo. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Imposta la posizione del cursore nelle coordinate fisiche.<br/>                                                                                                                                                                                                                                    |
| [**Funzione SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Consente a un'applicazione di personalizzare i cursori di sistema. Sostituisce il contenuto del cursore di sistema specificato dal parametro *ID* con il contenuto del cursore specificato dal parametro *HCur* , quindi Elimina *HCur*. <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Consente di visualizzare o nascondere il cursore. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Notifiche del cursore



| Nome                                  | Descrizione                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_cursore WM**](wm-setcursor.md) | Inviato a una finestra se il mouse determina lo spostamento del cursore all'interno di una finestra e l'input del mouse non viene acquisito. <br/> |



 

### <a name="cursor-structures"></a>Strutture di cursori



| Nome                             | Descrizione                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Contiene informazioni globali sui cursori.<br/> |



 

 

 





