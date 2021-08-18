---
title: Inserimento di formati di flusso nativi nei file ASF (QASF)
description: Inserimento di formati di flusso nativi nei file ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows MEDIA Format SDK, formati di flusso nativi (QASF)
- Windows MEDIA Format SDK, inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), inserimento di formati di flusso nativi (QASF)
- ASF (Advanced Systems Format), inserimento di formati di flusso nativi (QASF)
- Advanced Systems Format (ASF), formati di flusso nativi (QASF)
- ASF (Advanced Systems Format), formati di flusso nativi (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, formati di flusso nativi (QASF)
- DirectShow,inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK,QASF
- Advanced Systems Format (ASF),QASF
- ASF (Advanced Systems Format),QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b395748520943a62645a88c018131f909577191ebafbe1f9c4d3a80219cb39f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701778"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Inserimento di formati di flusso nativi nei file ASF (QASF)

Per impostazione predefinita, [WM ASF Writer](wm-asf-writer-filter.md) prevede flussi audio e video non compressi sui pin di input e usa Windows Media Format SDK per accedere ai codec audio e video multimediali di Windows e Windows, che comprimeno i flussi. Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati. Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e DRM (Digital Rights Management), senza dover transcodificare il contenuto.

Per creare un file ASF contenente contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico dei filtri a monte di WM ASF Writer e ignorare il meccanismo di compressione di WM ASF Writer chiamando [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) come indicato di seguito:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Configurare quindi il filtro con il profilo desiderato. È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo. In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato in modo che corrisponda. Per altre informazioni, vedere [Per creare file ASF usando codec di terze parti.](to-create-asf-files-using-third-party-codecs.md)

Quando si connette WM ASF Writer al filtro upstream, usare il **metodo IGraphBuilder::ConnectDirect.** Non usare metodi di "connessione intelligente", ad esempio **IGraphBuilder::Connessione** o **IGraphBuilder::RenderFile,** per connettere il filtro, perché in questo modo verrà disabilitata la modalità di "bypass della compressione" del filtro.

 

 




