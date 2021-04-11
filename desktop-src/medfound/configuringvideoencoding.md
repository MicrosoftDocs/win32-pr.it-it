---
description: Configurazione della codifica video
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configurazione della codifica video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127950"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configurazione della codifica video (Microsoft Media Foundation)

Per configurare il codificatore video, seguire questa procedura:

1.  Impostare le proprietà del codificatore DMO usando **IPropertyBag:: Write**. Nell'elenco seguente viene riepilogato il set minimo di proprietà necessarie per codificare un flusso video CBR (per tutti questi valori sono disponibili impostazioni predefinite che è possibile utilizzare):

    -   La[proprietà \_ VIDEOWINDOW di MFPKEY](mfpkey-videowindowproperty.md) specifica la finestra del buffer da usare per il flusso. Per ulteriori informazioni sull'impostazione di Windows del buffer e sul relativo impatto sul contenuto, vedere [metodi di codifica](encodingmethods.md). La finestra buffer predefinita è di tre secondi, che è appropriata per molti scenari.
    -   La complessità del video viene impostata in modo da determinare il compromesso tra la qualità del contenuto codificato e il tempo necessario per la codifica. Se non si imposta un valore, viene utilizzato il valore predefinito. Tuttavia, è possibile trovare le modalità consigliate per un codec specifico chiamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) per recuperare g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline e g \_ wszWMVCComplexityExMax. È quindi possibile impostare [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) su un valore compreso tra 0 e la massima complessità indicata.
    -   [MFPKEY \_ CRISP](mfpkey-crispproperty.md) specifica l'importanza relativa della fluidità del video e la qualità dell'immagine dei frame codificati. Nella maggior parte dei casi, il valore predefinito funziona correttamente.
    -   Per il contenuto video archiviato in un contenitore diverso da ASF, la proprietà [ \_ ASFOVERHEADPERFRAME di MFPKEY](mfpkey-asfoverheadperframeproperty.md) deve essere impostata su 0. Questo non è il valore predefinito.

    Per informazioni sulla configurazione dei flussi VBR, vedere [using VBR Encoding](usingvbrencoding.md).

2.  Configurare la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) per il tipo di input o, se si usa l'SDK Media Foundation, usare la funzione [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Usare una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) che descrive il contenuto di input non compresso. Il codec non ridimensiona il video o converte lo spazio colore.
3.  Impostare il tipo di input usando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) o [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configurare il tipo di output per il codificatore. Dopo aver impostato il tipo di input, il codificatore enumera i tipi di output completi, ad eccezione del membro **dwBitrate** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) dell'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Se si recupera un tipo di output prima di impostare un tipo di input, alla struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) recapitato non sarà associato alcun **VIDEOINFOHEADER**.
5.  Recuperare i dati privati del codec e aggiungerli alla struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) passata alla struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) o a [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype). Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).
6.  Impostare il tipo di output chiamando il metodo [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) o [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Passare la struttura [**del \_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) con la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) completata (inclusi i dati privati aggiunti) a cui viene fatto riferimento nel membro **pbFormat** o costruire un [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chiamando [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> L'oggetto Video Encoder supporta due output. Il secondo output è per il codificatore "post-visualizzazione". Recapita gli esempi non compressi perché verranno recapitati dal decodificatore. In questo modo è possibile monitorare la qualità della codifica senza dover attendere l'elaborazione dell'intero flusso. Questo output è facoltativo. Se si vuole usarlo, configurare il tipo seguendo lo stesso processo usato per impostare il tipo di input del codificatore.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
