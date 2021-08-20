---
title: Per usare il telecine inverso
description: Per usare il telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, telefono inverso
- Windows Media Format SDK, tele tele tele
- Advanced Systems Format (ASF), telefono inverso
- ASF (Advanced Systems Format), telefono inverso
- Advanced Systems Format (ASF), televideo
- ASF (Advanced Systems Format),televideo
- televida inversa
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7885caffea83460d73b1eca26dbfd94eb50d99ac4aa8589113875ffc4358c029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585321"
---
# <a name="to-use-inverse-telecine"></a>Per usare il telecine inverso

Telejavax è il processo di conversione di film, che ha 24 fotogrammi al secondo, in video, che ha 60 campi (semi fotogrammi) al secondo. Questo processo inserisce le immagini di ogni fotogramma del film in più campi video.

Quando si codifica digitalmente un video creato da una filmato usando il telegrafo, il processo di compressione può causare artefatti del movimento e altre riduzione della qualità. Per evitare effetti sulla qualità dell'output digitale, il codec Windows Media Video 9 supporta il teletrasmissione inversa. Quando si usa il telefono inverso, il codec ricostruisce i 24 fotogrammi di film originali al secondo dal video di input prima di codificare il contenuto.

Per usare il televersi inverso, è necessario:

-   Usare un profilo con un flusso video impostato su 24 fotogrammi al secondo.
-   Conoscere la configurazione del campo del video di input.

Per usare il telemetra inverso per un input per il writer, seguire questa procedura.

1.  Configurare il writer come di consueto. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md)
2.  Prima di iniziare a scrivere esempi, ottenere un puntatore [**all'interfaccia IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) chiamando **IWMWriter::QueryInterface.**
3.  Identificare il flusso da ricostruire chiamando [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per il numero di input desiderato. Passare g \_ wszDeinterlaceMode come impostazione e WM \_ DM \_ DEINTERLACE \_ INVERSETELESTRUZIONE come valore.
4.  Chiamare **di nuovo SetInputSetting** per impostare g \_ wszInitialPatternForInverseTeleinit.
5.  Scrivere il file come di consueto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




