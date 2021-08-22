---
description: In questa sezione vengono illustrate le procedure relative alle finestre. A ogni finestra è associata una routine della finestra che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Routine della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7892c1547d7f5ed1bf5d70a9242e3bb5bc6a3c8e93121470d27ecbd64fb912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548461"
---
# <a name="window-procedures"></a>Routine della finestra

A ogni finestra è associata una routine della finestra, ovvero una funzione che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe. Tutti gli aspetti dell'aspetto e del comportamento di una finestra dipendono dalla risposta della routine della finestra a questi messaggi.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                         | Descrizione                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle routine delle finestre](about-window-procedures.md)       | Vengono illustrate le procedure relative alle finestre. Ogni finestra è un membro di una determinata classe di finestra. La classe window determina la routine di finestra predefinita utilizzata da una singola finestra per elaborare i messaggi.<br/> |
| [Uso di routine di finestra](using-window-procedures.md)       | Viene illustrato come eseguire le attività seguenti associate alle routine della finestra.<br/>                                                                                                                        |
| [Informazioni di riferimento sulla routine della finestra](window-procedure-reference.md) | Contiene il riferimento all'API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Funzioni



| Nome                                     | Descrizione                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Passa le informazioni sul messaggio alla routine della finestra specificata. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Chiama la routine della finestra predefinita per fornire l'elaborazione predefinita per tutti i messaggi di finestra non elaborati da un'applicazione. Questa funzione garantisce che ogni messaggio sia elaborato. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Funzione definita dall'applicazione che elabora i messaggi inviati a una finestra. Il **tipo WNDPROC** definisce un puntatore a questa funzione di callback. [*WindowProc è*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) un segnaposto per il nome della funzione definita dall'applicazione. <br/>                                                            |



 

 

 
