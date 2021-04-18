---
title: Negoziazione del formato
description: Negoziazione del formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Plug-in di Windows Media Player, negoziazione del formato
- plug-in, negoziazione del formato
- plug-in di elaborazione dei segnali digitali, negoziazione del formato
- Plug-in DSP, negoziazione del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298655"
---
# <a name="format-negotiation"></a>Negoziazione del formato

Per Windows Media Player e un plug-in DSP per la condivisione di dati, entrambi i programmi devono accettare il formato dei dati elaborati. Il plug-in DSP implementa i metodi che il lettore chiama per determinare quali formati supportano il plug-in. Il plug-in implementa anche metodi che il lettore chiama per impostare il formato corrente.

Se il plug-in funge da DirextX Media Object (DMO), Windows Media Player individua e imposta i formati multimediali chiamando i metodi dell'interfaccia **IMediaObject** . Ad esempio, il lettore chiama ripetutamente il plug-in **IMediaObject:: GetInputType** per ottenere un elenco di tutti i formati di input supportati dal plug-in. I plug-in DMO utilizzano la struttura del **\_ \_ tipo di supporto DMO** per organizzare le informazioni che specificano un formato multimediale. Per ulteriori informazioni sul modo in cui i plug-in DMO e il lettore negoziano il formato, vedere [informazioni su IMediaObject](about-imediaobject.md).

Se il plug-in funge da trasformazione Media Foundation (MFT), Windows Media Player individua e imposta i formati multimediali chiamando i metodi dell'interfaccia **IMFTransform** . Ad esempio, il lettore chiama ripetutamente il plug-in **IMFTransform:: GetInputAvailableType** per ottenere un elenco di tutti i formati di input supportati dal plug-in. I plug-in di MFT e il lettore usano l'interfaccia **IMFMediaType** per organizzare e scambiare informazioni sul formato.

Windows Media Player utilizzerà un plug-in DSP audio solo se il plug-in supporta la stessa profondità di bit dell'audio digitale riprodotto. Se, ad esempio, l'audio digitale è a 20 bit, il plug-in deve essere scritto per elaborare audio a 20 bit. Per audio CD, i plug-in DSP devono supportare l'elaborazione a 20 bit.

Durante la negoziazione del formato del contenuto multicanale in un computer configurato per l'uso con altoparlanti stereo, Windows Media Player prima di tutto tenta di connettersi a un plug-in DSP audio usando il formato di input e output esistente chiamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**. Una volta eseguita questa negoziazione iniziale, il giocatore enumera i formati supportati dal plug-in e tenta di negoziare la combinazione di formato migliore per il lettore e il plug-in. Se il plug-in accetta audio stereo (definito da una struttura **WAVEFORMATEX** ) come formato di input durante la negoziazione iniziale e successivamente accetta solo audio multicanale (definito da una struttura **WAVEFORMATEXTENSIBLE** ), il lettore fornirà audio multicanale come formato di input per il plug-in. Questo comportamento durante la negoziazione del formato è disponibile per l'utilizzo nel sistema operativo Microsoft Windows XP. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




