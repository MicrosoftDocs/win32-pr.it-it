---
description: Uso del filtro Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Uso del filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314383"
---
# <a name="using-the-smart-tee-filter"></a>Uso del filtro Smart Tee

Se un filtro di acquisizione presenta pin di acquisizione e di anteprima distinti, è possibile acquisire da uno durante l'anteprima dell'altro. Tuttavia, se il filtro non ha un pin di anteprima, è possibile eseguire la stessa operazione includendo il filtro [Smart Tee](smart-tee-filter.md) nel grafico. Questo filtro suddivide i dati dal pin di acquisizione in due flussi identici, uno per l'acquisizione e uno per l'anteprima. La figura seguente illustra questo processo.

![Acquisisci grafico con filtro Smart Tee](images/vidcap05.png)

Se necessario, il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente il filtro Smart Tee. Tuttavia, se si usano i metodi **IGraphBuilder** per compilare il grafo e non **RenderStream**, potrebbe essere necessario inserire il filtro Smart Tee.

Prima di eseguire il rendering dei pin nel filtro di acquisizione, controllare se il filtro ha un pin di anteprima o un PIN della porta video. In caso contrario, aggiungere il filtro Smart Tee al grafico e connetterlo al pin di acquisizione nel filtro di acquisizione.

> [!Note]  
> È possibile trattare un PIN della porta video (VP) come tipo di pin di anteprima, pertanto un filtro con un pin VP non necessita di un filtro per Smart Tee. Tuttavia, i pin VP hanno altri requisiti particolari. Per altre informazioni, vedere [pin della porta video](video-port-pins.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md)
</dt> <dt>

[Utilizzo delle categorie pin](working-with-pin-categories.md)
</dt> </dl>

 

 



