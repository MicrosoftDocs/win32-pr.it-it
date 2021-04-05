---
title: Recupero e impostazione del formato video
description: Recupero e impostazione del formato video
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- capGetVideoFormat (macro)
- capGetVideoFormatSize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872486"
---
# <a name="obtaining-and-setting-the-video-format"></a>Recupero e impostazione del formato video

La struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) è di lunghezza variabile per supportare i formati di dati standard e compressi. Poiché questa struttura ha una lunghezza variabile, le applicazioni devono sempre eseguire una query sulle dimensioni della struttura e allocare memoria prima di recuperare il formato video corrente. Nell'esempio seguente viene utilizzata la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) per recuperare le dimensioni del buffer e viene quindi chiamata la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) per recuperare il formato video corrente.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Le applicazioni possono usare la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (o il messaggio [**\_ \_ \_ VIDEOFORMAT WM set**](wm-cap-set-videoformat.md) ) per inviare una struttura di intestazione [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) alla finestra di acquisizione. Poiché i formati video sono specifici del dispositivo, l'applicazione deve controllare il valore restituito per determinare se il formato è stato accettato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 