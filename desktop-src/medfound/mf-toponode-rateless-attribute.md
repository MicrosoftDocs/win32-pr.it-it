---
description: Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4de6b132bf2b49e327be45588a497374043794ec73925eb61f2dab16fd1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448871"
---
# <a name="mf_toponode_rateless-attribute"></a>Attributo MF \_ TOPONODE \_ RATELESS

Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di output (**MF \_ TOPOLOGY \_ OUTPUT \_ NODE**).

Se il valore di questo attributo è diverso da zero, media Session considera il sink multimediale come un sink senza frequenza, indipendentemente dal fatto che il sink multimediale restituisca la caratteristica **MEDIASINK \_ RATELESS.** Se questo attributo non è impostato, si presuppone che il sink multimediale non sia senza frequenza.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




