---
description: Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Attributo MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332384"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a>\_ \_ \_ \_ \_ Attributo indicazione livello profilo audio \_ MF mt AAC

Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo contiene il valore del campo **audioProfileLevelIndication** , come definito da ISO/IEC 14496-3.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




