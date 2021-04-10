---
description: Specifica la velocità in bit audio massima per il sink del supporto Digital Living Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Attributo MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967042"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>\_ \_ \_ Attributo velocità in bit \_ audio MF MP2DLNA

Specifica la velocità in bit audio massima per il sink del supporto Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è la velocità in bit massima di destinazione per il flusso audio codificato, in bit al secondo. Il valore deve essere una delle velocità in bit consentite per l'audio MPEG-2 Layer 2 per DLNA. Il valore predefinito è 192000 (192 Kbps).

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




