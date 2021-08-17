---
description: Specifica la velocità in bit audio massima per il sink multimediale DLNA (Digital Living Network Alliance).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE attributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104767"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>Attributo MF \_ MP2DLNA \_ AUDIO \_ BIT \_ RATE

Specifica la velocità in bit audio massima per il sink multimediale DLNA (Digital Living Network Alliance).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è la velocità in bit massima di destinazione per il flusso audio codificato, in bit al secondo. Il valore deve essere una delle velocità in bit consentite per l'audio MPEG-2 di livello 2 per DLNA. Il valore predefinito è 192000 (192 Kbps).

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Per impostare questo attributo nel sink multimediale DLNA, eseguire una query sul sink multimediale per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




