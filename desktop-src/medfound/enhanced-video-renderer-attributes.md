---
description: Attributi EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Attributi EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974540"
---
# <a name="evr-attributes"></a>Attributi EVR

Gli attributi seguenti possono essere usati per configurare enhanced video renderer (EVR).



| Attributo                                                                                                         | Descrizione                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Consente all'EVR di eseguire chiamate in batch al metodo Microsoft **Direct3D IDirect3DDevice9::P resent.**                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Consente all'EVR di migliorare le prestazioni usando bob deinterlacing.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Consente all'EVR di migliorare le prestazioni ignorando il secondo campo di ogni fotogramma interlacciato.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Consente all'EVR di limitare l'output in modo che corrisponda alla larghezza di banda GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Consente all'EVR di combinare il video all'interno di un rettangolo più piccolo del rettangolo di output e quindi di ridimensionare il risultato. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Forza l'EVR alle chiamate batch al **metodo IDirect3D9Device::P resent.**                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Impone all'EVR di usare bob deinterlacing.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Forza l'EVR a ignorare il secondo campo di ogni fotogramma interlacciato.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Forza l'EVR a combinare il video all'interno di un rettangolo più piccolo del rettangolo di output e quindi ridimensiona il risultato. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Forza l'EVR a limitare l'output in modo che corrisponda alla larghezza di banda GPU.                                                               |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md)         | Specifica un oggetto di attivazione che crea un mixer video personalizzato per il renderer video avanzato (EVR).                  |
| [**\_CLSID DEL \_ \_ MIXER VIDEO \_ PERSONALIZZATO \_ ATTIVATO DA MF**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID di un mixer video personalizzato per l'EVR.                                                                               |
| [**MF \_ ATTIVA FLAG DEL \_ \_ MIXER VIDEO \_ \_ PERSONALIZZATO**](mf-activate-custom-video-mixer-flags-attribute.md)               | Specifica come creare un mixer personalizzato per l'EVR.                                                                      |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Specifica un oggetto di attivazione che crea un presentatore video personalizzato per l'EVR.                                        |
| [**CLSID DEL PRESENTATORE VIDEO PERSONALIZZATO \_ \_ ATTIVAZIONE \_ \_ \_ MF**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID di un presentatore video personalizzato per l'EVR.                                                                           |
| [**MF \_ ATTIVA FLAG DEL \_ \_ PRESENTATORE VIDEO \_ \_ PERSONALIZZATO**](mf-activate-custom-video-presenter-flags-attribute.md)       | Specifica come creare un presentatore personalizzato per l'EVR.                                                                  |
| [**FINESTRA VIDEO DI ATTIVAZIONE MF \_ \_ \_**](mf-activate-video-window-attribute.md)                                         | Handle per la finestra di ritaglio video.                                                                                     |
| [**CONTEGGIO DEI CAMPIONI NECESSARI PER LA FIRMA DI ACCESSO \_ \_ CONDIVISO \_ \_ DI MF**](mf-sa-required-sample-count-attribute.md)                                  | Indica il numero di buffer non compressi necessari al sink multimediale EVR per la deinterlacing.                         |
| [**RETTA \_ DI ZOOM \_ VIDEO**](video-zoom-rect-attribute.md)                                                            | Specifica il rettangolo di zoom per il mixer EVR.                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> </dl>

 

 



