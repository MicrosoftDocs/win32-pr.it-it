---
description: La funzione GetSystemMetrics restituisce i valori per il monitor primario, ad eccezione di SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, che fanno riferimento all'intero desktop.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Più metriche del sistema di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130755"
---
# <a name="multiple-monitor-system-metrics"></a>Più metriche del sistema di monitoraggio

La funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce i valori per il monitor primario, ad eccezione di SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, che fanno riferimento all'intero desktop. Le metriche seguenti sono le stesse per tutti i driver di dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Le funzionalità di visualizzazione seguenti sono le stesse per tutti i monitoraggi: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) dispone inoltre di costanti che fanno riferimento solo a un sistema a più monitor. SM \_ XVIRTUALSCREEN e SM \_ YVIRTUALSCREEN identificano l'angolo superiore sinistro dello schermo virtuale, SM \_ CXVIRTUALSCREEN e SM \_ CYVIRTUALSCREEN sono le misurazioni verticali e orizzontali dello schermo virtuale, SM \_ CMONITORS è il numero di monitoraggi collegati al desktop e SM \_ SAMEDISPLAYFORMAT indica se tutti i monitoraggi sul desktop hanno lo stesso formato di colore.

Per ottenere informazioni su un singolo monitor di visualizzazione o su tutti i monitoraggi di visualizzazione in un desktop, usare EnumDisplayMonitors. Il rettangolo della finestra desktop restituito da [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) è sempre uguale al rettangolo del monitor primario, per compatibilità con le applicazioni esistenti. Quindi, il risultato di


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



sarà:


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Per modificare l'area di lavoro di un monitoraggio, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA e *pvParam* che punta a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) presente sul monitor desiderato. Se *pvParam* è **null**, l'area di lavoro del monitor primario viene modificata. L'uso \_ di SPI GETWORKAREA restituisce sempre l'area di lavoro del monitor primario. Per ottenere l'area di lavoro di un monitoraggio diverso dal monitoraggio primario, chiamare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
