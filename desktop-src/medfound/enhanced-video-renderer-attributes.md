---
description: Attributi EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Attributi EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508b036a7880c48e65d3c07a80ba5baaa5a52306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305386"
---
# <a name="evr-attributes"></a>Attributi EVR

Per configurare il renderer video avanzato (EVR), è possibile usare gli attributi seguenti.



| Attributo                                                                                                         | Descrizione                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [\_AllowBatching EVRConfig](evrconfig-allowbatching.md)                                                           | Consente a EVR di eseguire il batch delle chiamate al metodo Microsoft Direct3D **IDirect3DDevice9::P** reinviate.                            |
| [\_AllowDropToBob EVRConfig](evrconfig-allowdroptobob.md)                                                         | Consente al EVR di migliorare le prestazioni tramite la deinterlacciamento Bob.                                                        |
| [\_AllowDropToHalfInterlace EVRConfig](evrconfig-allowdroptohalfinterlace.md)                                     | Consente al EVR di migliorare le prestazioni ignorando il secondo campo di ogni frame interlacciato.                            |
| [\_AllowDropToThrottle EVRConfig](evrconfig-allowdroptothrottle.md)                                               | Consente al EVR di limitare l'output in modo che corrisponda alla larghezza di banda della GPU.                                                               |
| [\_AllowScaling EVRConfig](evrconfig-allowscaling.md)                                                             | Consente a EVR di combinare il video in un rettangolo di dimensioni inferiori rispetto al rettangolo di output, quindi ridimensionare il risultato. |
| [\_ForceBatching EVRConfig](evrconfig-forcebatching.md)                                                           | Impone a EVR di inviare in batch le chiamate al metodo **IDirect3D9Device::P** reinviate.                                               |
| [\_ForceBob EVRConfig](evrconfig-forcebob.md)                                                                     | Impone a EVR di utilizzare il deinterlacciamento Bob.                                                                                 |
| [\_ForceHalfInterlace EVRConfig](evrconfig-forcehalfinterlace.md)                                                 | Impone a EVR di ignorare il secondo campo di ogni frame interlacciato.                                                       |
| [\_ForceScaling EVRConfig](evrconfig-forcescaling.md)                                                             | Impone a EVR di combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato. |
| [\_ForceThrottle EVRConfig](evrconfig-forcethrottle.md)                                                           | Impone a EVR di limitare l'output in modo che corrisponda alla larghezza di banda della GPU.                                                               |
| [**\_attivazione del \_ \_ mixer video \_ personalizzato \_ MF Activate**](mf-activate-custom-video-mixer-activate-attribute.md)         | Specifica un oggetto attivazione che consente di creare un mixer video personalizzato per il renderer video avanzato (EVR).                  |
| [**MF \_ attivazione \_ del \_ mixer video personalizzato \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID di un mixer video personalizzato per la EVR.                                                                               |
| [**MF \_ attiva \_ i \_ \_ flag del mixer video personalizzati \_**](mf-activate-custom-video-mixer-flags-attribute.md)               | Specifica come creare un mixer personalizzato per EVR.                                                                      |
| [**\_ \_ \_ \_ attiva attivazione del Presenter video \_ personalizzato MF**](mf-activate-custom-video-presenter-activate-attribute.md) | Specifica un oggetto attivazione che crea un presentatore video personalizzato per EVR.                                        |
| [**MF \_ attivare \_ il \_ \_ CLSID del Presenter video personalizzato \_**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID di un presentatore video personalizzato per la EVR.                                                                           |
| [**MF \_ attiva \_ i \_ \_ flag del Presenter video personalizzati \_**](mf-activate-custom-video-presenter-flags-attribute.md)       | Specifica come creare un Presenter personalizzato per EVR.                                                                  |
| [**\_finestra attiva \_ video \_ MF**](mf-activate-video-window-attribute.md)                                         | Handle per la finestra di ritaglio video.                                                                                     |
| [**\_ \_ \_ conteggio campioni richiesti per MF SA \_**](mf-sa-required-sample-count-attribute.md)                                  | Indica il numero di buffer non compressi richiesti dal sink multimediale EVR per la deinterlacciamento.                         |
| [**ZOOM del VIDEO \_ \_ Rect**](video-zoom-rect-attribute.md)                                                            | Specifica il rettangolo di zoom per il mixer EVR.                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 



