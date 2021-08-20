---
description: La funzione GetSystemMetrics restituisce i valori per il monitoraggio primario, ad eccezione di SM \_ CXMAXTRACK e SM CYMAXTRACK, che fanno riferimento \_ all'intero desktop.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Metriche di sistema con più monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3143562116561bb220bc6f0b5ecfa4ad8f5103c3e4532cab639c4c2b37f59467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037709"
---
# <a name="multiple-monitor-system-metrics"></a>Metriche di sistema con più monitor

La [**funzione GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce i valori per il monitoraggio primario, ad eccezione di SM \_ CXMAXTRACK e SM CYMAXTRACK, che fanno riferimento \_ all'intero desktop. Le metriche seguenti sono le stesse per tutti i driver di dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Le funzionalità di visualizzazione seguenti sono le stesse per tutti i monitoraggi: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) include anche costanti che fanno riferimento solo a un sistema a più monitor. SM CXVIRTUALSCREEN e SM YVIRTUALSCREEN identificano l'angolo superiore sinistro dello schermo \_ \_ virtuale, SM \_ CXVIRTUALSCREEN e SM \_ CYVIRTUALSCREEN sono le misurazioni verticali e orizzontali dello schermo virtuale, SM CMONITORS è il numero di monitor collegati al desktop e \_ SM \_ SAMEDISPLAYFORMAT indica se tutti i monitor sul desktop hanno lo stesso formato di colore.

Per ottenere informazioni su un singolo monitor di visualizzazione o su tutti i monitor di visualizzazione in un desktop, usare EnumDisplayMonitors. Il rettangolo della finestra desktop restituito da [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) è sempre uguale al rettangolo del monitoraggio primario, per la compatibilità con le applicazioni esistenti. Di conseguenza, il risultato di


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



Per modificare l'area di lavoro di un monitoraggio, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA e *pvParam* che puntano a una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) che si trova nel monitoraggio desiderato. Se *pvParam* è **NULL,** l'area di lavoro del monitoraggio primario viene modificata. \_L'uso di SPI GETWORKAREA restituisce sempre l'area di lavoro del monitoraggio primario. Per ottenere l'area di lavoro di un monitoraggio diverso dal monitoraggio primario, chiamare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
