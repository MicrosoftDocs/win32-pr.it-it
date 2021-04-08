---
title: Scrittura di flussi con pixel non quadrati
description: Scrittura di flussi con pixel non quadrati
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, scrittura di flussi video
- Windows Media Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK, pixel (non quadrato)
- Formato di sistemi avanzati (ASF), scrittura di flussi video
- ASF (Advanced Systems Format), scrittura di flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Formato di sistemi avanzati (ASF), pixel non quadrati
- ASF (formato avanzato dei sistemi), pixel non quadrati
- Formato di sistemi avanzati (ASF), pixel (non quadrato)
- ASF (formato avanzato dei sistemi), pixel (non quadrato)
- scrittura di flussi video
- flussi video, scrittura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrato)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046301"
---
# <a name="writing-streams-with-non-square-pixels"></a>Scrittura di flussi con pixel non quadrati

Esistono due modi per creare flussi video con pixel non quadrati che verranno visualizzati correttamente in Windows Media Player. La prima tecnica consiste nell'impostare gli attributi a livello di flusso nell'intestazione del file. La seconda tecnica prevede l'aggiunta di un'estensione di unità dati a un flusso nel profilo e quindi l'impostazione di un valore per esso in ogni esempio scritto.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Per usare gli attributi di intestazione a livello di flusso per impostare le proporzioni in pixel

1.  Configurare l'oggetto writer. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).
2.  Creare o caricare un profilo con uno o più flussi video. Per ulteriori informazioni, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).
3.  Chiamare [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Chiamare sempre questo metodo prima di impostare gli attributi di intestazione.
4.  Chiamare **QueryInterface** per ottenere l'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) e chiamare [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) due volte per aggiungere [**AspectRatioX**](aspectratiox.md) e [**AspectRatioY**](aspectratioy.md) come attributi a livello di flusso del flusso video. Questi attributi sono valori **DWORD** .
5.  Scrivere il file.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Per utilizzare le estensioni dell'unità dati per impostare le proporzioni in pixel

**Prima della scrittura:**

1.  Configurare l'oggetto writer. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).
2.  Creare o caricare un profilo con uno o più flussi video. Per ulteriori informazioni, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).
3.  Per ogni flusso (di qualsiasi tipo di supporto) nel profilo, chiamare [**IWMStreamConfig:: Sestreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) per specificare un nome univoco a scelta. Non assegnare a due flussi lo stesso nome.
4.  Usare [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) nel flusso video per aggiungere un'estensione dell'unità dati per le proporzioni in pixel.
5.  Chiamare [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Scrivere il file.

**Durante la scrittura:**

-   Per ogni esempio, chiamare [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) e specificare la proprietà WM \_ SampleExtensionGUID \_ PixelAspectRatio insieme al valore corretto. I valori delle proporzioni vengono scritti come due valori concatenati a due cifre. 16:9, ad esempio, viene scritto come 1609 o 0x0649. Si tratta sempre di un valore a 2 byte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per leggere e scrivere flussi video con pixel non quadrati**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




