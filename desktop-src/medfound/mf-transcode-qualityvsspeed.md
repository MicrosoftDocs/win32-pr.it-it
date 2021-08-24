---
description: Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7498cd319f347d8509f42e1713e1b2e267b32406eceb073ea9ca1e4cb4ea8d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604671"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>Attributo MF \_ TRANSCODE \_ QUALITYVSSPEED

Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore di questa proprietà ha l'intervallo seguente.



| Valore                                                                          | Significato                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Qualità inferiore, codifica più veloce.<br/>  |
| <dl> <dt>100</dt> </dl> | Maggiore qualità, codifica più lenta.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo ha lo stesso valore GUID della proprietà [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definita per [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)e ha la stessa interpretazione.

L'applicazione può impostare questo attributo sul profilo di transcodifica prima di compilare la topologia di transcodifica per Windows codec multimediali. Il valore deve essere compreso nell'intervallo da 0 a 100. Per il flusso video, il generatore di topologie di transcodifica esegue il mapping di un valore al valore specificato dall'applicazione e fornisce il valore mappato alla proprietà **MFPKEY \_ COMPLEXITYEX** del codificatore. I valori inferiori consentono al codificatore di usare algoritmi di codifica meno complessi. L'uso di algoritmi più semplici produce un output di qualità inferiore, ma il processo di codifica è più veloce e richiede meno potenza di elaborazione.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
