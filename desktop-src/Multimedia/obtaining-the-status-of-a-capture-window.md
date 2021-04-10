---
title: Ottenere lo stato di una finestra di acquisizione
description: Ottenere lo stato di una finestra di acquisizione
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus (macro)
- Struttura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956408"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Ottenere lo stato di una finestra di acquisizione

Nell'esempio seguente viene usata la funzione [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) per impostare la dimensione della finestra di acquisizione sulle dimensioni complessive del flusso video in arrivo in base alle informazioni restituite dalla macro [**CapGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) nella struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 