---
title: Interazione della finestra Parent-Child
description: Interazione della finestra Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725863"
---
# <a name="parent-child-window-interaction"></a>Interazione della finestra Parent-Child

Alcuni messaggi a livello di sistema, ad esempio [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), vengono inviati solo alle finestre di primo livello e sovrapposte. Se una finestra di acquisizione è una finestra figlio, è necessario che l'elemento padre inoltri questi messaggi.

Analogamente, se la finestra padre cambia dimensione, potrebbe essere necessario inviare messaggi di notifica alla finestra di acquisizione. Viceversa, se le dimensioni del video acquisito cambiano, la finestra di acquisizione potrebbe dover inviare messaggi di notifica alla finestra padre. Il modo più semplice per gestire questo problema consiste nel lasciare sempre le dimensioni della finestra di acquisizione uguali alle dimensioni del flusso video acquisito, inviando una notifica all'elemento padre ogni volta che queste dimensioni cambiano.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisisci Windows](capture-windows.md)
</dt> </dl>

 

 