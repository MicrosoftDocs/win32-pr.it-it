---
description: Elaborazione dell'input e dell'output del codec MFT
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Elaborazione dell'input e dell'output del codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226511"
---
# <a name="processing-codec-mft-input-and-output"></a>Elaborazione dell'input e dell'output del codec MFT

Dopo aver configurato il tipo di input e il tipo di output per un MFT, è possibile iniziare l'elaborazione degli esempi di dati. Passare i campioni alla MFT per l'elaborazione usando il metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e quindi recuperare l'esempio elaborato chiamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). È necessario impostare indicatori di tempo e durate accurati per tutti gli esempi di input passati. I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video. Se non si dispone dei timestamp per gli esempi, è preferibile lasciarli invariati rispetto all'utilizzo di valori incerti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



