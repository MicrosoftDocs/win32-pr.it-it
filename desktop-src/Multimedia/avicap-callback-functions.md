---
title: Funzioni di callback AVICap
description: Funzioni di callback AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Classe AVICap, funzioni di callback
- Funzioni di callback di AVICap, informazioni
- Messaggio WM_CAP_SET_CALLBACK_CAPCONTROL
- Messaggio WM_CAP_SET_CALLBACK_ERROR
- Messaggio WM_CAP_SET_CALLBACK_FRAME
- Messaggio WM_CAP_SET_CALLBACK_STATUS
- Messaggio WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Messaggio WM_CAP_SET_CALLBACK_WAVESTREAM
- Messaggio WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl (macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame (macro)
- capSetCallbackOnStatus (macro)
- capSetCallbackOnVideoStream (macro)
- capSetCallbackOnWaveStream (macro)
- capSetCallbackOnYield (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955803"
---
# <a name="avicap-callback-functions"></a>Funzioni di callback AVICap

L'applicazione può registrare le funzioni di callback con una finestra di acquisizione per notificare all'applicazione quando lo stato viene modificato, quando si verificano errori, quando i fotogrammi video e i buffer audio diventano disponibili e vengono restituiti durante l'acquisizione del flusso. I messaggi seguenti impostano la funzione di callback.



| Message                                                                        | Descrizione                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CAPCONTROL di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-capcontrol.md)   | Specifica la funzione di callback nell'applicazione chiamata per fornire un controllo preciso sull'inizio e la fine dell'acquisizione. È anche possibile usare la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) per inviare questo messaggio.                   |
| [**\_errore di \_ callback del set di estremità WM \_ \_**](wm-cap-set-callback-error.md)             | Specifica la funzione di callback nell'applicazione chiamata quando si verifica un errore. È anche possibile usare la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) per inviare questo messaggio.                                                           |
| [**\_frame di \_ \_ callback \_ per set di estremità WM**](wm-cap-set-callback-frame.md)             | Specifica la funzione di callback nell'applicazione chiamata quando vengono acquisiti i frame di anteprima. È anche possibile usare la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) per inviare questo messaggio.                                               |
| [**\_stato di \_ callback per set di estremità WM \_ \_**](wm-cap-set-callback-status.md)           | Specifica la funzione di callback nell'applicazione chiamata quando lo stato cambia. È anche possibile usare la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) per inviare questo messaggio.                                                      |
| [**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-videostream.md) | Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer video. È anche possibile usare la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) per inviare questo messaggio. |
| [**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-wavestream.md)   | Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer audio. È anche possibile usare la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) per inviare questo messaggio.   |
| [**\_rendimento di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-yield.md)             | Specifica la funzione di callback nell'applicazione chiamata quando cede durante l'acquisizione di flussi. È anche possibile usare la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) per inviare questo messaggio.                                         |



 

Negli argomenti seguenti vengono descritte le diverse funzioni di callback, le notifiche inviate alle funzioni e i relativi utilizzi.

 

 




