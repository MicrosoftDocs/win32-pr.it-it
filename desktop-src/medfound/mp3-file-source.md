---
description: L'origine file MP3 analizza i file MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origine file MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130498"
---
# <a name="mp3-file-source"></a>Origine file MP3

L'origine file MP3 analizza i file MP3.

I buffer di output del file MP3 contengono i frame audio MPEG-1. Non decodifica l'audio.

## <a name="file-extensions-and-mime-types"></a>Estensioni di file e tipi MIME

L'origine file MP3 è l'origine multimediale predefinita per la seguente estensione del nome file:

-   mp3

È anche l'origine multimediale predefinita per i tipi MIME seguenti.

-   audio/MPEG
-   audio/x-MP3
-   audio/x-MPEG

## <a name="media-types"></a>Tipi di supporto

Il tipo di supporto offerto dall'origine file MP3 contiene gli attributi seguenti.



| Attributo                                                                                    | Descrizione                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                                    | Uguale a **MFMediaType \_ audio**.                                                                                                                   |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                           | Uguale a **MFAudioFormat \_ MP3** o **MFAudioFormat \_ MPEG**.                                                                                        |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Numero medio di byte al secondo.                                                                                                                |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)             | Uguale a 1.                                                                                                                                        |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                   | Numero dei canali audio.                                                                                                                          |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)      | Numero di campioni audio al secondo.                                                                                                                |
| [**\_ \_ dati utente MF \_ mt**](mf-mt-user-data-attribute.md)                                      | Contiene la parte di una struttura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) visualizzata dopo il membro **wfx** della struttura. |



 

## <a name="interfaces"></a>Interfacce

L'origine file MP3 espone le interfacce seguenti tramite [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Espone inoltre le interfacce seguenti tramite [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):



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
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
<blockquote>
[!Note]<br />
Vedere <a href="shell-metadata-providers.md">provider di metadati della shell</a>.
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Origini e sink multimediali](media-sources-and-sinks.md)
</dt> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
