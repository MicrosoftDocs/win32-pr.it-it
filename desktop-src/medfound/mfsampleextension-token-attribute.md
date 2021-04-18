---
description: 'Contiene un puntatore al token fornito al metodo IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Attributo MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309088"
---
# <a name="mfsampleextension_token-attribute"></a>\_Attributo token MFSampleExtension

Contiene un puntatore al token fornito al metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Questo attributo si applica agli esempi di supporti. Il valore dell'attributo è il puntatore **IUnknown** passato al parametro *PToken* del metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . Il chiamante usa questo attributo per tenere traccia dello stato della richiesta.

Se si sta scrivendo un'origine multimediale personalizzata, impostare questo attributo sull'esempio quando il flusso multimediale recapita un campione in risposta al metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a meno che il valore di *PToken* non sia **null**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 




