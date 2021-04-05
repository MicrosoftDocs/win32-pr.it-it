---
title: Buffer video
description: Buffer video
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712583"
---
# <a name="video-buffers"></a>Buffer video

I buffer usati con l'acquisizione video si trovano nell'heap di memoria. Il numero di buffer utilizzati in un'operazione di acquisizione può variare e dipende dal valore del membro **wNumVideoRequested** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) e della memoria di sistema disponibile.

È possibile recuperare il valore corrente dei buffer video richiesti usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ WM Cap Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Il numero di buffer video corrente richiesto viene archiviato nel membro **wNumVideoRequested** della struttura **CAPTUREPARMS** . È possibile richiedere la posizione e il numero di buffer aggiornando questo membro, quindi inviando la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ del set**](wm-cap-set-sequence-setup.md) di test WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

 

 




