---
description: Attributi di esempio
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Attributi di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56593978a411b314e6e988c031ee36869c4ea44212fd7f154e3ba18478400b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776981"
---
# <a name="sample-attributes"></a>Attributi di esempio

Gli attributi seguenti si applicano a [Media Samples.](media-samples.md) Per ottenere gli attributi da un esempio multimediale, usare [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| Attributo                                                                                                      | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Specifica se un campione multimediale contiene un fotogramma video 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Specifica la modalità di archiviazione di un fotogramma video 3D in un campione multimediale.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Specifica la dominanza del campo per un fotogramma video interlacciato.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | Estrinsics della fotocamera per l'esempio.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | Archivio [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per tutti i metadati correlati alla pipeline di acquisizione.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indica se un campione video è un fotogramma chiave.                                                                                                                                                                                                   |
| [MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)                                       | Imposta l'ID chiave per l'esempio.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Specifica se un fotogramma video con risoluzione deinterlaced è stato derivato dal campo superiore o dal campo inferiore.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Timestamp del driver di dispositivo.                                                                                                                                                                                                             |
| [**Discontinuità di MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md)                          | Specifica se un campione multimediale è il primo campione dopo un gap nel flusso.                                                                                                                                                                    |
| [Crittografia MFSampleExtension \_ \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Specifica le dimensioni del blocco di byte crittografato per la crittografia basata su modelli basati su campioni.                                                                                                                                                                       |
| [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Specifica lo schema di protezione per gli esempi crittografati.                                                                                                                                                                                             |
| [MFSampleExtension \_ Encryption \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Specifica l'ID di un esempio crittografato.                                                                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Specifica le dimensioni del blocco di byte non crittografate per la crittografia basata su modelli basati su campioni.                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Imposta il mapping del sotto-campione per l'esempio che indica i byte non crittografati e non crittografati nei dati di esempio.                                                                                                                                            |
| [Frame \_ MFSampleExtensionCorruption](mfsampleextension-framecorruption.md)                                    | Specifica se un fotogramma video è danneggiato.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Ottiene un oggetto di tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenente oggetti [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che contengono unità del livello di astrazione di rete (NALU) e unità SEI (Supplemental Enhancement Information) inoltrate da un decodificatore. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Specifica il tipo, NALU o SEI, di un'unità collegata a [**un oggetto IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una [raccolta MFSampleExtension \_ ForwardedDecodeUnits.](mfsampleextension-forwardeddecodeunits.md)                                                    |
| [**Interlacciato MFSampleExtension \_**](mfsampleextension-interlaced-attribute.md)                                | Indica se un fotogramma video è interlacciato o progressivo.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Specifica le informazioni sui fotogrammi di riferimento a lungo termine e viene restituito nell'esempio di output.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Questo attributo restituisce la differenza media assoluta (MAD) in tutti i macro-blocchi nel piano Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Specifica i limiti del payload per un frame. Questo vale per gli esempi crittografati.                                                                                                                                                                   |
| [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)                                      | Contiene l'anteprima di una foto di [**un oggetto IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contiene [**L'elemento IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che descrive il tipo di formato dell'immagine contenuto [nell'attributo MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | Intrinseci della fotocamera pin tunnel per l'esempio.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Specifica se ripetere il primo campo in un frame interlacciato.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Specifica i limiti dell'area di interesse che indica l'area del frame che richiede qualità diversa.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Specifica se un campione video contiene un singolo campo o due campi interleaved                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Valore in Nits che specifica la luminazione della retroilluminazione globale di destinazione per il fotogramma video associato.                                                                                                                                           |
| [**MFSampleExtension \_ Token**](mfsampleextension-token-attribute.md)                                          | Contiene un puntatore al token fornito al [**metodo IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Specifica i limiti dell'area di interesse che indica l'area del frame che richiede qualità diversa.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Specifica il parametro di quantizzazione usato per codificare un campione video.                                                                                                                                                                  |



 

Non tutti gli esempi di supporti contengono tutti gli attributi elencati qui. In alcuni casi, un attributo si applica solo a determinati tipi di dati. Ad esempio, alcuni attributi si applicano solo agli esempi video e non devono essere visualizzati nei campioni audio. In altri casi, l'attributo ha un valore predefinito che si applica se l'attributo non è impostato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 



