---
description: Attributi di trasformazione
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Attributi di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d5b7a5f4ff6174a48058c81fe1cdea382b18c058985da803efa4110eb12e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034563"
---
# <a name="transform-attributes"></a>Attributi di trasformazione

Gli attributi seguenti si applicano [Media Foundation trasformazioni](media-foundation-transforms.md) (MFT) [](activation-objects.md) o agli oggetti di attivazione per MFT o a entrambi.



| Attributo                                                                                                     | Descrizione                                                                                                                                                                                   | Si applica a                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ ACTIVATE \_ MFT \_ LOCKED**](mf-activate-mft-locked-attribute.md)                                         | Specifica se il caricatore della topologia modificherà i tipi di supporti in un MFT.                                                                                                                  | MFT                        |
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                                                       | Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX.                                                                                                     | MFT                        |
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                                                | Specifica se un MFT esegue l'elaborazione asincrona.                                                                                                                                    | MFT                        |
| [SBLOCCO \_ ASINCRONO MF \_ \_ TRANSFORM](mf-transform-async-unlock.md)                                                 | Abilita l'uso di un MFT asincrono.                                                                                                                                                       | MFT                        |
| [Attributo \_ MF TRANSFORM \_ CATEGORY \_](mf-transform-category-attribute.md)                                     | Specifica la categoria per un MFT.                                                                                                                                                            | Oggetti di attivazione MFT      |
| [Attributo \_ MF TRANSFORM \_ FLAGS \_](mf-transform-flags-attribute.md)                                           | Contiene flag per un oggetto di attivazione MFT.                                                                                                                                                  | Oggetti di attivazione MFT      |
| [Attributo \_ MFT CODEC \_ MERIT \_](mft-codec-merit-attribute.md)                                                 | Contiene il valore di merito di un codec hardware.                                                                                                                                                 | Oggetti di attivazione MFT      |
| [ATTRIBUTO DEL FLUSSO \_ CONNESSO \_ \_ MFT](mft-connected-stream-attribute.md)                                       | Contiene un puntatore agli attributi del flusso connesso in un MFT basato su hardware.                                                                                                  | MFT                        |
| [MFT \_ CONNESSO AL FLUSSO \_ \_ \_ HW](mft-connected-to-hw-stream.md)                                              | Specifica se un MFT basato su hardware è connesso a un altro MFT basato su hardware.                                                                                                            | MFT                        |
| [IL DECODIFICATORE MFT \_ ESPONE I TIPI DI OUTPUT IN ORDINE \_ \_ \_ \_ \_ \_ NATIVO](mft-decoder-expose-output-types-in-native-order.md) | Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcoding) prima di altri formati.                                                                                   | MFT                        |
| [SUGGERIMENTO DI RISOLUZIONE \_ \_ VIDEO FINALE DEL \_ DECODIFICATORE \_ MFT \_](mft-decoder-final-video-resolution-hint.md)                   | Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.                                                                                                           | MFT                        |
| [IL CODIFICATORE MFT \_ \_ SUPPORTA \_ L'EVENTO \_ CONFIG](mft-encoder-supports-config-event.md)                                | Specifica che il codificatore MFT supporta la ricezione di [eventi MEEncodingParameter durante](meencodingparameters.md) lo streaming.                                                                     | MFT                        |
| [LUID \_ DELL'ADAPTER DI \_ ENUMERAZIONE MFT \_](mft-enum-adapter-luid.md)                                                         | Specifica un identificatore univoco per una scheda video. Usare questo attributo quando si chiama MFTEnum2 per enumerare le MFT associate a un adattatore specifico.                                             | MFT                        |
| [Attributo URL \_ HARDWARE ENUM MFT \_ \_ \_](mft-enum-hardware-url-attribute.md)                                    | Contiene il collegamento simbolico per un MFT basato su hardware.                                                                                                                                          | Oggetti di attivazione MFT/MFT |
| [Attributo ID FORNITORE \_ HARDWARE MFT ENUM \_ \_ \_ \_](mft-enum-hardware-vendor-id-attribute.md)                       | Specifica l'ID fornitore per una trasformazione basata Media Foundation hardware                                                                                                                       | MFT                        |
| [ATTRIBUTO \_ TRANSCODE SOLO \_ DELL'ENUMERAZIONE \_ \_ MFT](mft-enum-transcode-only-attribute.md)                                | Specifica se un decodificatore è ottimizzato per la transcoding anziché per la riproduzione.                                                                                                            | MFT                        |
| [Attributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                     | Contiene un [**puntatore IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) che può essere usato per sbloccare MFT.                                                                            | Oggetti di attivazione MFT      |
| [Attributo MFT \_ FRIENDLY \_ NAME \_](mft-friendly-name-attribute.md)                                             | Contiene il nome visualizzato per un MFT basato su hardware.                                                                                                                                           | Oggetti di attivazione MFT      |
| [Attributi MFT \_ INPUT \_ TYPES \_](mft-input-types-attributes.md)                                               | Contiene i tipi di input registrati per un MFT.                                                                                                                                               | Oggetti di attivazione MFT      |
| [Attributi MFT \_ OUTPUT \_ TYPES \_](mft-output-types-attributes.md)                                             | Contiene i tipi di output registrati per un MFT.                                                                                                                                              | Oggetti di attivazione MFT      |
| [PROFILO DEL \_ CODIFICATORE PREFERITO MFT \_ \_](mft-preferred-encoder-profile.md)                                         | Contiene le proprietà di configurazione per un codificatore.                                                                                                                                             | Oggetti di attivazione MFT      |
| [Attributo MFT \_ PREFERRED \_ \_ OUTPUTTYPE](mft-preferred-outputtype-attribute.md)                               | Specifica il formato di output preferito per un codificatore.                                                                                                                                         | Oggetti di attivazione MFT      |
| [Attributo MFT \_ PREFERRED \_ \_ OUTPUTTYPE](mft-preferred-outputtype-attribute.md)                               | Specifica il formato di output preferito per un codificatore.                                                                                                                                         | Oggetti di attivazione MFT      |
| [Attributo MFT \_ PROCESS \_ \_ LOCAL](mft-process-local-attribute.md)                                             | Specifica se un MFT è registrato solo nel processo dell'applicazione.                                                                                                                     | Oggetti di attivazione MFT      |
| [MFT \_ REMUX \_ MARK \_ I \_ PICTURE \_ AS \_ CLEAN \_ POINT](mft-remux-mark-i-picture-as-clean-point.md)                 | Specifica se il MFT di remux video H.264 deve contrassegnare le immagini I come punto pulito per una migliore capacità di ricerca. Ciò può essere danneggiato nelle ricerca nei file MP4 finali non conformi. | Oggetti di attivazione MFT      |
| [SUPPORTO MFT \_ \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopico 3D.                                                                                                          | Oggetti di attivazione MFT      |
| [**MODIFICA DEL FORMATO DINAMICO DEL SUPPORTO \_ \_ \_ \_ MFT**](mft-support-dynamic-format-change-attribute.md)                  | Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche di formato dinamico.                                                                                                         | MFT                        |
| [Attributo \_ \_ CLSID MFT TRANSFORM \_](mft-transform-clsid-attribute.md)                                         | Contiene l'identificatore di classe (CLSID) di un MFT.                                                                                                                                              | Oggetti di attivazione MFT      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 



