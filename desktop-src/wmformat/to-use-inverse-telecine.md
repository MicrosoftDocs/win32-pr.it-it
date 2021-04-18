---
title: Per usare il telecine inverso
description: Per usare il telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, telecine inversa
- Windows Media Format SDK, telecine
- ASF (Advanced Systems Format), telecine inversa
- ASF (formato avanzato dei sistemi), telecine inversa
- Formato di sistemi avanzati (ASF), telecine
- ASF (formato avanzato dei sistemi), telecine
- Telecine inversa
- telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299521"
---
# <a name="to-use-inverse-telecine"></a>Per usare il telecine inverso

La telecine è il processo di conversione di film, che include 24 fotogrammi al secondo, in video, con 60 campi (metà fotogrammi) al secondo. Questo processo inserisce le immagini da ogni fotogramma di film in più campi video.

Quando si codifica digitalmente un video creato da un film usando la telecine, il processo di compressione può causare la qualità degli artefatti di movimento e di altre riduzioni. Per evitare di influire sulla qualità dell'output digitale, il codec Windows Media Video 9 supporta la telecine inversa. Quando si usa la telecine inversa, il codec ricostruisce i 24 fotogrammi originali al secondo dal video di input prima di codificare il contenuto.

Per utilizzare la telecine inversa, è necessario:

-   Usare un profilo con un flusso video impostato su 24 fotogrammi al secondo.
-   Conosce la configurazione del campo del video di input.

Per utilizzare la telecine per un input per il writer, seguire questa procedura.

1.  Configurare il writer come di consueto. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).
2.  Prima di iniziare a scrivere esempi, ottenere un puntatore all'interfaccia [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) chiamando **IWMWriter:: QueryInterface**.
3.  Identificare il flusso da ricostruire chiamando [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per il numero di input desiderato. Passare g \_ wszDeinterlaceMode come impostazione e WM \_ DM \_ deinterlacciare \_ INVERSETELECINE come valore.
4.  Chiamare nuovamente **SetInputSetting** per impostare g \_ wszInitialPatternForInverseTelecine.
5.  Scrivere il file come di consueto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




