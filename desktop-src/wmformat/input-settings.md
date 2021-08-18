---
title: Input Impostazioni
description: Input Impostazioni
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, costanti globali
- Advanced Systems Format (ASF), costanti globali
- ASF (Advanced Systems Format), costanti globali
- costanti globali, elenco di
- Windows Media Format SDK,costanti
- Advanced Systems Format (ASF), costanti
- ASF (Advanced Systems Format), costanti
- costanti, elenco di
- Windows Media Format SDK, impostazioni di input
- Advanced Systems Format (ASF), impostazioni di input
- ASF (Advanced Systems Format), impostazioni di input
- impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad72a8a5cc70dc28dcaa7be1e24b721e0b3f644e7694ea5c00d87ba2418846a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701806"
---
# <a name="input-settings"></a>Input Impostazioni

Le costanti globali seguenti vengono usate per identificare le impostazioni di input per il writer.



| Costante globale                        | TIPO DI \_ DATI WMT ATTR \_                                                                                                                       | Descrizione di *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ TYPE \_ DWORD** impostato su uno dei valori nella tabella mode nell'argomento [To Deinterlace Video](to-deinterlace-video.md).            | Se impostato, specifica il tipo di contenuto interlacciato dell'input. Per altre informazioni, vedere [To Deinterlace Video](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Se impostato su True, indica al codec di non rilasciare fotogrammi durante la codifica. In questo modo la [*frequenza dei*](wmformat-glossary.md) fotogrammi del flusso video di output sarà costante. La frequenza dei fotogrammi del flusso di input non deve essere costante. |
| g \_ wszInitialPatternForInverseTelecine | **WMT \_ TYPE \_ DWORD** impostato su uno dei valori nella tabella dei criteri iniziale nell'argomento [To Deinterlace Video](to-deinterlace-video.md). | Quando la modalità deinterlace è impostata su WM \_ DM \_ DEINTERLACE INVERSETELECINE, questa opzione può essere impostata per specificare il \_ modello dell'input [*telecina.*](wmformat-glossary.md) Per altre informazioni, vedere [To Deinterlace Video](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Se impostato su True, specifica che il codec deve codificare il flusso come contenuto interlacciato. Per altre informazioni, vedere [Per usare video interlacciato.](to-use-interlaced-video.md)                                                                                       |
| g \_ wszJPEGCompressionQuality           | **DWORD \_ DI TIPO \_ WMT**                                                                                                                      | Specifica il livello di qualità JPEG (da 1 a 100) da usare nell'input.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **GUID DEL \_ TIPO \_ WMT**                                                                                                                       | Il valore è impostato sul GUID del limite.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **STRINGA DI TIPO WMT \_ \_**                                                                                                                     | Il valore è impostato sulla configurazione del limite. Questo valore varia a seconda del limite DMO. Per altre informazioni, vedere la documentazione del sistema di filigrane.                                                                                   |



 

> [!Note]  
> Le impostazioni di input configurate per un flusso non vengono rese persistenti nel file scritto. Se si vuole che il lettore personalizzato abbia accesso a questi parametri di codifica, è necessario creare attributi personalizzati per archiviarli nell'intestazione del file.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




