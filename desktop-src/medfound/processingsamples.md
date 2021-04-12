---
description: Elaborazione dell'input e dell'output del codec DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Elaborazione dell'input e dell'output del codec DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344411"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="82183-103">Elaborazione dell'input e dell'output del codec DMO</span><span class="sxs-lookup"><span data-stu-id="82183-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="82183-104">Dopo aver configurato il tipo di input e il tipo di output per un DMO, è possibile iniziare l'elaborazione degli esempi di dati.</span><span class="sxs-lookup"><span data-stu-id="82183-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="82183-105">Passare i campioni a DMO per l'elaborazione usando il metodo **IMediaObject::P rocessinput** e quindi recuperare l'esempio elaborato chiamando **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="82183-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="82183-106">È necessario impostare indicatori di tempo e durate accurati per tutti gli esempi di input passati.</span><span class="sxs-lookup"><span data-stu-id="82183-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="82183-107">I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video.</span><span class="sxs-lookup"><span data-stu-id="82183-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="82183-108">Se non si dispone dei timestamp per gli esempi, è preferibile lasciarli invariati rispetto all'utilizzo di valori incerti.</span><span class="sxs-lookup"><span data-stu-id="82183-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82183-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82183-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82183-110">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="82183-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



