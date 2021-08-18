---
title: Panoramica dell'anteprima DWM
description: Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprima delle finestre dell'applicazione.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gestione finestre desktop (DWM), anteprime
- DWM (Gestione finestre desktop), anteprime
- Gestione finestre desktop (DWM), relazioni di anteprima
- DWM (Gestione finestre desktop), relazioni di anteprima
- anteprime in miniatura
- relazioni di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b333d84496828c451ff6e0eb7dbf3a86f91d629623d9939f66e874cfa82ee47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279773"
---
# <a name="dwm-thumbnail-overview"></a>Panoramica dell'anteprima DWM

Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprima delle finestre dell'applicazione. Non si tratta di snapshot statici di una finestra, ma di connessioni dinamiche e costanti tra una finestra di origine dell'anteprima e una posizione in una finestra di destinazione che riceve il rendering dell'anteprima dinamica. In questo modo è possibile visualizzare rapidamente le applicazioni in esecuzione passando il puntatore del mouse sull'applicazione sulla barra delle applicazioni o usando il movimento ALT+TAB per visualizzare e passare rapidamente a un'applicazione.

L'immagine seguente illustra l'anteprima Windows vista live visualizzata quando si passa il mouse sull'applicazione sulla barra delle applicazioni.

![Screenshot che mostra l'anteprima di D W M visualizzata quando si passa il mouse su un'app nella barra delle applicazioni.](images/dwm-livethumbnail.png)

L'immagine seguente illustra la Windows Vista Flip (ALT-TAB) abilitata da DWM.

![Screenshot della scheda ALT+TAB abilitata per dwm](images/dwm-flip.png)

> [!Note]  
> Le anteprime DWM non consentono agli sviluppatori di creare applicazioni come la Windows Vista Flip3D (WINKEY-TAB). Il rendering delle anteprime viene eseguito direttamente nella finestra di destinazione in 2D.

 

## <a name="dwm-thumbnail-relationships"></a>Relazioni di anteprima DWM

Per visualizzare le anteprime nell'applicazione, è innanzitutto necessario stabilire una relazione tra una finestra di origine e una finestra di destinazione. Questa operazione viene eseguita chiamando la [**funzione DwmRegisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail)

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) non esegue il rendering di un'anteprima nella finestra di destinazione, ma crea semplicemente la relazione e fornisce l'handle di anteprima. Il rendering dell'anteprima viene eseguito dopo l'impostazione di PROPRIETÀ THUMBNAIL [**DWM \_ \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) e la chiamata della funzione [**DwmUpdateThumbnailProperties.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) Le chiamate successive a **DwmUpdateThumbnailProperties** aggiornano l'anteprima con un nuovo set di proprietà. DWM fornisce anche la funzione helper [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) per ottenere le dimensioni della finestra di origine dall'anteprima.

Per terminare una relazione di anteprima, chiamare [**la funzione DwmUnregisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail)

L'esempio seguente illustra come creare una nuova distribuzione con il desktop Windows e visualizzarla in un'applicazione.


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari di Gestione finestre desktop](dwm-overview.md)
</dt> <dt>

[Abilitare e controllare la composizione DWM](composition-ovw.md)
</dt> <dt>

[Considerazioni sulle prestazioni e procedure consigliate](bestpractices-ovw.md)
</dt> </dl>

 

 




