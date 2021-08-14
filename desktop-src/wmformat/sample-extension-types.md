---
title: Tipi di estensioni di esempio
description: Tipi di estensioni di esempio
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows MEDIA Format SDK, estensioni di esempio
- Advanced Systems Format (ASF), estensioni di esempio
- ASF (Advanced Systems Format),estensioni di esempio
- Windows MEDIA Format SDK, estensioni di unità dati
- Advanced Systems Format (ASF), estensioni per unità dati
- ASF (Advanced Systems Format),estensioni unità dati
- Windows Media Format SDK, proprietà buffer
- Advanced Systems Format (ASF), proprietà del buffer
- ASF (Advanced Systems Format),proprietà buffer
- estensioni di esempio, tipi
- estensioni unità dati,tipi
- proprietà del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94161486fee7a31419f2e7fb9af2ed7fc968f00e8b43b81c58254547ec2f74e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345391"
---
# <a name="sample-extension-types"></a>Tipi di estensioni di esempio

Le estensioni di esempio, denominate anche estensioni per unità dati (DUE) o proprietà del buffer, sono elementi di dati collegati agli esempi di supporti nella sezione data del file ASF. Diversi tipi di estensioni di esempio sono definiti in Windows Media Format SDK. È anche possibile creare tipi di estensione personalizzati.

Per usare estensioni di esempio, è necessario identificare il tipo di estensione nei dati di configurazione del flusso del profilo. Chiamare il [**metodo IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per configurare un flusso per accettare esempi con dati estesi.

È necessario aggiungere singole estensioni di esempio agli esempi di input chiamando il [**metodo INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Durante la lettura degli esempi, è possibile chiamare il [**metodo INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) per recuperare i dati dell'estensione. È anche possibile usare i metodi [**dell'interfaccia INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) per enumerare le estensioni delle unità dati associate a un esempio.

Nella tabella seguente sono elencati gli identificatori di estensione per unità dati predefiniti e vengono descritti i dati associati agli esempi per ognuno di essi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID dell'estensione di esempio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>I dati indicano se l'esempio è un <a href="wmformat-glossary.md"><em>punto di pulizia.</em></a> Il valore zero indica che il campione non è un punto di pulizia. Un valore diverso da zero indica che si tratta di un punto pulito. Questo tipo di estensione per unità dati di esempio (DUE) viene usato per tenere traccia dei punti di pulizia durante la scrittura di flussi multimediali precompressi codificati con codec di terze parti.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>I dati sono una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>struttura WMT_TIMECODE_EXTENSION_DATA</strong></a> contenente dati SMPTE time code dati associati all'esempio. La dimensione di due è sempre WM_SampleExtension_Timecode_Size, ovvero 14 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Questo tipo di estensione di esempio viene usato per i flussi di file. I dati in un esempio di flusso di file sono una parte di un file di dati. I dati nell'estensione di esempio specificano il nome del file da cui è stato prelevato il contenuto dell'esempio. Il nome file è una stringa di caratteri wide contenente il nome file nel formato name.extension senza informazioni sul percorso.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>I dati identificano il tipo di contenuto contenuto nell'esempio. Questo tipo di estensione di esempio viene usato con i flussi video interlacciati. Tutto il contenuto interlacciato usa il flag WM_CT_INTERLACED <strong></strong> combinato da un OR bit per bit con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.<br/> L'ordine dei campi non viene usato nel processo di codifica, ma viene mantenuto con gli esempi compressi in modo che possa essere passato all'hardware di rendering. La riproduzione di contenuto interlacciato con l'ordine dei campi non corretto introduce artefatti come l'instabilità del movimento nel video.<br/> Le dimensioni per questo due sono sempre WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>I dati indicano le proporzioni in pixel del contenuto nell'esempio. Si applica solo ai video. Questo tipo di estensione viene usato per identificare le proporzioni dei pixel non quadrati. Per altre informazioni, vedere <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Flussi with Non-Square Pixels</a>(Per leggere e scrivere video con pixel non quadrati).<br/> I valori delle proporzioni vengono archiviati come parola il cui byte basso è l'aspetto X e il cui byte massimo è l'aspetto Y. Ad esempio, 16:9 viene archiviato come 0x0910.<br/> La dimensione di due è sempre WM_SampleExtension_PixelAspectRatio_Size, ovvero 2 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>I dati indicano la durata, in millisecondi, del campione contenuto nell'oggetto buffer. Durante la riproduzione, se l'opzione DUE è impostata, l'oggetto lettore lo userà per sovrascrivere il valore di durata del campione esistente. L'opzione DUE viene impostata automaticamente dai componenti di run-time dell'SDK nei flussi video con velocità in bit di 100 kbps o superiori, in cui il sovraccarico delle informazioni due non è significativo. Non è impostato per i flussi con velocità in bit inferiori a 100 kbps. Le applicazioni non devono impostare questa proprietà manualmente perché il writer (su flussi a velocità in bit elevata) sovrascriverà il valore con i propri dati.<br/> La dimensione di due è sempre WM_SampleExtension_SampleDuration_Size, ovvero 2 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>I dati indicano il tipo di sottocampionamento chroma usato nel formato video I420. Il valore di questa estensione è impostato su uno dei valori seguenti:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Questa estensione dell'unità dati non è configurata nel profilo. È incluso nell'output degli esempi del decodificatore.<br/> La dimensione di due è sempre WM_SampleExtension_ChromaLocation_Size, ovvero 1 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>I dati forniscono informazioni sullo spazio colore usato per il fotogramma video corrente. Il valore di questa estensione è una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> struttura .<br/> Questa estensione dell'unità dati non è configurata nel profilo. È incluso nell'output degli esempi del decodificatore.<br/> La dimensione di due è sempre WM_SampleExtension_ColorSpaceInfo_Size, ovvero 3 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>I dati sono dati utente personalizzati. I primi quattro byte dei dati contengono le dimensioni dei dati personalizzati.<br/> Il byte successivo contiene il tipo di dati utente forniti nell'estensione di esempio. Sono supportati i tipi seguenti:<br/>
<ul>
<li>0x1F- Dati utente a livello di sequenza</li>
<li>0x1E- Dati utente a livello di punto di ingresso</li>
<li>0x1D - Dati utente a livello di frame</li>
<li>0x1C- Dati utente a livello di campo</li>
<li>0x1B - Dati utente a livello di sezione</li>
</ul>
Il sesto byte e i byte successivi contengono i dati utente. Sono presenti tutti i byte di dati utente specificati dal numero nei primi quattro byte.<br/> Questa estensione dell'unità dati non è configurata nel profilo. È incluso negli esempi restituiti dal decodificatore.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>I dati vengono crittografati da sample. Questo tipo di estensione di esempio viene usato per il contenuto importato da un formato di file non ASF e uno schema di protezione dei diritti diverso da Windows Media DRM. Quando si importa contenuto protetto, ogni esempio deve includere un salt univoco. In genere, questo valore è un contatore a incremento costante.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 





