---
description: In questo argomento vengono illustrati i timer. Un timer è una routine interna che misura ripetutamente un intervallo specificato, in millisecondi.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318354"
---
# <a name="timers"></a>Timer

Un timer è una routine interna che misura ripetutamente un intervallo specificato, in millisecondi.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                   | Descrizione                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui timer](about-timers.md)       | Viene descritto come creare, identificare, impostare ed eliminare i timer.<br/>                                                     |
| [Utilizzo di timer](using-timers.md)       | Viene illustrato come creare ed eliminare i timer e come utilizzare un timer per intercettare l'input del mouse a intervalli specificati.<br/> |
| [Riferimento timer](timer-reference.md) | Contiene il riferimento all'API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Funzioni timer



| Nome                           | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Elimina il timer specificato. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Crea un timer con il valore di timeout specificato.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Funzione di callback definita dall'applicazione che elabora i messaggi del [**\_ timer WM**](wm-timer.md) . Il tipo **TIMERPROC** definisce un puntatore a questa funzione di callback. [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) è un segnaposto per il nome della funzione definita dall'applicazione. <br/> |



 

### <a name="timer-notifications"></a>Notifiche timer



| Nome                          | Descrizione                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_timer WM**](wm-timer.md) | Inserito nella coda di messaggi del thread di installazione quando scade un timer. Il messaggio viene inserito dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . <br/> |



 

 

 
