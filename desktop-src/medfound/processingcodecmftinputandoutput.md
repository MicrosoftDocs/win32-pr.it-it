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
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="43434-103">Elaborazione dell'input e dell'output del codec MFT</span><span class="sxs-lookup"><span data-stu-id="43434-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="43434-104">Dopo aver configurato il tipo di input e il tipo di output per un MFT, è possibile iniziare l'elaborazione degli esempi di dati.</span><span class="sxs-lookup"><span data-stu-id="43434-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="43434-105">Passare i campioni alla MFT per l'elaborazione usando il metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e quindi recuperare l'esempio elaborato chiamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="43434-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="43434-106">È necessario impostare indicatori di tempo e durate accurati per tutti gli esempi di input passati.</span><span class="sxs-lookup"><span data-stu-id="43434-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="43434-107">I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video.</span><span class="sxs-lookup"><span data-stu-id="43434-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="43434-108">Se non si dispone dei timestamp per gli esempi, è preferibile lasciarli invariati rispetto all'utilizzo di valori incerti.</span><span class="sxs-lookup"><span data-stu-id="43434-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43434-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43434-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43434-110">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="43434-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



