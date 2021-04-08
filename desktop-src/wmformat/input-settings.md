---
title: Impostazioni di input
description: Impostazioni di input
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, costanti globali
- Advanced Systems Format (ASF), costanti globali
- ASF (formato avanzato dei sistemi), costanti globali
- costanti globali, elenco di
- Windows Media Format SDK, costanti
- Advanced Systems Format (ASF), costanti
- ASF (formato avanzato dei sistemi), costanti
- costanti, elenco di
- Windows Media Format SDK, impostazioni di input
- ASF (Advanced Systems Format), impostazioni di input
- ASF (formato avanzato dei sistemi), impostazioni di input
- impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046275"
---
# <a name="input-settings"></a>Impostazioni di input

Le costanti globali seguenti vengono utilizzate per identificare le impostazioni di input per il writer.



| Costante globale                        | tipo di dati \_ attr WMT \_                                                                                                                       | Descrizione di *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ Digitare \_ DWORD** impostato su uno dei valori nella tabella modalità nell'argomento [per deinterlacciare il video](to-deinterlace-video.md).            | Se impostato, specifica il tipo di contenuto interlacciato dell'input. Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **\_tipo WMT \_ bool**                                                                                                                       | Se impostato su true, indica al codec di non eliminare i frame durante la codifica. In questo modo la [*frequenza dei fotogrammi*](wmformat-glossary.md) del flusso video di output sarà costante. Non è necessario che la frequenza dei fotogrammi del flusso di input sia costante. |
| g \_ wszInitialPatternForInverseTelecine | **WMT \_ Digitare \_ DWORD** impostato su uno dei valori nella tabella dei criteri iniziali nell'argomento [per deinterlacciare il video](to-deinterlace-video.md). | Quando la modalità di deinterlacciamento è impostata su WM \_ DM \_ deinterlacciare \_ INVERSETELECINE, questo può essere impostato per specificare il modello di input di [*telecine*](wmformat-glossary.md) . Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **\_tipo WMT \_ bool**                                                                                                                       | Se impostato su true, specifica che il codec deve codificare il flusso come contenuto interlacciato. Per altre informazioni, vedere [per usare un video interlacciato](to-use-interlaced-video.md).                                                                                       |
| g \_ wszJPEGCompressionQuality           | **WMT \_ tipo \_ DWORD**                                                                                                                      | Specifica il livello di qualità JPEG (da 1 a 100) da usare per l'input.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **\_GUID di tipo WMT \_**                                                                                                                       | Il valore viene impostato sul GUID della filigrana.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **\_stringa di tipo WMT \_**                                                                                                                     | Il valore viene impostato sulla configurazione della filigrana. Questo valore varia in base al limite DMO. Per ulteriori informazioni, consultare la documentazione del sistema di filigrana.                                                                                   |



 

> [!Note]  
> Le impostazioni di input configurate per un flusso non sono salvate in modo permanente nel file scritto. Se si vuole che il lettore personalizzato abbia accesso a questi parametri di codifica, è necessario creare attributi personalizzati per archiviarli nell'intestazione del file.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




