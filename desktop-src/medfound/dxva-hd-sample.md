---
description: Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Esempio di DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878446"
---
# <a name="dxva-hd-sample"></a>Esempio di DXVA-HD

Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

Questo esempio è essenzialmente una porta dell' [esempio DXVA2 \_ VideoProc](dxva2-videoproc-sample.md). Ha le stesse funzioni di base e la maggior parte dei comandi della tastiera sono gli stessi.

L'esempio genera un video a livello di codice con un flusso primario e un sottoflusso. Il flusso primario Visualizza le barre dei colori SMPTE. Il sottoflusso è in alfa Blend nel flusso primario usando la chiave Luma. L'utente può modificare i parametri di elaborazione video, inclusi i valori alfa planari, i rettangoli di origine e di destinazione, le regolazioni dei colori e lo spazio colore. Nell'immagine seguente viene illustrato il video generato.

![screenshot dell'esempio DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>API illustrate

Questo esempio illustra le interfacce DXVA-HD seguenti:

-   [**\_Dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**\_VIDEOPROCESSOR IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



