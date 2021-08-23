---
description: Elaborazione di codec DMO input e output
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Elaborazione di codec DMO input e output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3b159ea9e8a323a8e980b9dbba227aa2a62d76316b90e09f45592044091f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035089"
---
# <a name="processing-codec-dmo-input-and-output"></a>Elaborazione di codec DMO input e output

Dopo aver configurato il tipo di input e il tipo di output per un DMO, è possibile iniziare a elaborare gli esempi di dati. Si passano esempi al DMO per l'elaborazione usando il metodo **IMediaObject::P rocessInput** e quindi si recupera l'esempio elaborato chiamando **IMediaObject::P rocessOutput**. È necessario impostare timestamp e durate accurati per tutti i campioni di input passati. I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video. Se non si hanno i timestamp per i campioni, è meglio lasciarli fuori che usare valori incerti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 



