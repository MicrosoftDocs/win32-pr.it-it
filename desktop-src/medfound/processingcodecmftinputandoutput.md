---
description: Elaborazione dell'input e dell'output MFT del codec
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Elaborazione dell'input e dell'output MFT del codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101840"
---
# <a name="processing-codec-mft-input-and-output"></a>Elaborazione dell'input e dell'output MFT del codec

Dopo aver configurato il tipo di input e il tipo di output per un MFT, è possibile iniziare a elaborare gli esempi di dati. È possibile passare gli esempi a MFT per l'elaborazione usando il metodo [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e quindi recuperare l'esempio elaborato chiamando [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). È necessario impostare timestamp e durate accurati per tutti i campioni di input passati. I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video. Se non si hanno i timestamp per i campioni, è meglio lasciarli fuori che usare valori incerti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei codec MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



