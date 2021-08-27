---
title: Recupero dello stato di una finestra di acquisizione
description: Recupero dello stato di una finestra di acquisizione
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- Macro capGetStatus
- Struttura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038371"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Recupero dello stato di una finestra di acquisizione

Nell'esempio seguente viene utilizzata la funzione [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) per impostare le dimensioni della finestra di acquisizione sulle dimensioni complessive del flusso video in ingresso in base alle informazioni restituite dalla macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) nella [**struttura CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 