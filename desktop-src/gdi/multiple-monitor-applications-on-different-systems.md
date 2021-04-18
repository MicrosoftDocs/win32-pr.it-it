---
description: Per fare in modo che l'applicazione monitoraware sia in funzione nei sistemi con e senza supporto per più monitor, collegare l'applicazione a multimon. h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Più applicazioni di monitoraggio su sistemi diversi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5d470861136ac9362d986b8647c86abee7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978527"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Più applicazioni di monitoraggio su sistemi diversi

Per fare in modo che l'applicazione monitoraware sia in funzione nei sistemi con e senza supporto per più monitor, collegare l'applicazione a multimon. h. È anche necessario definire gli \_ \_ Stub di compilazione multimon in un solo file C. Se il sistema non supporta più monitoraggi, restituisce i valori predefiniti di [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) e le funzioni di monitoraggio multiplo agiscono come se fosse presente una sola visualizzazione. Su più sistemi di monitoraggio, l'applicazione funzionerà normalmente.

Poiché le coordinate negative possono essere facilmente rilevate in un sistema a più monitor, è necessario recuperare le coordinate compresse in lParam usando le macro **get \_ X \_ lParam** e **get \_ Y \_ lParam** .

Non usare coordinate negative o coordinate maggiori di SM \_ CXSCREEN e SM \_ CYSCREEN per nascondere una finestra. Le finestre che usano questi limiti per nascondere possono essere visualizzate in un altro monitor. Analogamente, non usare questi limiti per tenere visibile una finestra perché ciò può causare la visualizzazione di una finestra sul monitor primario. È consigliabile riesaminare le applicazioni esistenti per questi problemi. Tuttavia, è possibile ridurre al minimo i problemi nelle applicazioni esistenti eseguendo l'applicazione sul monitor primario o mantenendo il monitor principale nell'angolo superiore sinistro dello schermo virtuale.

Si noti che SM \_ CXMAXTRACK e SM \_ CYMAXTRACK sono definiti per il desktop, non solo un monitor. Potrebbe essere necessario ridefinire Windows con questi limiti.

Una finestra padre o correlata potrebbe non trovarsi nello stesso monitoraggio di una finestra figlio. Per individuare il monitoraggio di una finestra, le applicazioni devono utilizzare la funzione [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) .

Per visualizzare un screen saver su tutti i monitoraggi, collegare con la versione più recente di scrnsave. lib. In caso contrario, il screen saver può essere visualizzato solo sul monitor primario e lasciare invariati gli altri monitor. Gli screen saver collegati con la versione più recente di scrnsave. lib funzioneranno su sistemi di monitoraggio singoli e multipli. Per avere un screen saver diverso su ciascun monitor, usare le funzioni di monitoraggio multiplo per gestire ogni monitoraggio separatamente.

I dispositivi di input che inviano coordinate al sistema in coordinate assolute, ad esempio i tablet, hanno un input di cursore limitato al monitor primario. Per passare dall'input del tablet tra i monitoraggi, vedere le istruzioni riportate nell'OEM.

Per eseguire il mapping dell'input del mouse inviato in coordinate assolute all'intero schermo virtuale, usare la struttura di [**input**](/windows/win32/api/winuser/ns-winuser-input) con MOUSEEVENTF \_ Absolute e MOUSEEVENTF \_ VIRTUALDESKTOP.

La funzione [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funziona bene per più sistemi di monitoraggio. Tuttavia, le funzioni [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)e [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) avranno esito negativo se i contesti di dispositivo di origine e di destinazione sono diversi.

 

 
