---
title: Tipi di estensioni di esempio
description: Tipi di estensioni di esempio
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, estensioni di esempio
- Advanced Systems Format (ASF), estensioni di esempio
- ASF (Advanced Systems Format), estensioni di esempio
- Windows Media Format SDK, estensioni di unità dati
- Advanced Systems Format (ASF), estensioni unità dati
- ASF (Advanced Systems Format), estensioni unità dati
- Windows Media Format SDK, proprietà del buffer
- Advanced Systems Format (ASF), proprietà del buffer
- ASF (Advanced Systems Format), proprietà del buffer
- estensioni di esempio,tipi
- estensioni unità dati,tipi
- proprietà del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1404dfee60c3de179df2bee0f7f123112002108
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479777"
---
# <a name="sample-extension-types"></a>Tipi di estensioni di esempio

Le estensioni di esempio, denominate anche estensioni unità dati (DUE) o proprietà del buffer, sono elementi di dati collegati agli esempi di supporti nella sezione dei dati del file ASF. Diversi tipi di estensioni di esempio sono definiti in Windows Media Format SDK. È anche possibile creare tipi di estensione personalizzati.

Per usare le estensioni di esempio, è necessario identificare il tipo di estensione nei dati di configurazione del flusso del profilo. Chiamare il [**metodo IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per configurare un flusso per accettare esempi con dati estesi.

Le singole estensioni di esempio devono essere aggiunte agli esempi di input chiamando il [**metodo INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Durante la lettura degli esempi, è possibile chiamare il [**metodo INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) per recuperare i dati dell'estensione. È anche possibile usare i metodi [**dell'interfaccia INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) per enumerare le estensioni di unità dati associate a un esempio.

Nella tabella seguente sono elencati gli identificatori di estensione di unità dati predefiniti e vengono descritti i dati associati agli esempi per ognuno di essi.




| GUID dell'estensione di esempio | Descrizione | 
|-----------------------|-------------|
| WM_SampleExtensionGUID_OutputCleanPoint | I dati indicano se l'esempio è un <a href="wmformat-glossary.md"><em>oggetto cleanpoint.</em></a> Il valore zero indica che l'esempio non è un punto pulito. Un valore diverso da zero indica che si tratta di un punto pulito. Questo tipo di estensione per unità dati di esempio (DUE) viene usato per tenere traccia dei punti puliti durante la scrittura di flussi multimediali precompressi codificati con codec di terze parti. | 
| WM_SampleExtensionGUID_Timecode | I dati sono una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> che contiene dati time code SMPTE associati all'esempio. La dimensione di due è sempre WM_SampleExtension_Timecode_Size, ovvero 14 byte.<br /> | 
| WM_SampleExtensionGUID_FileName | Questo tipo di estensione di esempio viene usato per i flussi di file. I dati in un esempio di flusso di file sono una parte di un file di dati. I dati nell'estensione di esempio specificano il nome del file da cui è stato tratto il contenuto dell'esempio. Il nome file è una stringa di caratteri wide contenente il nome file nel formato name.extension senza informazioni sul percorso.<br /> | 
| WM_SampleExtensionGUID_ContentType | I dati identificano il tipo di contenuto contenuto nell'esempio. Questo tipo di estensione di esempio viene usato con flussi video interlacciati. Tutto il contenuto interlacciato usa il flag WM_CT_INTERLACED combinato da UN <strong>OR</strong> bit per bit con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.<br /> L'ordine dei campi non viene usato nel processo di codifica, ma viene gestito con gli esempi compressi in modo che possa essere passato all'hardware di rendering. La riproduzione di contenuto interlacciato con l'ordine dei campi non corretto introduce artefatti come jitter di movimento nel video.<br /> Le dimensioni di QUESTO DUE sono sempre WM_SampleExtension_ContentType_Size.<br /> | 
| WM_SampleExtensionGUID_PixelAspectRatio | I dati indicano le proporzioni in pixel del contenuto nell'esempio. Questo vale solo per i video. Questo tipo di estensione viene usato per identificare le proporzioni dei pixel non quadrati. Per altre informazioni, vedere <a href="to-read-and-write-video-streams-with-non-square-pixels.md">Per leggere e scrivere video Flussi con pixel non quadrati.</a><br /> I valori delle proporzioni vengono archiviati come una parola il cui byte basso è l'aspetto X e il cui byte alto è l'aspetto Y. Ad esempio, 16:9 viene archiviato come 0x0910.<br /> Le dimensioni di DUE sono sempre WM_SampleExtension_PixelAspectRatio_Size, ovvero 2 byte.<br /> | 
| WM_SampleExtensionGUID_SampleDuration | I dati indicano la durata, in millisecondi, del campione contenuto nell'oggetto buffer. Durante la riproduzione, se l'opzione DUE è impostata, l'oggetto lettore lo userà per sovrascrivere il valore di durata del campione esistente. Questo DUE viene impostato automaticamente dai componenti di run-time SDK nei flussi video con velocità in bit di 100 kbps o superiori, in cui il sovraccarico delle informazioni DUE non è significativo. Non è impostato per i flussi con velocità in bit inferiori a 100 kbps. Le applicazioni non devono impostare questa proprietà DUE manualmente perché il writer (nei flussi a velocità in bit elevata) sovrascriverà il valore con i propri dati.<br /> La dimensione di due byte è sempre WM_SampleExtension_SampleDuration_Size, ovvero 2 byte.<br /> | 
| WM_SampleExtensionGUID_ChromaLocation | I dati indicano il tipo di sottocampionamento chroma usato nel formato video I420. Il valore di questa estensione è impostato su uno dei valori seguenti:<br /><ul><li>WM_CL_INTERLACED420</li><li>WM_CL_PROGRESSIVE420</li></ul>Questa estensione dell'unità dati non è configurata nel profilo. È incluso nell'output degli esempi del decodificatore.<br /> Le dimensioni di QUESTO DUE sono sempre WM_SampleExtension_ChromaLocation_Size, ovvero 1 byte.<br /> | 
| WM_SampleExtensionGUID_ColorSpaceInfo | I dati forniscono informazioni sullo spazio colore usato per il fotogramma video corrente. Il valore di questa estensione è una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> struttura .<br /> Questa estensione dell'unità dati non è configurata nel profilo. È incluso nell'output degli esempi del decodificatore.<br /> Le dimensioni di DUE sono sempre WM_SampleExtension_ColorSpaceInfo_Size, ovvero 3 byte.<br /> | 
| WM_SampleExtensionGUID_UserDataInfo | I dati sono dati utente personalizzati. I primi quattro byte dei dati contengono le dimensioni dei dati personalizzati.<br /> Il byte successivo contiene il tipo di dati utente forniti nell'estensione di esempio. Sono supportati i tipi seguenti:<br /><ul><li>0x1F - Dati utente a livello di sequenza</li><li>0x1E - Dati utente a livello di punto di ingresso</li><li>0x1D - Dati utente a livello di frame</li><li>0x1C - Dati utente a livello di campo</li><li>0x1B - Dati utente a livello di sezione</li></ul>Il sesto byte e i byte successivi contengono i dati utente. Sono presenti tutti i byte di dati utente specificati dal numero nei primi quattro byte.<br /> Questa estensione dell'unità dati non è configurata nel profilo. È incluso negli esempi restituiti dal decodificatore.<br /> | 
| WM_SampleExtensionGUID_SampleProtectionSalt | I dati vengono crittografati in base all'esempio. Questo tipo di estensione di esempio viene usato per il contenuto importato da un formato di file non ASF e uno schema di protezione dei diritti diverso da Windows Media DRM. Quando si importa contenuto protetto, ogni esempio deve includere un salt univoco. In genere, questo valore è un contatore con aumento monotona.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 





