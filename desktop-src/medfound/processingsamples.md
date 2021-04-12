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
# <a name="processing-codec-dmo-input-and-output"></a>Elaborazione dell'input e dell'output del codec DMO

Dopo aver configurato il tipo di input e il tipo di output per un DMO, è possibile iniziare l'elaborazione degli esempi di dati. Passare i campioni a DMO per l'elaborazione usando il metodo **IMediaObject::P rocessinput** e quindi recuperare l'esempio elaborato chiamando **IMediaObject::P rocessoutput**. È necessario impostare indicatori di tempo e durate accurati per tutti gli esempi di input passati. I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video. Se non si dispone dei timestamp per gli esempi, è preferibile lasciarli invariati rispetto all'utilizzo di valori incerti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



