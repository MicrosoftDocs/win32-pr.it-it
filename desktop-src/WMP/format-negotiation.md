---
title: Negoziazione del formato
description: Negoziazione del formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player plug-in, negoziazione del formato
- plug-in, negoziazione del formato
- plug-in di elaborazione del segnale digitale, negoziazione del formato
- plug-in DSP, negoziazione del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69669bc3af82400ea62d154335d117fef185d0b34184be4101ffa5ae309e6ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054969"
---
# <a name="format-negotiation"></a>Negoziazione del formato

Per Windows Media Player e un plug-in DSP per condividere i dati, entrambi i programmi devono accettare il formato dei dati che stanno elaborando. Il plug-in DSP implementa i metodi che il lettore chiama per determinare i formati supportati dal plug-in. Il plug-in implementa anche i metodi che il lettore chiama per impostare il formato corrente.

Se il plug-in funge da oggetto multimediale DirextX (DMO), Windows Media Player individua e imposta i formati multimediali chiamando i metodi **dell'interfaccia IMediaObject.** Ad esempio, Player chiama ripetutamente **IMediaObject::GetInputType** del plug-in per ottenere un elenco di tutti i formati di input supportati dal plug-in. DMO plug-in usano la **DMO \_ MEDIA \_ TYPE** per organizzare le informazioni che specificano un formato multimediale. Per altre informazioni su come DMO plug-in e il formato di negoziazione del lettore, vedere [Informazioni su IMediaObject](about-imediaobject.md).

Se il plug-in funge da Media Foundation Transform (MFT), Windows Media Player individua e imposta i formati multimediali chiamando i metodi **dell'interfaccia IMFTransform.** Ad esempio, Player chiama ripetutamente **IMFTransform::GetInputAvailableType** del plug-in per ottenere un elenco di tutti i formati di input supportati dal plug-in. I plug-in MFT e Player usano **l'interfaccia IMFMediaType** per organizzare e scambiare informazioni sul formato.

Windows Media Player un plug-in DSP audio verrà utilizzato solo se il plug-in supporta la stessa profondità in bit dell'audio digitale riprodotto. Ad esempio, se l'audio digitale è a 20 bit, il plug-in deve essere scritto per elaborare l'audio a 20 bit. Per l'audio CD, i plug-in DSP devono supportare l'elaborazione a 20 bit.

Durante la negoziazione del formato del contenuto multicanale in un computer configurato per l'uso con altoparlanti stereo, Windows Media Player tenta innanzitutto di connettersi a un plug-in DSP audio usando il formato di input e output esistente chiamando **IMediaObject::SetInputType** e **IMediaObject::SetOutputType**. Una volta eseguita questa negoziazione iniziale, il lettore enumera quindi i formati supportati dal plug-in e tenta di negoziare la combinazione di formato migliore per il lettore e il plug-in. Se il plug-in accetta l'audio stereo (definito da una struttura **WAVEFORMATEX)** come formato di input durante la negoziazione iniziale e successivamente accetta solo audio multicanale (definito da una struttura **WAVEFORMATEXTENSIBLE),** Player fornirà audio multicanale come formato di input al plug-in. Questo comportamento durante la negoziazione del formato è disponibile per l'uso nel sistema operativo Microsoft Windows XP. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




