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
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="9d9e5-105">Recupero e impostazione del formato video</span><span class="sxs-lookup"><span data-stu-id="9d9e5-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="9d9e5-106">La struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) è di lunghezza variabile per supportare i formati di dati standard e compressi.</span><span class="sxs-lookup"><span data-stu-id="9d9e5-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="9d9e5-107">Poiché questa struttura ha una lunghezza variabile, le applicazioni devono sempre eseguire una query sulle dimensioni della struttura e allocare memoria prima di recuperare il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="9d9e5-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="9d9e5-108">Nell'esempio seguente viene utilizzata la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) per recuperare le dimensioni del buffer e viene quindi chiamata la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) per recuperare il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="9d9e5-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="9d9e5-109">Le applicazioni possono usare la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (o il messaggio [**\_ \_ \_ VIDEOFORMAT WM set**](wm-cap-set-videoformat.md) ) per inviare una struttura di intestazione [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) alla finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9d9e5-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="9d9e5-110">Poiché i formati video sono specifici del dispositivo, l'applicazione deve controllare il valore restituito per determinare se il formato è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="9d9e5-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d9e5-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d9e5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d9e5-112">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9d9e5-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 