---
title: Formati stencil non supportati con le risorse affiancate
description: I formati che contengono stencil non sono supportati con le risorse affiancate.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043993"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>Formati stencil non supportati con le risorse affiancate

I formati che contengono stencil non sono supportati con le risorse affiancate.

I formati che contengono stencil includono DXGI \_ Format \_ D24 \_ UNORM \_ S8 \_ uint (e i formati correlati nella famiglia R24G8) e DXGI \_ Format \_ D32 \_ float \_ S8X24 \_ uint (e i formati correlati nella famiglia R32G8X24).

Alcune implementazioni archiviano la profondità e lo stencil in allocazioni separate mentre altre le archiviano insieme. La gestione dei riquadri per i due schemi dovrebbe essere diversa e nessuna API singola può astrarre o razionalizzare le differenze. Si consiglia di usare un hardware futuro per supportare superfici di profondità e stencil indipendenti, ognuna affiancata in modo indipendente. 32 i riquadri di profondità di bit 128x128 e gli stencil a 8 bit avrebbero riquadri 256x256. Pertanto, le applicazioni devono vivere con un errato allineamento delle forme dei riquadri tra profondità e stencil. Tuttavia, lo stesso problema esiste già con formati di superficie di destinazione di rendering diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Condivisione tra processi e dispositivi affiancati per le risorse](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




