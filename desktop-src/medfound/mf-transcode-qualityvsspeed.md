---
description: Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Attributo MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331351"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>\_Attributo transcode \_ QUALITYVSSPEED MF

Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore                                                                          | Significato                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Qualità inferiore, codifica più veloce.<br/>  |
| <dl> <dt>100</dt> </dl> | Maggiore qualità, codifica più lenta.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo ha lo stesso valore GUID della proprietà [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definita per [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)e ha la stessa interpretazione.

L'applicazione può impostare questo attributo sul profilo transcode prima di compilare la topologia transcode per i codec Windows Media. Il valore deve essere compreso tra 0 e 100. Per il flusso video, il generatore di topologie transcodifica esegue il mapping di un valore al valore specificato dall'applicazione e fornisce il valore mappato alla proprietà **\_ COMPLEXITYEX di MFPKEY** del codificatore. I valori inferiori consentono al codificatore di usare algoritmi di codifica meno complessi. L'uso di algoritmi più semplici produce un output di qualità inferiore, ma il processo di codifica è più veloce e richiede una minore potenza di elaborazione.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
