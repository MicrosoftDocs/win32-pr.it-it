---
title: Finestre di dialogo video
description: Finestre di dialogo video
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE messaggio
- Macro capDlgVideoSource
- WM_CAP_DLG_VIDEOFORMAT messaggio
- Macro capDlgVideoFormat
- WM_CAP_DLG_VIDEODISPLAY messaggio
- macro capDlgVideoDisplay
- WM_CAP_DLG_VIDEOCOMPRESSION messaggio
- Macro capDlgVideoCompression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93674b8ed4e6f6ff594013cc27825aea601cc005fc082ca8a8954b661c1f4317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135559"
---
# <a name="video-dialog-boxes"></a>Finestre di dialogo video

Ogni driver di acquisizione può fornire fino a quattro finestre di dialogo per controllare gli aspetti del processo di digitalizzazione e acquisizione video e per definire gli attributi di compressione usati per ridurre le dimensioni dei dati video. Il contenuto di queste finestre di dialogo è definito dal driver di acquisizione video.

La finestra di dialogo Origine video controlla la selezione dei canali di input video e dei parametri che interessano l'immagine video digitalizzata nel buffer dei fotogrammi. Questa finestra di dialogo enumera i tipi di segnali che collegano l'origine video alla scheda di acquisizione (in genere SVHS e input compositi) e fornisce controlli per modificare la tonalità, il contrasto o la saturazione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md) (o la macro [**capDlgVideoSource).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource)

La finestra di dialogo Formato video controlla la selezione delle dimensioni dei fotogrammi video digitalizzati, la profondità dell'immagine e le opzioni di compressione del video acquisito. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (o la macro [**capDlgVideoFormat).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat)

La finestra di dialogo Visualizzazione video controlla l'aspetto del video sul monitor durante l'acquisizione. I controlli in questa finestra di dialogo non hanno alcun effetto sui dati video digitalizzati, ma potrebbero influire sulla presentazione del segnale digitalizzato. Ad esempio, i dispositivi di acquisizione che supportano la sovrapposizione possono consentire la modifica di tonalità e saturazione, colore chiave o allineamento della sovrimpressione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) (o la macro [**capDlgVideoDisplay).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay)

La finestra di dialogo Compressione video controlla gli attributi di compressione video post-acquisizione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) (o la macro [**capDlgVideoCompression).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression)

 

 




