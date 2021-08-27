---
description: In questo argomento vengono illustrati i timer. Un timer è una routine interna che misura ripetutamente un intervallo specificato, espresso in millisecondi.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd8eced20e7d8b1eca5ec8a952f10798f92f1650db3c77bca76aca756cdd569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110691"
---
# <a name="timers"></a>Timer

Un timer è una routine interna che misura ripetutamente un intervallo specificato, espresso in millisecondi.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                   | Descrizione                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui timer](about-timers.md)       | Viene descritto come creare, identificare, impostare ed eliminare timer.<br/>                                                     |
| [Uso dei timer](using-timers.md)       | Viene illustrato come creare ed eliminare i timer e come usare un timer per intercettare l'input del mouse a intervalli specificati.<br/> |
| [Informazioni di riferimento sul timer](timer-reference.md) | Contiene il riferimento all'API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Funzioni timer



| Nome                           | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Elimina il timer specificato. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Crea un timer con il valore di timeout specificato.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Funzione di callback definita dall'applicazione che elabora i [**messaggi WM \_ TIMER.**](wm-timer.md) Il **tipo TIMERPROC** definisce un puntatore a questa funzione di callback. [*TimerProc è*](/windows/win32/api/winuser/nc-winuser-timerproc) un segnaposto per il nome della funzione definita dall'applicazione. <br/> |



 

### <a name="timer-notifications"></a>Notifiche timer



| Nome                          | Descrizione                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ TIMER**](wm-timer.md) | Inviato alla coda di messaggi del thread di installazione alla scadenza di un timer. Il messaggio viene inviato dalla [**funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) <br/> |



 

 

 
