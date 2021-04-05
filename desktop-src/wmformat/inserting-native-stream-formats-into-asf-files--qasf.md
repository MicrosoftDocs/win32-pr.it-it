---
title: Inserimento di formati di flusso nativi in file ASF (QASF)
description: Inserimento di formati di flusso nativi in file ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media Format SDK, formati di flussi nativi (QASF)
- Windows Media Format SDK, inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK, DirectShow
- Formato di sistemi avanzati (ASF), inserimento di formati di flussi nativi (QASF)
- ASF (Advanced Systems Format), inserimento di formati di flusso nativi (QASF)
- ASF (Advanced Systems Format), formati di flussi nativi (QASF)
- ASF (formato avanzato dei sistemi), formati di flussi nativi (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, formati di flussi nativi (QASF)
- DirectShow, inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856693"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Inserimento di formati di flusso nativi in file ASF (QASF)

Per impostazione predefinita, il [writer WM ASF](wm-asf-writer-filter.md) prevede flussi audio e video non compressi nei pin di input e usa Windows Media Format SDK per accedere ai codec Windows Media Audio e Windows Media video, che comprimono i flussi. Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati. Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e Digital Rights Management (DRM), senza la necessità di transcodificare il contenuto.

Per creare un file ASF che contiene contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico del filtro a Monte del writer ASF WM e ignorare il meccanismo di compressione del writer ASF WM chiamando [**IConfigAsfWriter2:: separat**](iconfigasfwriter2-setparam.md) nel modo seguente:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Configurare quindi il filtro con il profilo desiderato. È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo. In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato per la corrispondenza. Per ulteriori informazioni, vedere [per creare file ASF con codec di terze parti](to-create-asf-files-using-third-party-codecs.md).

Quando si connette il writer ASF WM al filtro upstream, usare il metodo **IGraphBuilder:: ConnectDirect** . Non usare alcun metodo di "connessione intelligente", ad esempio **IGraphBuilder:: Connect** o **IGraphBuilder:: RenderFile** per connettere il filtro in quanto questa operazione Disabilita la modalità "bypass Compression" del filtro.

 

 




