---
title: Transcodifica di file (QASF)
description: Transcodifica di file (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows Media Format SDK, file di transcodifica (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), file di transcodifica (QASF)
- ASF (formato avanzato dei sistemi), transcodifica dei file (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, transcoding Files (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566666"
---
# <a name="transcoding-files-qasf"></a>Transcodifica di file (QASF)

È possibile creare un grafico di filtro per la transcodifica di file usando il [writer ASF WM](wm-asf-writer-filter.md) in diversi modi. Il modo più semplice consiste nel creare, configurare e aggiungere il writer ASF WM al grafo del filtro e quindi usare il metodo **IGraphBuilder:: RenderFile** per creare automaticamente il grafo.

In alternativa, è possibile aggiungere manualmente ogni filtro al grafico e connettere i pin. Dopo aver aggiunto il writer WM ASF, configurarlo usando i metodi **IConfigAsfWriter** se il profilo predefinito non è adatto e connettere i pin di input del writer ASF WM ai pin di output corrispondenti nei filtri upstream.

Nella figura seguente viene illustrata la tipica configurazione del grafico di filtro per la transcodifica del writer WM ASF.

![grafici tipici del filtro di transcodifica](images/asf-transcode.png)

 

 




