---
title: Funzioni di callback AVICap
description: Funzioni di callback AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Classe AVICap, funzioni di callback
- Funzioni di callback AVICap, informazioni
- WM_CAP_SET_CALLBACK_CAPCONTROL messaggio
- WM_CAP_SET_CALLBACK_ERROR messaggio
- WM_CAP_SET_CALLBACK_FRAME messaggio
- WM_CAP_SET_CALLBACK_STATUS messaggio
- WM_CAP_SET_CALLBACK_VIDEOSTREAM messaggio
- WM_CAP_SET_CALLBACK_WAVESTREAM messaggio
- WM_CAP_SET_CALLBACK_YIELD messaggio
- Macro capSetCallbackOnCapControl
- capSetCallbackOnErrormacro
- Macro capSetCallbackOnFrame
- Macro capSetCallbackOnStatus
- Macro capSetCallbackOnVideoStream
- Macro capSetCallbackOnWaveStream
- Macro capSetCallbackOnYield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee000f03df5bb23ed46f3692ded692630c85a292dfe3dccfcd24a8867849d5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691961"
---
# <a name="avicap-callback-functions"></a>Funzioni di callback AVICap

L'applicazione può registrare le funzioni di callback con una finestra di acquisizione in modo che invii una notifica all'applicazione quando lo stato cambia, quando si verificano errori, quando i buffer audio e dei fotogrammi video diventano disponibili e da cedere durante l'acquisizione di streaming. I messaggi seguenti impostano la funzione di callback.



| Message                                                                        | Descrizione                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Specifica la funzione di callback nell'applicazione chiamata per fornire un controllo preciso sull'inizio e sulla fine dell'acquisizione. È anche possibile usare la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) per inviare questo messaggio.                   |
| [**ERRORE DI \_ CALLBACK WM CAP \_ SET \_ \_**](wm-cap-set-callback-error.md)             | Specifica la funzione di callback nell'applicazione chiamata quando si verifica un errore. È anche possibile usare la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) per inviare questo messaggio.                                                           |
| [**FRAME DI \_ CALLBACK WM CAP \_ SET \_ \_**](wm-cap-set-callback-frame.md)             | Specifica la funzione di callback nell'applicazione chiamata quando vengono acquisiti i frame di anteprima. È anche possibile usare la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) per inviare questo messaggio.                                               |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)           | Specifica la funzione di callback nell'applicazione chiamata quando cambia lo stato. È anche possibile usare la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) per inviare questo messaggio.                                                      |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md) | Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione di streaming quando diventa disponibile un nuovo buffer video. È anche possibile usare la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) per inviare questo messaggio. |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)   | Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione di streaming quando diventa disponibile un nuovo buffer audio. È anche possibile usare la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) per inviare questo messaggio.   |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)             | Specifica la funzione di callback nell'applicazione chiamata durante la cedinge durante l'acquisizione del flusso. È anche possibile usare la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) per inviare questo messaggio.                                         |



 

Negli argomenti seguenti vengono descritte le diverse funzioni di callback, le notifiche inviate alle funzioni e il relativo utilizzo.

 

 




