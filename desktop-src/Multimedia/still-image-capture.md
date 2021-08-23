---
title: Still-Image capture
description: Still-Image capture
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP messaggio
- WM_CAP_GRAB_FRAME messaggio
- Macro capGrabFrameNoStop
- Macro capGrabFrame
- WM_CAP_EDIT_COPY messaggio
- Macro capEditCopy
- WM_CAP_FILE_SAVEDIB messaggio
- Macro capFileSaveDIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0d822292489be4093998ac18d70191dbe2b87327a33adaba26e8442420d93b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688601"
---
# <a name="still-image-capture"></a>Still-Image capture

Se vuoi acquisire un singolo frame come immagine fissa, puoi usare il messaggio [**WM CAP GRAB FRAME \_ \_ \_ \_ NOSTOP**](wm-cap-grab-frame-nostop.md) o [**WM CAP GRAB \_ \_ \_ FRAME**](wm-cap-grab-frame.md) (o la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) o [**capGrabFrame)**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) per acquisire l'immagine digitalizzata in un buffer di frame interno. È possibile bloccare la visualizzazione nell'immagine acquisita usando WM \_ CAP \_ GRAB \_ FRAME. In caso contrario, usare WM \_ CAP \_ GRAB FRAME \_ \_ NOSTOP.

Dopo l'acquisizione, è possibile copiare l'immagine per l'uso da parte di altre applicazioni. È possibile copiare un'immagine dal buffer dei frame negli Appunti usando il messaggio [**WM \_ CAP EDIT \_ \_ COPY**](wm-cap-edit-copy.md) (o la macro [**capEditCopy).**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) È anche possibile copiare l'immagine dal buffer dei frame a una bitmap indipendente dal dispositivo (DIB) usando il messaggio [**WM \_ CAP FILE \_ \_ SAVEDIB**](wm-cap-file-savedib.md) (o la macro [**capFileSaveDIB).**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib)

L'applicazione può anche usare i due messaggi di acquisizione a frame singolo per modificare una sequenza fotogramma per fotogramma o per creare una sequenza di sequenza temporale.

 

 




