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
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="e2b48-103">Più metriche del sistema di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="e2b48-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="e2b48-104">La funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce i valori per il monitor primario, ad eccezione di SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, che fanno riferimento all'intero desktop.</span><span class="sxs-lookup"><span data-stu-id="e2b48-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="e2b48-105">Le metriche seguenti sono le stesse per tutti i driver di dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON.</span><span class="sxs-lookup"><span data-stu-id="e2b48-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="e2b48-106">Le funzionalità di visualizzazione seguenti sono le stesse per tutti i monitoraggi: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span><span class="sxs-lookup"><span data-stu-id="e2b48-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="e2b48-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) dispone inoltre di costanti che fanno riferimento solo a un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="e2b48-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="e2b48-108">SM \_ XVIRTUALSCREEN e SM \_ YVIRTUALSCREEN identificano l'angolo superiore sinistro dello schermo virtuale, SM \_ CXVIRTUALSCREEN e SM \_ CYVIRTUALSCREEN sono le misurazioni verticali e orizzontali dello schermo virtuale, SM \_ CMONITORS è il numero di monitoraggi collegati al desktop e SM \_ SAMEDISPLAYFORMAT indica se tutti i monitoraggi sul desktop hanno lo stesso formato di colore.</span><span class="sxs-lookup"><span data-stu-id="e2b48-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="e2b48-109">Per ottenere informazioni su un singolo monitor di visualizzazione o su tutti i monitoraggi di visualizzazione in un desktop, usare EnumDisplayMonitors.</span><span class="sxs-lookup"><span data-stu-id="e2b48-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="e2b48-110">Il rettangolo della finestra desktop restituito da [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) è sempre uguale al rettangolo del monitor primario, per compatibilità con le applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="e2b48-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="e2b48-111">Quindi, il risultato di</span><span class="sxs-lookup"><span data-stu-id="e2b48-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="e2b48-112">sarà:</span><span class="sxs-lookup"><span data-stu-id="e2b48-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="e2b48-113">Per modificare l'area di lavoro di un monitoraggio, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA e *pvParam* che punta a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) presente sul monitor desiderato.</span><span class="sxs-lookup"><span data-stu-id="e2b48-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="e2b48-114">Se *pvParam* è **null**, l'area di lavoro del monitor primario viene modificata.</span><span class="sxs-lookup"><span data-stu-id="e2b48-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="e2b48-115">L'uso \_ di SPI GETWORKAREA restituisce sempre l'area di lavoro del monitor primario.</span><span class="sxs-lookup"><span data-stu-id="e2b48-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="e2b48-116">Per ottenere l'area di lavoro di un monitoraggio diverso dal monitoraggio primario, chiamare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="e2b48-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
