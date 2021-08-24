---
title: Scrittura Flussi con pixel non quadrati
description: Scrittura Flussi con pixel non quadrati
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows MEDIA Format SDK, scrittura di flussi video
- Windows MEDIA Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows MEDIA Format SDK, pixel (non quadrati)
- Advanced Systems Format (ASF), scrittura di flussi video
- ASF (Advanced Systems Format), scrittura di flussi video
- Advanced Systems Format (ASF), flussi video
- ASF (Advanced Systems Format),flussi video
- Advanced Systems Format (ASF), pixel non quadrati
- ASF (Advanced Systems Format), pixel non quadrati
- Advanced Systems Format (ASF), pixel (non quadrati)
- ASF (Advanced Systems Format),pixel (non quadrati)
- scrittura di flussi video
- flussi video, scrittura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b44df1e4b4ce3f2bf2cb0e1d795b4caf396b6396e3e70b68b9040ad9a5456f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657951"
---
# <a name="writing-streams-with-non-square-pixels"></a>Scrittura Flussi con pixel non quadrati

Esistono due modi per creare flussi video con pixel non quadrati che verranno visualizzati correttamente in Windows Media Player. La prima tecnica prevede l'impostazione di attributi a livello di flusso nell'intestazione del file. La seconda tecnica prevede l'aggiunta di un'estensione per unità dati a un flusso nel profilo e l'impostazione di un valore per tale estensione in ogni esempio scritto.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Per usare gli attributi di intestazione a livello di flusso per impostare le proporzioni dei pixel

1.  Configurare l'oggetto writer. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md)
2.  Creare o caricare un profilo con uno o più flussi video. Per altre informazioni, vedere [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).
3.  Chiamare [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Chiamare sempre questo metodo prima di impostare gli attributi di intestazione.
4.  Chiamare **QueryInterface** per ottenere [**l'interfaccia IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) e chiamare [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) due volte per aggiungere [**AspectRatioX**](aspectratiox.md) e [**AspectRatioY**](aspectratioy.md) come attributi a livello di flusso del flusso video. Questi attributi sono **valori DWORD.**
5.  Scrivere il file.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Per utilizzare le estensioni delle unità dati per impostare le proporzioni dei pixel

**Prima di scrivere:**

1.  Configurare l'oggetto writer. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md)
2.  Creare o caricare un profilo con uno o più flussi video. Per altre informazioni, vedere [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).
3.  Per ogni flusso (di qualsiasi tipo di supporto) nel profilo, chiamare [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) per specificare un nome univoco a scelta. Non assegnare a due flussi lo stesso nome.
4.  Usare [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) nel flusso video per aggiungere un'estensione dell'unità dati per le proporzioni pixel.
5.  Chiamare [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Scrivere il file.

**Durante la scrittura:**

-   Per ogni esempio, chiamare [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) e specificare la proprietà WM \_ SampleExtensionGUID \_ PixelAspectRatio insieme al valore corretto. I valori delle proporzioni vengono scritti come due valori concatenati a due cifre. Ad esempio, 16:9 viene scritto come 1609 o 0x0649. Si tratta sempre di un valore a 2 byte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per leggere e scrivere video Flussi con pixel non quadrati**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




