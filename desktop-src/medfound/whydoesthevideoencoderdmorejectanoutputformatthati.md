---
description: Perché il codificatore video rifiuta un formato di output che si tenta di impostare quando il formato viene recuperato dallo stesso oggetto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Perché il codificatore video rifiuta un formato di output che si tenta di impostare quando il formato viene recuperato dallo stesso oggetto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2e744285140df13a9aa251983ab801033c481d1452029c955ee3a39235fcea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112891"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Perché il codificatore video rifiuta un formato di output che si tenta di impostare quando il formato viene recuperato dallo stesso oggetto?

A differenza dei tipi di output del codificatore audio, gli output supportati enumerati dai codificatori video non sono completi come recapitati. È necessario impostare la velocità in bit del flusso nel membro **dwBitrate** della struttura **VIDEOINFOHEADER** in modo che corrisponda al valore impostato per la proprietà [MFPKEY \_ RAVG.](mfpkey-ravgproperty.md)

Dopo aver impostato tutte le opzioni nel modo desiderato, è necessario recuperare i dati privati del codec e accodarli alla **struttura VIDEOINFOHEADER.** Per altre informazioni, vedere [Uso dei dati privati del codec video](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 



