---
description: Per fare in modo che l'applicazione monitoraware funzioni sia nei sistemi con e senza supporto di più monitor, collegare l'applicazione a Multimon.h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Più applicazioni di monitoraggio in sistemi diversi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037719"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Più applicazioni di monitoraggio in sistemi diversi

Per fare in modo che l'applicazione monitoraware funzioni sia nei sistemi con e senza supporto di più monitor, collegare l'applicazione a Multimon.h. È anche necessario definire STUBS COMPILE \_ MULTIMON \_ in esattamente un file C. Se il sistema non supporta più monitor, restituisce i valori predefiniti da [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) e le funzioni di monitoraggio multiple agiscono come se fosse presente una sola visualizzazione. In più sistemi di monitoraggio, l'applicazione funzionerà normalmente.

Poiché le coordinate negative possono verificarsi facilmente in un sistema multimonitor, è consigliabile recuperare le coordinate che vengono imballate in lParam usando le macro **GET \_ X \_ LPARAM** e **GET Y \_ \_ LPARAM.**

Non usare coordinate negative o coordinate maggiori di SM \_ CXSCREEN e SM \_ CYSCREEN per nascondere una finestra. Windows che usano questi limiti per nascondere possono essere visualizzati in un altro monitoraggio. Analogamente, non usare questi limiti per mantenere visibile una finestra perché ciò può causare lo snap di una finestra al monitoraggio primario. È meglio rieseminare le applicazioni esistenti per questi problemi. Tuttavia, è possibile ridurre al minimo i problemi nelle applicazioni esistenti eseguendo l'applicazione sul monitoraggio primario o mantenendo il monitoraggio primario nell'angolo superiore sinistro dello schermo virtuale.

Si noti che SM CXMAXTRACK e SM CYMAXTRACK sono definiti per il \_ \_ desktop, non un solo monitoraggio. Windows usare questi limiti potrebbe essere necessario ridefinire.

Una finestra padre o correlata potrebbe non essere sullo stesso monitor di una finestra figlio. Per individuare il monitoraggio di una finestra, le applicazioni devono usare la [**funzione MonitorFromWindow.**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)

Per visualizzare un screen saver su tutti i monitoraggi, collegarsi alla versione più recente di Scrnsave.lib. In caso contrario, screen saver solo sul monitor primario e lasciare invariati gli altri monitoraggi. Gli screen saver collegati alla versione più recente di Scrnsave.lib funzioneranno sia in sistemi a monitor singolo che a più monitor. Per avere un'screen saver diversa in ogni monitoraggio, usare le funzioni di monitoraggio multiple per gestire ogni monitoraggio separatamente.

I dispositivi di input che recapitano le coordinate al sistema in coordinate assolute, ad esempio i tablet, hanno l'input del cursore limitato al monitor primario. Per cambiare l'input del tablet da un monitor all'altro, vedere le istruzioni dell'OEM.

Per eseguire il mapping dell'input del mouse inviato in coordinate assolute all'intero schermo virtuale, usare la struttura [**INPUT**](/windows/win32/api/winuser/ns-winuser-input) con MOUSEEVENTF \_ ABSOLUTE e MOUSEEVENTF \_ VIRTUALDESKTOP.

La [**funzione BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funziona bene per più sistemi di monitoraggio. Tuttavia, le [**funzioni MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)e [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) avranno esito negativo se i contesti di dispositivo di origine e di destinazione sono diversi.

 

 
