---
title: Modalità di anteprima e sovrimpressione
description: Modalità di anteprima e sovrimpressione
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW messaggio
- Macro capPreview
- WM_CAP_SET_PREVIEWRATE messaggio
- Macro capPreviewRate
- WM_CAP_SET_SCALE messaggio
- Macro capPreviewScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9359b1380c5d6efe049bc4bea52a08a92f880af5d35558f4e65e21070f20c0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372370"
---
# <a name="preview-and-overlay-modes"></a>Modalità di anteprima e sovrimpressione

Un driver di acquisizione può implementare due metodi per la visualizzazione di un flusso video in ingresso: la modalità di anteprima e la modalità di sovrapposizione. Se un driver di acquisizione implementa entrambi i metodi, l'utente può scegliere il metodo da usare.

La modalità di anteprima trasferisce i fotogrammi digitalizzati dall'hardware di acquisizione alla memoria di sistema e quindi visualizza i fotogrammi digitalizzati nella finestra di acquisizione usando le funzioni GDI (Graphics Device Interface). Le applicazioni potrebbero ridurre la frequenza di anteprima quando la finestra padre perde lo stato attivo e aumentare la frequenza di anteprima quando la finestra padre ottiene lo stato attivo. Questa azione migliora la velocità di risposta generale del sistema perché l'operazione di anteprima richiede un utilizzo intensivo del processore.

Sono disponibili tre messaggi per controllare l'operazione di anteprima.

-   Usare il [**messaggio WM CAP SET \_ \_ \_ PREVIEW**](wm-cap-set-preview.md) per abilitare o disabilitare la modalità di anteprima inviando (o la macro [**capPreview)**](/windows/desktop/api/Vfw/nf-vfw-cappreview) a una finestra di acquisizione.
-   Usare il [**messaggio WM CAP SET \_ \_ \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate)**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) per impostare la frequenza di visualizzazione dei fotogrammi in modalità di anteprima
-   Usare il [**messaggio WM CAP SET \_ \_ \_ SCALE**](wm-cap-set-scale.md) (o la macro [**capPreviewScale)**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) per abilitare o disabilitare il ridimensionamento del video di anteprima.

Quando l'anteprima e il ridimensionamento sono entrambi abilitati, il fotogramma video acquisito viene adattato alle dimensioni della finestra di acquisizione. L'abilitazione della modalità di anteprima disabilita automaticamente la modalità di sovrapposizione.

La modalità sovrimpressione è una funzione hardware che visualizza il contenuto del buffer di acquisizione sul monitor senza usare le risorse della CPU. È possibile abilitare e disabilitare la modalità di sovrapposizione inviando il messaggio [**WM \_ CAP SET \_ \_ OVERLAY**](wm-cap-set-overlay.md) (o la macro [**capOverlay)**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) a una finestra di acquisizione. L'abilitazione della modalità di sovrapposizione disabilita automaticamente la modalità di anteprima.

È anche possibile impostare la posizione di scorrimento del fotogramma video all'interno dell'area client della finestra di acquisizione per la modalità di anteprima o di sovrapposizione inviando il messaggio [**WM \_ CAP SET \_ \_ SCROLL**](wm-cap-set-scroll.md) (o la macro [**capSetScrollPos)**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) a una finestra di acquisizione.

 

 




