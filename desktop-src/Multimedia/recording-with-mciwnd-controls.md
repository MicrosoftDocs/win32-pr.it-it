---
title: Registrazione con controlli MCIWnd
description: Registrazione con controlli MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Funzione MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805561"
---
# <a name="recording-with-mciwnd-controls"></a>Registrazione con controlli MCIWnd

L'esempio seguente registra l'audio della forma d'onda usando i controlli predefiniti della finestra MCIWnd. Nell'esempio viene creata una finestra MCIWnd usando lo stile della finestra MCIWNDF RECORD con la \_ [**funzione MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) per aggiungere un **pulsante Record** alla barra degli strumenti. La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica che un nuovo file è associato alla finestra MCIWnd e che un dispositivo waveform-audio fornirà il contenuto. Un secondo comando di menu, IDM SAVEMCIWND, consente all'utente di salvare la registrazione e selezionare un nome file usando la \_ macro [**MCIWndSaveDialog.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




