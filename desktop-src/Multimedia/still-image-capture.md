---
title: Acquisizione di Still-Image
description: Acquisizione di Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Messaggio WM_CAP_GRAB_FRAME_NOSTOP
- Messaggio WM_CAP_GRAB_FRAME
- capGrabFrameNoStop (macro)
- capGrabFrame (macro)
- Messaggio WM_CAP_EDIT_COPY
- capEditCopy (macro)
- Messaggio WM_CAP_FILE_SAVEDIB
- capFileSaveDIB (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116785"
---
# <a name="still-image-capture"></a>Acquisizione di Still-Image

Se si vuole acquisire un singolo fotogramma come immagine ancora, è possibile usare il messaggio di cattura del frame di acquisizione di [**WM \_ Cap \_ \_ \_**](wm-cap-grab-frame-nostop.md) o la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) o [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) per acquisire l'immagine digitalizzata in un [**buffer frame interno \_ \_ \_**](wm-cap-grab-frame.md) . È possibile bloccare la visualizzazione sull'immagine acquisita usando WM \_ Cap \_ afferra \_ frame. In caso contrario, usare WM \_ Cap \_ Acquisisci \_ frame \_ NOSTOP.

Una volta acquisita, è possibile copiare l'immagine per l'uso da parte di altre applicazioni. È possibile copiare un'immagine dal buffer dei frame negli appunti usando il messaggio di [**\_ copia della \_ modifica \_ di WM Cap**](wm-cap-edit-copy.md) (o la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). È anche possibile copiare l'immagine dal buffer del frame a una bitmap indipendente dal dispositivo (DIB) usando il messaggio [**\_ \_ \_ SAVEDIB**](wm-cap-file-savedib.md) (o la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).

L'applicazione può anche usare i due messaggi di acquisizione con frame singolo per modificare un frame di sequenza in base al frame oppure per creare una sequenza di fotogrammi fotografica di time-lapse.

 

 




