---
description: Specifica la modalità del codec vocale.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303a86adbf9c443149ff78a47d19922284e38d2c0aeb56dcc13a74ca20cd54a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113121"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>Proprietà MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode

Specifica la modalità del codec vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACMusicSpeechClassMode

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="remarks"></a>Commenti

Il valore 1 indica al codec che il contenuto è solo vocale, il valore 2 indica che il codec determina automaticamente la modalità e qualsiasi altro valore indica al codec di usare la modalità musica.

Se la modalità automatica non codifica correttamente musica e voce mista, è possibile specificare la codifica per singole sezioni del file usando la proprietà [MFPKEY \_ WMAVOICE \_ ENC \_ EDL.](mfpkey-wmavoice-enc-edlproperty.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




