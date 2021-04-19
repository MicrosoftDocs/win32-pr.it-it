---
description: Specifica un tipo di supporto se ogni campione è indipendente dagli altri esempi nel flusso.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Attributo MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309558"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>\_ \_ Attributo indipendente di tutti gli esempi MF mt \_ \_

Specifica un tipo di supporto se ogni campione è indipendente dagli altri esempi nel flusso.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **false**, alcuni esempi non possono essere usati senza fare riferimento ad altri esempi nel flusso. Se, ad esempio, un formato video contiene frame Delta, questo attributo deve essere **false**.

Questo attributo corrisponde al campo **bTemporalCompression** nella struttura del [**tipo di \_ supporto \_ DirectShow am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Impostare questo attributo su **true** per tutti i tipi di supporto non compressi.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
