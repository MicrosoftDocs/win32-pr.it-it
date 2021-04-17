---
description: Attributi di esempio
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Attributi di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527841"
---
# <a name="sample-attributes"></a>Attributi di esempio

Gli attributi seguenti si applicano agli [esempi di supporti](media-samples.md). Per ottenere gli attributi da un esempio multimediale, usare l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Attributo                                                                                                      | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_3DVideo MFSampleExtension](mfsampleextension-3dvideo.md)                                                    | Specifica se un esempio multimediale contiene un frame video 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Specifica il modo in cui un frame video 3D viene archiviato in un esempio di supporto.                                                                                                                                                                                        |
| [**\_BottomFieldFirst MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Specifica la dominanza del campo per un fotogramma video interlacciato.                                                                                                                                                                                       |
| [\_CameraExtrinsics MFSampleExtension](mfsampleextension-cameraextrinsics.md)                                  | La fotocamera estrinseca per l'esempio.                                                                                                                                                                                                              |
| [\_CaptureMetadata MFSampleExtension](mfsampleextension-capturemetadata.md)                                    | Archivio [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per tutti i metadati correlati alla pipeline di acquisizione.                                                                                                                                             |
| [**\_CleanPoint MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md)                                | Indica se un campione video è un fotogramma chiave.                                                                                                                                                                                                   |
| [\_KeyId contenuto \_ MFSampleExtension](mfsampleextension-content-keyid.md)                                       | Imposta l'ID chiave per l'esempio.                                                                                                                                                                                                                    |
| [**\_DerivedFromTopField MFSampleExtension**](mfsampleextension-derivedfromtopfield-attribute.md)              | Specifica se un fotogramma video deinterlacciato è stato derivato dal campo superiore o dal campo inferiore.                                                                                                                                                  |
| [\_DeviceTimestamp MFSampleExtension](mfsampleextension-devicetimestamp.md)                                    | Timestamp del driver di dispositivo.                                                                                                                                                                                                             |
| [**\_Discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md)                          | Specifica se un esempio di supporto è il primo campione dopo un gap nel flusso.                                                                                                                                                                    |
| [\_CryptByteBlock di crittografia MFSampleExtension \_](mfsampleextension-encryption-cryptbyteblock.md)               | Specifica la dimensione del blocco di byte crittografato per la crittografia del modello basata su campione.                                                                                                                                                                       |
| [\_ProtectionScheme di crittografia MFSampleExtension \_](mfsampleextension-encryption-protectionscheme.md)           | Specifica lo schema di protezione per gli esempi crittografati.                                                                                                                                                                                             |
| [\_SampleId di crittografia MFSampleExtension \_](mfsampleextension-encryption-sampleid.md)                           | Specifica l'ID di un campione crittografato.                                                                                                                                                                                                           |
| [\_SkipByteBlock di crittografia MFSampleExtension \_](mfsampleextension-encryption-skipbyteblock.md)                 | Specifica la dimensione del blocco di byte cancellata (non crittografata) per la crittografia dei modelli basata sul campione.                                                                                                                                                           |
| [\_SubSampleMappingSplit di crittografia MFSampleExtension \_](mfsampleextension-encryption-subsamplemappingsplit.md) | Imposta il mapping dei sottocampionamenti per l'esempio che indica i byte cancellati e crittografati nei dati di esempio.                                                                                                                                            |
| [\_FrameCorruption MFSampleExtension](mfsampleextension-framecorruption.md)                                    | Specifica se un frame video è danneggiato.                                                                                                                                                                                                      |
| [\_ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md)                          | Ottiene un oggetto di tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenente gli oggetti [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che contengono le unità di astrazione del livello di rete (NALUs) e le informazioni sul miglioramento supplementare (sei) che vengono trasmesse da un decodificatore. |
| [\_ForwardedDecodeUnitType MFSampleExtension](mfsampleextension-forwardeddecodeunittype.md)                    | Specifica il tipo, NALU o SEI, di un'unità collegata a un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una raccolta di [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .                                                    |
| [**MFSampleExtension \_ interlacciato**](mfsampleextension-interlaced-attribute.md)                                | Indica se un frame video è interlacciato o progressivo.                                                                                                                                                                                      |
| [\_LongTermReferenceFrameInfo MFSampleExtension](mfsampleextension-longtermreferenceframeinfo.md)              | Specifica le informazioni del frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.                                                                                                                                                               |
| [\_MeanAbsoluteDifference MFSampleExtension](mfsampleextension-meanabsolutedifference.md)                      | Questo attributo restituisce la differenza assoluta media (MAD) in tutti i blocchi di macro nel piano Y.                                                                                                                                                  |
| [**\_PacketCrossOffsets MFSampleExtension**](mfsampleextension-packetcrossoffsets-attribute.md)                | Specifica i limiti del payload per un frame. Questo vale per gli esempi crittografati.                                                                                                                                                                   |
| [Anteprima di MFSampleExtension \_](mfsampleextension-photothumbnail.md)                                      | Contiene l'anteprima della foto di un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [\_PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md)                    | Contiene [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che descrive il tipo di formato di immagine contenuto nell'attributo di [ \_ Anteprima MFSampleExtension](mfsampleextension-photothumbnail.md) .                                                      |
| [\_PinholeCameraIntrinsics MFSampleExtension](mfsampleextension-pinholecameraintrinsics.md)                    | Funzioni intrinseche della fotocamera pinhole per l'esempio.                                                                                                                                                                                                      |
| [**\_RepeatFirstField MFSampleExtension**](mfsampleextension-repeatfirstfield-attribute.md)                    | Specifica se ripetere il primo campo in un frame interlacciato.                                                                                                                                                                                |
| [\_ROIRectangle MFSampleExtension](mfsampleextension-roirectangle.md)                                          | Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.                                                                                                                            |
| [**\_SingleField MFSampleExtension**](mfsampleextension-singlefield-attribute.md)                              | Specifica se un esempio video contiene un solo campo o due campi con interfoliazione                                                                                                                                                                 |
| [\_TargetGlobalLuminance MFSampleExtension](mfsampleextension-targetgloballuminance.md)                        | Valore in nit che specifica la luminanza della retroilluminazione globale di destinazione per il frame video associato.                                                                                                                                           |
| [**\_Token MFSampleExtension**](mfsampleextension-token-attribute.md)                                          | Contiene un puntatore al token fornito al metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .                                                                                                             |
| [\_VideoEncodePictureType MFSampleExtension](mfsampleextension-videoencodepicturetype.md)                      | Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.                                                                                                                            |
| [\_VideoEncodeQP MFSampleExtension](mfsampleextension-videoencodeqp.md)                                        | Specifica il parametro di quantizzazione (QP) usato per codificare un campione video.                                                                                                                                                                  |



 

Non tutti gli esempi di supporti contengono tutti gli attributi elencati di seguito. In alcuni casi, un attributo si applica solo a determinati tipi di dati. Alcuni attributi, ad esempio, si applicano solo agli esempi video e non devono essere visualizzati in esempi audio. In altri casi, l'attributo ha un valore predefinito che viene applicato se l'attributo non è impostato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 



