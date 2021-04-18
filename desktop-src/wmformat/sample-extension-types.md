---
title: Tipi di estensioni di esempio
description: Tipi di estensioni di esempio
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, estensioni di esempio
- ASF (Advanced Systems Format), estensioni di esempio
- ASF (formato avanzato dei sistemi), estensioni di esempio
- Windows Media Format SDK, estensioni di unità dati
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- Windows Media Format SDK, proprietà del buffer
- ASF (Advanced Systems Format), proprietà del buffer
- ASF (formato avanzato dei sistemi), proprietà del buffer
- estensioni di esempio, tipi
- estensioni unità dati, tipi
- Proprietà buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "106299537"
---
# <a name="sample-extension-types"></a>Tipi di estensioni di esempio

Le estensioni di esempio, denominate anche estensioni di unità dati (quote) o proprietà del buffer, sono elementi di dati allegati agli esempi di supporti nella sezione dati del file ASF. In Windows Media Format SDK sono definiti diversi tipi di estensioni di esempio. È anche possibile creare i propri tipi di estensione.

Per usare le estensioni di esempio, è necessario identificare il tipo di estensione nei dati di configurazione del flusso del profilo. Chiamare il metodo [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per configurare un flusso in modo che accetti esempi con dati estesi.

È necessario aggiungere singole estensioni di esempio agli esempi di input chiamando il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Quando si leggono gli esempi, è possibile chiamare il metodo [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) per recuperare i dati dell'estensione. È inoltre possibile utilizzare i metodi dell'interfaccia [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) per enumerare le estensioni dell'unità dati associate a un esempio.

Nella tabella seguente sono elencati gli identificatori di estensione di unità dati predefiniti e vengono descritti i dati allegati agli esempi per ciascuno di essi.



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
<td>I dati indicano se l'esempio è un <a href="wmformat-glossary.md"><em>cleanpoint</em></a>. Un valore pari a zero indica che l'esempio non è un cleanpoint. Un valore diverso da zero indica che si tratta di un cleanpoint. Questo tipo di estensione di unità dati di esempio viene usato per tenere traccia di cleanpoints durante la scrittura di flussi multimediali precompressi che sono stati codificati con codec di terze parti.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>I dati sono una struttura di <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> contenente i dati del codice Time SMPTE associati all'esempio. Le dimensioni di questa operazione sono sempre WM_SampleExtension_Timecode_Size, ovvero 14 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Questo tipo di estensione di esempio viene usato per i flussi di file. I dati in un esempio di flusso di file sono una parte di un file di dati. I dati nell'estensione di esempio specificano il nome del file da cui è stato utilizzato il contenuto del campione. Il nome del file è una stringa di caratteri wide contenente il nome del file in formato nome. estensione senza informazioni sul percorso.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>I dati identificano il tipo di contenuto contenuto nell'esempio. Questo tipo di estensione di esempio viene usato con i flussi video interlacciati. Tutto il contenuto interlacciato usa il flag di WM_CT_INTERLACED combinato da <strong>un operatore OR</strong> bit per bit con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.<br/> L'ordine dei campi non viene utilizzato nel processo di codifica, ma viene mantenuto con gli esempi compressi, in modo che possa essere passato all'hardware di rendering. La riproduzione di contenuto interlacciato con l'ordine dei campi errato introduce elementi come l'instabilità del movimento nel video.<br/> Le dimensioni di questa operazione sono sempre WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>I dati indicano le proporzioni in pixel del contenuto nell'esempio. Questo vale solo per i video. Questo tipo di estensione viene utilizzato per identificare le proporzioni dei pixel non quadrati. Per altre informazioni, vedere <a href="to-read-and-write-video-streams-with-non-square-pixels.md">per leggere e scrivere flussi video con pixel non quadrati</a>.<br/> I valori delle proporzioni vengono archiviati come una parola il cui byte minimo è l'aspetto X e il cui byte elevato è l'aspetto Y. Ad esempio, 16:9 viene archiviato come 0x0910.<br/> Le dimensioni di questa operazione sono sempre WM_SampleExtension_PixelAspectRatio_Size, ovvero 2 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>I dati indicano la durata, in millisecondi, dell'esempio contenuto nell'oggetto buffer. In caso di riproduzione, se il valore è impostato, l'oggetto Reader lo userà per sovrascrivere il valore di durata campione esistente. Questa causa viene impostata automaticamente dai componenti di Runtime SDK sui flussi video con velocità in bit di 100 kbps o superiore, in cui il sovraccarico delle informazioni non è significativo. Non è impostato per i flussi con velocità in bit inferiore a 100 kbps. Poiché il writer (nei flussi a velocità elevata) sovrascriverà il valore con i propri dati, le applicazioni non devono impostare questa funzione.<br/> Le dimensioni di questa operazione sono sempre WM_SampleExtension_SampleDuration_Size, ovvero 2 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>I dati indicano il tipo di sottocampionamento Chroma usato nel formato video I420. Il valore di questa estensione è impostato su uno dei valori seguenti:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Questa estensione di unità dati non è configurata nel profilo. È incluso nell'output degli esempi dal decodificatore.<br/> La dimensione di questa operazione è sempre WM_SampleExtension_ChromaLocation_Size, ovvero 1 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>I dati forniscono informazioni sullo spazio di colore usato per il frame video corrente. Il valore di questa estensione è una struttura <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .<br/> Questa estensione di unità dati non è configurata nel profilo. È incluso nell'output degli esempi dal decodificatore.<br/> La dimensione di questa operazione è sempre WM_SampleExtension_ColorSpaceInfo_Size, ovvero 3 byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>I dati sono dati utente personalizzati. I primi quattro byte dei dati contengono la dimensione dei dati personalizzati.<br/> Il byte successivo contiene il tipo di dati utente specificati nell'estensione di esempio. Sono supportati i tipi seguenti:<br/>
<ul>
<li>0x1F-dati utente a livello di sequenza</li>
<li>0x1E-dati utente a livello di punto di ingresso</li>
<li>0x1D-dati utente a livello di frame</li>
<li>0x1C-dati utente a livello di campo</li>
<li>0x1B-dati utente a livello di sezione</li>
</ul>
Il sesto e i byte successivi contengono i dati dell'utente. Sono presenti molti byte di dati utente specificati dal numero nei primi quattro byte.<br/> Questa estensione di unità dati non è configurata nel profilo. È incluso negli esempi di output del decodificatore.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>I dati vengono crittografati in base all'esempio. Questo tipo di estensione di esempio viene utilizzato per il contenuto importato da un formato di file non ASF e uno schema di protezione dei diritti diverso da Windows Media DRM. Quando si importa contenuto protetto, ogni esempio deve includere un valore salt univoco. In genere, questo valore è un contatore a incremento progressivo costante.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 





