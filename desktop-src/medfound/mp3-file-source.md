---
description: L'origine file MP3 analizza i file MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origine file MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b5649f1bdbc9d9b3dfa0af2f04878dfa64852af85ff8e829d4d2d4c4d20d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240106"
---
# <a name="mp3-file-source"></a>Origine file MP3

L'origine file MP3 analizza i file MP3.

L'origine file MP3 restituisce buffer contenenti fotogrammi audio MPEG-1. Non decodifica l'audio.

## <a name="file-extensions-and-mime-types"></a>Estensioni di file e tipi MIME

L'origine file MP3 è l'origine multimediale predefinita per l'estensione di file seguente:

-   mp3

È anche l'origine multimediale predefinita per i tipi MIME seguenti.

-   audio/mpeg
-   audio/x-mp3
-   audio/x-mpeg

## <a name="media-types"></a>Tipi di supporti

Il tipo di supporto offerto dall'origine file MP3 contiene gli attributi seguenti.



| Attributo                                                                                    | Descrizione                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                    | Uguale a **MFMediaType \_ Audio.**                                                                                                                   |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                           | Uguale a **MFAudioFormat \_ MP3** o **MFAudioFormat \_ MPEG**.                                                                                        |
| [**MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Numero medio di byte al secondo.                                                                                                                |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | Uguale a 1.                                                                                                                                        |
| [**CANALI \_ NUM AUDIO MT MF \_ \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Numero dei canali audio.                                                                                                                          |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md)      | Numero di campioni audio al secondo.                                                                                                                |
| [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                                      | Contiene la parte di [**una struttura MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) visualizzata dopo il membro **wfx** della struttura . |



 

## <a name="interfaces"></a>Interfacce

L'origine file MP3 espone le interfacce seguenti tramite [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Espone inoltre le interfacce seguenti tramite [**IMFGetService:**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID servizio</th>
<th>Interfaccia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>Ipropertystore</strong></a>
<blockquote>
[!Note]<br />
Vedere <a href="shell-metadata-providers.md">Provider di metadati della shell</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Origini multimediali e sink](media-sources-and-sinks.md)
</dt> <dt>

[Origini multimediali](media-sources.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
