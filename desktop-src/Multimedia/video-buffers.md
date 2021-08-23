---
title: Buffer video
description: Buffer video
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687691"
---
# <a name="video-buffers"></a>Buffer video

I buffer usati con l'acquisizione video si trovano nell'heap di memoria. Il numero di buffer usati in un'operazione di acquisizione può variare e dipendere dal valore del membro **wNumVideoRequested** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) e della memoria di sistema disponibile.

È possibile recuperare il valore corrente dei buffer video richiesti usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Il numero corrente di buffer video richiesto viene archiviato nel membro **wNumVideoRequested** della **struttura CAPTUREPARMS.** È possibile richiedere il posizionamento e il numero di buffer aggiornando questo membro e quindi inviando la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)

 

 




