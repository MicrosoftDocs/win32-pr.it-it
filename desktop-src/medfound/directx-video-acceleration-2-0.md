---
description: Accelerazione video DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Accelerazione video DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225807"
---
# <a name="directx-video-acceleration-20"></a>Accelerazione video DirectX 2,0

DirectX Video Acceleration (DXVA) è un'API e un DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione dei codec video. I codec software e i processori video software possono usare DXVA per eseguire l'offload di alcune operazioni con utilizzo intensivo della CPU nella GPU. Un decodificatore software, ad esempio, può eseguire l'offload della trasformazione iDCT (discrete coseno) inversa nella GPU.

In questa sezione vengono trattati gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su DXVA 2,0](about-dxva-2-0.md)<br/>                                                   | Panoramica di DXVA 2 e relativa relazione con DXVA 1.<br/>                                                                                                                                                        |
| [Gestione dispositivi Direct3D](direct3d-device-manager.md)<br/>                                 | Gestione dispositivi Microsoft Direct3D consente a due o più oggetti di condividere lo stesso dispositivo Microsoft Direct3D 9.<br/>                                                                                      |
| [Supporto di DXVA 2,0 in DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow.<br/>                                                                                             |
| [Supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in una trasformazione Media Foundation (MFT) con Direct3D 9<br/>                                                                      |
| [Elaborazione video DXVA](dxva-video-processing.md)<br/>                                     | L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse. I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware. <br/>                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Specifica DXVA 1](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
