---
description: Accelerazione video DirectX 2.0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Accelerazione video DirectX 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150bf899d5e11a7e06db1ffdbc4cba9e04ab8e3245a040339088269ac06423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064120"
---
# <a name="directx-video-acceleration-20"></a>Accelerazione video DirectX 2.0

DirectX Video Acceleration (DXVA) è un'API e un DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione dei codec video. I codec software e i processori video software possono usare DXVA per scaricare determinate operazioni a elevato utilizzo di CPU nella GPU. Ad esempio, un decodificatore software può scaricare la trasformazione del coseno discreto inverso (iDCT) nella GPU.

In questa sezione vengono trattati gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su DXVA 2.0](about-dxva-2-0.md)<br/>                                                   | Panoramica di DXVA 2 e della relativa relazione con DXVA 1.<br/>                                                                                                                                                        |
| [Gestione dispositivi Direct3D](direct3d-device-manager.md)<br/>                                 | Gestione dispositivi Microsoft Direct3D consente a due o più oggetti di condividere lo stesso dispositivo Microsoft Direct3D 9.<br/>                                                                                      |
| [Supporto di DXVA 2.0 in DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | Questo argomento descrive come supportare DirectX Video Acceleration (DXVA) 2.0 in un filtro DirectShow decodificatore.<br/>                                                                                             |
| [Supporto di DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | Questo argomento descrive come supportare DirectX Video Acceleration (DXVA) 2.0 in una trasformazione Media Foundation (MFT) con Direct3D 9<br/>                                                                      |
| [Elaborazione video DXVA](dxva-video-processing.md)<br/>                                     | L'elaborazione video DXVA incapsula le funzioni dell'hardware grafico dedicate all'elaborazione di immagini video non compresse. I servizi di elaborazione video includono la delnterlacing e la combinazione di video.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware. <br/>                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation per programmatori](media-foundation-programming-guide.md)
</dt> <dt>

[Specifica DXVA 1](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
