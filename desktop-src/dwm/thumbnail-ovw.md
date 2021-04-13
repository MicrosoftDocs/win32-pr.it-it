---
title: Panoramica dell'anteprima di DWM
description: Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprime delle finestre dell'applicazione.
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
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104559704"
---
# <a name="dwm-thumbnail-overview"></a>Panoramica dell'anteprima di DWM

Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprime delle finestre dell'applicazione. Queste non sono snapshot statiche di una finestra, ma sono invece dinamiche, connessioni costanti tra una finestra di origine di anteprima e un percorso in una finestra di destinazione che riceve il rendering dell'anteprima in tempo reale. In questo modo è possibile visualizzare rapidamente le applicazioni in esecuzione passando il puntatore del mouse sull'applicazione sulla barra delle applicazioni o utilizzando il movimento ALT + TAB per visualizzare e passare rapidamente a un'applicazione.

Nell'immagine seguente viene illustrata l'anteprima di Windows Vista Live visualizzata quando si passa il mouse sull'applicazione sulla barra delle applicazioni.

![Screenshot che mostra l'anteprima D W M visualizzata quando si passa il puntatore del mouse su un'app nella barra delle applicazioni.](images/dwm-livethumbnail.png)

Nell'immagine seguente viene illustrata la versione di Windows Vista (ALT + TAB) abilitata da DWM.

![screenshot della pagina ALT-TAB abilitata per DWM](images/dwm-flip.png)

> [!Note]  
> Le anteprime di DWM non consentono agli sviluppatori di creare applicazioni come la funzionalità Windows Vista Flip3D (WINKEY-TAB). Il rendering delle anteprime viene eseguito direttamente nella finestra di destinazione in 2D.

 

## <a name="dwm-thumbnail-relationships"></a>Relazioni di anteprima di DWM

Per visualizzare le anteprime nell'applicazione, è innanzitutto necessario stabilire una relazione tra una finestra di origine e una finestra di destinazione. Questa operazione viene eseguita chiamando la funzione [**funzionalità DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .

[**Funzionalità DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) non esegue il rendering di un'anteprima nella finestra di destinazione, ma crea semplicemente la relazione e fornisce l'handle di anteprima. L'anteprima viene sottoposta a rendering dopo che sono state impostate le [**proprietà di \_ Anteprima \_ di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) e la funzione [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) è stata chiamata. Le chiamate successive a **DwmUpdateThumbnailProperties** aggiornano l'anteprima con un nuovo set di proprietà. DWM fornisce anche la funzione helper [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) per ottenere le dimensioni della finestra di origine dall'anteprima.

Per terminare una relazione di anteprima, chiamare la funzione [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .

Nell'esempio seguente viene illustrato come creare un releationship con il desktop di Windows e visualizzarlo in un'applicazione.


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

 

 




