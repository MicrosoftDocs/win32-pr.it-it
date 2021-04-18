---
title: Finestre di dialogo video
description: Finestre di dialogo video
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Messaggio WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource (macro)
- Messaggio WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat (macro)
- Messaggio WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay (macro)
- Messaggio WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297892"
---
# <a name="video-dialog-boxes"></a>Finestre di dialogo video

Ogni driver di acquisizione può fornire fino a quattro finestre di dialogo per controllare gli aspetti del processo di acquisizione e digitalizzazione dei video e per definire gli attributi di compressione usati per ridurre le dimensioni dei dati video. Il contenuto di queste finestre di dialogo viene definito dal driver di acquisizione video.

La finestra di dialogo origine video consente di controllare la selezione dei canali e dei parametri di input video che interessano l'immagine video che viene digitata nel buffer del frame. Questa finestra di dialogo enumera i tipi di segnali che connettono l'origine video alla scheda di acquisizione (in genere SVHS e input compositi) e fornisce controlli per modificare la tonalità, il contrasto o la saturazione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOSOURCE di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videosource.md) (o la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).

La finestra di dialogo Formato video controlla la selezione delle dimensioni del fotogramma video digitalizzato e la profondità dell'immagine e le opzioni di compressione del video acquisito. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOFORMAT di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videoformat.md) (o la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).

La finestra di dialogo visualizzazione video consente di controllare l'aspetto del video nel monitoraggio durante l'acquisizione. I controlli in questa finestra di dialogo non hanno alcun effetto sui dati video digitati, ma potrebbero influire sulla presentazione del segnale digitalizzato. Ad esempio, i dispositivi di acquisizione che supportano la sovrapposizione possono consentire la modifica di tonalità, saturazione, colore della chiave o allineamento della sovrimpressione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEODISPLAY di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videodisplay.md) (o la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).

La finestra di dialogo compressione video controlla gli attributi di compressione video post-acquisizione. Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videocompression.md) (o la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).

 

 




