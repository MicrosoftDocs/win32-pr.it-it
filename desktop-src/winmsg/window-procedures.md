---
description: In questa sezione vengono descritte le procedure di finestra. A ogni finestra è associata una routine di finestra che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Routine della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317861"
---
# <a name="window-procedures"></a>Routine della finestra

A ogni finestra è associata una routine della finestra, una funzione che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe. Tutti gli aspetti dell'aspetto e del comportamento di una finestra dipendono dalla risposta della routine della finestra a questi messaggi.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                         | Descrizione                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle routine della finestra](about-window-procedures.md)       | Descrive le routine della finestra. Ogni finestra è un membro di una particolare classe di finestra. La classe Window determina la routine della finestra predefinita utilizzata da una singola finestra per elaborare i messaggi.<br/> |
| [Utilizzo delle routine della finestra](using-window-procedures.md)       | Viene illustrato come eseguire le attività seguenti associate alle routine della finestra.<br/>                                                                                                                        |
| [Guida di riferimento alle procedure della finestra](window-procedure-reference.md) | Contiene il riferimento all'API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Funzioni



| Nome                                     | Descrizione                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Passa informazioni sul messaggio alla routine della finestra specificata. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Chiama la routine della finestra predefinita per fornire l'elaborazione predefinita per tutti i messaggi della finestra che un'applicazione non elabora. Questa funzione garantisce che ogni messaggio venga elaborato. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Funzione definita dall'applicazione che elabora i messaggi inviati a una finestra. Il tipo **WndProc** definisce un puntatore a questa funzione di callback. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) è un segnaposto per il nome della funzione definita dall'applicazione. <br/>                                                            |



 

 

 
