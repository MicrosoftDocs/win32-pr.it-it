---
description: Uso del filtro smart tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Uso del filtro smart tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8897a93e8be7582a4acce1a2822160c58cfe1df79eb2093bd5d96bad9629b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650777"
---
# <a name="using-the-smart-tee-filter"></a>Uso del filtro smart tee

Se un filtro di acquisizione ha pin di acquisizione e anteprima separati, è possibile acquisire da uno durante l'anteprima dall'altro. Se tuttavia il filtro non ha un segnaposto di anteprima, è possibile eseguire la stessa operazione includendo il [filtro Smart Tee](smart-tee-filter.md) nel grafico. Questo filtro suddivide i dati dal pin di acquisizione in due flussi identici, uno per l'acquisizione e uno per l'anteprima. La figura seguente illustra questo processo.

![Grafico di acquisizione con filtro smart tee](images/vidcap05.png)

Il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente il filtro smart tee, se necessario. Tuttavia, se si usano **i metodi IGraphBuilder** per compilare il grafico e non **RenderStream,** potrebbe essere necessario inserire il filtro Smart Tee.

Prima di eseguire il rendering dei pin nel filtro di acquisizione, verificare se il filtro dispone di un segnaposto di anteprima o di una porta video. In caso contrario, aggiungere il filtro Smart Tee al grafico e connetterlo al segnaposto di acquisizione nel filtro di acquisizione.

> [!Note]  
> È possibile considerare un pin di porta video (VP) come una sorta di pin di anteprima, in modo che un filtro con un pin VP non necessiti di un filtro Smart Tee. Tuttavia, i pin VP hanno altri requisiti speciali. Per altre informazioni, vedere [Pin di porta video.](video-port-pins.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti di acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md)
</dt> <dt>

[Uso delle categorie di aggiunta](working-with-pin-categories.md)
</dt> </dl>

 

 



