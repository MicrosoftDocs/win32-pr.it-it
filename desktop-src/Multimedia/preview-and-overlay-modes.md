---
title: Modalità anteprima e sovrapposizione
description: Modalità anteprima e sovrapposizione
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Messaggio WM_CAP_SET_PREVIEW
- capPreview (macro)
- Messaggio WM_CAP_SET_PREVIEWRATE
- capPreviewRate (macro)
- Messaggio WM_CAP_SET_SCALE
- capPreviewScale (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955357"
---
# <a name="preview-and-overlay-modes"></a>Modalità anteprima e sovrapposizione

Un driver di acquisizione può implementare due metodi per la visualizzazione di un flusso video in entrata, ovvero la modalità anteprima e la modalità sovrimpressione. Se un driver di acquisizione implementa entrambi i metodi, l'utente può scegliere il metodo da usare.

La modalità di anteprima trasferisce i frame digitalizzati dall'hardware di acquisizione alla memoria di sistema e quindi Visualizza i frame digitalizzati nella finestra di acquisizione usando le funzioni GDI (Graphics Device Interface). Le applicazioni potrebbero ridurre la frequenza di anteprima quando la finestra padre perde lo stato attivo e aumentare la frequenza di anteprima quando la finestra padre ottiene lo stato attivo. Questa azione migliora la velocità di risposta generale del sistema perché l'operazione di anteprima è a elevato utilizzo di processori.

Sono disponibili tre messaggi per controllare l'operazione di anteprima.

-   Usare il messaggio di [**Anteprima di WM \_ Cap \_ set \_**](wm-cap-set-preview.md) per abilitare o disabilitare la modalità di anteprima inviando (o la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) a una finestra di acquisizione.
-   Usare il [**messaggio \_ \_ \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) per impostare la frequenza di visualizzazione dei frame in modalità di anteprima
-   Per abilitare o disabilitare il ridimensionamento del video di anteprima, usare il messaggio [**WM \_ Cap \_ set \_ scale**](wm-cap-set-scale.md) (o la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ).

Quando l'anteprima e la scalabilità sono entrambe abilitate, il fotogramma video acquisito viene allungato alle dimensioni della finestra di acquisizione. L'abilitazione della modalità di anteprima Disabilita automaticamente la modalità overlay.

La modalità sovrimpressione è una funzione hardware che consente di visualizzare il contenuto del buffer di acquisizione sul monitoraggio senza utilizzare risorse della CPU. È possibile abilitare e disabilitare la modalità overlay inviando il messaggio di [**\_ \_ \_ sovrimpressione set di WM**](wm-cap-set-overlay.md) (o la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) a una finestra di acquisizione. L'abilitazione della modalità sovrapposizione Disabilita automaticamente la modalità di anteprima.

È anche possibile impostare la posizione di scorrimento del fotogramma video nell'area client della finestra di acquisizione per la modalità di anteprima o la modalità di sovrapposizione inviando il messaggio di [**scorrimento di WM \_ Cap \_ set \_**](wm-cap-set-scroll.md) (o la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) a una finestra di acquisizione.

 

 




