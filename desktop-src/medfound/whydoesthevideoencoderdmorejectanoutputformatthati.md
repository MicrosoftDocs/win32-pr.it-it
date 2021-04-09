---
description: Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049793"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?

A differenza dei tipi di output del codificatore audio, gli output supportati enumerati dai codificatori video non vengono completati come recapitati. È necessario impostare la velocità in bit del flusso nel membro **dwBitrate** della struttura **VIDEOINFOHEADER** in modo che corrisponda al valore impostato per la proprietà [ \_ RAVG di MFPKEY](mfpkey-ravgproperty.md) .

Dopo aver impostato tutte le opzioni nel modo desiderato, è necessario recuperare i dati privati del codec e aggiungerli alla struttura **VIDEOINFOHEADER** . Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 



