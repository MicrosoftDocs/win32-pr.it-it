---
description: Attributi di trasformazione
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Attributi di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485340"
---
# <a name="transform-attributes"></a>Attributi di trasformazione

Gli attributi seguenti si applicano alle [trasformazioni Media Foundation](media-foundation-transforms.md) (MFTS) o agli [oggetti attivazione](activation-objects.md) per MFTS o a entrambi.



| Attributo                                                                                                     | Descrizione                                                                                                                                                                                   | Si applica a                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ Activate \_ MFT \_ bloccato**](mf-activate-mft-locked-attribute.md)                                         | Specifica se il caricatore della topologia modificherà i tipi di supporto in un MFT.                                                                                                                  | MFTs                        |
| [**\_Compatibile con \_ D3D \_**](mf-sa-d3d-aware-attribute.md)                                                       | Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX.                                                                                                     | MFTs                        |
| [MF \_ trasforma \_ asincrono](mf-transform-async.md)                                                                | Specifica se un MFT esegue l'elaborazione asincrona.                                                                                                                                    | MFTs                        |
| [MF \_ trasforma \_ Async \_ sblocco](mf-transform-async-unlock.md)                                                 | Consente l'uso di un MFT asincrono.                                                                                                                                                       | MFTs                        |
| [\_Attributo di \_ categoria MF Transform \_](mf-transform-category-attribute.md)                                     | Specifica la categoria per un MFT.                                                                                                                                                            | Oggetti attivazione MFT      |
| [\_Attributo MF Transform \_ flags \_](mf-transform-flags-attribute.md)                                           | Contiene i flag per un oggetto di attivazione MFT.                                                                                                                                                  | Oggetti attivazione MFT      |
| [\_ \_ Attributo Merit codec \_ MFT](mft-codec-merit-attribute.md)                                                 | Contiene il valore Merit di un codec hardware.                                                                                                                                                 | Oggetti attivazione MFT      |
| [\_ \_ attributo flusso connesso \_ MFT](mft-connected-stream-attribute.md)                                       | Contiene un puntatore agli attributi del flusso del flusso connesso in una MFT basata su hardware.                                                                                                  | MFTs                        |
| [MFT \_ connesso \_ al \_ \_ flusso HW](mft-connected-to-hw-stream.md)                                              | Specifica se una MFT basata su hardware è connessa a un'altra MFT basata su hardware.                                                                                                            | MFTs                        |
| [il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output in \_ \_ ordine nativo](mft-decoder-expose-output-types-in-native-order.md) | Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.                                                                                   | MFTs                        |
| [\_hint per \_ la \_ risoluzione video finale \_ del decodificatore MFT \_](mft-decoder-final-video-resolution-hint.md)                   | Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.                                                                                                           | MFTs                        |
| [il \_ codificatore MFT \_ supporta l' \_ \_ evento config](mft-encoder-supports-config-event.md)                                | Specifica che il codificatore MFT supporta la ricezione di eventi [MEEncodingParameter](meencodingparameters.md) durante il flusso.                                                                     | MFTs                        |
| [\_LUID dell' \_ adapter di enumerazione MFT \_](mft-enum-adapter-luid.md)                                                         | Specifica un identificatore univoco per una scheda video. Utilizzare questo attributo quando si chiama MFTEnum2 per enumerare MFTs associate a un adapter specifico.                                             | MFTs                        |
| [\_ \_ \_ Attributo URL hardware dell'enumerazione MFT \_](mft-enum-hardware-url-attribute.md)                                    | Contiene il collegamento simbolico per una MFT basata su hardware.                                                                                                                                          | Oggetti attivazione MFTs/MFT |
| [\_ \_ \_ \_ Attributo ID fornitore hardware dell'enumerazione MFT \_](mft-enum-hardware-vendor-id-attribute.md)                       | Specifica l'ID fornitore per una trasformazione Media Foundation basata su hardware                                                                                                                       | MFTs                        |
| [\_ \_ attributo solo transcodifica dell'enumerazione \_ MFT \_](mft-enum-transcode-only-attribute.md)                                | Specifica se un decodificatore è ottimizzato per la transcodifica anziché per la riproduzione.                                                                                                            | MFTs                        |
| [\_Attributo di \_ sblocco \_ FIELDOFUSE MFT](mft-fieldofuse-unlock-attribute.md)                                     | Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che può essere usato per sbloccare il MFT.                                                                            | Oggetti attivazione MFT      |
| [\_Attributo nome descrittivo MFT \_ \_](mft-friendly-name-attribute.md)                                             | Contiene il nome visualizzato per una MFT basata su hardware.                                                                                                                                           | Oggetti attivazione MFT      |
| [\_Attributi di \_ tipi di input MFT \_](mft-input-types-attributes.md)                                               | Contiene i tipi di input registrati per un MFT.                                                                                                                                               | Oggetti attivazione MFT      |
| [\_Attributi di \_ tipi di output MFT \_](mft-output-types-attributes.md)                                             | Contiene i tipi di output registrati per un MFT.                                                                                                                                              | Oggetti attivazione MFT      |
| [\_profilo del \_ codificatore preferito MFT \_](mft-preferred-encoder-profile.md)                                         | Contiene le proprietà di configurazione per un codificatore.                                                                                                                                             | Oggetti attivazione MFT      |
| [\_ \_ Attributo OUTPUTTYPE preferito \_ MFT](mft-preferred-outputtype-attribute.md)                               | Specifica il formato di output preferito per un codificatore.                                                                                                                                         | Oggetti attivazione MFT      |
| [\_ \_ Attributo OUTPUTTYPE preferito \_ MFT](mft-preferred-outputtype-attribute.md)                               | Specifica il formato di output preferito per un codificatore.                                                                                                                                         | Oggetti attivazione MFT      |
| [\_ \_ Attributo locale del processo MFT \_](mft-process-local-attribute.md)                                             | Specifica se una MFT è registrata solo nel processo dell'applicazione.                                                                                                                     | Oggetti attivazione MFT      |
| [\_ \_ immagine di REMUX di MFT contrassegnata \_ \_ \_ come \_ punto di pulitura \_](mft-remux-mark-i-picture-as-clean-point.md)                 | Specifica se il video H. 264 remux MFT dovrebbe contrassegnare le immagini come punto di pulitura per una migliore capacità di ricerca. Questo può causare danneggiamenti nelle ricerche in file MP4 finali non conformi. | Oggetti attivazione MFT      |
| [Supporto per MFT \_ \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopici 3D.                                                                                                          | Oggetti attivazione MFT      |
| [**la \_ \_ modifica del \_ formato \_ dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md)                  | Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche al formato dinamico.                                                                                                         | MFTs                        |
| [\_ \_ Attributo CLSID Transform \_ MFT](mft-transform-clsid-attribute.md)                                         | Contiene l'identificatore di classe (CLSID) di un MFT.                                                                                                                                              | Oggetti attivazione MFT      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



