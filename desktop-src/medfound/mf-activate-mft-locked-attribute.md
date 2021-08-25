---
description: Specifica se il caricatore della topologia modificherà i tipi di supporti in una trasformazione Media Foundation (MFT). Le applicazioni in genere non usano questo attributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060911"
---
# <a name="mf_activate_mft_locked-attribute"></a>Attributo MF \_ ACTIVATE \_ MFT \_ LOCKED

Specifica se il caricatore della topologia modificherà i tipi di supporti in una trasformazione Media Foundation (MFT). Le applicazioni in genere non usano questo attributo.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se il valore di questo attributo è diverso da zero, il caricatore della topologia non modificherà i tipi di supporti in MFT. Il caricatore della topologia imposta questo attributo dopo il caricamento della topologia.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




